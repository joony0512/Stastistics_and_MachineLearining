# 5.로지스틱회귀분류(Logistic regression classifier)

## 1.적응선형뉴런(Adative Linear Neuron, ALN)

- 0 또는 1이 Target variable
- pi = yi가 1일 확률

## 2.로지스틱회귀

- odds = 성공확률 /실패확률
    - pi가 0으로 가면 odds도 0 pi가 1로가면 무한대로 감
    - log를 씌워서 pi의 범위 문제를 해결한다 → pi에 대하여 풀면 sigmoid로 정리된다
- 결과 적으로는 z의 값에 시그모이드를 씌운것이 된다.

### w의 추정 및 분류(classification)  - 6 p

- 우도함수에 로그씌우고 -붙이면 loss함수가 된다
- loss fcn = binary cross entropy

### Multi-class Logistic Model -7 p

- 모형 : class의 개수가 3이상인 경우의 Logistic Regression Model
- 3번 돌리면됨
- Softmax

## 3.과대적합에 대한 규제화

- t test결과는 n이 커지면 무조건 커지기 때문에, 데이터가 커지면 믿을 수 없다.
- 과적합의 주요 발생원인 → 특성변수가 너무 많다.
- 8 p : 라쏘 회귀

## 4.Scikit-Learn을 이용한 로지스틱 회귀

- c=100→ 람다 = 0.01 → C가 클수록 람다가 작아지므로 규제 강도가 줄어든다.
    - 성능은 줄지만 일반화 성능을 찾기 가 중요하다.
    - 트레이닝의 적합을 낮춰서 테스트가 일반화 되게 한다.
