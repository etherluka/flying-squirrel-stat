# OLS와 능형회귀의 총분산 비교

다중공선성이 있을 때 능형 회귀를 사용하는 것은 결국 회귀계수의 분산을 작게 만들기 위해서이다. 
따라서 능형 회귀의 총분산이 OLS보다 작아야 할 것이다. 

앞 포스팅에서 OLS 회귀에서의 총분산을 구했으니, 이번에는 능형 회귀의 총분산을 구해 둘을 비교해보자. 

다음과 같이 (X'X)의 고유값을 대각성분으로 가지는 행렬과 고유벡터 P<sub>i</sub>로 이루어진 행렬 P를 정의하자. 
위 관계는 정의에 따라 아래처럼 적힌다.

![KakaoTalk_20250610_234447737](https://github.com/user-attachments/assets/bfc7c7b4-acbf-47a3-9ec5-849129f9350a)

(X'X) 행렬은 대칭행렬이므로, Transpose와 inverse가 같다. 
따라서 아래와 같이 고유값 분해(eigenvalue decomposition)가 가능하다. 

![KakaoTalk_20250610_234447737_01](https://github.com/user-attachments/assets/d0c70c7e-1d97-4a14-a539-28a4d523e2ee)

고유 벡터를 활용해서 OLS식을 다음과 같이 변형해본다. 

![KakaoTalk_20250610_234447737_02](https://github.com/user-attachments/assets/c9965d54-e738-4745-9f83-dab9a8e555bd)

이번에는 능형 회귀로서 K를 삽입해, 능형 회귀계수와 그의 분산을 구해본다.

![KakaoTalk_20250610_234447737_03](https://github.com/user-attachments/assets/769965fb-af32-4751-aad9-41a6f4863448)

따라서 다음과 같이 능형회귀의 총분산과 OLS의 총분산을 비교해볼 수 있다. 능형회귀 분산의 k에 0을 대입하면 OLS 분산이 나오는 것을 확인할 수 있으며,
k의 존재로 능형 회귀의 분산이 OLS보다 더 작아지는 것을 확인해볼 수 있다. 

![KakaoTalk_20250610_234447737_04](https://github.com/user-attachments/assets/0a703dfe-570e-480a-a230-d098c5e3307c)
