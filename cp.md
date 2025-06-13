# Mallows C<sub>p</sub>

회귀방정식의 평가 기준으로
p개의 변수만을 사용한 모형의 SSE<sub>p</sub>를 가지고 모형을 평가하는 척도 중 하나가 Mallows의 C<sub>p</sub>이다.

수식은 아래와 같이 생겼다.

![KakaoTalk_20250613_115516534](https://github.com/user-attachments/assets/44191351-837a-4c80-9d67-081399d2c2ce)

이 직관적이지 않은 수식은 기댓값(E(C<sub>p</sub>))이 p가 되도록 설계된 통계량이다.

# E(SSE<sub>p</sub>)
먼저 위 과정을 이해하기 위해서는 SSE<sub>p</sub>의 기댓값을 알아볼 필요가 있다. 
SSE의 구성을 살펴본다.

![KakaoTalk_20250613_115516534_01](https://github.com/user-attachments/assets/e3a824fd-2ed2-4c73-9320-1a4a46a0735d)

p개의 변수로만 만들어진 모형에서 '오차제곱의 합(Sum of Squares errors)'이다. 

이제 여기에 기댓값을 씌워본다.
이는 아래와 같이 세 가지 term으로 분리된다.
![KakaoTalk_20250613_115516534_02](https://github.com/user-attachments/assets/514f8ff5-073b-4886-a6b5-8cdfa7ea7b44)

![KakaoTalk_20250613_115516534_05](https://github.com/user-attachments/assets/7cb1cae3-fb41-46ec-b92c-992d2ba0786c)
![KakaoTalk_20250613_115516534_03](https://github.com/user-attachments/assets/9a3a1e0a-2899-4a63-95cb-f3c0ac61e31c)

이제 SSE<sub>p</sub>에 기댓값을 걸어주면, 기댓값의 선형성에 따라 각 term에 기댓값과 같아지고
결국 아래와 같이 결과가 표현된다.

![KakaoTalk_20250613_115516534_04](https://github.com/user-attachments/assets/a5a51028-eac4-4684-b81d-1d2a4ca70c08)

# E(C<sub>p</sub>)

마지막으로 C<sub>p</sub>에 기댓값을 걸어주면, 위에서 구한 E(SSE<sub>p</sub>)를 이용하여 기댓값이 p가 되는 것을 확인할 수 있다.

![KakaoTalk_20250613_115516534_06](https://github.com/user-attachments/assets/bf2d59d6-83d8-4904-bd55-d226c8aad686)

