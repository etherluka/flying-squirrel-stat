## 단순 최소제곱법

단순회귀모형에서 최소제곱법을 통해 회귀계수를 구해본다.
단순회귀모형이라면 하나의 x변수를 가지는 모형이므로, 통상 아래와 같이 표현한다.

# y<sub>i</sub> = β<sub>0</sub> + β<sub>1</sub>x<sub>i</sub> + ε<sub>i</sub>

이제 오차제곱을 최소화하는 β를 구하려면, 두 개의 미지수를 가진 함수 관계를 생각해야 한다. 
이변량 함수의 최솟값은 
각 변수에 대한 편미분을 0으로 만드는 식을 조합하여 풀면 된다.

![KakaoTalk_20250723_182910511](https://github.com/user-attachments/assets/02554e36-4dda-4c40-b91b-28f499983bce)

하지만 단순히 편미분을 0으로 만드는 값을 찾는다고 해서, 그 지점이 최솟값을 보장하진 않는다.
그 지점이 Local Minimum일 수도 있고, Local Maximum일 수도 있다.

따라서 이변량 함수의 최솟값을 구하려면 다음과 같은 조건이 만족해야 한다.
여기서 D는 행렬식을 말하는 것으로, 이변량 함수 f의 이차 편도함수로 이루어진 행렬의 행렬식을 말한다.

![KakaoTalk_20250723_182910511_01](https://github.com/user-attachments/assets/eafabac3-1cfa-4459-b0ce-e4a134b90d38)

위 조건이 왜 이변량 함수가 최솟값을 가지는 조건이 될까?
D > 0이라는 것을 알게 되면, f<sub>xx</sub> > 0만 알면 결국 또 다른 변수 y에 대한 f<sub>yy</sub> > 0도 보장된다.
왜냐면 D라는 것은 D= f<sub>xx</sub> f<sub>yy</sub> - (f<sub>xy</sub>)<sup>2</sup>로 계산되는데, 
D가 양수라는 것은 f<sub>xx</sub>와 f<sub>yy</sub>의 부호가 같다는 의미이기 때문이다. (뒤에 빼지는 부분이 음수이므로, 전체가 양수이려면 앞부분이 양수여야 한다.)

f<sub>xx</sub>와 f<sub>yy</sub>의 부호가 같다는 것은 x방향과 y방향의 곡률 부호가 같다는 것이고, 이는 첫번째 이미지에서 볼 수 있듯 최솟값을 가지거나 아니면 최댓값을 가지게 된다.
즉, 두 개의 축에 대해 같은 방향성을 가진다. (saddle point가 나오지 않는다는 이야기이다.)

단순회귀모형의 목적함수는 위 조건을 만족하므로, 최솟값을 가진다고 말할 수 있다. 

다시 본론으로 돌아와 이젠 각 변수에 대해 편미분한 뒤 0으로 놓은 식을 풀어본다. 
먼저 β<sub>0</sub>에 대해 편미분한 식을 푼다. 

![KakaoTalk_20250723_182910511_02](https://github.com/user-attachments/assets/4188aba0-088a-4262-b309-97b1493cb594)

그 다음에는 위에서 구한 식을 만족하는 β<sub>0</sub> 값(β<sub>0</sub> 축 방향으로 최솟값)을 대입하여 두번째 식을 풀어준다.

![KakaoTalk_20250723_182910511_03](https://github.com/user-attachments/assets/1e3ff4ea-d10e-4e7b-a7d0-ea4902a5f150)

위 이미지를 보면 β<sub>1</sub>을 최종 정리하기 전 모양과 'no intercept model', 즉 중심화된 변수들을 다룰 때 β<sub>1</sub>의 모양 간의 관계가 보인다. 

중심화된 변수들로 구한 β<sub>1</sub> 기준으로 볼 때, intercept를 포함한 모델은 분모, 분자에 특정 양을 '뺀 것'과 같은 모양을 하고 있다. 

상수항(intercept)을 포함한 β<sub>1</sub>을 최종 정리하면 다음과 같다. 

![KakaoTalk_20250723_182910511_04](https://github.com/user-attachments/assets/d0837698-6451-4f88-8534-134602412924)

![KakaoTalk_20250723_182910511_05](https://github.com/user-attachments/assets/2818dc04-c717-4a92-a688-b54e7509e879)


