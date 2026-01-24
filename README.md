# 프로필

- 이름: 김창회
- 생일: 1996.04.17
- 지역: 서울

안녕하세요. 저는 창업가 김창회입니다. 미래를 만드는 것에 관심이 많습니다. 창업 이전 엔지니어로서 5년 정도 일하면서 주로 플랫폼 팀의 일을 했습니다. Devtool, 대규모 트래픽을 받는 서비스, 어려운 공학적인 문제를 푸는 걸 좋아합니다. Physical AI에 대한 지식은 매우 부족하지만 타이트한 환경에서 최적의 퍼포먼스를 만들어야 하는 엔지니어링에 매우 관심과 호기심이 많습니다.

# 기술

## 언어

- **Go**
- **NodeJS TypeScript**, **Python**

## 인프라

- **Docker & Docker Compose**
- **GCP**, **AWS**
- **Kubernetes**

## 기타

- **MongoDB**, **MySQL**, **DynamoDB**
- 기억하고 싶은 것들을 간략하게 기록해둡니다.
  - <https://changhoi.kim>

# 학력

## 한양대학교

- 서울
- 주전공: 정보시스템학과
- 부전공: 빅데이터융합전공
- 2017.02 ~ 2022.02
- 누적 평점 4.03/4.5
- 전공 평점 4.29/4.5
  - [관련 수업 이수 내역](./COURSE.md)

# 경력

## [Bayesians](https://www.linkedin.com/company/bayesians/)
- 2025.01 ~ 2025.10
- Co-Founder
- 9개월 동안 7개 정도의 아이템을 시도해보았고, Friday까지 함께 만들고 회사를 나왔습니다.

### Friday: AI that calls you for self-reflection
- 특정 시각에 전화를 걸어 회고를 작성하도록 도와주는 Voice AI Friday를 만들었습니다.
- [Product Hunt Daily #1](https://www.producthunt.com/products/friday-8)

## 창업
- 2024.04 ~ 2024.12
- 공동 창업자를 찾고 여러 PMF를 찾기 위해 노력했습니다.
- 2024년 초 Lovable과 유사한 제품을 시도하고 중순에는 LLMOps 플랫폼을 만들었습니다.
- 2024년 하반기 Antler KOR5 batch에 참여해 공동창업자를 찾으며 여러 아이템 빌드를 했습니다.

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
- Co-Founder
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

## [구름](https://goorm.io/)

- 2019.06 ~ 2019.10
- Fullstack Software Engineer
- 구름 에듀의 서비스를 개발했습니다.

# 외부 활동

## F-Lab 멘토
- 주니어 엔지니어를 대상으로 Software Engineering 관련 멘토링을 진행하고 있습니다.

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

# 언어

- 한국어 (모국어)
- 영어 (능숙함)

# 링크

- email: <changhoi0522@gmail.com>
- [Blog](https://changhoi.kim)
- [GitHub](https://github.com/changhoi)
- [LinkedIn](https://www.linkedin.com/in/changhoi/)
