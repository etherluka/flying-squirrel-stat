# 대칭행렬 Eigen vectors의 기저 가능성

# ■ 대칭행렬

대칭행렬은 주대각선을 기준으로 오른쪽 위, 왼쪽 아래에 있는 성분들이 대칭인 행렬을 말한다. 
A<sub>ij</sub> = A<sub>ji</sub>으로 보일 수 있다.

이를 만족하기 위해서는 정방행렬이어야 함도 알 수 있다.
![KakaoTalk_20250523_115501782](https://github.com/user-attachments/assets/8081a1c7-f0bb-46b7-ac9c-dfebf93d752a)

# ■ 대칭행렬의 Eigen vectors의 새로운 기저 가능성

대칭행렬의 Eigen vectors는 서로 직각을 이루게 된다. 따라서 Eigen value가 각각 1인 벡터를 생각해볼 때
평면을 Eigen vector들로 이루어진 행렬로 선형변환(길이가 1이니까 단순 회전이 되겠다)시키면,
이들은 원래 평면의 기저였던 i<sub>^</sub>과 j<sub>^</sub>을 대신할 수 있는 새로운 기저가 될 가능성이 있어보인다.

![KakaoTalk_20250523_115501782_01](https://github.com/user-attachments/assets/54f37853-9a29-44db-98d4-bc5d083de844)


(대칭행렬은 A<sup>T</sup>이 A<sup>-1</sup>가 같다.) 
![KakaoTalk_20250523_115501782_02](https://github.com/user-attachments/assets/4bf459f3-4019-4a2a-973d-00d317ee0a6a)
