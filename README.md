# BOGEOM

### Summary
"오프라인 상점에서 간편하게 상품 정보, 리뷰, 온라인 가격을 검색할 수 없을까?"라고 자주 생각했습니다. 쇼핑 중에 상품을 일일이 타자로 검색하기에는 많은 시간 비용이 들고, 신뢰성 있는 정보를 찾기 어려웠습니다. 그래서 빠르고 현명한 소비를 하고 싶은 소비자의 욕구를 충족시키기 위해 가격표를 촬영하는 것만으로도 상품에 대한 정보 및 리뷰를 한 번에 확인할 수 있는 ‘보검’ 서비스를 만들었습니다.

## 사용 기술
- Spring Boot
-  MySQL
-  JPA
-  JPQL
-  Thymeleaf
-  Lombok
-  Proxy
-  REST API

## 프로젝트 전체 구조
![image](https://github.com/Starlight258/Bogeom_Server/assets/78211281/fbb350ac-294e-4ab7-b038-cda62465660c)

- 모바일 애플리케이션: 사용자가 실시간으로 가격표 객체 탐지가 되는 카메라를 통해 상품의 가격표를 촬영하면 인식된 가격표 이미지가 웹 서버로 전송된다. 
- 웹 서버: 사용자로부터 전송받은 이미지를 다시 인공지능 서버로 전송한다. 
- 인공지능 서버: 광학 문자 인식, Parsing, Search Server 과정을 거쳐 웹 서버에게 상품명 및 가격을 제공한다. 
- 웹 서버: 상품명에 해당하는 데이터를 데이터베이스로부터 찾아 사용자 모바일에 전송한다. 
- 크롤링 서버: 일정 주기마다 상품 가격을 수집하여 데이터베이스에 업데이트한다. 
- Chat 서버: 사용자가 상품 추천 메시지를 보내면 Prompt Engineering 및 ChatGPT를 활용하여 모바일에 응답 메시지를 보낸다.

</br>

## 메인 서버 및 데이터베이스 설계
![image](https://github.com/Starlight258/Bogeom/assets/78211281/35f90b08-7854-4f74-9ef1-97d71e3d45d7)

![image](https://github.com/Starlight258/Bogeom_Server/assets/78211281/2ab8f4e2-dfcd-4c73-8301-1c37fcbf8ee3)
</br>

## API
![image](https://github.com/Starlight258/Bogeom_Server/assets/78211281/444621fb-f645-497d-898d-f57442c32c73)
![image](https://github.com/Starlight258/Bogeom_Server/assets/78211281/e6491657-c80d-47c5-9cdb-65207454ece4)

## 모바일 UI 디자인
![image](https://github.com/Starlight258/Bogeom_Server/assets/78211281/86395197-31b2-4411-a2cb-f80d0ea4c80b)

