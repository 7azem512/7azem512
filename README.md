<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0d1117,50:161b22,100:238636&text=HAZEM%20SAED&fontColor=ffffff&fontSize=45&fontAlignY=38&desc=Java%20Backend%20Developer&descAlignY=58&descSize=18&animation=fadeIn"/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=2200&pause=700&color=3FB950&center=true&vCenter=true&repeat=true&width=820&height=70&lines=%24+whoami;Java+Backend+Developer;%24+focus;Spring+Boot+%7C+Microservices+%7C+Distributed+Systems;%24+mission;Build+secure.+Build+reliable.+Understand+the+trade-offs." />

<br>

LinkedIn
   /   
Email
   /   
Repositories

</div>

> whoami

public class HazemSaed {

    String role = "Java Backend Developer";

    String[] mainStack = {
        "Java",
        "Spring Boot",
        "Spring Security",
        "Spring Cloud",
        "PostgreSQL",
        "Redis",
        "Kafka",
        "Keycloak",
        "Docker"
    };

    String[] interests = {
        "Backend Architecture",
        "Distributed Systems",
        "API Security",
        "Authentication & Authorization",
        "Databases",
        "Messaging",
        "Observability"
    };

    String currentMission =
        "Turning business requirements into secure, reliable and maintainable backend systems.";
}

I'm a Computer Science graduate from Menoufia University focused on backend engineering with Java and Spring Boot.

I enjoy working on the parts of software where correctness and system behavior actually matter:

Authentication
Authorization
REST API Design
Database Modeling
Caching
Business Logic
Concurrency
Messaging
Resilience
Observability
Architecture

My goal isn't just to make an endpoint return 200 OK.

I want to understand why the system works, how it fails, what trade-offs were made, and how to design it better.

<div align="center">

SYSTEM.out.println("Building...");

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=15&duration=1800&pause=500&color=8B949E&center=true&vCenter=true&repeat=true&width=850&lines=Designing+REST+APIs...;Securing+distributed+systems...;Handling+concurrency...;Publishing+events...;Tracing+requests...;Breaking+things...;Debugging+things...;Learning+why+they+broke..." />

</div>

01. Selected Work

EventHub

Microservices Event Management & Ticketing Platform

Repository: github.com/7azem512/EventHub

Release: v1.0.0

EventHub is a backend-focused event management and ticketing platform built around microservices, distributed communication, booking concurrency, reliable event publishing, security, and observability.

EVENTHUB
│
├── Business Services
│   ├── Event Service
│   ├── Booking Service
│   ├── User Service
│   ├── Media Service
│   └── Notification Service
│
├── Platform
│   ├── Spring Cloud Gateway
│   ├── Eureka Service Discovery
│   ├── Spring Cloud Config
│   └── Keycloak
│
├── Booking & Concurrency
│   ├── Redis Reservations
│   ├── Reservation TTL
│   ├── Atomic Capacity Protection
│   └── Booking Lifecycle
│       ├── PENDING
│       ├── CONFIRMED
│       ├── CANCELLED
│       └── EXPIRED
│
├── Event-Driven Architecture
│   ├── Apache Kafka
│   ├── Transactional Outbox
│   ├── At-Least-Once Delivery
│   └── Idempotent Consumer
│
├── Reliability
│   ├── Resilience4j Retry
│   └── Circuit Breaker
│
├── Observability
│   ├── Prometheus
│   ├── Grafana
│   ├── OpenTelemetry
│   └── Tempo
│
└── Data & Storage
    ├── PostgreSQL
    ├── Flyway
    ├── Redis
    ├── MinIO
    └── Cloudinary

<details>
<summary><b>Read more about EventHub</b></summary>

<br>

Architecture

EventHub uses a database-per-service approach with an API Gateway as the public entry point.

Synchronous communication is used where an immediate response is required, while Kafka is used for asynchronous booking lifecycle events.

Client
  |
  v
API Gateway
  |
  +------> Event Service
  |
  +------> User Service
  |
  +------> Media Service
  |
  +------> Booking Service
  |             |
  |             +------> Redis
  |             |
  |             +------> Outbox Table
  |                         |
  |                         v
  |                       Kafka
  |                         |
  |                         v
  +------> Notification Service

Booking Flow

The Booking Service validates the event, booking window, ticket type and available capacity before creating a booking.

Redis is used for temporary reservations and atomic capacity protection.

PENDING
   |
   +------> CONFIRMED
   |
   +------> CANCELLED
   |
   +------> EXPIRED

Reliable Messaging

Booking lifecycle changes are written to an outbox table inside the same database transaction as the booking change.

A background publisher sends unpublished events to Kafka.

The Notification Service consumes those events and protects itself against duplicate delivery using an idempotent consumer.

Booking Service
      |
      v
Transactional Outbox
      |
      v
Kafka
      |
      v
Notification Service
      |
      v
Idempotency Check
      |
      v
Notification Database

Handled booking events:

BOOKING_CREATED
BOOKING_CONFIRMED
BOOKING_CANCELLED
BOOKING_EXPIRED

Security

The platform uses Keycloak with:

OAuth2

OpenID Connect

JWT

Authorization Code Flow with PKCE

Role-based access control

Main roles:

USER
ORGANIZER
ADMIN

Observability

The project includes:

Micrometer · Prometheus · Grafana · OpenTelemetry · Tempo

This allows metrics collection, dashboards, and distributed tracing across service boundaries.

Stack

Java · Spring Boot · Spring Cloud · Spring Security · PostgreSQL · Redis · Kafka · Keycloak · Flyway · Resilience4j · Docker Compose · Prometheus · Grafana · OpenTelemetry · Tempo

</details>

FitLink

Multi-Role Fitness Platform Backend

Repository: github.com/7azem512/FitLink

FitLink is a backend platform connecting Trainees, Coaches, and Gyms through secure authentication, role-based access, profile management, and production-oriented backend workflows.

FITLINK
│
├── Identity & Access
│   ├── Registration
│   ├── Email OTP
│   ├── Login
│   ├── Password Recovery
│   ├── Google Sign-In
│   ├── JWT Access Token
│   └── Refresh Token Flow
│
├── Security
│   ├── Spring Security
│   ├── BCrypt
│   ├── RBAC
│   ├── Rate Limiting
│   └── Protected Resources
│
├── Persistence
│   ├── PostgreSQL
│   ├── Spring Data JPA
│   └── Hibernate
│
├── Infrastructure
│   ├── Redis
│   ├── S3-Compatible Storage
│   ├── Docker
│   ├── Docker Compose
│   └── GitHub Actions
│
└── Cross-Cutting
    ├── Validation
    ├── Centralized Exception Handling
    ├── AOP Logging
    └── OpenAPI / Swagger

<details>
<summary><b>Read more about FitLink</b></summary>

<br>

The project focuses heavily on backend concerns that appear in real applications rather than basic CRUD.

Authentication

Implemented multiple authentication flows including:

Email OTP verification

Access and refresh tokens

Password recovery

Google Sign-In

Role-based authorization

Secure password hashing

API Engineering

Built REST APIs with:

Request validation

Standardized error responses

Centralized exception handling

Rate limiting

API documentation

Structured application logging

Infrastructure

Used:

PostgreSQL · Redis · Docker · Docker Compose · GitHub Actions

</details>

EduNest

Mentorship & Learning Platform Backend

Repository: github.com/7azem512/EduNest

A Spring Boot backend designed around structured interactions between mentors and learners.

EDUNEST
│
├── Authentication
├── Authorization
├── Tasks
├── Quizzes
├── Projects
├── Certificates
├── Notifications
├── Mentor / Learner Interaction
└── WebSocket Communication

The application contains 6+ functional areas and includes JWT authentication, RBAC, REST APIs, WebSocket communication, Docker, and OpenAPI documentation.

<details>
<summary><b>Technical details</b></summary>

<br>

Backend

Java · Spring Boot · Spring Security

Communication

REST APIs · WebSocket

Engineering

JWT · RBAC · Docker · Swagger / OpenAPI

</details>

Bank API

Banking Backend

Repository: github.com/7azem512/BankApi

A secure Spring Boot REST API implementing common banking operations.

BANK API
│
├── Account Management
├── Balance Tracking
├── Money Transfers
├── Transaction History
│
├── Security
│   ├── Authentication
│   └── Authorization
│
├── Validation
├── Exception Handling
├── PDF Statements
└── Email Notifications

Built using:

Java · Spring Boot · Spring Security · JPA · Hibernate · MySQL

02. Backend Toolbox

language:
  - Java
  - SQL

backend:
  - Spring Boot
  - Spring MVC
  - Spring Security
  - Spring Data JPA
  - Hibernate

microservices:
  - Spring Cloud
  - API Gateway
  - Eureka Service Discovery
  - Spring Cloud Config
  - Load-Balanced Service Communication

messaging:
  - Apache Kafka
  - Transactional Outbox
  - Idempotent Consumer
  - Event-Driven Architecture

databases:
  - PostgreSQL
  - MySQL
  - MongoDB

cache:
  - Redis
  - TTL Reservations
  - Atomic Capacity Counters

api:
  - REST
  - OpenAPI
  - Swagger
  - WebSocket

security:
  - Spring Security
  - Keycloak
  - OAuth2
  - OpenID Connect
  - JWT
  - Access / Refresh Tokens
  - RBAC
  - BCrypt
  - OTP
  - Google Sign-In
  - Rate Limiting

reliability:
  - Resilience4j
  - Retry
  - Circuit Breaker
  - At-Least-Once Delivery
  - Idempotency

observability:
  - Micrometer
  - Prometheus
  - Grafana
  - OpenTelemetry
  - Tempo

engineering:
  - Business Rule Modeling
  - Concurrency Handling
  - Database-per-Service
  - Flyway Migrations
  - Validation
  - Centralized Exception Handling
  - AOP Logging

devops:
  - Docker
  - Docker Compose
  - Git
  - GitHub Actions
  - Maven

currently_learning:
  - Kubernetes
  - CI/CD for Microservices
  - Production Deployment
  - Secret Management
  - Advanced Kafka Reliability

03. How I Think About Backend

REQUEST
   |
   v
VALIDATION
   |
   v
AUTHENTICATION
   |
   v
AUTHORIZATION
   |
   v
BUSINESS RULES
   |
   v
TRANSACTION
   |
   v
DATABASE
   |
   v
RESPONSE
   |
   +-------> LOGGING
   |
   +-------> ERROR HANDLING
   |
   +-------> METRICS
   |
   +-------> TRACING

A backend isn't just:

Controller -> Service -> Repository

The interesting questions start after that.

What happens if two requests arrive together?

What happens when Redis is unavailable?

What happens when another service is down?

What happens when the same Kafka message arrives twice?

What happens when a token is stolen?

What happens when the database transaction fails halfway?

How do I avoid losing an event after committing business data?

Who owns this business rule?

Should this state live in PostgreSQL or Redis?

Can this operation safely be retried?

How do I trace one request across multiple services?

How do I debug this at 2 AM?

Those are the problems I enjoy learning to solve.

04. Current Learning Path

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=16&duration=1700&pause=450&color=58A6FF&center=true&vCenter=true&repeat=true&width=820&lines=Microservices+%3E+Deployment;Deployment+%3E+Kubernetes;Kubernetes+%3E+Helm;CI%2FCD+%2B+Secret+Management;Kafka+Reliability+%2B+Production+Hardening" />

</div>

Spring Boot
     |
     v
Microservices
     |
     +------------+------------+-------------+
     |            |            |             |
     v            v            v             v
 Gateway       Discovery      Config      Messaging
     |            |            |             |
     +------------+------------+-------------+
                       |
                       v
                 Observability
                       |
                       v
                Docker Compose
                       |
                       v
                  Kubernetes
                       |
             +---------+---------+
             |                   |
             v                   v
           Helm                CI/CD
             |                   |
             +---------+---------+
                       |
                       v
              Production Hardening

Currently studying:

Kubernetes · Helm · CI/CD for Microservices · Secret Management · Production Deployment · Advanced Kafka Reliability

05. Contribution Activity

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=7azem512&bg_color=0d1117&color=8b949e&line=3fb950&point=ffffff&area=true&area_color=238636&hide_border=true" width="100%"/>

</div>

06. Watch My Contributions Move

<div align="center">

<p>
  My contribution graph, but slightly more alive.
</p>

<img src="https://raw.githubusercontent.com/7azem512/7azem512/output/github-contribution-grid-snake-dark.svg" width="100%"/>

</div>

07. Current Status

[████████████████████████░░░░] Java / Spring Boot

[██████████████████████░░░░░░] Backend Security

[████████████████████░░░░░░░░] Microservices

[██████████████████░░░░░░░░░░] Distributed Systems

[████████████████░░░░░░░░░░░░] System Design

[████████░░░░░░░░░░░░░░░░░░░░] Kubernetes

while (true) {
    learn();
    build();
    breakThings();
    understandWhy();
    rebuildBetter();
}

08. Education

Bachelor of Science in Computer Science
Menoufia University
Graduated 2026

09. Open To

Java Backend Developer
Backend Software Engineer
Spring Boot Developer

I'm particularly interested in working on backend systems involving:

APIs · Security · Authentication · Databases · Microservices · Distributed Systems · Messaging · Architecture

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=2500&pause=900&color=3FB950&center=true&vCenter=true&repeat=true&width=700&lines=Build+it.;Break+it.;Understand+it.;Build+it+better." />

<br><br>

Hazem Saed

Java Backend Developer

LinkedIn
   /   
Email

<br>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:0d1117,50:161b22,100:238636&section=footer"/>

</div>
