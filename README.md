# **십이지신으로 보는 운세**

---

> 십이지신 중 닮은 상을 찾아 해당 운세를 보여드립니다.
> 

##  **System Architecture**

##  **Tech Stack**
|Dev-Ops|<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=black"> <img src="https://img.shields.io/badge/Amazon EC2-FF9900?style=for-the-badge&logo=Amazon%20EC2&logoColor=white"> <img src="https://img.shields.io/badge/S3%20Bucket-569A31?style=for-the-badge&logo=Amazon%20S3&logoColor=white"> <img src="https://img.shields.io/badge/Amazon RDS-527FFF?style=for-the-badge&logo=Amazon#20RDS&logoColor=black"> <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=NGINX&logoColor=black"> |
|----------|:-------------:|
|__Frontend__| <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=black"> <img src="https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=Redux&logoColor=black"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=TypeScript&logoColor=black"> <img src="https://img.shields.io/badge/styled%20components-DB7093?style=for-the-badge&logo=styled%20components&logoColor=black"> |
|__Backend__| <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=Django&logoColor=white"> <img src="https://img.shields.io/badge/Gunicorn-499848?style=for-the-badge&logo=Gunicorn&logoColor=black"> <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=Swagger&logoColor=black"> <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=RabbitMQ&logoColor=black"> <img src="https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=Celery&logoColor=black"> <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=Redis&logoColor=black"> |
|__DB__| <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=black"> |
|__Monitoring__| <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=black"> <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=Grafana&logoColor=black"> |
|__Others__| <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=black"> <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=Slack&logoColor=black"> <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white"> <img src="https://img.shields.io/badge/GitKraken-179287?style=for-the-badge&logo=GitKraken&logoColor=black"> <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=black"> |

### Mainpage

## 🌿 ERD

### **users api**

- ***api/v1/users/***
    - `GET` : 회원가입 시 아이디, 닉네임 중복 체크 결과
    - `POST` : 회원 가입 정보 저장
- ***api/v1/users/auth***
    - `POST` : access token, refresh token 갱신

### **animals api**

- ***api/v1/animals/animalist***
    - `GET` : 모든 십이지신 운세 정보
- ***api/v1/animals/rank***
    - `GET` : 가장 십이지신과 닮은 사람들의 랭킹 (기간 : 일주일)
- ***api/v1/animals/user/{user_id}***
    - `POST` : 사용자가 업로드한 사진 분석하는 task id
- ***api/v1/animals/user/{user_id}/tasks/{task_id}***
    - `POST` : task id을 이용한 사진 분석 결과
- ***api/v1/animals/user/{user_id}/mypage***
    - `GET` : 사용자가 올린 사진들에 대한 정보

## JWT

- used_library
    - `djangorestframework-jwt`
- JWT_Settings.py
    - set JWT’s default_settings
        
- JWT on frontEND
    - 리덕스를 활용하여 refresh token과 access token을 보관합니다.
    - 사용자의 정보가 필요하면 데이터베이스에 조회하지 않고 access token을 이용하여 사용자의 정보를 파악합니다.
    
- JWT on backEND
    - 요청이 들어오면 토큰으로 해당 유저가 맞는지 확인해주고 그에 맞는 응답을 해줍니다.
    - refresh token을 추가로 활용하여 보안을 강화하였습니다.



# **Members of Team-B**

