# ✨ Regression
### 📘 Reference Material: 『Regression Analysis by Example』5th Edition, Samprit Chatterjee, Ali S.Hadi

## [English Version]  

■ Independent Study
- [F-test model comparison](/regression/What-is-model-comparision-F-test)  
- [t² = F Relationship](/regression/t2-F-en)  

■ Variable Transformation
- [Linearization](/regression/variable-trans-en)  
- [Variance Stabilization by sqrt](/regression/variable-trans2-en1)  
- [Variance Stabilization by Xᵢ term](/regression/variable-trans3-en)  
- [Variance Stabilization by log](/regression/variable-trans4-en)

■ Weighted Least Squares
- [When the weight is already known](/regression/wls1-en)  
- [When the weight is theoretically known](/regression/wls2-en)  
- [When the weight is unknown](/regression/wls3-en)

■ Autocorrelation Problem
- [Autocorrelation Problem](/regression/autocorr1-en)
- [The Statistics](/regression/autocorr2-en.md)
- [Eliminating Autocorrelation through Transformation](/regression/autocorr3-en)
- [Autocorrelation and Omitted Predictors](/regression/autocorr4-en)
- [The Limitation of the Durbin–Watson Statistic](/regression/autocorr5-en)

■ Multicollinearity Problem
- [Understanding the Variance Structure of OLS Estimates](/regression/var-betahat-en)

● Basic Understanding on Principal Component
  
- [The basic concept of Principal Components](/regression/pca1-en)
- [Principal Components & Eigen Vector](/regression/pca2-en)
- [The expression of Principal Components](/regression/pca3-en)
- [How Covariance Matrix can represent the original X?](/regression/pca4-en)

● Principal Component Regression
  
- [The Workflow And Properties of Principal Component](/regression/pcr1-en)
  
## [Korean Version]  

■ 독립 조사
- [F-검정을 활용한 모형 비교](/regression/What-is-model-comparision-F-test)  
- [t² = F 관계](/regression/t2-F)  

- [표준화의 종류와 상관계수 표현](/regression/standardization)

■ 최소제곱법과 중회귀모형

- [단순회귀모형 최소제곱법](/regression/ols1)

■ 변수 변환 (회귀 가정에서 주로 '선형화'와 '등분산성' 조건을 맞추는 데 사용)
- [선형화](/regression/variable-trans)  
- [제곱근을 통한 분산 안정화](/regression/variable-trans2)  
- [Xᵢ 항을 통한 분산 안정화](/regression/variable-trans3)  
- [로그 변환을 통한 분산 안정화](/regression/variable-trans4)

■ 가중 최소제곱법  
- [가중치가 이미 알려진 경우](/regression/wls1.md)  
- [가중치가 이론적으로 유도된 경우](/regression/wls2.md)  
- [가중치가 알려지지 않은 경우](/regression/wls3.md)

■ 자기상관 문제  
- [자기상관 문제](/regression/autocorr1.md)  
- [자기상관 통계량](/regression/autocorr2.md)  
- [변환을 통한 자기상관 제거](/regression/autocorr3.md)  
- [자기상관과 누락된 예측 변수](/regression/autocorr4.md)  
- [더빈–왓슨 통계량의 한계](/regression/autocorr5.md)

■ 다중공선성 문제  

1) 문제 상황
- [OLS 추정량의 분산 구조 이해](/regression/var-betahat.md)
- [다중공선성이 초래하는 문제점](/regression/multicollinearity.md)


2) 문제 탐색
- [VIF와 Condition Index](/regression/vif_condition_index.md)
   
3) 해결 방안
   1. 그냥 특정 변수 제거
   2. 주성분 회귀
   3. 능형 회귀
   4. 변수선택
      
▶ 3-2) 주성분 회귀

 (1) 주성분에 대한 기초 이해  
- [주성분의 기본 개념](/regression/pca1.md)  
- [주성분과 고유벡터](/regression/pca2.md)  
- [주성분의 표현 방식](/regression/pca3.md)  
- [공분산 행렬이 X를 어떻게 나타내는가?](/regression/pca4.md)

 (2) 주요 흐름
- [주성분의 특성](/regression/pcr1.md)
- [주성분을 통해 상관된 변수들 알아내기](/regression/pcr3.md)
- [주성분 회귀모형과 본모형의 관계](/regression/pcr2.md)
- [주성분 회귀를 활용한 다중공선성 제거](/regression/pcr5.md)
- [주성분 직교성에 따른 회귀계수 해석 & 주성분 회귀계수의 편향성](/regression/pcr6.md)
- [주의점](/regression/pcr7.md)

 (3) 테크닉
- [제약 부과 & β에 관한 선형함수 탐색](/regression/pcr4.md)

▶ 3-3) 능형 회귀
- [고유값 분해](/regression/eigen_decomposition.md)
- [회귀계수의 전체분산](/regression/total_var.md)
- [능형 회귀 아이디어](/regression/ridge_idea.md)
- [OLS와 능형회귀의 총분산 비교](/regression/total_var2.md)

■ 변수 선택
- [RMS](/regression/rms.md)
- [Mallows C<sub>p</sub>](/regression/cp.md)
