# 임베디드 시스템 프로젝트 최종 결과 보고서  

---

## 결과 화면  

### 1. 습도가 낮을 때 메시지 출력  
![습도가 낮을 때 메시지 출력](https://github.com/user-attachments/assets/522819e8-23f4-47dc-9379-e13e999160a1)  

### 2. 습도가 높을 때 메시지 출력  
![습도가 높을 때 메시지 출력](https://github.com/user-attachments/assets/715d26eb-da5d-4fe5-892a-6ae5659ee1f7)  

### 3. 온도가 낮을 때 메시지 출력  
![온도가 낮을 때 메시지 출력](https://github.com/user-attachments/assets/3519f6fd-e58d-4e40-aaaa-c9ae95eb2891)  

### 4. 온도가 높을 때 메시지 출력  
![온도가 높을 때 메시지 출력](https://github.com/user-attachments/assets/d6957177-1eba-45b7-b7a4-2bfedc1abb9b)  

### 5. Grafana와 Node-RED의 연동 결과  
![Grafana와 Node-RED 연동 결과](https://github.com/user-attachments/assets/a640fb7a-c9b7-41a5-b69c-16bdc35a6d8e)  

---

## Node-RED 노드 구성  

![Node-RED 노드 구성](https://github.com/user-attachments/assets/8ad90ddf-4e04-424f-89bd-df7bb76c21ab)  

---

## Grafana & Node-RED & InfluxDB 연동 방법  

### 1. InfluxDB 노드 설치  
Node-RED에서 InfluxDB 노드를 설치하여 데이터를 저장하고 관리할 준비를 합니다.  

### 2. InfluxDB 설정  
![InfluxDB 설정 화면](https://github.com/user-attachments/assets/41edd7a6-280b-401a-8f75-3a7658ae296a)  
- **Host**: `127.0.0.1`  
- **Port**: `8086` (기본값)  
- **Database**: `nodered_data`  
- **Fields**: `temperature`, `humidity`  

### 3. 데이터 변환 작업  
InfluxDB는 데이터를 `float` 타입으로 받으므로, Function 노드를 사용하여 데이터를 변환합니다.  
![Function 노드 설정](https://github.com/user-attachments/assets/3bd389a3-f380-41a2-b251-d3eca2421ccf)  

### 4. Grafana 데이터 소스 설정  
Grafana에서 데이터 시각화를 위해 InfluxDB를 데이터 소스로 추가합니다.  
![Grafana 데이터 소스 설정](https://github.com/user-attachments/assets/1ab677db-857d-4fea-a337-cc609417a116)  
1. Grafana 설치 후 **"Add your first data source"** 클릭  
2. InfluxDB 선택 후 **Database** 필드에 `nodered_data` 입력  

### 5. 대시보드 및 시각화 생성  
![Grafana 대시보드 생성](https://github.com/user-attachments/assets/e7d70105-e9a5-47b8-b2d6-d8239a6ec4ed)  
- **"Create your first dashboard"** 선택 후 **"Add visualization"** 클릭  
- `temperature`와 `humidity` 데이터를 각각의 Query로 추가  
- 시각화를 통해 실시간 데이터 변화를 확인  

---