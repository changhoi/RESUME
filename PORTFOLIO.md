## 경력

### [닥터NOW](https://drnow.co.kr/)

- 2019.12 ~ 2020.08
- 초기 창업 멤버
- 내용: 리드 개발자로서, 서비스 전체의 설계 및 개발에 참여하고 배포와 관련된 인프라 구성 및 개발팀 문화에 기여했습니다.
    <details>
        <summary>자세히</summary>

        1. MVP 서비스 개발 및 개발팀 리드
        서비스의 초기 버전인 비대면 약 처방 및 배달 애플리케이션 설계와 개발에 참여했습니다. 개발팀 리더로서, 클라이언트와 백앤드의 기술 스택을 설정 및 개발, 그리고 협업에 대한 방식을 제시했습니다. 우선 애플리케이션은 크로스 플랫폼을 지원하는 React Native를 사용했습니다. API 서버의 경우, NestJS, PostgreSQL을 사용해 만들고 개발 환경을 Docker, Docker Compose를 사용했습니다. 저희는 인프라에 대한 노력을 최소화 하고자 서버리스 서비스인 AWS Fargate를 사용해, 컨테이너 이미지를 배포했습니다. 클라이언트 중 약사용 앱, 그리고 백앤드 개발을 전담했습니다. 또한 클라이언트 개발자와 API에 대한 정보를 공유하기 위해 Swagger를 사용해 API 문서를 개발 서버에 배포했습니다. 또한 브랜치 관리 전략인Git flow를 차용해 2주간 개발 주기를 가지고 주기적으로 배포할 수 있도록 했습니다.

        2. 이벤트성 코로나맵 설계 및 개발
        MVP 개발 중, 대구 지역 코로나 확산으로 코로나맵이 유행했습니다. 서비스를 홍보할 목적으로 확진자 수에 대한 정보와, 대구 지역의 비대면 진료가 가능한 병원 목록 및 약국 연락처를 제공하는 코로나맵을 빠르게 개발했습니다. 클라이언트 배포 과정과 백앤드 서버 개발을 전담했습니다. 빠른 개발을 위해 웹 서비스로 구성했습니다. 마스터 브랜치에 머지 되었을 때, AWS S3에 배포가 되도록 Github Actions를 사용했습니다. 백앤드는 타지역 정보를 추가해달라는 요청을 받기 위한 간단한 API를 제공해야 했습니다. 간단한 배포를 위해 Serverless Framework와 타입스크립트를 사용했고, 테이블 구성이 간단해 DynamoDB를 사용했습니다. 배포는 AWS Lambda, API Gateway를 통해 구성했습니다. 결과적으로, 대구 지역 외 정보 수집 요청 데이터를 서비스의 초기 제휴 약국 지역 선정에 잘 활용할 수 있었습니다.

    </details>
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
- 내용: 풀스택 개발자로서 구름 Edu 서비스 개발에 참여했습니다. 구름 IDE 리뉴얼 작업에 일부 기여했습니다.
- 기술:
  - Express, React, SCSS, Reactstrap
  - MongoDB

## 프로젝트

### The Football - [Github repo](https://github.com/TheFootball)
- 내용: Junction X Seoul 해커톤에 참여했습니다. AWS를 최대한 활용한 웹 게임을 기획하고, 백앤드를 맡아 스케일 아웃이 가능한 웹소켓을 통한 실시간 1:N 게임을 위해 Go와 Redis Pub/Sub를 사용해 개발했습니다. 
    <details>
        <summary>자세히</summary>

        Junction X Seoul 해커톤의 파트너사인 AWS의 과제를 선택해, AWS를 최대한 활용한 웹 게임을 만들기로 했습니다. 저희는 채팅 기반의 일 대 다수의 탄막 피하기 게임을 기획하고, 의도적으로 다수의 사용자들이 접근한다는 가정을 세우고 스케일아웃이 가능한 채팅을 구현하고자 했습니다. 기술 스택은 클라이언트는 Svelte를 사용하기로 했고, 백앤드는 Go, Fiber를 사용해 구현하기로 했습니다. 저는 주로 백앤드 작업을 했습니다. 단순 웹소켓만 사용한 채팅 서버 환경에서는, 여러 인스턴스에서 동작하는 서버들 사이에서 같은 게임 룸 안에 있는 사용자이지만, 컨넥션은 각각 다른 인스턴스에 있는 경우 채팅 내용을 공유하기 어렵다는 문제가 있었고, 해당 문제를 해결하기 여러 인스턴스들 사이에서 메시지를 공유해줄 통로가 필요하다는 생각을 했습니다. 관련된 케이스를 찾아보다가 Redis Pub/Sub을 사용해 메시지를 전달할 수 있음을 알게 되었고, 해당 방식을 사용해 채팅을 구현했습니다. 해커톤 행사 기간 동안 완성하지 못해, 학기를 마무리 하고 마무리 작업을 진행하고 있습니다.

    </details>
- 기간: 2021.05.21 ~ 2021.05.23 & 2021.07 ~ 진행 중
- 기술: [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/thefootball) Golang, Fiber, Websocket, Svelte, DynamoDB, Redis, Docker, Docker Compose, S3

### Mango Table
- 내용: 만다라트 차트를 사용한 프로젝트 매니지먼트 SaaS 기획하고 창업에 도전했습니다. 팀 리더를 맡아 개발 스택을 선택하고 서버와 클라이언트 모두 개발에 참여했습니다.
    <details>
        <summary>자세히</summary>

        기존 프로젝트 매니지먼트 서비스를 보완한 SaaS를 기획하고 창업에 도전했습니다. 저는 팀 리더를 맡아서 개발 스택을 정하고, 프로젝트 설계 및 개발에 참여했습니다. 개발 속도를 위해 가장 익숙한 프레임워크인 NestJS와 React를 주 스택으로 정했습니다. 핵심 데이터들 사이에 복잡한 연관이 있고, 유연한 스키마가 더 효율적이라고 판단해 MongoDB를 사용했습니다. 특히, 하나의 스키마를 재귀적으로 참조하는 구조가 있었는데, 이를 간단한 쿼리로 모두 불러오게 하기 위해 Ancestor를 배열에 저장하는 방식으로 설계해 자식 도큐먼트를 한 번의 쿼리로 불러올 수 있도록 했습니다. 클라이언트에서는 복잡한 상태를 관리하기 위해 Redux를 도입해 중앙에서 상태를 관리할 수 있도록 했고, API 로직을 Saga가 처리하게 했습니다. 프로젝트를 만드는 동안 React와 Email Register를 도와주는 API 서비스를 사용해 간단하게 서비스 핵심 컨셉을 담은 랜딩페이지를 만들어 Email Register가 가능하게 한 뒤, S3에 배포하고 Product Hunt라는 초기 프로젝트를 홍보할 수 있는 곳에 게시했습니다. 메인에 게시되는 약 3일간 85명의 Email을 등록 받았고, 100이 넘는 추천을 받았습니다. 2021년 예비창업패키지에 선정되지 못해 개인 프로젝트로 전환해 취미로 개발하고 있습니다.
        
    </details>
- 기간: 2021.01 ~ 2021.05
- 기술: [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/mango-table) Typescript, NestJS, MongoDB Atlas, Mongoose, React, Redux, Redux Saga, Sentry, Google Analytics, Auth0, AWS
- Link: <https://mangotable.me>

### STMT(Six Things Must TODO) - [Github repo](https://github.com/6-things-must-to-do)

- 내용: 소프트웨어공학이론, 인공지능 수업으로 생산성 향상 및 습관 만들기 애플리케이션을 구성했습니다. 팀장으로 참여해 개발 모든 과정에 참여하고 개발했습니다.
    <details>
        <summary>자세히</summary>

        학과 프로젝트 수업인 소프트웨어 공학이론 수업에서 팀장을 맡아 프로젝트를 이끌었습니다. 저희는 생산성 향상 및 습관 만들기 앱을 기획했습니다. React Native를 사용해 앱을 만들기로 했고 팀원들이 개발적 역량이 부족한 상태여서, JS와 React Native를 학습할 수 있도록 도와주고, 무료 레시피 API를 활용한 레시피 앱을 만드는 미니 프로젝트를 함께 진행해 본 프로젝트에 참여할 수 있도록 했습니다. API 서버는 제가 전담하여 평소 공부하고 싶던 스택을 사용했습니다. 우선 평소 Go언어의 생산성, 간단함, 속도 등 여러 장점을 들어와서 관심이 있던 상태라, Go를 사용해 개발을 진행하고자 했습니다. Go, Gin을 사용해 개발했으며 집에 있는 라즈베리파이 우분투에 빌드된 바이너리 파일을 우분투 service에 등록해 개발 서버를 구현했습니다. 공유기 설정에서 443 포트의 포트포워딩을 서버로 돌려두고, 도메인도 붙여 사용했습니다. 데이터베이스는 DynamoDB를 사용했습니다. 이유는 수업 자체가 AWS와 함께 하는 수업이기도 해서, AWS 서비스를 사용하려고 하기도 했고, 과거에 DynamoDB를 잘 알지 못하는 상태에서 간단한 테이블 구조를 갖는 서비스에 사용했던 적이 있었는데, 조금 더 복잡한 테이블 구성에서 더 자세히 공부하고 사용해보고 싶어서 해당 데이터베이스를 선택했습니다. DynamoDB 테이블 설계를 위해 AWS에서 공식적으로 추천하는 "Single Table Design"을 학습해 적용했습니다. 학습한 내용을 정리해 개인 블로그에 게시한 상태이고, 해당 글이 구글 검색 기준 "dynamodb design"과 유관한 검색어 최상단에 위치하고 있습니다.
        
    </details>
- 기간: 2020.10.25 ~ 2020.12.13
- 기술: [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/6-things-must-to-do) Go, Gin, Typescript, React Native, Redux, Redux-Saga, AWS DynamoDB
- [Documentation & demo](https://github.com/6-things-must-to-do/docs)

### 두근두근 라치오스 - [Github repo](https://github.com/weehan-dev/dodohan)

- 내용: 위한이 한양대학교 학생들에게만 제공하던 매칭 프로그램을 축제를 맞아 이벤트성으로 외부 학교의 신청을 받고 매칭해주는 프로그램을 만들었습니다.
    <details>
        <summary>자세히</summary>

        한양대학교 축제 기간 동안 외부 대학 학생들을 포함해 미팅을 할 수 있도록 매칭해주는 서비스를 만들었습니다. 신청은 구글 독스를 통해 받고, 받은 신청서를 csv 형식으로 파싱하고 매칭 알고리즘으로 매칭되도록 했습니다. 결과는 MongoDB에 저장하고 축제 당일에 SMS 및 메일로 결과를 발송해줬습니다. 프로그램은 CLI 형태로 NodeJS를 사용했습니다. 약 500명이 참여했으며, 반응도 괜찮았던 성공적인 프로젝트였습니다.

    </details>
- 기간: 2019.09.15 ~ 2019.09.23
- 기술: JS, MongoDB
- 약 500명 가량 참여