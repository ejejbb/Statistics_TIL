# 통계학 1주차 정규과제_Advanced

📌통계학 정규과제는 매주 정해진 분량의 『*데이터 분석가가 반드시 알아야 할 모든 것*』 을 읽고 학습하는 것입니다. 이번 주는 아래의 **Statistics_1st_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 교재를 다시 참고하여 보완하는 것이 좋습니다.

1주차는 데이터 분석을 위한 기초 체력을 다집니다.


## Statistics_1st_TIL

### 03. 변수와 척도  
3.3. 척도의 종류   

### 05. 확률과 확률변수
5.3. 분할과 베이지안 이론   
5.5. 심슨의 역설

### 06. 확률분포
6.2. 이산확률분포   
6.3. 연속확률분포   
6.4. 중심극한정리

### 07. 가설검정
7.1. 귀무가설과 대립가설    
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

# 03. 변수와 척도
```
✅ 학습 목표 :
* 척도에 따라 어떤 분석방법이 적절한지 판단할 수 있다.
```
## 3.3. 척도의 종류

> **🧚 어떤 분석 방법이 적절할까요?**
<br>

> 🔍 **Q1. 연속형 변수 간 유사성을 기반으로 그룹을
나누고자 하는 경우**   
Ex1) 고객을 유사한 구매 패턴이나 성향을 가진
그룹으로 나누는 경우   
Ex2) 유사한 주제를 가진 문서들을 같은 그룹으로
분류하는 경우

```
여기에 답을 작성해주세요!
```

<br>

> 🔍 **Q2. 범주형 변수 간 인과관계를 확인하고자 하는 경우**   
Ex1) 광고 유형(A/B 테스트)과 고객 구매 여부 간의
관계를 분석하는 경우     
Ex2) 성별과 특정 질병 유무 간의 연관성을 분석
하는 경우

```
여기에 답을 작성해주세요!
```

<br>

> 🔍 **Q3. 연속형 변수 간 인과관계가 존재하는 경우**   
Ex1) 광고비 지출과 매출 간의 관계를 분석하는 경우     
Ex2) 체중과 혈압 간의 관계를 분석하는 경우

```
여기에 답을 작성해주세요!
```

<br>

> 🔍 **Q4. 동일한 집단에서 처치 전후의 차이를 비교하고자 하는 경우**   
Ex1) 한 그룹의 학생들이 특정 학습법을 적용하기 전과 후의 시험 점수를 비교하는 경우   
Ex2) 동일한 환자들에게 신약을 투여하기 전과 후의 혈압 변화를 분석하는 경우

> 💝 **Hint** : 정규성을 가정할 수 있는 경우와 그렇지 않은 경우를 고려해보세요.

```
여기에 답을 작성해주세요!
```

<br>

> 🔍 **Q5. 서로 다른 두 독립 집단 간 평균 차이를 비교하고자 하는 경우**   
Ex1) A 마케팅 전략을 사용한 고객 그룹과 B 마케팅 전략을 사용한 고객 그룹의 평균 구매 금액 비교   
Ex2) 신약을 투여한 그룹과 기존 약을 복용한 그룹의 평균 혈압 비교

> 💝 **Hint** : 정규성을 가정할 수 있는 경우와 그렇지 않은 경우를 고려해보세요.

```
여기에 답을 작성해주세요!
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
여기에 답을 작성해주세요!
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
여기에 답을 작성해주세요!
```

# 06. 확률분포

```
✅ 학습 목표 :
* 이산확률분포의 종류에 대해 알고, 각각의 특징과 활용 사례를 설명할 수 있다.
* 연속확률분포의 종류와 특징을 설명할 수 있다. 
* 중심극한정리(CLT)의 개념을 이해하고 실험적으로 검증할 수 있다.
```
[이산확률분포와 연속확률분포 추가자료](https://velog.io/@tngus0325/%EC%9D%B4%EC%82%B0%ED%99%95%EB%A5%A0-%EB%B6%84%ED%8F%AC%EC%99%80-%EC%97%B0%EC%86%8D%ED%99%95%EB%A5%A0-%EB%B6%84%ED%8F%AC-%EC%A0%95%EB%A6%AC)

## 6.2. 이산확률분포

> **🧚 이산확률분포에 대해 학습한 내용을 정리해주세요.**

<!--수식과 공식을 암기하기보다는 분포의 개념과 특성을 위주로 공부해주세요. 분석 대상의 데이터가 어떠한 확률분포의 특성을 가지고 있는지를 아는 것이 더 중요합니다.-->

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

<!-- 추가 자료를 참고하여 이산확률분포에 대해 정리해주셔도 좋습니다-->

```
여기에 답을 작성해주세요!
```

## 6.3. 연속확률분포

> **🧚 연속확률분포에 대해 학습한 내용을 정리해주세요.**

<!--수식과 공식을 암기하기보다는 분포의 개념과 특성을 위주로 공부해주세요. 분석 대상의 데이터가 어떠한 확률분포의 특성을 가지고 있는지를 아는 것이 더 중요합니다.-->

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

<!-- 추가 자료를 참고하여 연속확률분포에 대해 정리해주셔도 좋습니다-->

```
여기에 답을 작성해주세요!
```

## 6.4. 중심극한정리

[중심극한정리 시뮬레이션](https://www.youtube.com/watch?v=aIPvgiXyBMI)

> **🧚 중심극한정리에 대해 학습한 내용을 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

<!-- 추가 자료를 참고하여 중심극한정리에 대해 정리해주셔도 좋습니다-->

```
여기에 답을 작성해주세요!
```

# 07. 가설검정

```
✅ 학습 목표 :
* 귀무가설과 대립가설의 개념을 이해하고, 가설을 설정하는 원리를 설명할 수 있다.
* 가설검정의 유의수준과 p값의 의미를 이해하고, p값을 해석하여 귀무가설을 기각할지 여부를 판단할 수 있다.
* 1종 오류와 2종 오류의 차이를 설명하고, 실제 사례에서 어떤 오류를 더 중요하게 고려해야 하는지 분석할 수 있다.
```

## 7.1. 귀무가설과 대립가설

> **🧚 귀무가설과 대립가설에 대해 학습한 내용을 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->


## 7.3. 가설검정의 유의수준과 p값

> **🧚 가설검정의 유의수준과 p값에 대해 학습한 내용을 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->



## 7.4. 1종 오류와 2종 오류

> **🧚 1종 오류와 2종 오류에 대해 학습한 내용을 정리해주세요.**

<!-- 정해진 답은 없습니다. 자유롭게 작성해주세요-->

<br>
<br>

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
여기에 답을 작성해주세요!
```


### 🎉 수고하셨습니다.
