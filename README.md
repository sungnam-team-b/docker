# **십이지신으로 보는 운세**

---

> 십이지신 중 닮은 상을 찾아 해당 운세를 보여드립니다.
> 

##  **System Architecture**

##  **Tech Stack**
|Dev-Ops|<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=black"> <img src="https://img.shields.io/badge/Amazon EC2-FF9900?style=for-the-badge&logo=Amazon%20EC2&logoColor=white"> <img src="https://img.shields.io/badge/S3%20Bucket-569A31?style=for-the-badge&logo=Amazon%20S3&logoColor=white"> <img src="https://img.shields.io/badge/Amazon RDS-527FFF?style=for-the-badge&logo=Amazon#20RDS&logoColor=black"> <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=NGINX&logoColor=black"> |
|----------|:-------------:|
|__Frontend__| <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=black"> <img src="https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=Redux&logoColor=black"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=TypeScript&logoColor=black"> <img src="https://img.shields.io/badge/MUI-007FFF?style=for-the-badge&logo=MUI&logoColor=black"> <img src="https://img.shields.io/badge/styled%20components-DB7093?style=for-the-badge&logo=styled%20components&logoColor=black"> |
|__Backend__| <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=Django&logoColor=white"> <img src="https://img.shields.io/badge/Gunicorn-499848?style=for-the-badge&logo=Gunicorn&logoColor=black"> <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=Swagger&logoColor=black"> <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=RabbitMQ&logoColor=black"> <img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=Elasticsearch&logoColor=black"> <img src="https://img.shields.io/badge/Kibana-005571?style=for-the-badge&logo=Kibana&logoColor=black"> <img src="https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=Celery&logoColor=black"> <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=Redis&logoColor=black"> |
|__DB__| <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=black"> |
|__AI__| <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=PyTorch&logoColor=black"> <img src="https://img.shields.io/badge/YOLOv5-00FFFF?style=for-the-badge&logo=YOLO&logoColor=black"> <img src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=Google%20Colab&logoColor=black"> |
|__Monitoring__| <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=black"> <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=Grafana&logoColor=black"> <img src="https://img.shields.io/badge/cAdvisor-2496ED?style=for-the-badge&logo=cAdvisor&logoColor=white"> |
|__Others__| <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=black"> <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=Slack&logoColor=black"> <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white"> <img src="https://img.shields.io/badge/GitKraken-179287?style=for-the-badge&logo=GitKraken&logoColor=black"> <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=black"> |

### Mainpage

## 🌿 ERD

### **users api**

- ***api/users/***
    - `GET` : 회원가입 시 아이디, 닉네임 중복 체크 결과
    - `POST` : 회원 가입 정보 저장
- ***api/users/auth***
    - `POST` : access token, refresh token 갱신

### **animal api**

- ***api/challenges***
    - `GET` : 모든 도전과제 정보
- ***api/statistics/ranking***
    - `GET` : 인기순으로 정렬된 일주일간의 재활용 데이터
- ***api/users/{user_id}/results/tasks***
    - `POST` : 사용자가 업로드한 사진 분석 비동기 처리
- ***api/users/{user_id}/results/tasks/{task_id}***
    - `GET` : task_id로 분석 완료 여부 확인, 프론트에서 polling
- ***api/users/{user_id}/challenges***
    - `GET` : 사용자가 달성한 도전과제 정보
- ***api/users/{user_id}/pages/{page_number}***
    - `GET` : 사용자가 업로드한 재활용 이미지 데이터, 페이지네이션 이용
- ***api/trash/users/{user_id}/statistics***
    - `GET` : 사용자가 업로드한 모든 재활용 데이터의 통계
- ***api/trash/users/{user_id}/statistics/period/{from_date}/{to_date}***
    - `GET` : 사용자가 설정한 날에 따른 재활용 데이터 통계

## JWT

- used_library
    - `djangorestframework-jwt`
- JWT_Settings.py
    - set JWT’s default_settings
        
- JWT on frontEND
    - restore tokens by using redux
    - if we need some user data, we don’t need to make connection with backend
    by opening JWT payload, we can get user data
    
- JWT on backEND
    - after we identify user by check login data, give authorization by using JWT
    - by using refresh_token, we enhanced our security level



# **Members of Team-B**

