# Profile

- Name: Changhoi Kim
- Birth: 1996.04.17
- Location: Seoul, Korea

Hello! I'm a software engineer. I want to be a developer who solves challenging problems related to managing large data or massive traffic in a rapidly growing service. I enjoy working collaboratively and communicating well to improve the quality of the code base, such as test code or code review. And I also like to research how to solve problems most optimally, and to learn the solution even if it is unfamiliar.

# Skills

## Programming Language

- **Go**
- **Nodejs TypeScript**
- Java, Kotlin

## Infrastructure

- **Docker & Docker Compose**
- **AWS**, GCP
- Kubernetes

## E.T.C

- **MongoDB**, **MySQL**,  **DynamoDB**
- REST, gRPC
- Git
- React & Redux
- Tech blog: <https://changhoi.kim>

# Education

## Hanyang University

- Seoul, Korea
- Major: Dept. of Information System
- Minor: Big Data Science
- 2017.02 - 2022.02
- Cumulative GPA: 4.03/4.5
- Major Cumulative GPA: 4.29/4.5
  - [Relevant coursework](https://github.com/changhoi/RESUME/blob/master/en/COURSE.md)

# Work Experiences

## [Bucketplace](https://www.bucketplace.com/)

- 2022.04 - Present
- Core Platform team, Software Engineer

### Logging Platform

- Developed a logging pipeline for handling logs from various systems.
- Go, Kafka, Kotlin, React.
- Engineered a log server that acts as the initial receiver for logs sent from clients. This server has a straightforward role of forwarding messages to Kafka, serving as an aggregator. The primary focus was on optimizing processing performance. To enhance processing speed, a parser with better performance than the Standard Library's JSON parser was employed. The custom parser confirmed only the incoming byte sequence format as a JSON array, without inspecting the internals, leading to a direct message dispatch. The custom parser demonstrated approximately a 5x improvement in performance compared to using the Standard Library and basic types. Additionally, to reduce message size during operation, the Kafka Snappy compression option was introduced. This resulted in approximately a 58% reduction in message size when sending randomly generated data of a certain size and around a 66% reduction when experimenting with identical and straightforward data.

### Feature Flag
- Engaged in the development of dynamic feature toggles, as described in [Feature Toggles](https://martinfowler.com/articles/feature-toggles.html).
- Go, ETCD, Github Action.
- Developed a proof-of-concept (POC) version of Feature Flag using Github as a metadata management repository. Created a CLI to validate and sync the metadata merged into the storage, etcd. Investigated and implemented etcd Lock and Transactions to safely update values in etcd, considering that multiple clients write values to etcd. Presented the research and application of these two features as a topic in a company-wide technical session.
- Developed an SDK in Go to easily use Feature Flag data. Instead of using the common method of inputting feature keys as strings, enabled the use of static types which is generated, based on the metadata in etcd.
- Experienced SDK development with a focus on backward compatibility. Managed and operated with consideration for how to develop and enhance the SDK to handle future complex features.

### Gohouse
- Managed a universally used common Go package across the organization.
- Provided a Go Style Guide and Testing Guide, aiming to prevent fragmentation within the internal Go ecosystem. 
- Introduced various tools, including Lint, to ensure cohesion and consistency in the internal Go ecosystem.

## [Karrot](https://www.daangn.com/)

- 2021.11 - 2022.01
- Intern at the GeoLocation Platform Development Team
- Developed services commonly needed by the Daangn Market(Karrot) service development team especially related to geolocation.

### GeoLocation
- Developed a GeoLocation gRPC server that determines country information based on the user's latitude and longitude or IP address.
- Python, Go, gRPC.
- Experienced designing architecture according to requirements and developing a service to achieve predictable performance. After deploying the project, conducted performance tests, identified bottlenecks, and improved the final version's performance by approximately 66% compared to the initial application by resolving specific issues.
- [Building Predictable Large-scale Services](https://medium.com/daangn/%EC%98%88%EC%B8%A1-%EA%B0%80%EB%8A%A5%ED%95%9C-%EB%8C%80%EA%B7%9C%EB%AA%A8-%EC%84%9C%EB%B9%84%EC%8A%A4-%EA%B0%9C%EB%B0%9C%ED%95%98%EA%B8%B0-a33e2f3cef88)
  - Wrote an article summarizing the project
- Open-source contribution to [daangn/gogeos](https://github.com/daangn/gogeos)
  - Added functions required for the project, and released a new version.

## [Doctor NOW](https://drnow.co.kr/)

- 2019.12 - 2020.08
- Founding Member, Lead Developer, involved in the overall design and development of the service, contributed to infrastructure setup related to deployment, and fostered development team culture.

### MVP Service Development

- Backend: Typescript, NestJS, PostgreSQL, Docker, AWS
- Client: Typescript, React Native, React, Redux, Redux-saga
- Contributed to the design and development of the initial version of a telemedicine and medication delivery application. Developed the pharmacist client application using React Native and the API server using NestJS and PostgreSQL.
- Learned and applied Dockerfile Best Practices to reduce the size of Docker images during the Node server Dockerizing process. As a result, the image size was reduced by more than 70% compared to the initial version.
  - [Learnings and Summary of Docker Best Practices](https://changhoi.kim/posts/docker/Docker-best-practices)
- Quickly created and deployed a COVID map during the Daegu COVID outbreak. It was a map app that introduced hospitals offering remote consultations and pharmacies providing remote prescriptions. Promoted through various channels, generated significant traffic, and helped publicize the service and understand user needs, even before the service was officially launched.

## [goorm](goorm.io)

- 2019.07 - 2019.10
- Fullstack engineer
- Developed goormEDU, goormIDE services.
- Express, React, SCSS, Reactstrap, MongoDB

# Professional Experiences

## Inflearn Large-Scale System Design Part 1 Lecture

- Uploaded a lecture on large-scale system design on the online learning platform "Inflearn."
- [Link to the Course](https://www.inflearn.com/course/%EB%8C%80%EA%B7%9C%EB%AA%A8%EC%8B%9C%EC%8A%A4%ED%85%9C-%EC%84%A4%EA%B3%84-%ED%8C%8C%ED%8A%B81)

## NAVER Boost Camp 7th Back-end Reviewer

- Participated as a backend code reviewer for the 7th Naver Boost Camp.
- 2022.09 - 2022.10

## Engineering Session

- Initiated an engineering sessions where peers share what we've learned.
- 2022.02 ~ 2022.12
- Conducted technical sessions to share knowledge and insights with fellow developers.
- Topics covered in sessions:
  - [Technologies Empowering gRPC](https://changhoi.kim/posts/backend/grpc-internals/)
  - [Understanding Go Garbage Collection](https://changhoi.kim/posts/go/go-gc/)
  - [DynamoDB Internals - Part 1](https://changhoi.kim/posts/database/dynamodb-internals-1/) and [Part 2](https://changhoi.kim/posts/database/dynamodb-internals-2/)
  - [Exploring Kafka Internals](https://calico-silence-e0f.notion.site/Kafka-Internals-5fc6996622834dfd9c107f23f78e4371)
  - [Cache Algorithms with DragonflyDB](https://calico-silence-e0f.notion.site/DragonflyDB-bd73f811f8774056bd4160c6ce284386)
  - [Understanding Rust Ownership](https://changhoi.kim/posts/rust/rust-ownership/)
  - Database Internals book study
  - Designing Data-Centric Applications

## Linux programming with Go mentor

- Led the study as a mentor at FORIF, a programming club at Hanyang University.
- 2021.09 - 2021.12
- The study was conducted with "[Go systems programming](https://www.oreilly.com/library/view/go-systems-programming/9781787125643/)" and other books.

## Deep CS

- Computer Science study club
- 2021.08 - 2021.10
- Studied about popular CS topic with engineers
- [Link](https://changhoi.notion.site/Deep-CS-a36ac1380d4843c69867b184b36a50c3)

# Projects

## Mango Table

- 2021.01 ~ 2021.05
- Conceptualized and ventured into entrepreneurship by enhancing an existing project management service into a SaaS. As the team leader, defined the development stack and actively participated in project design and development.

### MVP Service Introduction Page Development

- AWS S3, CloudFront, React, Typescript
- Executed a landing page project to gather demand-related metrics for the purpose of obtaining support from national programs and attracting investment. Solely responsible for developing the main page and deploying it. Developed using Typescript and React, and utilized the Waitlist SaaS to reduce backend effort. Deployment was achieved simply using S3 and CloudFront. Developed the landing page in three days, posted it on Product Hunt, and during the three days it was featured, received over 100 upvotes and 85 emails.

### Main Service Development

- Typescript, NestJS, MongoDB, React, AWS
- Prepared and deployed a closed beta for users who registered their emails on the introduction page over approximately three months to create an MVP for the project management service. Used Typescript and React for client development. Employed Redux and Redux Saga for asynchronous handling and state management on the client side. Developed the server using NestJS and the Typescript stack. Due to frequent changes in the initial service and the need for a flexible schema, used DocumentDB MongoDB for development. Deployed using AWS EC2 and Atlas MongoDB. Utilized various SaaS to expedite the service development process, including Auth0 for user authentication, Mailgun for mail services, and Sentry for error log collection. Eventually progressed to the final meeting with FastVentures, gaining valuable experience in interacting with numerous services.

## STMT (Six Things Must TODO) - [Github Repo](https://github.com/6-things-must-to-do)

- 2020.10.25 ~ 2020.12.13
- Go, Typescript, React Native, AWS DynamoDB
- Configured a productivity enhancement and habit-building application for the software engineering theory and artificial intelligence project classes. As a team leader, actively participated in and led the entire development process. Taught team members React and Redux and guided them to create a simple recipe app, ensuring everyone's participation in the project. Also, took charge of server development. Delved into detailed learning of data modeling in DynamoDB, documented it on a blog, and applied it to the project.
  - [Learning and Documentation of DynamoDB Design Approach](https://changhoi.kim/posts/database/dynamodb-single-table-design/)

## Dodohan Lachios - [Github Repo](https://github.com/weehan-dev/dodohan)

- 2019.09.15 ~ 2019.09.23
- JavaScript (JS), MongoDB
- Developed a matching program for matching during a festival. Created a Google Form for people to apply for matching. Parsed the received applications in CSV format and implemented a matching algorithm for the pairing process. Explored and adopted the matching algorithm, and after the matching process, stored the results in MongoDB. On the day of the festival, sent the results via SMS and email to the participants. Successfully concluded the project with around 500 participants.

# Leadership

As a representative and management team member, I worked hard to achieve a common goal with my teammates. It was also an experience that allowed me to think about how to communicate with people in various positions, and administrative teams.

- President of the Student Council of Dept. of Information Systems, HYU (2018.01 - 2018.12)
- President of Webzine of Dept. of Information System, HYU (2018.01 - 2018.12)
- P.rogramming management team (2019.03 - 2019.10)
- Weehan, HYU Community, development team (2018.12 - 2020.06)
- Weehan, HYU Community, development team leader (2019.06 - 2020.06)
- Representative of Mango Table team (2021.01 - 2021.05)

# Language

- Korean
- English
  - Reading & Writing - Proficient
  - Listening & Speaking - Conversational

# Link

- email: <0417kch@naver.com>
- [Blog](https://changhoi.github.io)
- [GitHub](https://github.com/changhoi)
- [LinkedIn](https://www.linkedin.com/in/changhoi/)
