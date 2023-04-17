# 8.써포트 벡터 머신(Support Vector Machine)

## 1.선형 써포트벡터머신
- SVM : 간격 제일 넓은 것 찾기

3p

- p차원 보다 한차원 낮은 공간을 hyperplane이라고 부름

4p

- 최대 마진 분류기 : 폭 가장 넓은것을 분류모형을 선택

14p

### 제한조건 하에서 최적화

- 라그랑주 승수법 :등식 제한 조건이 있는 경우 사용
    - x, $\lambda$에 대해 미분해서 0, 연립
- KKT 제약조건 : 영역으로 주어졌을때 사용



## 2. 커널 svm

- RBF 가 제일 나음

- $\beta_0 와  \beta$의 추정

## 3. Scikit learn 을 이용한 svm

- c가 클수록 어떻게 되는지 시험 문제 냄 앞에서 설명함 : 알파의 역할

26p

- f1-score클수록 좋음
- precision : 세로
- recall : 가로

27p

- kernel rbf사용
- c의 역할, gamma역할 알기 → 조절해보기
- gamma가 커질수록 과대적합 위험있음 : 자료 많이 씀

29p

- 주성분분석으로 특성변수를 150개로 줄임

30p

- GridSearchCV : 전부받아서 계산. 최적화 값 찾기
- 최적의 모수 찾기 : tunning
