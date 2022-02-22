## 경력

### [당근마켓](https://www.daangn.com/)

- 2021.11 ~ 2022.01
- 플랫폼 개발실 인턴
- Go, gRPC
- [예측 가능한 대규모 서비스 개발하기](https://medium.com/daangn/%EC%98%88%EC%B8%A1-%EA%B0%80%EB%8A%A5%ED%95%9C-%EB%8C%80%EA%B7%9C%EB%AA%A8-%EC%84%9C%EB%B9%84%EC%8A%A4-%EA%B0%9C%EB%B0%9C%ED%95%98%EA%B8%B0-a33e2f3cef88)
  - 인턴 기간 동안 했던 프로젝트를 글로 정리했습니다.
  - 유저의 위·경도, 혹은 IP를 기반으로 국가 정보를 찾아주는 GeoLocation gRPC 서버를 새롭게 독립적으로 만들었습니다. 요구사항에 맞게 아키텍처를 설계하고 예측할 수 있는 성능을 낼 수 있도록 서비스를 개발하는 과정을 경험했습니다. 프로젝트를 배포한 이후 퍼포먼스 테스트를 진행하고 구체적으로 어떤 부분에서 병목이 발생하는지 파악하고 해당 문제를 해결함으로써 초기 애플리케이션의 성능에 비해 최종 버전에서 약 66배 향상시켰습니다.
- [daangn/gogeos](https://github.com/daangn/gogeos) 오픈소스 기여
  - GEOS를 Go로 포팅한 `gogeos`에 필요한 함수들을 추가하고, 새로운 버전을 릴리즈 했습니다.

### [닥터NOW](https://drnow.co.kr/)

- 2019.12 ~ 2020.08
- 초기 창업 멤버
- 내용: 리드 개발자로서, 서비스 전체의 설계 및 개발에 참여하고 배포와 관련된 인프라 구성 및 개발팀 문화에 기여했습니다.

  1. MVP 서비스 개발 및 개발팀 리드  
     서비스의 초기 버전인 비대면 약 처방 및 배달 애플리케이션 설계와 개발에 참여했습니다. 클라이언트와 백앤드의 기술 스택을 설정 및 개발, 그리고 협업에 대한 방식을 제시했습니다. 우선 애플리케이션은 크로스 플랫폼을 지원하는 React Native를 사용하고 상태 관리를 위해 Redux와 관련 생태계를 활용했습니다. API 서버의 경우 NestJS, PostgreSQL을 사용해 만들고 개발 환경을 Docker, Docker Compose로 구성했습니다. 서비스를 개발하면서 인프라 구성을 위한 노력을 최소화 하고자 AWS 서버리스 컨테이너 관리 서비스인 AWS Fargate를 사용해 컨테이너 이미지를 배포했습니다. 클라이언트 중 약사용 앱과 백앤드 개발을 전담했습니다. 클라이언트 개발자와 API에 대한 정보를 공유하기 위해 Swagger를 사용해 API 문서를 개발 서버에 배포했습니다. 또한 브랜치 관리 전략인Git flow를 차용해 2주간 개발 주기를 가지고 주기적으로 배포할 수 있도록 했습니다.

- 기술:
  - Backend
    - Typescript, NestJS, TypeORM, Swagger
    - PostgreSQL
    - AWS RDS, S3, EC2, ECR, ECS Fargate
    - Docker, Docker Compose
  - Client
    - Typescript, React Native, React, Redux, Redux-saga

### [구름(goorm)](goorm.io)

- 2019.07 ~ 2019.10
- 풀스택 개발자
- 내용: 풀스택 개발자로서 개발 교육 관련 서비스인 구름 Edu 서비스 개발에 참여했습니다. 또한 구름 IDE 리뉴얼 작업에 일부 기여했습니다.
- 기술:
  - Express, React, SCSS, Reactstrap
  - MongoDB

## 프로젝트

### The Football - [Github repo](https://github.com/TheFootball)

- 내용: Junction X Seoul 해커톤 파트너사인 AWS의 과제를 선택해 AWS를 활용한 채팅 기반의 게임을 기획했습니다. 한 게임룸에 최대 천 명의 다수 사용자와 함께 하는 게임을 기획해 아주 많은 사용자가 사용하는 것을 가정하고 프로젝트를 진행했습니다. 저는 채팅 서버를 맡아 스케일 아웃이 가능한 구조를 구성하는 것을 목표로 했습니다. 웹소켓만 사용했을 때 같은 게임룸에 있지만 다른 인스턴스와 연결된 상황을 해결해야 했습니다. 여러 프로세스 사이에 공유되는 메시지 통로가 필요하다고 판단했는데 관련된 내용으로 서치를 했을 때 Pub/Sub 구조로 구성된 케이스를 많이 볼 수 있었습니다. 가장 많이 보였던 방식이 Redis의 Pub/Sub 기능을 사용하는 것과 Kafka를 사용하는 것이었습니다. 둘 다 익숙하지 않아서 무엇을 사용하든 비슷한 러닝 커브가 있었을 것이라 생각되지만, Redis는 간단하게라도 사용해봤던 경험도 있어서 Redis를 선택했습니다. 결과적으로 Go, Websocket, Redis를 사용해 스케일 아웃이 가능한 채팅 서버를 구현할 수 있었습니다.

- 기간: 2021.05.21 ~ 2021.05.23
- 기술: [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/thefootball) Golang, Fiber, Websocket, Svelte, DynamoDB, Redis, Docker, Docker Compose, S3

### Mango Table

- 내용: 기존 프로젝트 매니지먼트 서비스를 보완한 SaaS를 기획하고 창업에 도전했습니다. 저는 팀 리더를 맡아서 개발 스택을 정하고, 프로젝트 설계 및 개발에 참여했습니다.

  1. MVP 서비스 소개 페이지 제작  
     국가 지원 사업 및 투자자에게 수요와 관련된 지표를 제시해야 하는 필요가 발생했습니다. 서비스 수요를 확인하기 위해 서비스에 대한 설명이 있는 랜딩 페이지를 만들고 Product Hunt라는 초기 서비스를 홍보할 수 있는 웹사이트에 게시했습니다. 저는 웹 개발과 배포를 전담했는데 개발은 React와 Typescript를 사용했습니다. 해당 페이지에 대한 관심있는 사람들에게 본 서비스 배포 후 알람을 주기 위해서 이메일을 수집했는데, 별도의 서버를 배포하지 않고 빠르게 개발하기 위해서 해당 기능을 제공해주는 “Waitlist”라는 API 서비스를 사용했습니다. 개발한 페이지는 AWS S3, CloudFront를 사용해 배포했습니다. 결과적으로 Product Hunt에 메인으로 게시되는 약 3일 동안 100개가 넘는 추천과 85명 이상의 Email Register를 받았습니다.

  2. 본 서비스 개발  
     프로젝트 매니지먼트 서비스 MVP를 만들기 위해 약 3개월 동안 소개 페이지에서 이메일을 등록한 유저들을 대상으로 클로즈 베타를 준비하고 배포했습니다. 웹 애플리케이션 개발 및 배포, API 서버 개발 및 배포에 약 70% 기여했습니다. 클라이언트는 React와 Typescript를 사용했고 거대한 프로젝트의 상태 관리를 용이하게 하기 위해 Redux를 사용했습니다. 또한 Redux의 비동기 처리를 위해 Redux Saga를 사용했습니다. 백앤드는 빠른 개발을 위해 가장 익숙한 NestJS와 Typescript 스택을 기본으로 사용했습니다. 초기 서비스의 변경 사항이 많다는 특징과 서비스 자체적으로 자유도 높은 스키마가 요구되었기 때문에 MongoDB를 사용했습니다. 배포는 AWS EC2와 Atlas MongoDB를 사용해 배포했습니다. 서비스 개발 과정을 단축하기 위해 여러 서비스를 사용했습니다. 사용자 인증을 위해 Auth0, 메일 서비스를 위해 Mailgun, 에러 로그 수집을 위해 Sentry를 사용했습니다. 결과적으로 FastVentures의 최종 미팅까지 갈 수 있었고, 많은 서비스와 상호 작용하는 방법을 경험했습니다.

- 기간: 2021.01 ~ 2021.05
- 기술: [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/mango-table) Typescript, NestJS, MongoDB Atlas, Mongoose, React, Redux, Redux Saga, Sentry, Google Analytics, Auth0, AWS

### STMT(Six Things Must TODO) - [Github repo](https://github.com/6-things-must-to-do)

- 내용: 학과 프로젝트 수업인 소프트웨어공학이론, 인공지능 수업으로 생산성 향상 및 습관 만들기 애플리케이션을 구성했습니다. 팀장으로 참여해 개발 모든 과정에 참여하고 개발했습니다.

  1. 앱 개발 및 팀 리딩  
     학교의 소프트웨어 공학이론 수업에서 AWS 서비스를 사용해 개발하는 프로젝트를 진행했습니다. 프로젝트의 팀장을 맡아 클라이언트를 개발하는 팀원들을 학습시키고 함께 프로젝트를 진행할 수 있도록 했습니다. 앱은 React Native를 사용해서 개발했습니다. 개발을 잘 모르는 팀원들에게 간단한 뷰를 만들 수 있도록 학습 자료를 제공하고 무료로 제공되는 음식 레시피 API를 사용해 레시피 정보를 보여주는 간단한 React Native 서비스를 만들어 보도록 했습니다. 그렇게 함으로써 뷰를 만드는 작업을 팀원들이 일부 참여해주고 저는 애플리케이션에서 필요한 서비스 로직도 함께 구성하며 클라이언트를 데모 버전까지 작업을 마무리 할 수 있었습니다.

  2. API 서버 개발  
     백앤드는 제가 전담해 개발하게 되었는데 당시 Go언어와 DynamoDB를 배우고 싶은 생각을 가지고 있었습니다. Go는 생산성이 뛰어나고 빠른 속도를 자랑하며 정적 타입과 컨벤션의 통일 등으로 안정적인 개발이 가능하다고 들어왔고, DynamoDB는 사용 경험이 있었으나 온전히 이해하고 쓰지 않아서 다시 공부를 많이 해보고 조금 복잡한 테이블을 설계 해보고 싶었습니다. 해당 기술들에 대해 공부하면서 서비스를 만들었습니다. Go의 REST API 프레임워크인 Gin을 사용해 서버를 구성해서 라즈베리파이 우분투에 컴파일된 바이너리를 System service에 등록해 개발용 서버를 배포했습니다. 또한 DynamoDB의 설계 방법 중 AWS에서 공식적으로 추천하는 Single Table Design에 대해서 공부해서 설계를 했습니다. 공부한 내용을 개인 블로그에 게시해 구글 검색 기준 “dynamodb design”과 유관한 검색 결과 상위에 게시되고 있습니다.

- 기간: 2020.10.25 ~ 2020.12.13
- 기술: [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/6-things-must-to-do) Go, Gin, Typescript, React Native, Redux, Redux-Saga, AWS DynamoDB
- [Documentation & demo](https://github.com/6-things-must-to-do/docs)

### 두근두근 라치오스 - [Github repo](https://github.com/weehan-dev/dodohan)

- 내용: 위한이 한양대학교 학생들에게만 제공하던 매칭 프로그램을 축제를 맞아 이벤트성으로 외부 학교의 신청을 받고 매칭해주는 프로그램을 만들었습니다. 신청은 구글 독스를 통해 받고, 받은 신청서를 csv 형식으로 파싱하고 매칭 알고리즘으로 매칭되도록 했습니다. 매칭 알고리즘을 알아보고 도입하는 과정이 있었고, 매칭 이후 결과는 MongoDB에 저장 후 축제 당일에 SMS 및 메일로 결과를 발송해줬습니다. 프로그램은 CLI 형태로 NodeJS를 사용했습니다. 약 500명이 참여했으며, 반응도 괜찮았던 성공적인 프로젝트였습니다.

- 기간: 2019.09.15 ~ 2019.09.23
- 기술: JS, MongoDB
- 약 500명 가량 참여
