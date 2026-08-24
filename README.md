<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0d1117,50:161b22,100:238636&text=HAZEM%20SAED&fontColor=ffffff&fontSize=45&fontAlignY=38&desc=Java%20Backend%20Developer&descAlignY=58&descSize=18&animation=fadeIn"/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=2200&pause=700&color=3FB950&center=true&vCenter=true&repeat=true&width=760&height=70&lines=%24+whoami;Java+Backend+Developer;%24+current_stack;Spring+Boot+%7C+Spring+Security+%7C+PostgreSQL+%7C+Redis;%24+mission;Build+secure.+Build+clean.+Build+for+scale." />

<br>

[LinkedIn](https://www.linkedin.com/in/hazem-saed-36092525a)
   /   
[Email](mailto:hazemsaed512@gmail.com)
   /   
[Repositories](https://github.com/7azem512?tab=repositories)

</div>

---

## `> whoami`

```java
public class HazemSaed {

    String role = "Java Backend Developer";

    String[] mainStack = {
        "Java",
        "Spring Boot",
        "Spring Security",
        "PostgreSQL",
        "Redis",
        "Docker"
    };

    String[] interests = {
        "Backend Architecture",
        "API Security",
        "Authentication",
        "Databases",
        "Distributed Systems"
    };

    String currentMission =
        "Turning business requirements into secure and maintainable backend systems.";
}
```

I'm a **Computer Science graduate from Menoufia University** focused on backend engineering with Java and Spring Boot.

I enjoy working on the parts of software where correctness actually matters:

`Authentication`
`Authorization`
`REST API Design`
`Database Modeling`
`Caching`
`Business Logic`
`Error Handling`
`Security`
`Architecture`

My goal isn't just to make an endpoint return `200 OK`.

I want to understand **why the system works, how it fails, and how to design it better.**

---

<div align="center">

### `SYSTEM.out.println("Building...");`

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=15&duration=1800&pause=500&color=8B949E&center=true&vCenter=true&repeat=true&width=750&lines=Designing+REST+APIs...;Securing+endpoints...;Modeling+data...;Handling+edge+cases...;Containerizing+services...;Breaking+things...;Debugging+things...;Learning+why+they+broke..." />

</div>

---

# `01. Selected Work`

## FitLink

### Multi-Role Fitness Platform Backend

**Repository:** [github.com/7azem512/FitLink](https://github.com/7azem512/FitLink)

FitLink is a backend platform connecting **Trainees, Coaches, and Gyms** through secure authentication, role-based access, profile management, and production-oriented backend workflows.

```text
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
```

<details>
<summary><b>Read more about FitLink</b></summary>

<br>

The project focuses heavily on backend concerns that appear in real applications rather than basic CRUD.

### Authentication

Implemented multiple authentication flows including:

* Email OTP verification
* Access and refresh tokens
* Password recovery
* Google Sign-In
* Role-based authorization
* Secure password hashing

### API Engineering

Built REST APIs with:

* Request validation
* Standardized error responses
* Centralized exception handling
* Rate limiting
* API documentation
* Structured application logging

### Infrastructure

Used:

`PostgreSQL · Redis · Docker · Docker Compose · GitHub Actions`

</details>

---

## EduNest

### Mentorship & Learning Platform Backend

**Repository:** [github.com/7azem512/EduNest](https://github.com/7azem512/EduNest)

A Spring Boot backend designed around structured interactions between mentors and learners.

```text
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
```

The application contains **6+ functional areas** and includes JWT authentication, RBAC, REST APIs, WebSocket communication, Docker, and OpenAPI documentation.

<details>
<summary><b>Technical details</b></summary>

<br>

**Backend**

`Java · Spring Boot · Spring Security`

**Communication**

`REST APIs · WebSocket`

**Engineering**

`JWT · RBAC · Docker · Swagger / OpenAPI`

</details>

---

## Bank API

### Banking Backend

**Repository:** [github.com/7azem512/BankApi](https://github.com/7azem512/BankApi)

A secure Spring Boot REST API implementing common banking operations.

```text
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
```

Built using:

`Java · Spring Boot · Spring Security · JPA · Hibernate · MySQL`

---

# `02. Backend Toolbox`

```yaml
language:
  - Java
  - SQL

backend:
  - Spring Boot
  - Spring MVC
  - Spring Security
  - Spring Data JPA
  - Hibernate

databases:
  - PostgreSQL
  - MySQL
  - MongoDB

cache:
  - Redis

api:
  - REST
  - OpenAPI
  - Swagger
  - WebSocket

security:
  - JWT
  - Access / Refresh Tokens
  - RBAC
  - BCrypt
  - OTP
  - Google Sign-In
  - Rate Limiting

engineering:
  - Clean Architecture
  - Validation
  - Centralized Exception Handling
  - AOP Logging

devops:
  - Docker
  - Docker Compose
  - Git
  - GitHub Actions
  - Maven

learning:
  - Microservices
  - Spring Cloud
  - API Gateway
  - Service Discovery
  - Resilience
  - Messaging
  - Kubernetes
```

---

# `03. How I Think About Backend`

```text
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
   +-------> OBSERVABILITY
```

A backend isn't just:

```text
Controller -> Service -> Repository
```

The interesting questions start after that.

```text
What happens if two requests arrive together?

What happens when Redis is unavailable?

What happens when a token is stolen?

What happens when the database transaction fails halfway?

Who owns this business rule?

Should this state live in the database or cache?

Can this operation safely be retried?

How do I debug this at 2 AM?
```

Those are the problems I enjoy learning to solve.

---

# `04. Current Learning Path`

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=16&duration=1700&pause=450&color=58A6FF&center=true&vCenter=true&repeat=true&width=720&lines=Modular+Monolith+%3E+Domain+Boundaries;Domain+Boundaries+%3E+Microservices;Microservices+%3E+Spring+Cloud;Spring+Cloud+%3E+Service+Discovery;Gateway+%2B+Config+%2B+Resilience;Messaging+%2B+Docker+%2B+Kubernetes" />

</div>

```text
Spring Boot
     |
     v
Modular Monolith
     |
     v
Domain Boundaries
     |
     v
Microservices
     |
     +----------+----------+----------+
     |          |          |          |
     v          v          v          v
 Discovery   Gateway     Config   Resilience
     |          |          |          |
     +----------+----------+----------+
                    |
                    v
             Messaging / Events
                    |
                    v
                  Docker
                    |
                    v
               Kubernetes
```

Currently studying:

**Spring Cloud · Config Server · Service Discovery · API Gateway · Resilience Patterns · Messaging · Docker · Kubernetes**

---

# `05. Contribution Activity`

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=7azem512&bg_color=0d1117&color=8b949e&line=3fb950&point=ffffff&area=true&area_color=238636&hide_border=true" width="100%"/>

</div>

---

# `06. Watch My Contributions Move`

<div align="center">

<p>
  My contribution graph, but slightly more alive.
</p>

<img src="https://raw.githubusercontent.com/7azem512/7azem512/output/github-contribution-grid-snake-dark.svg" width="100%"/>

</div>

---

# `07. Current Status`

```text
[████████████████████░░░░] Java / Spring Boot

[████████████████░░░░░░░░] Backend Security

[██████████████░░░░░░░░░░] System Design

[████████████░░░░░░░░░░░░] Microservices

[████████░░░░░░░░░░░░░░░░] Kubernetes
```

```java
while (true) {
    learn();
    build();
    breakThings();
    understandWhy();
    rebuildBetter();
}
```

---

# `08. Education`

**Bachelor of Science in Computer Science**
Menoufia University
Graduated 2026

---

# `09. Open To`

```text
Java Backend Developer
Backend Software Engineer
Spring Boot Developer
```

I'm particularly interested in working on backend systems involving:

**APIs · Security · Authentication · Databases · Distributed Systems · Architecture**

---

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=2500&pause=900&color=3FB950&center=true&vCenter=true&repeat=true&width=700&lines=Build+it.;Break+it.;Understand+it.;Build+it+better." />

<br><br>

### Hazem Saed

Java Backend Developer

[LinkedIn](https://www.linkedin.com/in/hazem-saed-36092525a)
   /   
[Email](mailto:hazemsaed512@gmail.com)

<br>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:0d1117,50:161b22,100:238636&section=footer"/>

</div>
