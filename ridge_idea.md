# 능형 회귀의 아이디어

X'X 행렬을 상관행렬로 다루기 위해서, 먼저 X를 다음과 같이 표준화를 진행해준다.

![KakaoTalk_20250610_205609196](https://github.com/user-attachments/assets/6dd15336-896e-4016-b3d1-650986f8bdd0)

다음과 같이 두 변수만 있는 X 데이터를 생각해보자. (회귀계수의 분산을 계산할 때 (X'X)<sup>-1</sup>의 대각성분이 곱해진다는 것을 인지한다.)
만약 X1과 X2의 상관관계가 크다면 이는 역행렬에서 대각성분의 분모에 반영된다. 상관계수 r12의 제곱은 최대값이 1이니, 공선성이 클수록 분산은 무한대로 커진다.
역행렬에서 분모에 들어가는 요소들이 1/(ad - bc)라는 것을 고려해볼 때, 이는 1과 r12<sup>2</sup>의 ##상대적 차이의 문제가 된다.

![KakaoTalk_20250610_205609196_01](https://github.com/user-attachments/assets/4f64be65-1338-4dd2-9627-0838fdaf9542)

능형 회귀는 이 상대적 차이를 직관적으로 보호하기 위한 도구이다. 만약 대각성분에 k만큼의 힘을 실어주면
다음과 같이 그것이 역행렬의 대각성분이 되었을 때, 분자는 커지게 또 분모는 작아지게 도움을 준다.

![KakaoTalk_20250610_210520823](https://github.com/user-attachments/assets/d9f2367e-308e-47e1-8425-08a9b79a17f8)

결국 1/(ad - bc)에서 ad 부분을 키움으로써 상대적 차이를 크게 만드는 것이고, 동시에 분자도 k 만큼 커지게 하는 효과를 만들 수 있다.
이와 같은 방법으로 다중공선성에 의해서 회귀계수의 분산이 커지는 것을 막을 수 있다.

# ■ 편향으로서의 k

그러나 OLS 추정량이 최소불편추정량인 것을 감안했을 때, k를 넣는 것은 그만큼 '편향'을 발생시킨다. 
편향이 증가하는 것 만큼, 그를 충분히 상쇄할 분산 감소가 있어야 그 행동이 정당화될 것이다.
따라서 무조건 큰 k를 쓴다고 좋은 것이 아니며, "분산을 안정화시키는 최소 k"를 사용해야 편향을 최소화할 수 있다.
