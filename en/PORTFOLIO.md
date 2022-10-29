# Work Experience

## [Bucketplace](https://www.bucketplace.com/)

- 2022.04 ~ current
- Core Platform Engineer
- Built common services, infrastructure components, and libraries for engineers

### Logging Pipeline

- Built logging server for every client send logs
- Developed a logging pipeline that receives logs from across multiple clients
- Go, Kafka, Kotlin, React
- Especially, I built the log server that receives every log data from many clients. The goal of it is reliability in high traffic situation. The server parses log data from byte array and send to the kafka.

### Feature Flag

- Built [feature flag](https://martinfowler.com/articles/feature-toggles.html) pilot service that changes feature's configuration dynamically
- Go, ETCD, Github Action
- Whole feature contexts are managed in GitHub repository. Engineers can review and merge the feature context safely on familiar platform. Feature contexts are pushed to ETCD and other application servers watch the key and change feature configurations dynamically.

### Gohouse

- Created and maintained Go common package library.
- Document Go style guide and testing guide

## [Karrot](https://www.daangn.com/)

- 2021.11 ~ 2022.01
- GeoInformation System platform team, Intern
- Built common services that is related to GIS for application engineers

### GeoLocation

- Built GeoLocation gRPC service which finds national information from IP or coordinates
- Python, Go, gRPC
- The pilot project is built by Python for POC. PoC enabled us to identify which parts could cause bottlenecks and plan in advance how to improve them. After that, the project is built by Go, and it has better performance(+6600%) than the PoC version.
- [Link - Developing predictable service for massive traffic](https://medium.com/daangn/%EC%98%88%EC%B8%A1-%EA%B0%80%EB%8A%A5%ED%95%9C-%EB%8C%80%EA%B7%9C%EB%AA%A8-%EC%84%9C%EB%B9%84%EC%8A%A4-%EA%B0%9C%EB%B0%9C%ED%95%98%EA%B8%B0-a33e2f3cef88)
  - Wrote the blog article about I built in internship period.
- [daangn/gogeos](https://github.com/daangn/gogeos) opensource contribution
  - Added new functions and test codes on `gogeos` which is porting version of GEOS

## [Doctor NOW](https://drnow.co.kr/)

- 2019.12 ~ 2020.08
- Founding member, Lead engineers
- Built main services, Organized infrastructures, build pipelines, and engineering team's culture

### MVP Service development & Leading engineering team

- Backend
  - Typescript, NestJS, TypeORM, Swagger
  - PostgreSQL
  - AWS RDS, S3, EC2, ECR, ECS Fargate
  - Docker, Docker Compose
- Client
  - Typescript, React Native, React, Redux, Redux-saga
- Built MVP services that are Non-face-to-face drug prescription and delivery applications
- Built the application that is for pharmacist using React Native, Typescript, Redux
- Built the API server using NestJS, PostgreSQL
- Dockerized development environment, deploied the server in AWS Fargate with ECR
- Documented API docs for client engineers using Swagger
- Introduced Git flow into engineering team and make two-week sprint and deployment cycle

## [goorm](goorm.io)

- 2019.07 ~ 2019.10
- Fullstack Engineer

### goormEDU

- Express, React, SCSS, Reactstrap, MongoDB
- Developed goormEDU service which is engineering education service

### goormIDE Renewer

- HTML, CSS, Bootstrap
- Renewed goormIDE service that is web IDE

# Project

## The Football - [Github repo](https://github.com/TheFootball)

- 2021.05.21 ~ 2021.05.23
- Built chatting game for Junction X Seoul hackathon with AWS

### Chat server

- [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/thefootball) Golang, Fiber, Websocket, Svelte, DynamoDB, Redis, Docker, Docker Compose, S3
- Built scalable chat server using Redis, Go, Websocket

## Mango Table

- 2021.01 ~ 2021.05
- Built a project management SaaS named "MangoTable" for startup as team leader
- Design the service's architecture, infrastructures, language and tech stack as team leader.

### Landing page

- AWS S3, CloudFront, React, Typescript, SaaS (Waitlist)
- Built a landing page to create demand-related indicators to funding using Typescript, React, Waitlist SaaS service.
- Deploied the service fastly to S3 and CloudFront
- During 3 days for posted in Product Hunt, over 100 recommandations and emails are received.

### MVP service

- [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/mango-table) Typescript, NestJS, MongoDB Atlas, Mongoose, React, Redux, Redux Saga, Sentry, Google Analytics, Auth0, AWS
- Built MVP service and open closed beta for registered emails
- Built a web client using Typescript, React, Redux, Redux Saga
- Built a backend using NestJS, Typescript, MongoDB
- Deploied service using AWS EC2, Atlas MongoDB, S3, CloudFront
- Introduced many SaaS services like Auth0, Mailgun, Sentry

## STMT(Six Things Must TODO) - [Github repo](https://github.com/6-things-must-to-do)

- 2020.10.25 ~ 2020.12.13
-
- Built productivity improvement and habit creation application, called STMT in Software Engineering class
- [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/changhoi/6-things-must-to-do) Go, Gin, Typescript, React Native, Redux, Redux-Saga, AWS DynamoDB
- [Documentation & demo](https://github.com/6-things-must-to-do/docs)

### Application & Team leading

- Trained team for client engineering
  - Taught Javascript and react than gave them assignment that creates recipe application with Simple API
- Built React Native application

### API server

- Built API server with Go, DynamoDB
- Because this project is my first Go project and I'm not familiar with DynamoDB, I studied all of those during project
- Used Gin for REST API framework and deploied the service on Ubuntu RasberryPI
- Studied DynamoDB table design pattern called "Single Table Design" which is recommended on AWS documentation and made article about the design pattern [in my tech blog](https://changhoi.kim/posts/database/dynamodb-single-table-design/)

## Rachios dating program - [Github repo](https://github.com/weehan-dev/dodohan)

- 2019.09.15 ~ 2019.09.23
- Built the application that makes matching for dating during HYU's festival using NodeJS, MongoDB
- Collected forms from google docs and exported the forms as CSV.
- About 500 people participated
