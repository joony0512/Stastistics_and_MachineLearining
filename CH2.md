# 2.사전과정과 최적화

## 1.실수자료로의 전환(vectorization)

- 11p
    - plotly → matplotlib대신에 사용한듯
    - PolynomialFeatures사용
        - include_bias사용
    - fit_transform사용
        - np.newaxis → 머신러닝은 2d텐서 사용해야해서 1d를 2d로 변경
- 13p
    - None, np.nan둘다 결측치임
    - impute : 결측치를 채운다는 뜻, Sklearn에서 제공, 머신러닝에서 사용(빨라서)
        - SimpleImputer : 내가 원래 갖고있던 정보를 가지고 하는것
        - strategy = ‘mean’ → 열의 평균값으로 대체

## 2.자료의 특성

- 14p
    - 변수 특성 파악
    - matplotlib, plotly등등

## 3.사례분석

- 21p
    - 범주변수 → 가변수로 바꿈
    - reshape(-1,1) : 길이n짜리 데이터를 n*1의 모양으로 바꿔줌. n을 몰라도 됨
    

## 4.불균형 자료의 처리

- 23p
    - Under Sampling vs Over Sampling → 통계적으로 Over Sampling이 맞음
    - Synthetic : 합성
- 24p : SMOTE
    - 변주형 자료는 가변수 처리되어 있어야함 ( ex. 원핫인코딩)
    - xsyn은 벡터임
- 25p : ADASYN
    - 다수 클래스의 표본수에 비례하도록 추출

## 5.특성변수의 선택

- 27p
    - 정규분포 f분포 카이스퀘어통계량
- 28p : 카이스퀘어 통계량
    - 값이 클수록 도움이 되는 변수
- 30p : F통계량
    - 알파i = 0으로 수정

## 6.손실함수와 최적화

- 35p
    
    ⭐categorical cross entropy 
    
    - 라벨링이 되어있어야한다.
    - 정답과 다르면 값이 커진다.
    
- 36p : MLE가 가장 중요하다
    - maximum likelihood : 가장 좋음 (정규분포라고 가정할때)
    - 
- 38p : Gradient Descent
    - ⭐시험문제 : 테일러 급수 이용해서 기울기 구하기
