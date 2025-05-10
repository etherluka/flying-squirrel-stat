# 가중최소제곱법 (WLS) 세 번째 사례

이번에는 이분산성의 구체적인 구조를 표본에 근거하여 '경험적'으로 결정하는 경우를 살펴본다.

가장 좋은 것은 
연구자가 탁월한 직관으로 데이터를 몇 개의 그룹으로 나누고, 
각 그룹 내의 분산을 구해 가중치로 사용하는 방법이다.

등분산성이 어긋나는 상황을 대수적으로 조사하는 한 가지 방법은
고정된 x값들을 두고 그에 해당하는 데이터를 여러번 뽑아내는 것이다. 그림을 보면 쉽게 이해가 간다.

![스크린샷 2025-05-10 145751](https://github.com/user-attachments/assets/77d5da55-67bf-407c-9afa-c89320fcdc1d)

등분산 가정이란, 
모든 x에 대해 y 조건부 분포의 분산이 같아야 한다는 것이다. 

![스크린샷 2025-02-03 135432](https://github.com/user-attachments/assets/4911ff37-5703-4720-9edb-6adb4b281a30)

따라서 방금 소개한 '고정된 특정 x들에 대해 y를 반복적으로 뽑는다'는 이야기는
y|x 조건부 분포를 직접 만든다는 말과 같다. (위 이미지의 아이디어 참고)

물론 데이터를 특정 그룹으로 나눈 연구자의 선택이 좋은 것이었다면
각 x값에 대해 체계적으로 다른 분산의 모양이 나타나게 될 것이고
이 분산들을 각 그룹에 대한 가중치로 사용해주면 된다. 

---
다음 모형을 생각해본다.

![KakaoTalk_20250510_153652174](https://github.com/user-attachments/assets/1eee59d7-641e-4acf-8ffe-3e496acd5113)

오차에 대한 분산은 다음과 같이 나타날 것이다. 이는 우리가 j개로 나눈 각 그룹 내에서는 데이터들이 같은 분산을 따른다는 것을 의미한다.
(i에 대해서는 변동하지 않고, j에 대해서만 달라진다.)

![KakaoTalk_20250510_153652174_01](https://github.com/user-attachments/assets/8b33d6c5-20e9-466f-a7c6-bf80c477a93c)

이 각 그룹에 대한 분산을 구해보면 다음과 같이 나타낼 수 있다.
![KakaoTalk_20250510_153652174_02](https://github.com/user-attachments/assets/273833ee-707e-4ddd-9d4f-90d96d9b6332)

이 각 그룹에 대한 분산을, 전체 분산을 이용해서 표현해본다. 그러면 공통된 상수 σ를 제외하고, 그룹에 대해 변동하는 부분을 C<sub>j</sub>으로 표시할 수 있다. 
![KakaoTalk_20250510_153652174_03](https://github.com/user-attachments/assets/77ddd6cb-60b9-46d1-b8e1-7c5563c53398)

사실상 이 C<sub>j</sub> 부분이 그룹 간의 분산 차이를 나타내는 부분이 될 것이다. 따라서 C<sub>j</sub>로 가중치를 구성할 수 있다.
위 이미지에 있는 식을 C<sub>j</sub>에 대한 식으로 만들어주고, 각 값들은 다음과 같이 구할 수가 있다.
![KakaoTalk_20250510_153652174_04](https://github.com/user-attachments/assets/beaa1be3-4d63-4be5-b3d6-cbf9502d48bd)

최종적으로는 다음과 같이 가중치를 사용하게 된다.
![KakaoTalk_20250510_153652174_05](https://github.com/user-attachments/assets/bea67b02-13e2-4abc-b60a-50b0c6e0120f)

