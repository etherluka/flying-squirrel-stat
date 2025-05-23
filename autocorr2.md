# 자기상관의 포착

보통은 먼저 그래프를 통해 자기상관의 여부를 포착한다. 이때 오차항이 index에 따라 특정 패턴을 보이는지 관찰하고, 
특정 패턴이란 결국 오차항들이 지역(region) 별로 묶여있는 것을 뜻한다. 

이런 직관을 수량적으로 증명해줄 두 검정 방법을 기록한다.

---
# ■ 연검정(Run Test)

연(run)이란 같은 부호를 가진 연속된 오차항 그룹의 갯수를 말한다. 말로 하면 어려우니 바로 예시를 보도록 한다.

+++ -- ++ --- + -

다음 경우에 연(run)은 6개이다. '+++'이 첫번째 연, '--'가 두 번째 연, '++'가 세 번째 연, '---'가 네 번째 연, '+'가 다섯번째, '-'가 여섯번째이다. 
이렇게 같은 부호의 오차항이 연속된 부근이 하나의 연으로 묶이게 된다.

양의 잔차가 n1개, 그리고 음의 잔차가 n2개 있다면, n1과 n2가 충분히 크고 오차항이 랜덤이라는 가정하에서, 연(run)의 갯수의 기댓값과 분산은

μ = 2 n1n2/ (n1+n2), σ<sup>2</sup>= 2 n1n2(2 n1n2 - n1 - n2)/ (n1+n2)<sup>2</sup>(n1+n2-1)

이는 연(run)이 정규분포를 따른다는 계산에 기반한 것이며, 우리 오차항에서 연의 갯수(위에서 6개)는 z검정의 검정 통계량이 된다.

이렇게 연(run)의 갯수를 세어 검정통계량을 구하고
이를 z검정을 통해 우리의 오차항이 랜덤하게 이루어진 것인지, 아니면 특정한 패턴을 따른다고 봐야 하는 것인지 결정할 수 있다.

---
# ■ 더빈-왓슨(Durbin-Watson) 검정

먼저 자기상관을 어떻게 수식으로 표현할 수 있는지 살펴보자. 

ε<sub>t</sub>= ρε<sub>t-1</sub> + w<sub>t</sub>

ρ는 ε<sub>t-1</sub>과 ε<sub>t</sub>의 상관계수로, |ρ|<1로 가정한다. 
w<sub>t</sub>는 평균이 0이고 분산이 상수인 정규분포를 따른다. 이른바 백색오차라고 할 수 있을 것이다. 

결국 더빈-왓슨 검정은 ρ가 0인지 아닌지 검정하는 작업이 된다고 할 수 있다. (오차항끼리는 독립적이어야 한다는 것을 기억하는가?)

먼저 ρ가 어떻게 계산되는지부터 살펴보도록 하자.
t=1일 때 ε<sub>t-1</sub>은 존재하지 않으므로, 두 벡터는 모두 t=2부터 시작하는 것을 알 수 있다. 따라서 총 n-1개의 데이터 포인트에 대한 상관계수가 된다.
![KakaoTalk_20250511_213403154](https://github.com/user-attachments/assets/0de1d179-2f22-4495-a275-b318a6fc4fd5)

e<sub>t</sub>의 평균은 0이 되므로, 상관계수 공식은 다음과 같이 변형이 된다.
![KakaoTalk_20250511_213403154_01](https://github.com/user-attachments/assets/9deb2272-57f8-4ab8-806e-a9485d97043d)

마지막은 더빈-왓슨 통계량이다. 
모형에 의해 추정량 e<sub>t</sub>는 ε<sub>t</sub>와 달리 왜곡되는 면이 있기에,
이 통계량에서는 e<sub>t</sub>와 e<sub>t-1</sub>의 차이를 직접 계산한다.

왜 추정량 e<sub>t</sub>는 모형에 의해 왜곡이 되는지, 위 방식이 e<sub>t</sub>의 왜곡 정도를 어떻게 보정하는지는 아직 알지 못하기에
이는 향후 포스팅의 좋은 주제로 남겨두도록 한다. 
![KakaoTalk_20250511_213403154_02](https://github.com/user-attachments/assets/cb067578-4a38-43a2-9415-e137dd935ea6)

계산이 암시하고 있는 내용을 생각해보면, 통계량의 분자가 e<sub>t</sub>와 e<sub>t-1</sub>의 차이들의 합이기 때문에 
통계량이 0에 가까우면(분모, 분자 모두 제곱의 형태이기 때문에 음수는 나올 수가 없다), 연이은 두 오차항(e<sub>t</sub>와 e<sub>t-1</sub>) 간의 사이들이 다 0에 가깝다는 것이기에
서로 굉장히 닮아있다는 의미가 된다. 따라서 둘의 상관계수인 ρ도 클 수밖에 없다. 

반면 분자 값이 크다는 의미는, 연이은 두 오차항 간의 거리가 크다는 의미가 될 것이고
오차항 e<sub>t</sub>의 평균은 0이 된다는 것을 감안해볼 때 0 수평선을 기준으로 위 아래로 랜덤하게 퍼져있는 오차항의 모습을 상상해볼 수 있다.

더빈-왓슨 통계량 d는 2(1-ρ)라는 관계가 있다고 알려져 있고,
d는 [0, 4] 사이의 값을 가지게 된다.
