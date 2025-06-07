# VIF(Variance Inflation Factor)와 Condition index

# ■ VIF (Variation Inflation Factor)

VIF는 직관적인 정의를 따른다. 한 X<sub>j</sub> 변수가 나머지 X 변수들에 의해 얼마나 설명될 수 있는가를 R<sup>2</sup>으로 표현해낸다.

![KakaoTalk_20250607_142848714](https://github.com/user-attachments/assets/de729f48-15bd-4da2-ae6c-5d74335e271f)

R<sub>j</sub><sup>2</sup>의 값이 클수록, VIF의 분모값은 작아지게 되고 결과적으로 전체 VIF 값은 크게 터지게 된다.

![KakaoTalk_20250607_143908175_01](https://github.com/user-attachments/assets/ee4253d6-9dc2-409d-b3e0-dbd6efa9cd87)

따라서 각 X<sub>j</sub>는 VIF 값을 가지게 되며, 이 값이 10을 넘어가게 되면 다중공선성이 있다고 판단한다. 

# ■ Condition index

Condition Index는 (X'X) 행렬의 고유값(eigenvalues)를 활용한다. 상관행렬의 고유값을 고려한다는 것은 해당 데이터가 어떤 분포를 보이는지 확인하는 것이다.
이때 '작은' 고유값이 주목하는 포인트가 되는데, 이는 그 자체로 큰 다중공선성을 의미할 수 있기 때문이다.
아래 그림을 참고하자.

![KakaoTalk_20250607_143908175_02](https://github.com/user-attachments/assets/15038fe4-72d2-4294-88fb-9d5a06683141)

첫번째 그림보다 두 번째 그림에서 두 변수가 더 강한 선형관계를 나타내고 있음을 볼 수 있다. 
강한 선형관계라는 것은 가장 큰 고유값이 길게 늘어진 데 반해, 작은 고유값은 아주 그 폭이 좁은 상태임을 의미한다. 

따라서 Condition index는 이를 반영해, 가장 큰 고유값과 가장 작은 고유값의 비율로 표현된다. 
제곱근이 취해지긴 했지만, 결국 중요한 의미는 고유값 간의 크기 차이이다.
따라서 굳이 Condition index의 모형(제곱근이 취해진 값)을 갖추지 않아도, 고유값만 가지고 있다면 그들 간의 비율 크기로 다중공선성을 짐작해볼 수 있다. 
Condition index의 기준값은 보통 15 정도를 사용한다. 따라서 15라는 것은 가장 큰 고유값과 해당 고유값의 비율이 225배라는 것이다. 

![KakaoTalk_20250607_143908175](https://github.com/user-attachments/assets/2bb34935-d247-410d-b0df-98083d57c851)

다만 VIF도 그렇지만, 고유값은 특정 열과 대응되는 것이 아니기 때문에 
위 기준들을 사용하여 전체 X 데이터 안의 다중공선성 여부는 확인할 수 있지만, 구체적으로 어떤 변수들 간 강한 선형관계가 있는지까지는 알아낼 수 없다. 
따라서 이후 상관행렬을 그리거나 산점도를 확인하여 이를 탐색하는 과정이 필요하다.
