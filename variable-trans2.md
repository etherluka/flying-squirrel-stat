# 변수변환(분산 안정화 변환)

이번에는 변수변환을 분산 안정화를 위해 사용할 수 있다. OLS에서는 회귀계수의 검정을 위해 등분산성이 요구되는데, 변수변환을 통해 이분산성 문제를 해결할 수 있다.

예를 들어 Y<sub>i</sub>~Poisson(M<sub>i</sub>)라고 해보자.

![KakaoTalk_20250507_223226342](https://github.com/user-attachments/assets/7d821ca9-98af-4b49-9327-643c9009afc7)

Poisson 분포의 특징은 E(X)=Var(X)=M로 기댓값과 분산이 같다는 것이다. 

따라서 OLS 직선(평면)에서 Ŷ<sub>i</sub>이 커져감에 따라(기댓값이 커져감에 따라) 분산도 함께 커지는 이분산성이 나타난다. 
그럴 때 Y<sub>i</sub>에 &radic;를 취하는 변환을 사용하면 분산을 상수로 고정시킬 수가 있게 된다.

---
# Delta Method

테일러 전개를 통해 분산을 표현하는 방법을 Delta Method라고 한다. 포아송 분포를 따르는 Y<sub>i</sub> 역시 &radic;을 취한 값을 테일러 전개를 하여 분산을 표현할 수 있다.

![KakaoTalk_20250507_223226342_01](https://github.com/user-attachments/assets/24bfa2a4-7657-48db-9e4a-de14e2112e05)

이제 분산을 전개해보면 &radic;를 취했을 때 그 분산이 상수로 수렴(다시 말해 등분산성 만족)하는 모습을 확인할 수 있다. 

![KakaoTalk_20250507_223226342_02](https://github.com/user-attachments/assets/d895bba5-9885-4e63-8e88-da3d55d89243)
