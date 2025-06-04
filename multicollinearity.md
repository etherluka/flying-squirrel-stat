# 다중공선성 문제

# ■ 예시 모형

다음과 같은 데이터로 회귀모형을 만들어보고자 한다. X1, X2, y 세 개의 벡터가 있으며, 이들 모두 표준화된 상태이다. 
따라서 평균은 0, 분산은 1을 가지고 있다. 

![KakaoTalk_20250604_234811721_01](https://github.com/user-attachments/assets/4215ea48-9fc1-4500-82bc-6bb2d4efeae7)

다음과 같은 모형을 고려해보자. X1, X2 두 개의 설명변수만 있는 선형회귀모형이다.
위에서 본 것처럼 표준화를 한 상태이므로, 상수항은 없는 모형이 만들어질 것이다.

![KakaoTalk_20250604_234811721](https://github.com/user-attachments/assets/a3fa5867-9839-4da8-a4ea-7e1161fa637f)

# ■ (X<sup>T</sub>X)<sup>-1</sup>

바로 이전 포스팅에서 살펴본 것처럼, 회귀계수의 분산은 (X<sup>T</sub>X)<sup>-1</sup>σ으로 표현된다.
따라서 표준화된 X 데이터일 때 상관계수 행렬이 되는 (X<sup>T</sub>X)<sup>-1</sup>를 살펴보아야 한다.

![KakaoTalk_20250604_234811721_02](https://github.com/user-attachments/assets/4d2d44a0-8345-43b9-8cba-f7d4b286a32f)

상관계수 행렬의 각 요소(element)는 교차하는 두 변수의 dot product로 이루어져 있다. 따라서 두 벡터가 서로 얼마나 닮았는지를 나타낸다.
우리가 원하는 (X<sup>T</sub>X)<sup>-1</sup>를 구하기 위해서는, 이 상관계수 행렬의 역행렬을 구해주어야 한다. 
다행히 X 변수가 2개인 상황이므로, 잘 알려진 2×2 행렬의 역행렬 공식을 이용해 다음과 같이 행렬을 표현해낸다. 

![KakaoTalk_20250604_234811721_03](https://github.com/user-attachments/assets/0e8c6dca-7750-4a4e-bdc1-eb0bffe84fca)

# ■ 회귀계수의 분산-공분산 행렬

미리 알고 있는 회귀계수의 분산 공식에 따라 다음과 같이 분산-공분산 행렬을 써본다. 
## 행렬에서 볼 수 있듯이, '회귀계수의 분산'은 분산-공분산 행렬에서 대각원소들에 해당한다. 

![KakaoTalk_20250604_234811721_04](https://github.com/user-attachments/assets/0068a28f-62fc-4536-87d6-f9b6c77d0c12)

회귀계수의 분산은 다음과 같이 작성할 수 있다. 이때 분모의 구조가 '1-r<sub>12</sub>'이란 걸 확인할 수 있다.

![KakaoTalk_20250604_234811721_05](https://github.com/user-attachments/assets/690c97d7-8580-474e-925d-ee9bf2cc0ecb)

따라서 두 변수 X1, X2 간의 상관계수(선형적 관련성)가 커질수록, 회귀계수의 분산은 극도로 커지게 된다. (분모가 커지므로)
그에 따라 회귀계수 추정량은 분산이 아주 큰, 다시 말하면 뽑을 때마다 달라지는 '매우 불안정한' 값이 된다.

이것이 바로 다중공선성이 초래하는 문제점이다.

