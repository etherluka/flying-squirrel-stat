# 상관된 오차항의 문제

자기상관이란 관측값들이 얻어지는 자연스러운 순서에 따라 그들이 서로 연관되어 있는 경우를 말한다. 
## cov(ε<sub>i</sub>, ε<sub>j</sub>), i≠j 
이는 오차항(ε)은 서로 독립이라는 회귀모형 가정에 기반한다. 

따라서 자기상관이란 개념은 '시계열 데이터'에서 유효하다. 횡단면 데이터에서 관측값이 나타나는 순서라는 것은 임의적일 수밖에 없기 때문이다. (애초에 순서가 있는 데이터가 아니니)

# ■ 자기상관의 원인 해결

- 자기상관은 데이터 해석에 중요한 '시간과 관련된 변수'를 모형에 포함하지 못했을 때 발생할 수 있다. 즉, 자기상관으로 나타나는 데이터의 패턴을 고정시켜줄 설명변수의 부제를 의미할 수 있다.
따라서 이런 경우 그 변수를 모형에 포함시켜주면 자연스럽게 자기상관은 해결된다.

- 위와 달리 데이터가 순수한 자기상관을 가지는 경우, 데이터 변환을 통하여 해결될 수 있다. 여기서는 Cochrane-Orcutt가 제한한 자기상관을 없앤 OLS 추정방식을 소개하도록 한다.
