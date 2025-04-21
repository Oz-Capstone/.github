<div align="center">

# SimCar - 중고차 쇼핑몰 프로젝트

<img src="https://github.com/user-attachments/assets/84dd02b2-3598-4d85-a9f3-72f111860336" width="200">


중고차 매매 시장의 정보 비대칭성 해소를 위한 AI 기반 중고차 진단 및 거래 플랫폼

</div>

## 📚 목차
- 홈페이지 (https://simcar.kro.kr)
- [프로젝트 소개](#-프로젝트-소개)
- [기술 스택](#-기술-스택)
- [시스템 아키텍처](#-시스템-아키텍처)
- [기능 구성도](#-기능-구성도)
- [API 명세서](#-api-명세서)
- [코드 저장소](#-코드-저장소)
- [시연 영상](#-시연-영상)
- [작년 우수팀 비교표](#-작년-우수팀-비교표)
- [팀원 소개](#-팀원-소개)

## 🚗 프로젝트 소개

중고차 거래 시장의 가장 큰 문제점인 정보의 비대칭성을 해소하고 거래의 투명성을 높이기 위한 AI 기반 중고차 거래 플랫폼입니다.

### 핵심 기능
- AI 기반 차량 신뢰도 진단 서비스
- 실시간 매물 등록/관리 시스템
- 관심 차량 찜하기 및 알림 서비스
- OAuth2.0 기반 사용자 인증

## 🛠 기술 스택
<details>
<summary>기술 스택(클릭하면 내용 보입니다)</summary>
  
### Backend
<img src="https://img.shields.io/badge/Java 21-007396?style=flat&logo=java&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring Security-6DB33F?style=flat&logo=springsecurity&logoColor=white"/>
<img src="https://img.shields.io/badge/JPA-59666C?style=flat&logo=hibernate&logoColor=white"/>

### AI/ML
<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white"/>
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white"/>

### Frontend
<img src="https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white"/>
<img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black"/>
<img src="https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white"/>

### DevOps
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white"/>

</details>

## 🏗 시스템 아키텍처

<img src="https://github.com/user-attachments/assets/950535b4-34ac-4ce7-821e-f97753d030a1" width="800">

## 💡 기능 구성도

<details>
<summary>기능 구성도(클릭하면 내용 보입니다)</summary>
<img src="https://github.com/user-attachments/assets/aec344bb-0379-42b7-ad9a-d3e0ef401e7f" width="600">
</details>


## 📋 API 명세서

<details>
<summary>전체 API 명세 보기(클릭하면 내용 보입니다)</summary>

### 🚗 차량 관리 API

| Method | URI | Description | Request | Response |
|--------|-----|-------------|----------|-----------|
| POST | /api/cars | 차량 등록 | CarRegistrationRequest, MultipartFile[] | - |
| GET | /api/cars | 전체 차량 조회 | - | List<CarResponse> |
| GET | /api/cars/{carId} | 차량 상세 조회 | - | CarDetailResponse |
| PUT | /api/cars/{carId} | 차량 정보 수정 | CarRegistrationRequest | - |
| DELETE | /api/cars/{carId} | 차량 삭제 | - | - |
| GET | /api/cars/{carId}/diagnosis | 차량 신뢰도 진단 | - | CarDiagnosisResponse |
| POST | /api/cars/{carId}/images | 차량 이미지 추가 | MultipartFile[] | - |
| DELETE | /api/cars/{carId}/images/{imageId} | 차량 이미지 삭제 | - | - |
| PUT | /api/cars/{carId}/images/order | 이미지 순서 변경 | List<Long> | - |
| PUT | /api/cars/{carId}/thumbnail/{imageId} | 대표 이미지 변경 | - | - |

### 👤 회원 관리 API

| Method | URI | Description | Request | Response |
|--------|-----|-------------|----------|-----------|
| POST | /api/members/join | 회원가입 | MemberJoinRequest | - |
| POST | /api/members/login | 로그인 | MemberLoginRequest | - |
| POST | /api/members/logout | 로그아웃 | - | - |
| GET | /api/members/profile | 회원 프로필 조회 | - | MemberProfileResponse |
| PUT | /api/members/profile | 회원 프로필 수정 | MemberUpdateRequest | - |
| DELETE | /api/members/profile | 회원 탈퇴 | - | - |
| GET | /api/members/sales | 내 판매 목록 조회 | - | List<CarResponse> |

### ❤️ 찜하기 API

| Method | URI | Description | Request | Response |
|--------|-----|-------------|----------|-----------|
| POST | /api/favorites/{carId} | 찜하기 | - | - |
| DELETE | /api/favorites/{carId} | 찜하기 취소 | - | - |
| GET | /api/members/favorites | 찜한 차량 목록 조회 | - | List<CarResponse> |

</details>

## 📁 코드 저장소

- [AI Model Server](https://github.com/Oz-Capstone/Simcar-AI-modeling)
- [Spring Backend](https://github.com/Oz-Capstone/Simcar-Server-Spring)
- [React Frontend](https://github.com/Oz-Capstone/Simcar-Front-Web)
- [iOS App](https://github.com/Oz-Capstone/Simcar-Front-IOS)
- [Android App](https://github.com/Oz-Capstone/Simcar-Front-Flutter)

## 📊 App 설치

- [AppStore]
- [GooglePlay]

## 🎥 시연 영상

- [웹 PC 시연영상](https://www.youtube.com/watch?v=LyZfsUR9xug)
- [웹 모바일 시연영상](https://youtu.be/s3Ya8dttUxA)
- [iOS 시연영상](https://www.youtube.com/watch?v=-IjOtbxJREc)
- [Android 시연영상](https://www.youtube.com/watch?v=K1HOWMxT6fk)

## 📊 작년 우수팀 비교표

|  | SimCar | 최우수 | 우수1 | 우수2 | 우수3 |
|------|--------|---------|---------|---------|---------|
| Code | ✅ | ✅ | ✅ | ✅ | ✅ |
| Doc | ✅ | ✅ | ✅ | ❌ | ✅ |
| 영상 | ✅ | ✅ | ❌ | ❌ | ❌ |
| 화면 | I,A,R | R | R | R | R |
| AppStore/GooglePlay | ✅ | ❌ | ❌ | ❌ | ❌ |

최우수 : https://github.com/capstone-aloha</br>
우수1 : https://github.com/TeamCookCaps</br>
우수2 : https://github.com/godi00/capstone</br>
우수3 : https://github.com/Capic2024/server-flask
## 👥 팀원 소개

| 역할 | 이름 | GitHub |
|------|------|--------|
| AI | 오정선 | [@gosumjigi](https://github.com/gosumjigi) |
| 백엔드 | 박한빈 | [@kharabiner](https://github.com/kharabiner) |
| 프론트엔드 | 양정우 | [@mrangjw](https://github.com/mrangjw) |
| iOS | 김건우 | [@3DUCK](https://github.com/3DUCK) |
| Android | 박준희 | [@marulog](https://github.com/marulog) |

<div align="center">
Copyright © 2024 SimCar. All rights reserved.
</div>
