# 임베디드 시스템(Embedded System)

## 목차  
[1. 컴퓨터 기술의 용어 및 이해](#1-컴퓨터-기술의-용어-및-이해)  
[2. 임베디드 시스템이란?](#2-임베디드-시스템이란)  
[3. 임베디드 시스템의 특징](#3-임베디드-시스템의-특징)  
[4. 임베디드 시스템의 구성요소](#4-임베디드-시스템의-구성요소)  
[5. 임베디드 시스템의 장단점](#5-임베디드-시스템의-장단점)  
[6. 임베디드 시스템의 미래](#6-임베디드-시스템의-미래)  



## 1. 컴퓨터 기술의 용어 및 이해
컴퓨터의 구성요소 -> CPU, 메모리, 저장 장치, 입출력 장치....

1. CPU : **명령어를 해석하고 실행**하거나 **산술 및 논리 연산**을 맡는다.
2. 마이크로프로세서 : **CPU의 기능이 반도체 칩에 통합**된 형태를 말한다. Intel이나 AMD 등에 쓰인다.
3. 마이크로컨트롤러(MCU) : 메모리, 입출력 포트를 하나에 통합하여 특정 작업, 반복되는 작업을 처리한다.
4. SoC : 메모리, 입출력 장치, 프로세서 등이 **하나의 칩에 통합**되어 주로 모바일 기기에 쓰인다.

[자세히](https://velog.io/@hyunji015/%EC%BB%B4%ED%93%A8%ED%84%B0-%EA%B5%AC%EC%A1%B0-%EC%BB%B4%ED%93%A8%ED%84%B0%EB%A5%BC-%EA%B5%AC%EC%84%B1%ED%95%98%EB%8A%94-%EC%9A%94%EC%86%8C)


## 2. 임베디드 시스템이란?
정의 : 특정 기능을 수행하기 위해 설계된 컴퓨터 시스템  
예시 : 스마트폰, 로봇 청소기, 엔진 제어 모듈

## 3. 임베디드 시스템의 특징
1. 단일 기능 수행 : 특정 작업에 최적화
2. 제약 조건 : 전력, 크기, 비용 등등
3. 실시간 반응 : 환경 변화에 즉각적인 대응(ex. 드론의 자이로 센서로 비행 안정화, 에어컨 온도 센서)

## 4. 임베디드 시스템의 구성요소

* 하드웨어
  * 마이크로컨트롤러 : 라즈베리 파이, 아두이노
  * 센서 : 온도 센서, 압력 센서, 가속도 센서
  * 액추에이터 : 모터, 스피커, 디스플레이

* 소프트웨어
  * 펌웨어 : 하드웨어 제어를 위한 소프트웨어
  * 운영체제 : 실시간 운영체제(RTOS : Real-Time Operating System), 임베디드 리눅스
  * 애플리케이션 소프트웨어 : 사용자 인터페이스, 네트워크 통신 모듈

<img src = "https://github.com/user-attachments/assets/8e5363ce-b1b2-4bb8-9b27-18085ab8a128">



## 5. 임베디드 시스템의 장단점

**장점**
1. 높은 효율 : 특정 작업에 최적화
2. 저전력 소비 : 배터리의 수명 연장
3. 소형화 : 공간 절약 및 휴대성 증가

**단점**
1. 업그레이드 어려움 : 하드웨어 변경 불가
2. 유연성 부족 : 특정 작업에만 최적화
3. 보안 취약 : 업데이트 및 패치가 어려움

## 6. 임베디드 시스템의 미래

#### 1. IoT와 결합 
1-1. 스마트 홈 : 조명 제어, 온도 조절 등등  
1-2. 스마트 시티 : 교통 관리, 에너지 절약 등등  

#### 2. AI와 통합
2-1. 자율주행차량 : 실시간 도로 상황 인식 및 자율적 주행  
2-2. 스마트 헬스케어 : 건강 모니터링, 예측 진단  
2-3. 스마트 팩토리 : 생산 관리
****
