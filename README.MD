# Django 마켓 웹페이지 프로젝트

## 목차
1. [프로젝트 소개](#프로젝트-소개)
2. [기술 스택](#기술-스택)
3. [설치 및 실행 방법](#설치-및-실행-방법)
4. [주요 기능](#주요-기능)
5. [프로젝트 구조](#프로젝트-구조)
6. [웹페이지 구동 이미지](#웹페이지-구동-이미지) 
7. [문제 해결 및 배운 점](#문제-해결-및-배운-점)
8. [향후 계획](#향후-계획)

---

## 프로젝트 소개
Django를 활용해 개발한 마켓 웹페이지입니다. 
기본적인 웹페이지의 기능을 구현하는 것에 초점을 맞춘 프로젝트이며, 
회원가입, 프로필 페이지 등 기본적인 유저기능과 
물품 조회,등록,수정,삭제하기 등 기본적인 게시기능 등을 구현하였습니다다. 

### 주요 기능
- 사용자 인증 : 회원가입, 로그인, 로그아웃
- 유저 기능 : 프로필페이지, 찜 기능, 팔로우 기능능  
- 상품 관리 : 상품 등록, 수정, 삭제

**배포 URL:** [https:/http://127.0.0.1:8000/products/](https:/http://127.0.0.1:8000/products/)

---

## 기술 스택
- **언어:** Python 3.10.6
- **백엔드 프레임워크:** Django 4.2
- **프론트엔드:** HTML, CSS
- **데이터베이스:** SQLite (개발 단계), 
---

## 설치 및 실행 방법

### 1. 저장소 클론
```bash
git clone https://github.com/KUC23/new_spartamarket.git
```

### 2. 가상환경 생성 및 패키지 설치
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. 디렉토리 이동
```bash
cd new_spartamarket
```

### 4. 데이터베이스 마이그레이션
```bash
python manage.py migrate
```

### 5. 서버 실행
```bash
python manage.py runserver
```

---

## 프로젝트 구조
```plaintext
new_spartamarket/
├── accounts/    # 사용자 인증 관련 앱
├── media/images/# 개발 테스트용 이미지 폴더
├── products/    # 상품 관련 앱
├── spartamarket # 베이스 앱앱
├── templates/   # base.html 템플릿 파일
├── static/css   # 정적 파일 (CSS, JS, 이미지)
├── users/       # 유저 관련 앱앱
└── manage.py    # Django 관리 스크립트
```
## ERD
![ERD](https://github.com/KUC23/new_spartamarket/blob/main/readme_image/django_spartamarket.png)

---
## 웹페이지 구동 이미지
##### 홈페이지
- 홈페이지로서 기능되는 페이지입니다.
마켓로서 사용자가 제일 처음 들어왔을 때,
가장 필요로하는 기능인 물품목록을 띄워놓는 것이 좋다고 판단하여, 
홈페이지라는 것을 따로 만들기 보다는 현재 사이트에 올라와있는 페이지를 보여주었습니다.
![홈페이지](https://github.com/KUC23/new_spartamarket/blob/main/readme_image/01_%ED%99%88%ED%8E%98%EC%9D%B4%EC%A7%80.png)

##### 프로필 페이지
- 사용자의 프로필 페이지입니다.
기본적으로 자신이 등록한 상품의 목록을 볼 수 있으며,
자신이 찜한 목록과 팔로우 수 등을 확인할 수 있게 구현하였습니다.
![프로필페이지](https://github.com/KUC23/new_spartamarket/blob/main/readme_image/%ED%94%84%EB%A1%9C%ED%95%84%ED%8E%98%EC%9D%B4%EC%A7%80.png)

##### 물품 상세목록
- 물품의 상세목록입니다.
특별한 기능은 없지만, 물품의 상세목록을 볼 수 있는 페이지입니다. 

![물품상세목록](https://github.com/KUC23/new_spartamarket/blob/main/readme_image/02_%EB%AC%BC%ED%92%88%EC%83%81%EC%84%B8%EB%AA%A9%EB%A1%9D.png)
---

## 문제 해결 및 배운 점

### 문제 1: TemplateDoesNotExist, html 파일의 인식불가 오류
- **해결 방법:**
- 1. `settings.py` 의 `DIRS`에 각각의 템플릿의 경로를 설정
- 2. 추후 새로운 환경에서 재기동, 해결

### 문제 2: 상품 이미지 업로드 시 절대 경로 반환 문제
- **해결 방법:** `request.build_absolute_uri` 메서드를 사용해 절대 경로 반환

### 배운 점
- Django의 기본적인 구조에 대해 좀더 이해하게됨
- 경로 설정의 중요성을 다시한번 알게됨

---

## 향후 계획
- 검색 기능 추가
- 상품 카테고리 시스템 도입
- 프론트 엔드 개선
---



[def]: "D:\ai\9_w\project\new_project\spartamarket\readme_image\django_spartamarket.png"
