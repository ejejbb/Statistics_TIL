# 통계학 3주차 확인문제_answer

## 문제 1.

> **🧚 아래의 테이블을 조인한 결과를 출력하였습니다. 어떤 조인 방식을 사용했는지 맞춰보세요.**

> 사용한 테이블은 다음과 같습니다.

![TABLE1](https://github.com/ejejbb/Template/raw/main/File/2.6.PNG)|![TABLE2](https://github.com/ejejbb/Template/raw/main/File/2.7.PNG)
---|---|

> 보기: INNER, LEFT, RIGHT 조인

<!-- 테이블 조인의 종류를 이해하였는지 확인하기 위한 문제입니다. 각 테이블이 어떤 조인 방식을 이용하였을지 고민해보고 각 테이블 아래에 답을 작성해주세요.-->

### 1-1. 
![TABLE](https://github.com/ejejbb/Template/raw/main/File/2-1.PNG)
```
LEFT JOIN
```

### 1-2. 
![TABLE](https://github.com/ejejbb/Template/raw/main/File/2-3.PNG)
```
INNER JOIN
```

### 1-3. 
![TABLE](https://github.com/ejejbb/Template/raw/main/File/2-2.PNG)
```
RIGHT JOIN
```

## 문제 2.

> **🧚 다음과 같은 요구사항을 반영한 ERD를 설계할 때 엔터티와 주요 관계를 정의하세요.**

```
[시나리오]  

- 한 회사는 직원(Employee)을 관리하며, 각 직원은 직원 ID, 이름, 부서 ID를 가진다.
- 부서(Department)는 부서 ID, 부서명 속성을 가지며, 여러 직원이 한 부서에 속할 수 있다.
- 프로젝트(Project)는 프로젝트 ID, 프로젝트명을 가지며, 한 직원은 여러 프로젝트에 참여할 수 있다.
- 프로젝트 배정(Project_Assignment) 테이블을 통해 직원과 프로젝트 간의 관계를 관리하며, 배정 ID, 직원 ID(FK), 프로젝트 ID(FK), 배정 날짜를 포함한다. 
```

> **질문:   
1️⃣ 주요 엔터티와 그 속성을 정의하세요.   
2️⃣ 엔터티 간의 관계를 정의하세요.**

<!-- ERD에 관한 문제입니다. 엔터티의 정의와 관계 유형을 떠올려보세요.-->

```
1️⃣ 엔터티 및 속성
    - 직원(Employee): 직원 ID(PK), 이름, 부서 ID(FK)
   - 부서(Department): 부서 ID(PK), 부서명
   - 프로젝트(Project): 프로젝트 ID(PK), 프로젝트명
   - 프로젝트 배정(Project_Assignment): 배정 ID(PK), 직원 ID(FK), 프로젝트 ID(FK), 배정 날짜

2️⃣ 엔터티 간 관계
   - 직원(Employee) ↔ 부서(Department) → N:1 관계 (여러 직원이 하나의 부서에 속함)
   - 직원(Employee) ↔ 프로젝트(Project) → M:N 관계 (한 직원이 여러 프로젝트에 참여할 수 있고, 하나의 프로젝트에도 여러 직원이 배정될 수 있음)
   - 이를 위해 프로젝트 배정(Project_Assignment) 테이블을 사용하여 직원과 프로젝트 간의 M:N 관계를 관리함.
```

### 🎉 수고하셨습니다.
