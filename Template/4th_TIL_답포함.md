# 통계학 4주차 정규과제

📌통계학 정규과제는 매주 정해진 분량의 『*데이터 분석가가 반드시 알아야 할 모든 것*』 을 읽고 학습하는 것입니다. 이번 주는 아래의 **Statistics_4th_TIL**에 나열된 분량을 읽고 `학습 목표`에 맞게 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 추가자료와 교재를 다시 참고하여 보완하는 것이 좋습니다.

4주차는 `2부-11.데이터 전처리와 파생변수 생성`를 읽고 새롭게 배운 내용을 정리해주시면 됩니다.


## Statistics_4th_TIL

### 2부. 데이터 분석 준비하기
### 11.데이터 전처리와 파생변수 생성



## Study Schedule

|주차 | 공부 범위     | 완료 여부 |
|----|--------------|----------|
|1주차| 1부 ~p.79    | ✅      |
|2주차| 2부 ~p.120   | ✅      | 
|3주차| 2부 ~p.202   | ✅      | 
|4주차| 2부 ~p.299   | ✅      | 
|5주차| 3부 ~p.356   | 🍽️      | 
|6주차| 3부 ~p.437   | 🍽️      | 
|7주차| 3부 ~p.542   | 🍽️      | 
|8주차| 3부 ~p.615   | 🍽️      | 
|9주차|데이터 분석 실습| 🍽️      |

<!-- 여기까진 그대로 둬 주세요-->

# 11.데이터 전처리와 파생변수 생성

```
✅ 학습 목표 :
* 데이터 전처리 방법을 이해하고 적용할 수 있다.
* 데이터 변환과 가공 기법을 학습하고 활용할 수 있다.
* 모델 성능을 향상시키는 데이터 가공 기법을 이해하고 적용할 수 있다.
* 데이터의 유사도를 측정하는 다양한 거리 측정 방법을 이해하고 활용할 수 있다.
```
<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->

### 11.1. 결측값 처리

결측값을 처리하기 전 데이터 탐색을 통해 결측값의 비율이 어떻게 되는지, 한 변수에 결측값이 몰려있지는 않은지 등을 파악해야 함. 어떤 경우에는 빈 문자열이 입력되어 있어 결측값으로 인식되지 않을수도 있기 때문에 확인해주어야 한다.

```
[결측치의 종류]

# MCAR 완전 무작위 결측: 순수하게 결측치가 무작위로 발생한 경우
# MAR 무작위 결측: 다른 변수의 특성에 의해 해당 변수의 결측치가 체계적으로 발생한 경우
# NMAR 비무작위 결측: 결측값들이 해당 변수 자체의 특성을 가짐
```

```
[결측치 처리 방법]

# 표본 제거 방법: 결측값이 심하게 많은 변수를 제거하거나 결측값이 포함된 행을 제외하고 데이터 분석을 진행하는 방법
  - 전체 데이터에서 결측값의 비율이 10% 미만인 경우 사용
  - MCAR이 아닌 경우 적절하지 않음

# 평균 대치법: 결측값을 제외한 온전한 값들의 평균을 구한 다음, 그 평균 값을 결측값들에 대치하는 방법
  - MCAR이 아닌 경우 적절하지 않음

# 보간법: 전 시점 혹은 다음 시점의 값으로 대치하거나 전 시점과 다음 시점의 평균값으로 대치하는 방법(단순보간), 결측치가 연달아 있는 경우나 시점 인덱스 간격이 불규칙한 경우에는 선형적 수치값을 계산해 보간함(시점고려보간).
  - 데이터가 시계열적 특성을 가진 경우 효과적

# 회귀대치법: 해당 변수와 다른 변수 사이의 관계성을 고려하여 결측값을 계산, 추정하고자 하는 결측값을 가진 변수를 종속변수로 하고 나머지 변수를 독립변수로 하여 추정한 회귀식을 통해 결측값을 대치
  - EX. '연령' 변수와 '연 수입' 변수 : 연 수입이 높으면 상대적으로 높은 연령을 추정하여 결측값을 대치
  - 결측된 변수의 분산을 과소 추정하는 문제 -> 인위적으로 회귀식에 확률 오차항을 추가하는 '확률적 회귀대치법'을 사용하여 변동성을 조정하기도 함.

# 다중 대치법: 단순대치를 여러 번 수행하여 N개의 가상적 데이터를 생성하여 이들의 평균으로 결측값을 대치하는 방법
  - 대치단계 -> 분석단계 -> 결합단계
  - 대치단계: MCMC 방법이나 MICE 방법을 사용하여 대치값을 임의로 생성, 5개 내외 정도만 생성해도 충분
  - 분석단계: 모수의 추정치와 표준오차 계산
  - 결합단계: 계산된 추정치와 표준오차를 결합하여 최종 결측 대치값 산출
```


### 11.2. 이상치 처리

이상치란 일부 관측치의 값이 전체 데이터의 범위에서 크게 벗어난 아주 작거나 큰 극단적인 값을 갖는 것을 말한다.

```
[이상치 처리를 해야 하는 이유]
- 데이터의 모집단 평균이나 총합을 추정하는 것에 문제를 일으킴
- 분산을 과도하게 증가시켜 분석이나 모델링의 정확도를 감소시킴
```

```
[이상치 처리 방법]
- 이상치를 결측값으로 대체한 다음 결측치 처리
- Trimming: 해당 이상치를 제거
- 관측값 변경: 하한값과 상한값을 정한 후 하한값보다 작으면 하한값으로, 상한값보다 크면 상한값으로 대체
- 가중치 조정: 이상치의 영향을 감소시키는 가중치를 부여

* 통계치를 통한 무조건적인 이상치 탐색은 위험할 수 있다.
  예를 들어 고객의 연령이 225세로 입력되어 있다면 이상치가 아니라 잘못 입력된 데이터인 것을 알고 삭제하면 된다.
  연봉 이상치가 나타나는 경우 분석 모델에 직종(사무직/전문직) 변수를 추가하여 회귀선의 정확도를 높일 수 있다.
```

### 11.3. 변수 구간화

변수 구간화(Binning): 데이터 분석 성능 향상 or 해석의 편리성을 위해 이산형 변수를 범주형 변수로 변환

```
[구간을 나누는 방법]
# 동일 폭으로 변수 구간화
# 동일 빈도로 변수 구간화
# ML 기법 : 클러스터링, 의사결정나무
-> IV값이 높을수록 종속변수의 True와 False를 잘 구분할 수 있는 정보량이 많다는 뜻(0.3보다 크면 예측력이 우수)

[평활화 방법]
# 구간별 평균값으로 평활화
# 구간별 중앙값으로 평활화
# 구간별 경곗값으로 평활화
```

### 11.4. 데이터 표준화와 정규화 스케일링

표준화, 정규화 스케일링: 독립변수들이 서로 단위가 다르거나 편차가 심할 때 값의 스케일을 일정한 수준으로 변환하는 것   
-> 머신러닝 모델의 학습 효율을 증가시키기 때문에 많이 사용

[표준화]   
**StandardScaler**   
각 관측치의 값이 전체 평균을 기준으로 어느 정도 떨어져 있는지 나타낼 때 사용
$$z = {x-\mu\over σ}$$

[정규화]   
**MinMaxScaler**    
데이터의 범위를 0부터 1까지로 변환하여 데이터 분포를 조정하는 방법
$$x_{scaled}={x-x_{min}\over x_{max}-x_{min}}$$

[RoburtScaler]   
표준화와 정규화는 이상치에 민감하다는 단점을 보완한 스케일링 기법   
평균대신 중앙값을 사용

### 11.5. 모델 성능 향상을 위한 파생 변수 생성

`파생변수`는 데이터의 특성을 이용하여 분석 효율을 높이는 것이므로 무작정 변수를 가공해서 만들면 안되고 데이터의 특성과 흐름을 충분히 파악한 후 아이디어를 얻어서 만드는 것이 효과적이다.

파생변수는 기존의 변수를 활용해서 만들어낸 변수이기 때문에 다중공선성 문제가 발생할 가능성이 높다. 그러므로 파생변수를 만든 다음에는 상관분석을 통해 변수 간의 상관성을 확인해야 한다.

### 11.6. 슬라이딩 윈도우 데이터 가공

슬라이딩 윈도우: 실시간 네트워크 패킷 데이터를 처리하는 기법, 각각의 데이터 조각들이 서로 겹치며 데이터가 전송되는 것이 특징이다. 이로 인해 전체 데이터가 증가하는 원리를 차용한 것이 슬라이딩 윈도우 데이터 가공의 핵심이다.

### 11.7. 범주형 변수의 가변수 처리

dummy variable: 범주형 변수를 0과 1의 값을 가지는 변수로 변환해 주는 것, 연속형 변수만 사용 가능한 분석기법을 사용하기 위함.

범주가 3개 이상인 경우, 범주가 늘어날수록 변수의 수를 늘리면 된다.

가변수가 범주의 수보다 하나 적게 만들어지는 것은 데이터의 효율성 뿐만 아니라 변수 간 독립성을 확보하기 위함이기도 하다.

### 11.8. 클래스 불균형 문제 해결을 위한 언더샘플링과 오버샘플링

분류 모델은 클래스 불균형 문제가 발생하는 경우가 많다. 클래스 불균형 문제가 심하면 우리가 원하는 대로 학습이 이루어지지 않는다. 그 근본적인 이유는 대부분의 분류 모델에서 적은 비중의 클래스를 분류하는 것이 중요하기 때문이다.

이러한 불균형 문제를 해결하는 방법은 두 종류가 있다. 첫번째는 모델 자체에 중요도가 높은 클래스에 정확도 가중치를 주는 것(가중치 밸런싱)이고 두번째는 불균형 데이터 자체에 균형이 맞도록 가공한 다음 모델을 학습하는 것이다.(언더샘플링과 오버샘플링)

`언더샘플링`은 큰 비중의 클래스 데이터를 작은 비중의 클래스 데이터만큼 추출하여 학습시키는 것이고, `오버샘플링`은 적은 비중의 클래스 데이터를 큰 비중의 클래스 데이터의 수만큼 복제하여 학습시키는 것이다.

```
[언더샘플링 기법]
# 랜덤 언더샘플링
: 작은 비중의 클래스와 관측치 비율이 유사해질 때까지 무작위로 큰 비중의 클래스의 관측치를 제거
# EasyEnsemble
: 앙상블 기법
: 큰 비중의 클래스를 N개의 작은 비중의 클래스와 동일한 크기의 데이터셋으로 분리한 후, 작은 비중의 클래스 데이터와 분리한 큰 비중의 클래스 데이터를 바꿔가며 학습시키는 것
# CNN
: 딥러닝 알고리즘 CNN과 관계 없음
: 비중이 큰 클래스의 관측치 중에서 비중이 적은 클래스와 *속성값이 확연히 다른 관측치들은 제거*하여 굳이 학습에 사용하지 않아도 되는 관측치를 제거하는 것
```

```
[오버샘플링 기법]

오버샘플링을 적용할 때에는 과적합을 방지하기 위해 학습 셋과 테스트 셋을 분리한 다음에 적용해야 한다.

# 랜덤 오버샘플링
: 작은 클래스의 관측치를 단순 무작위 선택하여 반복 추출하는 방식, 정보의 양이 증가하지 않고 모델 과적합이 발생할 수 있음
# SMOTE
: 대표적인 오버샘플링 기법, KNN 기법 사용
# ADASYN
: SMOTE 기법을 발전시킨 방식
: 오버샘플링할 관측치의 양을 체계적으로 조절 가능
```

### 11.9. 데이터 거리 측정 방법

공간상 데이터들 간의 거리가 가까우면 가까울수록 유사하다고 볼 수 있기 때문에 데이터의 거리를 측정하는 것은 데이터 유사도 측정이라고도 할 수 있다. 때문에 분류모델이나 군집모델의 거의 필수적으로 데이터 거리를 활용한다. 데이터 거리를 측정하기 전에 데이터 표준화나 정규화 가공을 해줘야 한다.

[대표적인 거리 측정 방법]

1. 유클리드 거리
  * 피타고라스 정리를 활용한 것
  * n차원의 데이터에 대한 유클리드 거리 계산 방법
  $$d(A,B) = \sqrt{\sum_{i=1}^n (a_i-b_i)^2}$$

2. 맨해튼 거리
  * 택시 거리라고도 불림
  * 최단거리로 갈 수 없고 격자의 선으로만 지나갈 수 있을 때 사용
  $$d(A,B) = \sum_{i=1}^n |a_i-b_i|$$

3. 민코프스키 거리
  * 옵션값을 설정하여 거리 기준을 조정할 수 있는 거리 측정 방법
  $$d(A,B) = ({\sum_{i=1}^n |a_i-b_i|^p})^{1/p}$$

4. 체비쇼프 거리
  * 민코프스키 거리의 p값을 무한대로 설정한 경우
  * 군집 간 최대 거리를 구할 때 사용
  $$d(A,B) = max(|a_i-b_i|) = \lim_{n→∞}[{\sum_{i=1}^n |a_i-b_i|^n}]^{1/n}$$

5. 마할라노비스 거리
  * 유클리드 거리에 공분산을 고려한 거리 측정 방법
  * 확률분포를 고려
  * $\sum^{-1}$은 공분산 행렬이고 T는 변환행렬
  $$d(A,B) = \sqrt{(A-B)^{\sum^{-1}}(A-B)^T}$$
  ![마할라노비스 거리](/img/4.1.jpg)

6. 코사인 거리
  * 코사인 유사도
    - 벡터 사이의 각도를 구해 두 점 간의 유사도를 측정
    - 두 점 간의 각도가 작으면 유사도가 높고, 각도가 크면 유사도가 낮아짐
    - 일반적으로 0에서 1 사이의 값을 가짐
    - 1 이면 두 점 간 각도가 작음, 유사도가 매우 높음
    - 변수 간의 크기가 중요하지 않을 때 적합
    $$cos(\theta) = {AB \over ||A||||B||}$$
  * 코사인 거리 = 1 - 코사인 유사도


<br>
<br>

# 확인 문제

## 문제 1. 데이터 전처리

> **🧚 한 금융회사의 대출 데이터에서 `소득` 변수에 결측치가 포함되어 있다. 다음 중 가장 적절한 결측치 처리 방법은 무엇인가?   
1️⃣ 결측값이 포함된 행을 모두 제거한다.  
2️⃣ 결측값을 `소득` 변수의 평균값으로 대체한다.  
3️⃣ `연령`과 `직업군`을 독립변수로 사용하여 회귀 모델을 만들어 `소득` 값을 예측한다.  
4️⃣ 결측값을 보간법을 이용해 채운다.**

> **[데이터 특징]**     
    - `소득` 변수는 연속형 변수이다.  
    - 소득과 `연령`, `직업군` 간에 강한 상관관계가 있다.  
    - 데이터셋에서 `소득` 변수의 결측 비율은 15%이다.

<!--결측값이 무작위로 발생한 경우인지(MCAR, MAR, NMAR) 판단하고, 변수 간 관계를 고려해보세요.-->

```
답: 3번

해설:
- 결측 비율이 10% 이상이므로 단순 제거(1번)보다는 대치 방법이 필요하다.
(* 10%는 절대적인 수치는 아님)
- 평균 대치(2번)는 데이터 변동성을 줄여 분석 결과를 왜곡할 가능성이 있다.
- 보간법(4번)은 시계열 데이터에서 사용되므로 적절하지 않다.
- 회귀 모델을 활용한 대치(3번)는 다른 변수와의 관계를 고려하여 결측값을 채우므로 가장 적절한 방법이다.
```

## 문제 2. 이상치 처리

> **🧚 한 부동산 데이터에서 `주택 가격` 변수의 분포를 살펴본 결과, 대부분의 가격이 2억~5억 원 사이에 분포하지만, 100억 원 이상인 데이터가 일부 존재했다.**

> **🔍 Q1. 이러한 `주택 가격` 데이터를 이상치로 판단할 수 있는 방법을 한 가지 이상 서술하세요.**

```
1. IQR(사분위수 범위) 방법:
Q3+1.5×IQR보다 큰 값을 이상치로 간주

2. Z-score 방법: 평균과 표준편차를 이용하여 특정 Z-score(3 이상)를 이상치로 판별
```

> **🔍 Q2. 이상치를 처리하는 방법에 대해 고민해보고 어떤 방법이 가장 적절할지 서술해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
- 강남 지역 아파트의 경우 100억 원 이상 가격이 충분히 가능할 수도 있기 때문에 단순히 통계적 방법으로 제거하기보다는 도메인 지식을 활용하여 판단하는 것이 중요하다.

- 분석 목적이 평균적인 주택 가격을 예측하는 것이라면 Trimming이 효과적일 수 있으며, 특정 고가 주택을 포함한 분석이 필요하다면 Winsorizing이 적절할 수 있다.
```

## 문제 3. 데이터 스케일링

> **🧚 머신러닝 모델을 학습하는 과정에서, `연봉(단위: 억 원)`과 `근속연수(단위: 개월)`을 동시에 독립변수로 사용해야 합니다. 연봉과 근속연수를 같은 스케일로 맞추기 위해 어떤 스케일링 기법을 적용하는 것이 더 적절한가요?**

<!--표준화와 정규화의 차이점에 대해 고민해보세요.-->

```
- 단위 차이가 크므로 정규화(MinMaxScaler)보다는 표준화(StandardScaler)를 사용하는 것이 더 적절하다.  
- 특히 선형 회귀, PCA 등 거리 기반 알고리즘에서는 표준화가 더 효과적이다.
```

## 문제 4. 파생변수 생성

> **🧚 한 온라인 쇼핑몰에서는 고객의 구매 패턴을 분석하기 위해 기존 데이터에 파생변수를 추가하려고 한다.**

> 원본 데이터의 컬럼명: `총구매금액`, `방문횟수`, `최근 방문일`, `회원가입일`

> **🔍 Q1. 원본 데이터의 변수를 참고하여 의미 있는 파생 변수의 예시를 하나 이상 들어주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
예시 답:
활동기간 = 최근 방문일 - 회원가입일
구매 빈도 = 총구매금액 / 방문횟수
VIP 여부 = 총구매금액 > 100만 원이면 1, 아니면 0
```

> **🔍 Q2. 파생변수를 만들 때 주의해야 할 점을 설명하세요.**

```
- 파생 변수를 생성한 후 반드시 변수 간의 다중공선성을 확인해야 한다.
- 무작정 변수를 늘리기보다는, 도메인 지식을 고려하여 의미 있는 변수만 생성하는 것이 중요하다.
- 예를 들어, "구매 빈도" 변수는 총 구매금액과 방문횟수의 조합이므로, 이 변수가 기존 변수 대비 얼마나 추가적인 정보를 제공하는지 생각해보아야 한다.
```


## 문제 5. 클래스 불균형 해결

> **🧚 한 보험사에서 고객의 `사기 보험 청구 여부(0/1)`를 예측하는 분류 모델을 만들었다. 하지만 사기 청구 비율은 전체 데이터의 2%에 불과하다.**

> **🔍 Q1. 데이터 불균형 문제가 발생하면 모델 성능에 어떤 영향을 미칠 수 있나요?**

<!--사기 탐지 모델에서 발생할 데이터 불균형으로 인한 모델 성능에의 영향에 대해 구체적으로 고민해주세요.-->

```
모델이 다수 클래스(정상 청구)만 예측하는 경향, 적은 클래스(사기 청구)를 무시하는 현상 발생
```

> **🔍 Q2. 이 문제에서 적절한 해결 방법을 고민하여 서술해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
예시 답:
# 가중치 밸런싱: 정상 청구보다 사기 청구 데이터에 더 높은 가중치를 부여하여 학습하도록 조정

# 불균형 데이터 자체를 균형이 맞도록 조정
- 언더샘플링: 정상 청구(다수 클래스) 데이터를 일부 제거하여 사기 청구(소수 클래스) 데이터와 비율을 맞추는 방법
- 오버샘플링: 사기 청구(소수 클래스) 데이터를 반복하여 생성하거나 유사한 데이터를 추가하여 균형을 맞추는 방법
```

## 문제 6. 데이터 거리 측정

> **🧚 한 추천 시스템에서 고객 간 유사도를 측정하려고 합니다. 고객의 `구매 내역`을 벡터로 변환한 후, 두 고객이 얼마나 유사한지를 측정하려면 유클리드 거리와 코사인 거리 중 어떤 거리 측정 방법이 더 적절한가요?**

<!--유클리드 거리는 벡터의 크기(절대적 차이)를 고려하고, 코사인 유사도는 방향(패턴)을 고려합니다.-->

```
코사인 거리

- 구매 내역 데이터는 크기(절대적 차이)보다는 구매 패턴의 유사성을 보는 것이 중요하므로, 코사인 유사도를 사용하는 것이 더 적절하다.
- 예를 들어, 두 고객이 비슷한 카테고리의 상품을 구매했는지를 비교할 때는 코사인 유사도가 효과적이다.
- 반면, 상품 구매 수량과 가격 차이가 중요한 경우에는 유클리드 거리를 고려할 수 있다.
```


### 🎉 수고하셨습니다.