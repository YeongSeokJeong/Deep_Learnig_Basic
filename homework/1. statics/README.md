## 머신러닝을 위한 확률과 통계 이론

#### 불확실성

- 모델링 시스템의 고유 확률

   ex) 카드게임 프로그램에서 랜덤하게 섞는경우

- 미래에 대한 예측의 불확실성 ...



=> 모델링시 다양한 불확실성이 존재하기 때문에 복잡한 규칙 보다는 간단한 확률기반의 rule을 결정하는 경우가 많음

### Random Variable(확률 변수)

- 정의 : 각각의 값이 확률적으로 결정될수 있는 변수

- 표기 

  - Random variable : 확률 변수
    $$
    x_1, x_2 ...
    $$
    
- Random vector : 확률 벡터

$$
\boldsymbol{x_1, x_2}...
$$

### Discrete Variables and Probability Mass Function

- Discrete Variables : 불연속 변수(주사위 눈)
- Probability Mass Function(PMF) : Discrete Variables에 대한 확률 함수

$$
EX. \quad P(x) = 1, P(x) = 0 \; if\; clear \;P(x) = 1
$$

예) 동전 던지기, 주사위 던지기 ...



### Continuous Variables and Probability Density Function

- Continuous variables : 연속 변수

- Probability Density Function(PDF) : 연속 변수([a,b]를 만족) 를 변수로 하는 확률 함수
  $$
  \int_{[a,b]}{P(x)} = 1
  $$
  

---

### Marginal Probability

- 한계 확률

- x,y가 서로 joint Distribution을 만족할때 x의 확률
  $$
  P(y = y|x = x)= \sum_y{P(x = x, y = y)}
  $$

### Conditional Probability

- 조건부 확률 : x사건이 일어날때 y 사건이 일어날 확률
  $$
  P(y=y|x = x)=\frac{P(y=y,x=x)}{P(x = x)}
  $$

- 조건 P(x) > 0

### Chain Rule of Conditional Probabilities

- 모든 결합 확률을 다음과 같이 표기 가능
  $$
  P(x^{(1)},...,x^{(n)}) = P(x^{(1)})\Pi_{i=2}^{n}P(x^{(i)}|P(x^{(1)},...,x^{(n)}))
  $$
  

### Independence and conditional independence

- 두 변수 x, y 가 독립일 경우 다음을 만족함
  $$
  P(x = x,y = y) = P(x = x)P(y=y)
  $$
  또한 다음과 같이 나타냄
  $$
  x\bot y
  $$

- 독립변수 x,y에 대해 조건부 독립 z가 존재하는 경우 다음과 같이 표기
  $$
  P(x =  x, y=y|z=z) = P(x=x|z=z)P(y=y|z=z)
  $$
  또한 다음과 같이 나타냄
  $$
  x \bot y|z
  $$

---

### Expectation

- 기대값 함수 f(x)에 대해 분포 P(x)의 평균값
  $$
  E_{x\sim{P}}[f(x)] = \sum_xP(x)f(x)
  $$

- continuous variables
  $$
  E_{x\sim{P}}[f(x)] = \int p(x)f(x)dx
  $$



### Variance

- 분포 확률 변수 x에 대해 함수 f(x)의 값이 얼마나 퍼져 있는지를 나타냄
  $$
  Var(f(x)) = E[f(x)-E[f(x)]^2]
  $$
  