# 표준화의 종류와 상관계수 계산

# ■ 표준화의 종류

크게 두 가지 표준화 방법을 소개하고자 한다. 

![KakaoTalk_20250605_224909857](https://github.com/user-attachments/assets/abe9b83e-3124-4812-8761-7f1a18cf1f08)

먼저 첫번째는 기초 통계학에서 주로 다루는 표준화 방법이다. 각 관측치에서 평균을 빼 중심화를 하고, 표준편차로 나누어서 단위를 바꾸는 것이다.
이번에 주목해서 볼 표준화 방법은 두 번째이다. 중심화까지는 같지만, 표준편차로 나누는 것이 아니라 제곱합으로 나누었다.
'벡터 정규화'라고도 표현한다.

이는 길이를 통일하는 의미가 있다. X<sub>i</sub>-mean(X)이 각 관측치가 되니, 그 관측치들을 모두 합친 것에서 각 관측치의 상대적 크기를 측정한다.
(여기에 100을 곱해면 백분율과 같은 형태가 될 것이다.) 

다만 중심화된 관측치들의 총 합은 항상 0이 되니, 제곱합의 제곱근으로 위 상황을 표현한 것뿐이다. 

이는 마치 X'<sub>i</sub> 벡터를 그 크기(norm)로 나누어, '단위벡터'를 만든 것과 같다. 
각 관측치 제곱합의 제곱근으로 표현되는 norm의 정의와도 정확히 들어맞는다.

# ■ 표준화 벡터와 상관계수

피어슨의 상관계수는 다음과 같이 표현된다. 이 Raw 벡터로 계산한 상관계수로부터
중심화된 벡터, 표준화된 벡터로 변형해가며
결국 최종적으로는 표준화된 벡터의 dot product인 단순한 형태로 상관계수가 표현됨을 보일 것이다.

먼저 중심화된 벡터로 상관계수 공식을 재표현해준다.

![KakaoTalk_20250605_224909857_01](https://github.com/user-attachments/assets/bddd414d-c22d-43ca-b4b8-4d296d07a62d)

이제 이 중심화된 X' 벡터를 norm으로 나누어서 표준화를 해준 뒤, 그를 그대로 상관계수 공식에 대입해준다.

![KakaoTalk_20250605_224909857_02](https://github.com/user-attachments/assets/4e48ea63-d08d-4def-a956-62042b3b7c88)

모든 항에 루트 제곱합이 곱해져 있으므로, 이들을 따로 꺼내 묶어줄 수 있다.
그들은 분모에 있는 루트 제곱합과 정확히 일치하므로, 약분이 된다. 

![KakaoTalk_20250605_224909857_03](https://github.com/user-attachments/assets/944170df-fa19-442a-b2c3-145b3345a578)

따라서 최종적으로 피어슨 상관계수는 길이에 의해 표준화된 벡터들의 내적(dot product)으로 표현될 수 있음을 확인할 수 있다.
