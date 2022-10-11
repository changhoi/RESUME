# 경력

## [버킷플레이스](https://www.bucketplace.com/)

- 2022.04 ~ 재직 중
- Core Platform Engineer
- 버킷플레이스 개발팀이 공통적으로 사용해야 하는 인프라 및 서비스 개발

### Logging Pipeline

- 여러 서비스에서 공통적으로 로그를 보내는 로깅 파이프라인 개발에 참여했습니다.
- Go, Kafka, Kotlin, React
- Fiber 라는 프레임워크를 사용해 Webserver를 만들었습니다. HTTP Body를 통해 들어오는 값을 파싱하는 과정을 최대한 단순하게 만들기 위해 직접 Parser를 구현하고 배열 형태로 들어오는지만 확인하도록 만들었습니다. 받은 로그는 Aggregator 역할을 하는 Kafka 토픽으로 전달되도록 만들었습니다. 또한 파이프라인 중에 필터와 AVRO 스키마가 어떻게 적용되어 있는지를 확인할 수 있는 Admin 페이지를 간단하게 React & Typescript를 통해 구현했습니다.

### Feature Flag

- 동적으로 기능을 변경할 수 있는 [Feature Flag](https://martinfowler.com/articles/feature-toggles.html) 개발에 참여했습니다.
- Go, ETCD, Github Action
- 파일럿 프로젝트로 Github을 메타 데이터 스토리지로서 활용하는 개발을 진행했습니다. Github을 통해 데이터 변경이나 추가를 PR을 통해 진행하고 최종적으로 기능을 사용하는 팀의 리뷰를 거쳐 Merge되면 Github Action을 통해 ETCD에 정해진 규칙에 맞춰 데이터를 밀어 넣거나 삭제되도록 했습니다.

## [당근마켓](https://www.daangn.com/)

- 2021.11 ~ 2022.01
- 지리 정보 플랫폼 개발실 인턴
- 당근마켓 서비스 개발팀이 지리 정보와 관련된 개발을 할 때 공통적으로 필요로 하는 서비스를 개발

### GeoLocation

- 유저의 위·경도, 혹은 IP를 기반으로 국가 정보를 찾아주는 GeoLocation gRPC 서버를 개발했습니다.
- Python, Go, gRPC
- 요구사항에 맞게 아키텍처를 설계하고 예측할 수 있는 성능을 낼 수 있도록 서비스를 개발하는 과정을 경험했습니다. 프로젝트를 배포한 이후 퍼포먼스 테스트를 진행하고 구체적으로 어떤 부분에서 병목이 발생하는지 파악하고 해당 문제를 해결함으로써 초기 애플리케이션의 성능에 비해 최종 버전에서 약 66배 향상시켰습니다.
- [예측 가능한 대규모 서비스 개발하기](https://medium.com/daangn/%EC%98%88%EC%B8%A1-%EA%B0%80%EB%8A%A5%ED%95%9C-%EB%8C%80%EA%B7%9C%EB%AA%A8-%EC%84%9C%EB%B9%84%EC%8A%A4-%EA%B0%9C%EB%B0%9C%ED%95%98%EA%B8%B0-a33e2f3cef88)
  - 인턴 기간 동안 했던 프로젝트를 글로 정리했습니다.
- [daangn/gogeos](https://github.com/daangn/gogeos) 오픈소스 기여
  - GEOS를 Go로 포팅한 `gogeos`에 필요한 함수들을 추가하고, 새로운 버전을 릴리즈 했습니다.

## [닥터NOW](https://drnow.co.kr/)

- 2019.12 ~ 2020.08
- 초기 창업 멤버
- 리드 개발자, 서비스 전체의 설계 및 개발에 참여하고 배포와 관련된 인프라 구성 및 개발팀 문화에 기여

### MVP 서비스 개발 및 개발팀 리드

- Backend
  - Typescript, NestJS, TypeORM, Swagger
  - PostgreSQL
  - AWS RDS, S3, EC2, ECR, ECS Fargate
  - Docker, Docker Compose
- Client
  - Typescript, React Native, React, Redux, Redux-saga
- 서비스의 초기 버전인 비대면 약 처방 및 배달 애플리케이션 설계와 개발에 참여했습니다.
- React Native와 Redux를 사용해 약사용 클라이언트 애플리케이션을 개발했습니다.
- NestJS, PostgreSQL으로 API 서비스를 개발했습니다.
- 개발 환경을 Dockerizing하고 AWS Fargate와 ECR을 사용해 컨테이너 이미지를 배포했습니다.
- Swagger를 사용해 개발 서버에서 API 문서를 배포해 클라이언트 개발자와 협업했습니다.
- Git flow를 도입하고 2주 스프린트와 주기적인 배포 사이클을 만들었습니다.

## [구름(goorm)](goorm.io)

- 2019.07 ~ 2019.10
- 풀스택 개발자
- 회사 서비스 풀스택 개발

### 구름 Edu 서비스 개발

- Express, React, SCSS, Reactstrap, MongoDB
- 교육 컨텐츠 서비스인 구름 Edu 서비스 개발에 참여했습니다.

### 구름 IDE 리뉴얼

- HTML, CSS, Bootstrap
- 웹 IDE 서비인 구름 IDE 리뉴얼 작업에 참여했습니다.

# 프로젝트

## The Football - [Github repo](https://github.com/TheFootball)

- 2021.05.21 ~ 2021.05.23
- Junction X Seoul 해커톤 과제로 AWS를 활용한 채팅 기반 게임 개발에 참여했습니다.

### 채팅 서버

- [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/thefootball) Golang, Fiber, Websocket, Svelte, DynamoDB, Redis, Docker, Docker Compose, S3
- 각 게임마다 최대 천 명의 다수 사용자와 함께 하는 게임을 기획해 아주 많은 사용자가 사용하는 것을 가정하고 프로젝트를 진행했습니다. 저는 채팅 서버를 맡아 스케일 아웃이 가능한 구조를 구성하는 것을 목표로 했습니다. 확장 가능한 메시징 서비스를 위해 Redis를 Pub/Sub Message broker로서 활용해 채팅 서버를 만들었습니다.

## Mango Table

- 2021.01 ~ 2021.05
- 기존 프로젝트 매니지먼트 서비스를 보완한 SaaS를 기획하고 창업에 도전했습니다. 팀 리더로서 개발 스택을 정하고, 프로젝트 설계 및 개발에 참여했습니다.

### MVP 서비스 소개 페이지 제작

- AWS S3, CloudFront, React, Typescript, SaaS (Waitlist)
- 국가 지원 사업 지원 및 투자 유치 목적으로 수요 관련 지표를 모으기 위한 랜딩 페이지 프로젝트를 진행했습니다.
- 페이지 개발 및 배포를 전담했습니다. Typescript, React를 사용해 개발했으며 별도의 Backend 개발 공수를 줄이고자 Waitlist API를 활용했습니다. 배포는 S3, CloudFront를 활용해 간단히 배포했습니다.
- Product Hunt에 게시하고 메인으로 게시되는 약 3일 동안 100개가 넘는 추천과 85명 이상의 Email Register를 받았습니다.

### 본 서비스 개발

- [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/mango-table) Typescript, NestJS, MongoDB Atlas, Mongoose, React, Redux, Redux Saga, Sentry, Google Analytics, Auth0, AWS
- 프로젝트 매니지먼트 서비스 MVP를 만들기 위해 약 3개월 동안 소개 페이지에서 이메일을 등록한 유저들을 대상으로 클로즈 베타를 준비하고 배포했습니다.
- 클라이언트 개발에 Typescript, React를 사용해 개발했습니다. 클라이언트 사이드의 비동기 처리와 상태 관리를 위해 Redux, Redux Saga를 사용해 개발했습니다.
- 서버는 NestJS, Typescript 스택으로 개발했습니다. 초기 서비스의 변경 사항이 많고 서비스 자체적인 특징으로도 자유로운 스키마가 요구되어 DocumentDB인 MongoDB를 사용해 개발했습니다. 배포는 AWS EC2와 Atlas MongoDB를 사용해 배포했습니다.
- 서비스 개발 과정을 단축하기 위해 여러 SaaS를 활용했습니다. 사용자 인증을 위해 Auth0, 메일 서비스를 위해 Mailgun, 에러 로그 수집을 위해 Sentry를 사용했습니다.
- 결과적으로 FastVentures 최종 미팅까지 진행되었고 많은 서비스와 상호 작용하는 방법을 경험할 수 있었습니다.

## STMT(Six Things Must TODO) - [Github repo](https://github.com/6-things-must-to-do)

- 2020.10.25 ~ 2020.12.13
- 학과 프로젝트 수업인 소프트웨어공학이론, 인공지능 수업으로 생산성 향상 및 습관 만들기 애플리케이션을 구성했습니다. 팀장으로 참여해 개발 모든 과정에 참여하고 개발했습니다.
- 기술: [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/6-things-must-to-do) Go, Gin, Typescript, React Native, Redux, Redux-Saga, AWS DynamoDB
- [Documentation & demo](https://github.com/6-things-must-to-do/docs)

### 앱 개발 및 리딩

- 클라이언트를 개발하는 팀원들을 학습시키고 함께 프로젝트를 진행할 수 있도록 했습니다.
- 앱은 React Native를 사용해서 개발했습니다. 개발을 잘 모르는 팀원들에게 간단한 뷰를 만들 수 있도록 학습 자료를 제공하고 무료로 제공되는 음식 레시피 API를 사용해 레시피 정보를 보여주는 간단한 React Native 서비스를 만들어 보도록 했습니다.
- 결과적으로 본 개발에서 팀원들이 뷰를 만드는 작업에 참여할 수 있었습니다.

### API 서버 개발

- 백앤드는 제가 전담해 개발하게 되었는데 당시 Go언어와 DynamoDB를 배우고 싶은 생각을 가지고 있었습니다. Go는 생산성이 뛰어나고 빠른 속도를 자랑하며 정적 타입과 컨벤션의 통일 등으로 안정적인 개발이 가능하다고 들어왔고, DynamoDB는 사용 경험이 있었으나 온전히 이해하고 쓰지 않아서 다시 공부를 많이 해보고 조금 복잡한 테이블을 설계 해보고 싶었습니다.
- 해당 기술들에 대해 공부하면서 서비스를 만들었습니다. Go 웹 프레임워크인 Gin을 사용해 서버를 구성하고 컴파일된 바이너리를 Ubuntu System service에 등록해 개발용 서버를 배포했습니다. 또한 DynamoDB의 설계 방법 중 AWS에서 공식적으로 추천하는 Single Table Design에 대해서 공부해서 설계를 했습니다.
- Single Table Design을 학습하고 [블로그에 정리](https://changhoi.kim/posts/database/dynamodb-single-table-design/)했습니다.

## 두근두근 라치오스 - [Github repo](https://github.com/weehan-dev/dodohan)

- 2019.09.15 ~ 2019.09.23
- 위한이 한양대학교 학생들에게만 제공하던 매칭 프로그램을 축제를 맞아 이벤트성으로 외부 학교의 신청을 받고 매칭해주는 프로그램을 만들었습니다.
- JS, MongoDB
- 개발 과정을 줄이기 위해 신청은 간단하게 구글 독스를 통해 받았습니다.
- 받은 신청서를 csv 형식으로 파싱하고 매칭 알고리즘으로 매칭되도록 했습니다. 매칭 알고리즘을 알아보고 도입하는 과정이 있었고, 매칭 이후 결과는 MongoDB에 저장 후 축제 당일에 SMS 및 메일로 결과를 발송해줬습니다.
- 약 500명 가량 참여하며 성공적으로 프로젝트를 마무리 할 수 있었습니다.
