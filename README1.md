# 임베디드 시스템(Embedded System)


## 목차
[1. 원격 접속 및 제어를 위한 도구](#1-원격-접속-및-제어를-위한-도구)  
[2. 접속 환경 구축 방법](#2-접속-환경-구축-방법)


## 1. 원격 접속 및 제어를 위한 도구

* SSH(Secure Shell) : 네트워크에서 보안된 원격 접속을 제공하는 프로토콜
  * 원격 서버 접속
  * 데이터 암호화로 인한 보안 강화
  * 보안이 중요한 환경에서 주로 사용
 
* PuTTY : SSH나 Telnet 등 여러 네트워크 프로토콜을 지원하는 무료 터미널 에뮬레이터
  * 직관적이고 간단함
  * 윈도우 환경에서 가장 널리 사용되는 프로그램

* VNC(Virtual Network Computing) : 다른 컴퓨터의 데스크톱 화면을 원격으로 볼 수 있는 그래픽 원격 접속 프로토콜
  * 다수의 사용자가 동시에 같은 화면을 볼 수 있음
  * 원격 데스크톱 접속을 통해 컴퓨터 제어
  * 팀 간의 원격 협업 가능  

## 2. 접속 환경 구축 방법

#### 1. 모바일 핫스팟

▶ **설정** → **네트워크 및 인터넷** → **모바일 핫스팟**

<img src = "https://github.com/user-attachments/assets/f8bc76a1-a70a-4c60-b069-8a14860eb016" width="550" height="330">

#### 2. PuTTY, RealVNC VIewer 설치

<img src = "https://github.com/user-attachments/assets/6f2b978b-a3d0-46b3-a50f-1a4055bf2cd8" width = "550" height = "330"> 

<img src = "https://github.com/user-attachments/assets/a8d10cf4-1cf4-4c78-b6d1-5b2cf212de7a" width = "550" height = "330">

#### 3. 라즈베리 파이에 전원 공급
#### 4. PuTTY 실행 후 IP 주소 입력

<img src = "https://github.com/user-attachments/assets/3817630e-5503-4fb0-bf47-565745e36f2d" width = "550" height = "330">

#### 5. 로그인

<img src = "https://github.com/user-attachments/assets/c67e911b-3fca-4568-b658-a2da9d16c396" width = "550" height = "330">

▶ **ID : pi**  
▶ **PW : raspberry(입력해도 변동없음)**

#### 6. 로그인 후 명령어 입력

<img src = "https://github.com/user-attachments/assets/941e0c86-f5f0-42bb-8ed9-aa7d82fb88d1" width = "550" height = "330">

▶ **sudo raspi-config 입력** 

#### 7. 설정하기

<img src = "https://github.com/user-attachments/assets/cce5ccc5-b763-440d-afff-330782603788" width = "550" height = "330">

**7-1 Advanced Options -> Wayland -> X11 후 Finish(재부팅)**  
**7-2 종료 후 다시 [4], [5], [6]번 반복**  
**7-3 Interface Options -> VNC -> Yes**

#### 8. PuTTY 종료 후 RealVNC Viewer 실행 및 조작

<img src = "https://github.com/user-attachments/assets/6391cd24-110e-4b4b-9912-fc1509669a3e" width = "550" height = "330">

▶ **File → New connection**

#### 9. RealVNC Viewer 설정

<img src = "https://github.com/user-attachments/assets/7c31fbbe-a109-41e0-a9cd-68cb1ed49993" width = "600" height = "500">

▶ **VNC Server에 [5]번에서 사용했던 IP 주소 입력**   
▶ **접속 후 Username, PW는 [6]번과 동일**










