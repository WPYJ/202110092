# 임베디드 시스템(Embedded System)

## ▶라즈베리파이 & 카메라

<img src = "https://github.com/user-attachments/assets/ca43e67d-21d8-4207-9233-9e52a7988ae3" width="500" height="300">

**1. 라즈베리파이와 카메라 모듈 연결(+온습도센서)**

<img src = "https://github.com/user-attachments/assets/993d4ef7-0b80-4974-b008-c8f78c7cd3ba" width="550" height="300">
<img src = "https://github.com/user-attachments/assets/fa4b0cc0-05f9-48a3-840e-a7aeaf7f6b87" width="550" height="300">

**2. 카메라 사용을 위한 관련 라이브러리 설치**

<img src = "https://github.com/user-attachments/assets/9e934c83-7a5b-474b-8b8d-fcdf315dd281" width="550" height="300">

**3. ***fswebcam*** 명령어를 이용하여 'image_cam' 이라는 사진 촬영**

<img src = "https://github.com/user-attachments/assets/0e27ec1c-b253-42fd-823f-5fd18bc81657" width="550" height="300">

**4. Viewer에 접속 후 해당 이름으로 된 사진이 있다.**

## ※ 그외 추가 옵션 - 고해상도 촬영법

<img src = "https://github.com/user-attachments/assets/1b61037f-d695-4597-9d9a-3ba579b6922e" width="550" height="300">

**1. 상단 [3]번의 과정에서 원하는 해상도 설정**

<img src = "https://github.com/user-attachments/assets/e345abb2-9ae7-4c36-93f9-25dea36a2cec" width="550" height="300">

**2. 위의 결과물과 비교하여 픽셀 사이즈(해상도)가 커졌음**

## ▶온습도센서 & 카메라와 Node-Red

**노드 구성**

<img src = "https://github.com/user-attachments/assets/465c13fd-5443-4731-b1bb-3c01139dc83c" width="550" height="300">

**대시보드 설정**

<img src = "https://github.com/user-attachments/assets/95da3605-3850-405e-b635-e1dc4c50f272" width="550" height="400">

***base64 노드***

<img src = "https://github.com/user-attachments/assets/73c7ae20-d5f2-47e9-b689-c20335d070fc" width="550" height="400">

***image 노드***

<img src = "https://github.com/user-attachments/assets/f2f5cb83-4e96-4f87-b2d7-1e63617cc3e8" width="550" height="400">

***주황색 템플렛 ->img src="data:image/jpeg;base64,{{payload}}" alt="Image" style="max-width: 100%;"***

<img src = "https://github.com/user-attachments/assets/3e97a525-9ae0-454d-9017-41c5d5150100" width="550" height="400">

***초록색 템플렛***

<img src = "https://github.com/user-attachments/assets/588fc037-8bf3-470f-a25f-6385c57b1fed" width="550" height="400">

**결과**

<img src = "https://github.com/user-attachments/assets/98f3e1dd-550f-416c-b27f-e2f9b913b78f" width="550" height="300">


