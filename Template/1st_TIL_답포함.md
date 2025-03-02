# 통계학 1주차 정규과제

📌통계학 정규과제는 매주 정해진 분량의 『*데이터 분석가가 반드시 알아야 할 모든 것*』 을 읽고 학습하는 것입니다. 이번 주는 아래의 **Statistics_1st_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 교재를 다시 참고하여 보완하는 것이 좋습니다.

1주차는 데이터 분석을 위한 기초 체력을 다집니다.


## Statistics_1st_TIL

### 01. 통계학 이해하기
1.1. 왜 통계학을 알아야 할까?   
1.2. 머신러닝과 전통적 통계학의 차이   
1.3. 통계학의 정의와 기원   
1.4. 기술 통계와 추론 통계

### 02. 모집단과 표본추출
2.1. 모집단과 표본, 전수조사와 표본조사   
(2.4. 인지적 편향의 종류)   
2.5. 머신러닝 모델 측면의 편향과 분산   

### 03. 변수와 척도
3.1. 변수의 종류   
3.3. 척도의 종류   

### 04. 데이터의 기술 통계적 측정
(4.3. 산포도와 범위, 사분위수, 변동계수)   
4.4. 왜도와 첨도
4.5. 표준편차의 경험법칙

### 05. 확률과 확률변수
5.3. 분할과 베이지안 이론   
5.5. 심슨의 역설

### 06. 확률분포
6.2. 이산확률분포   
6.3. 연속확률분포   
6.4. 중심극한정리

### 07. 가설검정
7.1. 귀무가설과 대립가설   
7.2. 가설검정의 절차   
7.3. 가설검정의 유의수준과 p값   
7.4. 1종 오류와 2종 오류

## Study Schedule

|주차| 공부 범위     | 완료 여부 |
|---|--------------|----------|
|1주차| 1부 ~p.79    | ✅     |
|2주차| 10~19강      | 🍽️      | 
|3주차| 20~29강      | 🍽️      | 
|4주차| 30~39강      | 🍽️      | 
|5주차| 40~49강      | 🍽️      | 
|6주차| 50~59강      | 🍽️      | 
|7주차| 60~69강      | 🍽️      | 
|8주차| 70~79강      | 🍽️      | 
|9주차| 80~89강      | 🍽️      |

<!-- study schedule은 전체 공부가 끝나면 수정 예정입니다>
<!-- 여기까진 그대로 둬 주세요-->

# 01. 통계학 이해하기

```
✅ 학습 목표 :
* 통계학의 필요성을 안다.
* 기술통계와 추론통계의 특성을 구분하여 이해한다.
```

## 1.1. 왜 통계학을 알아야 할까?

> **🧚 Q. 데이터 분석가는 왜 통계학을 알아야 하나요?**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
데이터 과학은 기초 통계로부터 발전해 왔으며, 그 의미를 해석함에 있어서도 통계 이론에 기반해야 한다. 통계학 기본기가 충족되지 않은 상태에서 데이터 과학을 하는 것은 분석 결과가 진정 의미가 있는 것인지, 잘못된 부분은 없는지, 있다면 어떻게 개선해야 하는지를 알 수 없기 때문에 위험하다. 즉 데이터를 효과적으로 다루고자 한다면 통계학적 사고가 필요하다.
```

> **🧚 일반적인 데이터 과학의 프로세스를 적어주세요.**

```
[일반적인 데이터 과학의 프로세스]
데이터 수집 > 데이터 가공 > EDA 및 시각화 > ML 모델링 > 결과 해석 및 적용
```


## 1.2. 머신러닝과 전통적 통계학의 차이

> **🧚 빈칸을 채워주세요.**

<!-- 빈칸 안에 공부한 내용을 바탕으로 답을 작성해주세요. 빈칸의 수는 글자 수와 관계 없습니다.-->

> 머신러닝은 ⬜이 주된 목적이다. 따라서 고질적 문제인 ⬜ 해결에 집중한다.   
전통적 통계학은 ⬜이 주된 목적이다. 모집단에서 추출한 샘플에 대한 ⬜을 바탕으로 통계적 모델에 대한 적합성에 집중한다.

```
예측, 과적합(overfitting), 해석, 가정
```


## 1.3. 통계학의 정의와 기원

> **🧚 빈칸을 채워주세요.**

<!-- 빈칸 안에 공부한 내용을 바탕으로 답을 작성해주세요. 빈칸의 수는 글자 수와 관계 없습니다-->

>데이터는 의미 있는 형태인 ⬜로 전환 됐을 때 의사결정에 도움이 될 수 있다.

```
정보
```


## 1.4. 기술 통계와 추론 통계

> **🧚 빈칸을 채워주세요.**

<!-- 빈칸 안에 공부한 내용을 바탕으로 답을 작성해주세요. 빈칸의 수는 글자 수와 관계 없습니다.-->

> 기술통계는 주어진 데이터의 특성을 사실에 근거하여 설명하고 묘사하는 것이다. 데이터를 설명하는 가장 기본적인 방법은 그 데이터의 ⬜을 설명하는 것이다. 이를 설명하기 위해 단순히 수치만 적는 것보다는 ⬜를 사용하는 것이 효과적이다.

```
대푯값, 시각화
```


> **🧚 빈칸을 채워주세요.**

<!-- 빈칸 안에 공부한 내용을 바탕으로 답을 작성해주세요. 빈칸의 수는 글자 수와 관계 없습니다.-->

>추론통계는 ⬜으로부터 ⬜의 특성을 추론하는 것이다.

```
표본(집단), 모집단
```

# 02. 모집단과 표본추출

```
✅ 학습 목표 :
* 모집단과 표본, 모수와 통계량의 정의와 관계를 설명할 수 있다.
(* 분석가가 비논리적인 추론을 내리는 패턴인 인지적 편향의 종류를 이해한다.)
* 편향과 분산의 차이를 이해한다.
```
<!-- 분량 생략 확정 시 학습목표 조정-->

## 2.1. 모집단과 표본, 전수조사와 표본조사

> **🧚 빈칸을 채워주세요.**
<!-- 빈칸 안에 공부한 내용을 바탕으로 답을 작성해주세요. 빈칸의 수는 글자 수와 관계 없습니다.-->

<!-- 1, 2, 3은 각각 동일한 단어입니다.-->

> 통계 분석을 하려면 분석하고자 하는 대상의 데이터가 있어야 한다. 그러나 일반적인 상황에서 모든 데이터를 구하는 것은 현실적으로 어려움이 있다. 따라서 1️⃣의 일부를 추출하여 사용한다. 1️⃣의 일부를 추출한 것을 2️⃣(이)라고 한다. 1️⃣에서 추출한 2️⃣의 통계량을 이용해 3️⃣를 추정한다.

```
모집단, 표본(집단), 모수
```

(## 2.4. 인지적 편향의 종류)

> **🧚 다음은 인지적 편향의 종류를 빈칸으로 두고 문제를 작성한 것입니다. 각 빈칸에 적합한 편향의 종류를 채워보세요.**

보기
> **확증편향, 기준점편향, 선택지원편향, 분모편향, 생존자편향**

<!-- 2.4.을 제외할지 말지 고민입니다. 만일 포함하게 되면 표 삽입하겠습니다.-->


## 2.5. 머신러닝 모델 측면의 편향과 분산

> **🧚 편향과 분산의 차이에 대해 간단히 적어주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
# 편향
: 실제값과 예측값의 차이

# 분산
: 예측값들의 변동성
```

# 03. 변수와 척도
```
✅ 학습 목표 :
* 독립변수, 종속변수에 대해 이해한다.
* 척도(변수의 데이터적 속성)의 종류를 알아본다.
* 척도에 따라 어떤 분석방법이 적절한지 판단할 수 있다.
```

## 3.1. 변수의 종류

> **🧚 독립변수와 종속변수에 대해 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
독립변수와 종속변수는 서로 원인과 결과의 관계를 가지는 변수이다.

[독립변수와 종속변수의 다양한 명칭]

# 독립변수 = feature
          = input variable
          = 설명변수
# 종속변수 = target variable
          = outcome variable
          = 반응변수

독립변수와 종속변수는 기본적으로 서로 상관관계를 갖고 있다.(단순한 상관관계가 아니라 인과관계를 갖고 있어야 한다.) 유의할 점은 독립변수 간에도 상관관계를 가질 수 있다는 점이다. 독립변수 간에는 상관관계가 없어야 한다. 독립변수 간의 상관관계가 높으면(다중공선성 문제) 독립변수들과 종속변수와의 연관성을 측정하기 어렵다.
```
## 3.3. 척도의 종류

> **🧚 질적 척도와 양적 척도에 대해 간단하게 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
우선 변수가 질적/양적이나에 따라 질적척도(범주형)와 양적척도(연속형)로 분류된다.

# 질적척도
## 명목척도(nominal): 속성값을 범주로 나타냄, 다른 척도들보다 정보량이 가장 적다.
## 서열척도(ordinal): 속성값을 순위로 나타냄, 대상 간 순위와 우위에 대한 정보를 포함

# 양적척도
## 등간척도(interval): 서열척도가 갖고 있는 정보와 함께 조사대상이 갖고 있는 속성의 상대적 크기의 차이를 비교 가능
## 비율척도(ratio): 가장 많은 정보를 담을 수 있는 척도. 절대적 기준을 통한 비율 정보까지 포함. 가감승계가 모두 가능.
```

<br>
<br>

> **🧚 어떤 분석 방법이 적절할까요?**
<br>

> 🔍 **Q1. 연속형 변수 간 유사성을 기반으로 그룹을
나누고자 하는 경우**   
Ex1) 고객을 유사한 구매 패턴이나 성향을 가진
그룹으로 나누는 경우   
Ex2) 유사한 주제를 가진 문서들을 같은 그룹으로
분류하는 경우

```
clustering(군집화분석)
```

<br>

> 🔍 **Q2. 범주형 변수 간 인과관계를 확인하고자 하는 경우**   
Ex1) 광고 유형(A/B 테스트)과 고객 구매 여부 간의
관계를 분석하는 경우     
Ex2) 성별과 특정 질병 유무 간의 연관성을 분석
하는 경우

```
카이제곱검정
```

<br>

> 🔍 **Q3. 연속형 변수 간 인과관계가 존재하는 경우**   
Ex1) 광고비 지출과 매출 간의 관계를 분석하는 경우     
Ex2) 체중과 혈압 간의 관계를 분석하는 경우

```
회귀분석
```

<br>

> 🔍 **Q4. 동일한 집단에서 처치 전후의 차이를 비교하고자 하는 경우**   
Ex1) 한 그룹의 학생들이 특정 학습법을 적용하기 전과 후의 시험 점수를 비교하는 경우   
Ex2) 동일한 환자들에게 신약을 투여하기 전과 후의 혈압 변화를 분석하는 경우

> 💝 **Hint** : 정규성을 가정할 수 있는 경우와 그렇지 않은 경우를 고려해보세요.

```
정규성 가정 가능 -> paired t-test
정규성 가정 불가 -> Wilcoxon signed-rank test
```

<br>

> 🔍 **Q5. 서로 다른 두 독립 집단 간 평균 차이를 비교하고자 하는 경우**   
Ex1) A 마케팅 전략을 사용한 고객 그룹과 B 마케팅 전략을 사용한 고객 그룹의 평균 구매 금액 비교   
Ex2) 신약을 투여한 그룹과 기존 약을 복용한 그룹의 평균 혈압 비교

> 💝 **Hint** : 정규성을 가정할 수 있는 경우와 그렇지 않은 경우를 고려해보세요.

```
정규성 가정 가능 -> 2-sample t-test
정규성 가정 불가 -> Mann-Whitney U test
```

# 04. 데이터의 기술 통계적 측정

```
✅ 학습 목표 :
* 산포도의 의미와 산포도를 측정하는 방법에 대해 설명할 수 있다.
* 정규분포의 왜도값과 첨도값이 얼마인지 답할 수 있다.
```

## 4.3. 산포도와 범위, 사분위수, 변동계수  

> **🧚 Q. 산포도가 무엇인가요?**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
# 산포도: 대푯값을 중심으로 자료들이 흩어져 있는 정도
        분산과 표준편차를 포괄하는 상위 개념
```

> **🧚 산포도를 측정하는 방법에 대해 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
# 산포도 측정 방식: 범위, 분산, 표준편차, 사분위수 범위, 변동계수 등

## 범위(range): MAX-MIN

## 사분위수(quartile): Q1=하위25%, Q2=하위50%=중앙값, Q3=하위75%, Q4=하위100%=max

## IQR = Q3-Q1

## 변동계수(CV): 표준편차를 산술평균으로 나누어 준 값으로, 서로 다른 두 자료의 산포도를 비교할 수 있다. 단, 평균이 0이거나 0에 가까우면 CV가 무한히 커질 수 있다.
```

## 4.4. 왜도와 첨도

> **🧚Q. 정규분포의 왜도와 첨도값은 각각 얼마인가요?**

```
정규분포의 왜도=0, 첨도=3
```

## 4.5. 표준편차의 경험법칙

> **🧚 표준편차의 경험법칙에 대해 알게 된 내용을 간단히 정리해주세요.**

```
일반적인 정규분포에서는 표준편차를 통해 데이터 값들의 범위를 가늠할 수 있다.

A. 데이터의 약 68%는 평균으로부터 ±1σ 이내에 속한다. B. 데이터의 약 95%는 평균으로부터 ±2σ 이내에 속한다. C. 데이터의 약 99.7%는 평균으로부터 ±3σ 이내에 속한다.

정규분포의 경우 μ±3σ 내에 데이터의 약 99.7%가 속하므로 최댓값과 최솟값을 추정할 수 있다.

주어진 데이터가 정규분포가 아니거나 분포를 모를 경우 체비셰프의 정리에 따르면 μ±2σ 내에 75% 이상의 데이터가 존재하고 μ±3σ 내에 적어도 89%, μ±4σ 내에 적어도 94%가 존재한다.
```

# 05. 확률과 확률변수

```
✅ 학습 목표 :
* 베이즈 정리의 개념을 이해하고 이를 실생활 예제에 적용할 수 있다.
* 심슨의 역설을 경계하여 데이터를 분석할 때 세부 그룹별 패턴을 고려해 잘못된 결론을 방지할 수 있다.
```

## 5.3. 분할과 베이지안 이론

<!-- 분할과 베이지안 이론에 대해 학습하고 이해한 내용을 정리해주세요.-->

> **🧚Q. (주)다트비의 조일 과장은 이커머스 플랫폼의 마케팅 업무를 담당하고 있다. 최근 회사에서는 배너 광고의 클릭률(CTR)이 기대보다 낮아 최적의 광고 타겟층을 선정하는 프로젝트를 진행 중이다. 조 과장은 광고 효과를 높이기 위해 고민하던 중, 사이트 방문자의 70%가 모바일 유저, 30%가 PC 유저라는 정보를 알아냈다. 그래서 모바일 유저를 타깃으로 배너 광고를 올리면 되겠다 생각했는데 알고 보니 PC 유저의 광고 클릭률(CTR)이 5%로, 모바일 유저의 광고 클릭률(CTR)보다 4%p 높았다. 이런 경우, 모바일과 PC 중 어느 유저층에 집중하여 배너 광고를 올리는 것이 더 효과적일까? (소수점 둘째자리까지 반올림하여 답해주세요.)**

> 💝 **Hint**   
-P(클릭)을 구한다.  
-P(모바일 유저|클릭)과 P(PC 유저|클릭)을 구하고 값을 비교한다.

<!-- 베이즈 정리를 이해하였는지 확인하기 위한 문제입니다. 문제의 답과 풀이를 작성해주세요. 힌트를 참고하셔도 좋습니다.-->

```
답: PC 유저

풀이:
P(클릭)
=P(클릭∣모바일 유저)P(모바일 유저)+P(클릭∣PC 유저)P(PC 유저)
=(0.01×0.7)+(0.05×0.3)=0.007+0.015=0.022

P(모바일 유저∣클릭)
={P(클릭∣모바일 유저)P(모바일 유저)}/P(클릭)
=(0.01×0.7)/0.022=0.3182

P(PC 유저∣클릭)
={P(클릭∣ PC 유저)P(PC 유저)}/P(클릭)
=(0.05×0.3)/0.022=0.6818

광고를 클릭하는 사람 증 모바일 유저는 31.82%, PC 유저는 68.18% 이므로 PC 유저를 타깃하여 배너 광고를 올리는 것이 더 효과적이다.
```

## 5.5. 심슨의 역설

<!-- 데이터의 세부 그룹별로 일정한 추세나 경향성이 나타나지만, 전체적으로 보면 그 추세가 사라지거나 반대 방향의 경향성을 나타내기도 합니다. 때문에 데이터 분석가는 데이터를 어떻게 나누고 결합하고 가공하는가에 따라 결과가 정반대로 바뀔 수 있음을 항상 경계해야 합니다.-->

> **🧚Q. 한 대형 병원이 두 명의 외과 의사(A와 B)의 수술 성공률을 비교하려고 한다. 과거 1년간의 데이터를 보면, A 의사의 전체 수술 성공률은 80%, B 의사의 전체 수술 성공률은 90%였다. 이 데이터를 본 병원 경영진은 A 의사의 실력이 B 의사보다 별로라고 판단하여 A 의사의 수술 기회를 줄이는 방향으로 정책을 조정하려 한다.
그러나 일부 의료진은 이 결론에 의문을 제기했다.
그들은 "단순한 전체 성공률이 아니라 더 세부적인 데이터를 분석해야 한다"고 주장했다.    
-A 의사의 실력이 실제로 B 의사보다 별로라고 결론짓는 것이 타당한가?   
-그렇지 않다면, 추가로 확인해야 할 정보는 무엇인가?**

<!-- 심슨의 역설을 이해하였는지 확인하기 위한 문제입니다-->

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
A와 B 의사의 환자 상태(중증도)에 따른 수술 성공률을 확인해야 한다.
```

# 06. 확률분포

```
✅ 학습 목표 :
* 이산확률분포의 종류에 대해 알고, 각각의 특징과 활용 사례를 설명할 수 있다.
* 연속확률분포의 종류와 특징을 설명할 수 있다. 
* 중심극한정리(CLT)의 개념을 이해하고 설명 할 수 있다.
```

## 6.2. 이산확률분포

> **🧚Q. 이산확률분포에 대해 학습한 내용을 정리해주세요.**

<!--수식과 공식을 암기하기보다는 분포의 개념과 특성을 위주로 공부해주세요. 분석 대상의 데이터가 어떠한 확률분포의 특성을 가지고 있는지를 아는 것이 더 중요합니다.-->

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
# 균등분포: 확률변수가 동일한 확률을 가지는 분포
(이산일 수도 연속일 수도 있음)

# 이항분포: 결과가 2가지 중 하나만 나오는 시행을 n번 하는 경우 사용, 각 시행은 독립

# 초기하분포: 결과가 2가지 중 하나만 나오는 시행을 n번 하는 경우 사용, 각 시행은 독립적이지 않음(비복원추출)

# 포아송분포: 일정한 관측 공간에서 특정 사건이 발생하는 횟수를 나타냄, 표본크기라는 개념이 존재하지 않음
ex. 보험상품개발 - 특정 연령대 구간에 평균적으로 몇 번의 교통사고를 당하는지

## 포아송분포의 조건
- 발생하는 사건은 양의 정수 형태
- 모든 사건은 독립
- 해당 시공간에서 사건의 발생 비율은 항상 같음 (시공간이 두 배로 늘어나면 발생하는 사건도 두 배로 늘어난다.)
- 한 번에 둘 이상의 사건이 발생하지 않는다.
```

## 6.3. 연속확률분포

> **🧚Q. 연속확률분포에 대해 학습한 내용을 정리해주세요.**

<!--수식과 공식을 암기하기보다는 분포의 개념과 특성을 위주로 공부해주세요. 분석 대상의 데이터가 어떠한 확률분포의 특성을 가지고 있는지를 아는 것이 더 중요합니다.-->

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
# 정규분포: 평균을 중심으로 좌우 대칭의 종 모양 형태를 가지고 있으며 대부분의 분포를 정규분포에 근사하여 사용한다.

# 지수분포: 특정 사건이 발생한 시점으로부터 다음 사건이 발생할 때까지의 *시간*을 확률변수로 하는 확률분포, 확률변수인 시간이 증가할수록 사건 발생 확률이 지수적으로 감소
```

## 6.4. 중심극한정리

> **🧚Q. 중심극한정리에 대해 학습한 내용을 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
# 중심극한정리: 데이터의 크기가 일정한 양을 넘으면 각 표본의 평균의 분포가 정규분포에 근사한다는 이론
```

# 07. 가설검정

```
✅ 학습 목표 :
* 귀무가설과 대립가설의 개념을 이해하고, 가설을 설정하는 원리를 설명할 수 있다.
* 가설검정의 유의수준과 p값의 의미를 이해하고, p값을 해석하여 귀무가설을 기각할지 여부를 판단할 수 있다.
* 1종 오류와 2종 오류의 차이를 설명하고, 실제 사례에서 어떤 오류를 더 중요하게 고려해야 하는지 분석할 수 있다.
```

## 7.1. 귀무가설과 대립가설

> **🧚Q. 귀무가설과 대립가설에 대해 학습한 내용을 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
# 가설: 검정하고자 하는 주제, 데이터 분석의 나침반 역할

# 귀무가설(Null hypothesis): 증명하고자 하는 가설과 반대되는 가설로써, 효과와 차이가 없는 가설

# 대립가설(Alternative hypothesis): 귀무가설이 기각됐을 때 대안적으로 채택되는 가설

-> 무죄 추정의 원칙과 같이 충분한 증거가 있기 전까지는 귀무가설이 옳은 것으로 가정하는 것임.
-> 대립가설이 참임을 증명하는 것보다 귀무가설이 참이 아님을 증명하는 것이 훨씬 쉽기 때문에 이러한 형식으로 가설을 설정하고 검정함.
```

## 7.2. 가설검정의 절차

<!-- 공부한 내용을 자유롭게 기술해주세요.-->

> **🧚 OX 문제입니다.**

> **다음 명제가 유의수준 5%를 설정한 것과 동일한 의미인지 판단하세요.   
1️⃣ 표본이 귀무가설과 같을 확률이 5% 미만이다.   
2️⃣ 귀무가설이 참일 확률이 5%이다.   
3️⃣ 귀무가설이 참일 때, 극단적인 표본이 나올 확률을 5%로 설정한 것이다.**

<!-- 동일하면 O, 동일하지 않으면 X.-->

```
# 1번 (X):
유의수준은 표본이 귀무가설과 같을 확률을 의미하는 것이 아님
→ 유의수준은 귀무가설이 참일 때 표본이 기각역에 속할 확률을 의미

# 2번 (X):
유의수준 5%는 귀무가설이 참일 확률을 의미하지 않음
→ 통계적 검정에서 귀무가설이 참일 확률을 직접 계산할 수 없음

# 3번 (O):
유의수준 5%는 귀무가설이 참일 때, 표본이 기각역(극단적인 값)에 들어갈 확률을 5%로 설정한 것
```

## 7.3. 가설검정의 유의수준과 p값

> **🧚Q. 다음 중 귀무가설(H₀)을 기각해야 하는 경우는 언제인가요? 정답을 고르고, 그 이유를 간단히 설명해주세요.**

> **1️⃣ 유의수준(α)이 0.05이고, p값이 0.03일 때   
2️⃣ 유의수준(α)이 0.01이고, p값이 0.02일 때**

```
# 가설검정의 기본 원칙
- p값 < 유의수준 : 귀무가설 기각 (통계적으로 유의미한 차이가 있음)
- p값 > 유의수준 : 귀무가설 기각하지 않음

# 답: 1

p값이 높다는 것은 관찰된 데이터가 우연히 나올 확률이 높다는 의미이다.
따라서 실제로 귀무가설이 참일때(차이가 없을 때), 관찰한 데이터가 우연이 나올 확률이 높다면 차이가 없지 않다고 결론짓기 어렵다.
즉, 귀무가설 기각 어려움. -> 귀무가설 유지

p값이 낮다는 것은 귀무가설이 맞는데도 이런 극단적인 결과가 나올 확률이 너무 작다는 뜻이다.
따라서 "이런 데이터가 나올 가능성이 매우 낮다면, 애초에 귀무가설이 틀렸다고 보는 것(차이가 있다고 보는 것)이 더 합리적이지 않을까?"라는 논리를 따른다.
즉, 귀무가설이 맞다고 가정할 때 이런 결과가 나올 확률이 작다면, 귀무가설을 유지하기가 어려워지므로 기각.
```

## 7.4. 1종 오류와 2종 오류

> **🧚Q. 1종 오류와 2종 오류에 대해 학습한 내용을 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

```
# 1종 오류: 귀무가설이 참인데 귀무가설을 기각하는 오류
(실제로 효과가 없는데 효과가 있다고 판단)
-> 1종 오류가 발생할 확률을 α로 나타냄
-> 복합 귀무가설의 경우 α는 1종 오류가 발생할 확률의 최대치를 의미

# 2종 오류: 귀무가설이 거짓인데 귀무가설을 채택하는 오류
(실제로 효과가 있는데 효과가 없다고 판단)
-> 2종 오류가 발생할 확률을 β로 나타냄
-> 검정력(power) = 1-β
-> 유의수준이 주어지면 표본이 늘어나지 않는 이상 자동으로 결정됨 (α와 β의 trade-off 관계)

일반적으로 유의수준은 0.05, 검정력은 0.2 기준을 사용하고, 1종 오류를 2종 오류보다 더 중요하게 생각한다. 실제로 효과가 없는데 효과가 있다고 판단하는 것은 잘못 판단하는 것이므로 문제가 더 커질 수 있다. 다만, 암진단과 같은 경우에는 2종 오류를 더 중요하게 생각하고 환자를 진단한다. 실제로 암에 걸렸는데 암에 걸리지 않았다고 판단한다면 치료 시기를 놓쳐 더 위험하기 때문이다. 따라서 가설을 설정하는 목적과 환경을 고려하고 극단적이지 않은 결과가 나오도록 세밀한 실험 설계를 해야 한다.
```


> **🧚 아래의 문제를 풀고 오늘 배운 내용을 정리해보세요.**

수연이는 새로운 교육 프로그램이 학생들의 수학 성적에 미치는 영향을 조사하였습니다. 50명의 학생을 두 그룹으로 나누어, 한 그룹(실험군)에는 새로운 교육 프로그램을 적용하고, 다른 그룹(통제군)에는 기존 교육 방법을 유지하였습니다. 8주 후, 두 그룹의 수학 시험 점수를 비교한 결과는 다음과 같았습니다.

|그룹|	평균 점수|	표준편차|
|---|----------|---------|
|실험군|85.4|4.2|
|통제군|82.1|5.1|

t-검정을 실시한 결과, p값은 0.03으로 나타났습니다. 수연이는 유의수준(α)을 0.05로 설정하였습니다.


> **🔍 질문**   
1️⃣ 이 연구에서 귀무가설과 대립가설은 무엇인가요?   
2️⃣ p값과 유의수준을 고려할 때, 귀무가설을 기각해야 하나요?   
3️⃣ 이 결과를 해석해주세요.   
4️⃣ p값이 0.03이라는 것은 무엇을 의미하나요?

```
1️⃣
귀무가설 (H₀): 새로운 교육 프로그램은 기존 교육 방법과 차이가 없다.
              두 그룹(실험군과 통제군)의 평균 점수 차이는 통계적으로 유의하지 않다.
대립가설 (H₁): 새로운 교육 프로그램이 기존 교육 방법과 차이가 있다.
              두 그룹의 평균 점수 차이는 통계적으로 유의하다.

2️⃣
p값 < 유의수준(α)이므로 귀무가설(H₀)을 기각한다.
즉, 새로운 교육 프로그램이 기존 방법과 차이가 있을 가능성이 통계적으로 유의하다고 판단할 수 있다.

3️⃣
두 그룹 간 점수 차이는 통계적으로 유의미하다.

4️⃣
두 그룹 간 차이가 실제로 없다고 가정할 때, 현재와 같은 평균 점수 차이가 우연히 발생할 확률이 3%에 불과하다.
```

### 🎉 수고하셨습니다.
