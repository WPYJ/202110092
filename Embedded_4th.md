# 임베디드 시스템 정리

## 목차
### 1. Raspberry Pi에서 PCle
### 2. Raspberry Pi에서 GPIO  
### 3. Raspberry Pi에서 I2C SPI UART
### 4. 기초전자
  
  
## 1. Raspberry Pi에서 PCle(Peripheral Component Interconnect Express)

  * 고속 데이터 전송을 위한 **직렬 통신 인터페이스**
  * 컴퓨터와 외부 하드웨어 장치 간의 연결을 가능하게 함
  * 고성능 그래픽 카드, NVMe SSD, 네트워크 카드 등 다양한 장치 연결
  * 기본적으로는 USB 포트로 활용되지만, 특정 보드에서는 PCIe 슬롯으로 전환 가능


## 2. Raspberry Pi에서 GPIO(General Purpose Input/Output)

  * 디지털 신호를 입력받거나 출력할 수 있음(ex.신호받고 LED를 제어)
  
  * 전자 회로와의 상호작용을 위한 범용 핀  
      * GPIO 핀의 주요 기능  
        * 입력: 스위치 등 외부 장치로부터 신호 수신
        * 출력: LED 같은 장치 제어
        * PWM: 서보 모터와 같은 장치의 속도 및 위치 제어
        * I2C, SPI, UART: 통신 프로토콜을 사용한 외부 장치와의 데이터 교환
  <img src = "https://github.com/user-attachments/assets/82489b85-dadd-4ff0-abca-684e60acdcea" width="550" height="330">


  ## 3. Raspberry Pi - I2C(Inter-Integrated Circuit), SPI(Serial Peripheral Interface), UART(Universal Asynchronous Receiver-Transmitter)

  * I2C 특징 
    * 속도: 기본 속도는 100kHz, 최대 3.4MHz
    * 주소: 각 슬레이브 장치는 고유한 주소를 가짐
    * 핀이 적음: 두 개의 라인으로 여러 장치를 연결 (SDA: 데이터, SCL: 클럭)

  * SPI 특징
    * UART: 빠른 속도: MHz 단위의 빠른 데이터 전송 (최대 10MHz 이상)
    * 고해상도 디스플레이, SD 카드 등에 쓰임

        * 4개의 주요 핀:  
          **1**. MOSI (Master Out Slave In): 마스터에서 슬레이브로 데이터 전송  
          **2**. MISO (Master In Slave Out): 슬레이브에서 마스터로 데이터 전송  
          **3**. SCK (Serial Clock): 마스터가 제공하는 클럭 신호  
          **4**. CS (Chip Select): 슬레이브 장치를 선택  

  * UART 특징
    * 단일 장치 간 통신: 두 장치 간의 직렬 통신, 마스터-슬레이브 개념 없음
    * 핀이 적음: TX(전송), RX(수신) 두 개의 핀만 사용
    * 시리얼 콘솔, GPS 모듈, 블루투스 모듈에 쓰임


  * **최종 비교**
    * 속도: SPI > I2C > UART
    * 복잡성: SPI가 가장 복잡, I2C는 간단한 주소 체계, UART는 점대점 간 통신
    * 핀이 필요: SPI(4개 이상) > I2C(2개) > UART(2개)
    * 장치 수: I2C는 여러 슬레이브 가능, SPI는 여러 슬레이브 가능, UART는 1:1 통신


    # 기초전자
    * 전압과 전류
      * 전압 : 전기를 공급하기 위해 사용되는 전기적인 차이[단위 : 볼트(V)]
      * 전류 : 흐르는 전기의 양을 나타냄[단위 : 암페어(A)]

    * 옴의 법칙
      * 전압 = 전류 * 저항(전류가 증가하면 전압도 증가함)
      * 전류는 저항과 반비례(저항이 증가하면 전류는 감소함)
      * 저항은 전압과 비례(저항이 증가하면 전압도 증가)
    
    * 아날로그 신호와 디지털 신호
      * 아날로그 신호 : 연속적인 값으로 표현되는 신호이며 시간에 따라 연속적으로 변화함(ex. 소리, 음악, 온도)
      * 디지텅 신호 : 이산적인 값으로 표현되는 신호이며 시간에 따라 특정 간격으로 값이 변화하고 0과 1로 정보를 전달함

    * 직류와 교류
      * 직류 : 전압의 크기와 방향이 일정하게 유지되는 전류의 형태(ex. 건전지)
      * 교류 : 시간에 따라 전압의 크기와 방향이 주기적으로 변하는 전류의 형태. 가정에서 주로 쓰이는 전기가 교류임

    * PWM(Pulse Width Modulation)
      * 주로 LED의 밝기를 조절하거나 모터의 출력을 조절함
      * 예를 들어 10V에서 ON이 되어있는 시간(Duty Cycle)을 50%로 한다면 LED나 모터는 5V의 출력을 가짐
     
    * 수동소자와 능동소자
      * 수동소자 : 전기적 에너지를 소모, 축적, 통과하는 일만 함, 단독으로도 동작 가능함.(ex. 저항, 인덕터, 캐패시터)
      * 능동소자 : 작은 신호를 큰 출력으로 변화는 일을 함, 다른 곳에서 에너지를 얻어야만 함.(ex. 트랜지스터, 다이오드)
      * 다이오드 : 전류를 일정한 방향으로 흐르게끔 도와주는 소자
      * 트랜지스터 : 전기 신호를 증폭하거나 스위칭하는 기능을 가진 소자.(ex. 작은 소리를 크게 출력해주는 스피커, 전원을 켜고 끄는 스위치)
     
    * 저항, 인덕터, 캐패시터
      * 저항 : 전류의 흐름을 방해하는 소자이며 열로 에너지를 소모함
      * 인덕터 : 전류가 흐를 때 자기장을 만들어 전류의 변화를 막는 소자임
      * 캐패시터 : 전기적 에너지를 일시적으로 저장하는 소자임
     
    ### ★★저항 읽는 법★★


#### 4색 띠 저항 읽는 법

4색 띠 저항에서의 순서

1. **첫 번째 띠**: 첫 번째 숫자
2. **두 번째 띠**: 두 번째 숫자
3. **세 번째 띠**: 배율 (숫자를 몇 배로 곱할지)
4. **네 번째 띠**: 허용 오차 (저항 값의 정확도)

#### 5색 띠 저항 읽는 법

5색 띠 저항에서의 순서서

1. **첫 번째 띠**: 첫 번째 숫자
2. **두 번째 띠**: 두 번째 숫자
3. **세 번째 띠**: 세 번째 숫자
4. **네 번째 띠**: 배율
5. **다섯 번째 띠**: 허용 오차

## 저항 색 띠 표 (Color Code)

<img src = "https://github.com/user-attachments/assets/096f9d3f-6faf-4d2e-98be-1f14417d9d98" width="550" height="330">

## 실습해보기

### 단순 LED 제어
* 코드   * 장치 수: I2C는 여러 슬레이브 가능, SPI는 여러 슬레이브 가능, UART는 1:1 통신


    # 기초전자
    * 전압과 전류
      * 전압 : 전기를 공급하기 위해 사용되는 전기적인 차이[단위 : 볼트(V)]
      * 전류 : 흐르는 전기의 양을 나타냄[단위 : 암페어(A)]

    * 옴의 법칙
      * 전압 = 전류 * 저항(전류가 증가하면 전압도 증가함)
      * 전류는 저항과 반비례(저항이 증가하면 전류는 감소함)
      * 저항은 전압과 비례(저항이 증가하면 전압도 증가)
    
    * 아날로그 신호와 디지털 신호
      * 아날로그 신호 : 연속적인 값으로 표현되는 신호이며 시간에 따라 연속적으로 변화함(ex. 소리, 음악, 온도)
      * 디지텅 신호 : 이산적인 값으로 표현되는 신호이며 시간에 따라 특정 간격으로 값이 변화하고 0과 1로 정보를 전달함

    * 직류와 교류
      * 직류 : 전압의 크기와 방향이 일정하게 유지되는 전류의 형태(ex. 건전지)
      * 교류 : 시간에 따라 전압의 크기와 방향이 주기적으로 변하는 전류의 형태. 가정에서 주로 쓰이는 전기가 교류임

    * PWM(Pulse Width Modulation)
      * 주로 LED의 밝기를 조절하거나 모터의 출력을 조절함
      * 예를 들어 10V에서 ON이 되어있는 시간(Duty Cycle)을 50%로 한다면 LED나 모터는 5V의 출력을 가짐
     
    * 수동소자와 능동소자
      * 수동소자 : 전기적 에너지를 소모, 축적, 통과하는 일만 함, 단독으로도 동작 가능함.(ex. 저항, 인덕터, 캐패시터)
      * 능동소자 : 작은 신호를 큰 출력으로 변화는 일을 함, 다른 곳에서 에너지를 얻어야만 함.(ex. 트랜지스터, 다이오드)
      * 다이오드 : 전류를 일정한 방향으로 흐르게끔 도와주는 소자
      * 트랜지스터 : 전기 신호를 증폭하거나 스위칭하는 기능을 가진 소자.(ex. 작은 소리를 크게 출력해주는 스피커, 전원을 켜고 끄는 스위치)
     
    * 저항, 인덕터, 캐패시터
      * 저항 : 전류의 흐름을 방해하는 소자이며 열로 에너지를 소모함
      * 인덕터 : 전류가 흐를 때 자기장을 만들어 전류의 변화를 막는 소자임
      * 캐패시터 : 전기적 에너지를 일시적으로 저장하는 소자임
     
    ### ★★저항 읽는 법★★


#### 4색 띠 저항 읽는 법

4색 띠 저항에서의 순서

1. **첫 번째 띠**: 첫 번째 숫자
2. **두 번째 띠**: 두 번째 숫자
3. **세 번째 띠**: 배율 (숫자를 몇 배로 곱할지)
4. **네 번째 띠**: 허용 오차 (저항 값의 정확도)

#### 5색 띠 저항 읽는 법

5색 띠 저항에서의 순서서

1. **첫 번째 띠**: 첫 번째 숫자
2. **두 번째 띠**: 두 번째 숫자
3. **세 번째 띠**: 세 번째 숫자
4. **네 번째 띠**: 배율
5. **다섯 번째 띠**: 허용 오차

## 저항 색 띠 표 (Color Code)

<img src = "https://github.com/user-attachments/assets/096f9d3f-6faf-4d2e-98be-1f14417d9d98" width="550" height="330">

## 실습해보기

### 단순 LED 제어

* 코드
<img src = "https://github.com/user-attachments/assets/cb809aa0-536e-4139-bb2f-54ad2e4c80b0" width="550" height="330">

* 파이썬 구동
<img src = "https://github.com/user-attachments/assets/78e68b9a-9e34-46b4-9951-ddda0b154c5a" width="550" height="330">

* 결과  
<img src = "https://github.com/user-attachments/assets/5176c4c1-6fd6-48ca-a7a4-5f6102989cc4" width="550" height="330">

### 풀 업(Pull-Up) 예제

* 코드
<img src = "https://github.com/user-attachments/assets/cca19d80-9a4d-4398-ba3f-31dd90db5503" width="550" height="330">

* 파이썬 구동
<img src = "https://github.com/user-attachments/assets/d97f959d-a846-401e-9a92-0ca329e185ca" width="550" height="330">
<img src = "https://github.com/user-attachments/assets/d92c4496-0685-45c2-bb2c-7e4a06e3d6be" width="550" height="330">

* 결과
<img src = "https://github.com/user-attachments/assets/a5613349-8f3a-4c87-b52b-ea8771d3dd73" width="550" height="330">
<img src = "https://github.com/user-attachments/assets/3af2b39e-55f6-465b-801e-f47343fdf980" width="550" height="330">

### 풀 다운(Pull-Down) 예제

* 코드
<img src = "https://github.com/user-attachments/assets/a4d2c0b3-c8dd-4434-921d-17b540a2cf7d" width="550" height="330">

* 파이썬 구동
<img src = "https://github.com/user-attachments/assets/edb2d36c-9d39-469b-8e81-9e067c02baa8" width="550" height="330">
<img src = "https://github.com/user-attachments/assets/0da14cbe-46b2-40d1-a75b-4bda98ecefb9" width="550" height="330">

* 결과
<img src = "https://github.com/user-attachments/assets/ba295a0b-a5e2-4eab-aa7b-aa384bb699d7" width="550" height="330">
<img src = "https://github.com/user-attachments/assets/12ae35df-5c8a-4d56-9496-3e58ecd87cc6" width="550" height="330">








