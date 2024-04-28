# 프로필

- 이름: 김창회
- 생일: 1996.04.17
- 지역: 서울

안녕하세요. 저는 공학적인 문제를 해결하는 것을 좋아하는 엔지니어입니다. 도전적인 데이터, 트래픽, 공학적인 문제를 해결하고 싶어합니다. 어떤 기술에 대해 깊숙히 이해하고 어떤 문제를 어떻게 해결하려고 하는 기술인지, 어떻게 사용하는 것이 좋은지, 어떤 경우엔 좋은 선택이 아닌지 등을 이해하고 사용하는 것을 좋아합니다. 더 나은 방법을 찾기 위한 커뮤니케이션, 주도적이고 빠른 문제 해결과 그 결과를 바탕으로 피드백을 적용하는 흐름을 지향합니다.

# 기술

## 언어

- **Go**
- **NodeJS TypeScript**
- Java, Kotlin

## 인프라

- **Docker & Docker Compose**
- **AWS**, GCP
- Kubernetes

## 기타

- **MongoDB**, **MySQL**, **DynamoDB**
- Git
- React & Redux
- 공부한 내용들 기억하고 싶은 것들을 간략하게 기록해둡니다.
  - <https://changhoi.kim>

# 학력

## 한양대학교

- 서울
- 주전공: 정보시스템학과
- 부전공: 빅데이터융합전공
- 2017.02 ~ 2022.02
- 누적 평점 4.03/4.5
- 전공 평점 4.29/4.5
  - [관련 수업 이수 내역](https://github.com/changhoi/RESUME/blob/master/COURSE.md)

# 경력

## [버킷플레이스](https://www.bucketplace.com/)

- 2022.04 ~ 2024.03
- Core Platform Engineer
- 버킷플레이스 개발팀이 공통적으로 사용해야 하는 인프라 및 서비스 개발

### Logging Pipeline

- 여러 시스템에서 로그를 받아 처리하는 로깅 파이프라인을 개발했습니다.
- Go, Kafka, Kotlin, React
- 클라이언트에서 보내는 로그를 가장 앞에서 받아주는 로그 서버를 개발했습니다. 아주 단순하게 메시지를 받아 Aggregator 역할을 하는 Kafka로 보내는 역할을 하는 서버였고, 처리 성능에 가장 큰 초점이 맞춰져 있었습니다. 처리 성능을 높이기 위해 Standard Library의 JSON 파서가 아닌 더 성능이 좋은 파서를 사용하였고, 바이트 시퀀스가 JSON 배열 형태로 들어오는지만 확인하고 내부를 확인하지 않고 바로 메시지를 보내도록 JSON 파서를 커스텀 했습니다. 커스텀한 파서는 Standard Library와 기본 타입을 사용했을 때보다 약 5배 성능이 향상되었습니다. 또한 운영 중에 보내지는 메시지의 크기를 줄이고자 Kafka의 Snappy 압축 옵션을 추가해 일정 크기의 랜덤한 데이터를 보냈을 때는 약 58%, 동일하고 간단한 데이터로 실험 했을 때는 약 66% 가량 메시지 사이즈를 줄였습니다.

### Feature Flag

- 동적으로 기능을 변경할 수 있는 [Feature Flag](https://martinfowler.com/articles/feature-toggles.html) 개발에 참여했습니다.
- Go, ETCD, Github Action
- Github을 메타데이터 관리 레포지토리로서 사용하는 Feature Flag POC 버전을 개발했습니다. 레포지토리에 머지되는 메타데이터를 검증하고 etcd에 Sync 하는 CLI를 개발했습니다. CLI 외에 etcd에 값을 쓰는 클라이언트가 다수이기 때문에 etcd 값을 안전하게 업데이트 하기 위해 etcd Lock과 Transaction에 대해 조사하고 유즈 케이스에 적합한 Transaction을 사용해 다수의 클라이언트가 업데이트 시 안전하게 업데이트 될 수 있도록 했습니다. 이 두 기능을 조사하고 적용한 것을 전사 기술 세션 주제로 발표했습니다.
- Go에서 Feature Flag 데이터를 쉽게 사용할 수 있는 SDK를 개발했습니다. 오픈 소스에서 일반적으로 사용하는 방법처럼 Feature 키를 문자열로 입력해 사용하는 방법 대신 리뷰 후 머지된 메타데이터를 기반으로 정적인 타입을 사용할 수 있도록 코드를 생성했습니다.
- SDK를 개발해가며 Backward Compatibility를 고려한 SDK 개발을 경험했습니다. 어떻게 개발해야 앞으로 복잡해질 기능을 대비하며 SDK를 고도화해 갈 수 있을지 고민하며 운영했습니다.

### Gohouse

- 전사적으로 사용되는 공통 Go 패키지를 관리했으며, Go Style Guide, Testing Guide를 제공하고 Lint 등 기타 도구들을 도입해 사내 Go 생태계가 파편화 되지 않도록 노력했습니다.

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

### MVP 서비스 개발

- Backend
  - Typescript, NestJS, PostgreSQL, Docker, AWS
- Client
  - Typescript, React Native, React, Redux, Redux-saga
- 서비스의 초기 버전인 비대면 약 처방 및 배달 애플리케이션 설계와 개발에 참여했습니다. React Native를 사용해 약사용 클라이언트 애플리케이션을 개발했고, NestJS, PostgreSQL을 사용해 API 서버를 개발했습니다.
- Node 서버 Dockerizing 과정에서 도커 이미지의 사이즈를 줄이기 위해 Dockerfile Best Practice를 학습하고 이를 적용했습니다. 결과적으로 가장 초기에 비해 이미지 사이즈를 70% 이상 크게 줄일 수 있었습니다.
  - [Docker Best Practice 학습하고 정리한 글](https://changhoi.kim/posts/docker/Docker-best-practices)
- 대구 코로나 유행시기에 코로나 맵을 빠르게 만들어 배포했습니다. 사람들에게 원격 진료가 가능한 병원과 원격 처방이 가능한 약국을 소개해주는 지도 앱이었습니다. 여러 채널을 통해 홍보해 많은 유입을 만들었고 서비스가 나오지 않은 상황에서도 서비스에 대해 알리고 사용자의 니즈를 파악하는 데 도움이 되었습니다.

## [구름(goorm)](goorm.io)

- 2019.07 ~ 2019.10
- 풀스택 개발자

### goormEDU
- React, ExpressJS, MongoDB를 사용해 구름 EDU 서비스의 신규 기능을 개발했습니다.

# 외부 활동

## 인프런 강의 

- [대규모 시스템 설계 강의](https://www.inflearn.com/course/%EB%8C%80%EA%B7%9C%EB%AA%A8%EC%8B%9C%EC%8A%A4%ED%85%9C-%EC%84%A4%EA%B3%84-%ED%8C%8C%ED%8A%B81)
- [직접 만들면서 배우는 Git Internals](https://www.inflearn.com/course/%EC%A7%81%EC%A0%91-%EB%A7%8C%EB%93%A4%EB%A9%B4%EC%84%9C-%EB%B0%B0%EC%9A%B0%EB%8A%94-git-internals)

## 네이버 부스트캠프 7기 백엔드 리뷰어

- 네이버 부스트캠프 7기 웹 개발 백엔드 리뷰어로서 참여했습니다.
- 2022.09 ~ 2022.10

## 기술 세션

- 2022.02 ~ 2022.12
- 개발자들과 공부한 내용을 공유하는 기술 세션을 진행했습니다.
- 세션에서 발표한 내용
  - [gRPC를 지탱하는 기술](https://changhoi.kim/posts/backend/grpc-internals/)
  - [Go GC](https://changhoi.kim/posts/go/go-gc/)
  - [DynamoDB Internals - 1](https://changhoi.kim/posts/database/dynamodb-internals-1/), [DynamoDB Internals - 2](https://changhoi.kim/posts/database/dynamodb-internals-2/)
  - [Kafka Internals](https://calico-silence-e0f.notion.site/Kafka-Internals-5fc6996622834dfd9c107f23f78e4371)
  - [DragonflyDB로 알아보는 캐시 알고리즘](https://calico-silence-e0f.notion.site/DragonflyDB-bd73f811f8774056bd4160c6ce284386)
  - [Rust 오너십](https://changhoi.kim/posts/rust/rust-ownership/)
  - Database Internals 책 스터디
  - 데이터중심 애플리케이션 설계

## Linux programming with Go 멘토

- 2021.09 ~ 2021.12
- 한양대학교 프로그래밍 동아리 FORIF에서 멘토로서 스터디를 이끌었습니다.
- "[Go systems programming](https://www.oreilly.com/library/view/go-systems-programming/9781787125643/)" 외 여러 서적을 이용해 스터디를 진행했습니다.

# 프로젝트

## Mango Table

- 2021.01 ~ 2021.05
- 기존 프로젝트 매니지먼트 서비스를 보완한 SaaS를 기획하고 창업에 도전했습니다. 팀 리더로서 개발 스택을 정하고, 프로젝트 설계 및 개발에 참여했습니다.

### MVP 서비스 소개 페이지 제작

- AWS S3, CloudFront, React, Typescript
- 국가 지원 사업 지원 및 투자 유치 목적으로 수요 관련 지표를 모으기 위한 랜딩 페이지 프로젝트를 진행했습니다. 메인 페이지 개발을 전담해 배포까지 진행했습니다. Typescript, React를 사용해 개발했고, 별도의 Backend 공수를 줄이고자 Waitlist SaaS를 사용했습니다. 배포는 S3, CloudFront를 사용해 간단히 배포했습니다. 랜딩페이지를 3일 동안 개발하고 Product Hunt에 게시하고 메인으로 게시되는 약 3일 동안 100개가 넘는 추천과 85명의 메일을 받을 수 있었습니다.

### 본 서비스 개발

- Typescript, NestJS, MongoDB, React, AWS
- 프로젝트 매니지먼트 서비스 MVP를 만들기 위해 약 3개월 동안 소개 페이지에서 이메일을 등록한 유저들을 대상으로 클로즈 베타를 준비하고 배포했습니다. 클라이언트 개발에 Typescript, React를 사용해 개발했습니다. 클라이언트 사이드의 비동기 처리와 상태 관리를 위해 Redux, Redux Saga를 사용해 개발했습니다. 서버는 NestJS, Typescript 스택으로 개발했습니다. 초기 서비스의 변경 사항이 많고 서비스 자체적인 특징으로도 자유로운 스키마가 요구되어 DocumentDB인 MongoDB를 사용해 개발했습니다. AWS EC2와 Atlas MongoDB를 사용해 배포했습니다. 서비스 개발 과정을 단축하기 위해 여러 SaaS를 활용했습니다. 사용자 인증을 위해 Auth0, 메일 서비스를 위해 Mailgun, 에러 로그 수집을 위해 Sentry를 사용했습니다. 결과적으로 FastVentures 최종 미팅까지 진행되었고 많은 서비스와 상호 작용하는 방법을 경험할 수 있었습니다.

## STMT(Six Things Must TODO) - [Github repo](https://github.com/6-things-must-to-do)

- 2020.10.25 ~ 2020.12.13
- Go, Typescript, React Native, AWS DynamoDB
- 학과 프로젝트 수업인 소프트웨어공학이론, 인공지능 수업으로 생산성 향상 및 습관 만들기 애플리케이션을 구성했습니다. 팀장으로 참여해 개발 모든 과정에 참여하고 개발했습니다. 팀원들에게 React, Redux를 가르치고 간단한 레시피 앱을 만들도록 한 후 프로젝트에 팀원들이 모두 참여할 수 있도록 이끌었습니다. 또한 서버 개발을 전담해 개발했습니다. DynamoDB의 데이터 모델링에 대해 자세히 학습하고 블로그에 정리했으며 프로젝트에 적용했습니다.
  - [DynamoDB 설계 방법을 학습하고 정리한 글](https://changhoi.kim/posts/database/dynamodb-single-table-design/)

## 두근두근 라치오스 - [Github repo](https://github.com/weehan-dev/dodohan)

- 2019.09.15 ~ 2019.09.23
- JS, MongoDB
- 위한이 한양대학교 학생들에게만 제공하던 매칭 프로그램을 축제를 맞아 이벤트성으로 외부 학교의 신청을 받고 매칭해주는 프로그램을 만들었습니다. 매칭을 위해 사람들에게 구글 설문지를 만들어 신청하도록 했습니다. 받은 신청서를 csv 형식으로 파싱하고 매칭 알고리즘으로 매칭되도록 했습니다. 매칭 알고리즘을 알아보고 도입하는 과정이 있었고, 매칭 이후 결과는 MongoDB에 저장 후 축제 당일에 SMS 및 메일로 결과를 발송해줬습니다. 약 500명 가량 참여하며 성공적으로 프로젝트를 마무리 할 수 있었습니다.

# 리더십

대표로서, 운영진으로서 팀원들과 함께 공동의 목표를 달성하기 위해 노력했습니다. 또한 다양한 입장에 있는 사람들, 다양한 직업군, 다양한 행정팀과 의사소통하는 방법에 대해서 고민해볼 수 있는 경험들이었습니다.

- 한양대학교 정보시스템학과 학생회장 (2018.01 ~ 2018.12)
- 한양대학교 정보시스템학과 웹진 웹진장 (2018.01 ~ 2018.12)
- 연합 동아리 P.rogramming 운영진 (2019.03 ~ 2019.10)
- 한양대학교 위한 운영진 개발팀(2018.12 ~ 2020.06)
- 한양대학교 위한 운영진 개발팀장 (2019.06 ~ 2020.06)
- 창업팀 망고테이블 대표 (2021.01 ~ 2021.05)

# 언어

- 한국어 (모국어)
- 영어 (능숙함)

# 링크

- email: <changhoi0522@gmail.com>
- [Blog](https://changhoi.kim)
- [GitHub](https://github.com/changhoi)
- [LinkedIn](https://www.linkedin.com/in/changhoi/)
