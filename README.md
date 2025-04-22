# 💼 JobApplication - Spring Boot REST API

## 📘 Executive Summary
The **Spring Boot REST API Application** is a lightweight and scalable backend project developed to support core CRUD operations using RESTful services. Built on top of the Spring Boot framework, this application demonstrates clean architecture, layered code structure, and integrates PostgreSQL for persistent storage. It is ideal for microservice adoption or as a foundational template for enterprise-grade REST APIs.

---

## 🎯 Project Objective
To design and deploy a secure, scalable, and modular Job Portal backend system that supports end-to-end job posting and discovery operations. The system is built using a monolithic Spring Boot architecture, offering a suite of RESTful APIs for managing job entities, performing keyword-based searches, and handling data initialization. It is intended for cloud-native deployment and supports secure access, efficient data processing, and cross-platform integration.

---

## 🧩 Core Capabilities
- **Complete Job Posting Lifecycle** – Full CRUD support for job listings.
- **Advanced Search Functionality** – Search jobs via keyword filtering.
- **System Initialization** – Preload the database with default records.
- **CORS Support** – Enables integration with third-party frontends.
- **Security Layer** – Basic authentication and stateless session control.

---

## 📑 Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Dependencies Used](#dependencies-used)
- [System Architecture](#system-architecture)
- [Cloud Infrastructure](#cloud-infrastructure)
- [API Specification](#api-specification)
- [Folder Structure](#folder-structure)

---

## ✅ Features
- RESTful CRUD API endpoints
- PostgreSQL database integration
- Layered architecture (Controller, Service, Repository)
- Secure Spring Boot project setup
- Lombok annotations to reduce boilerplate code

---

## 💡 Technologies Used
| Component        | Technology           |
|------------------|----------------------|
| Backend Framework| Spring Boot 3.2.1    |
| Database         | PostgreSQL           |
| ORM              | Spring Data JPA      |
| Security         | Spring Security      |
| Build Tool       | Maven                |
| Language         | Java 21              |
| Utilities        | Project Lombok       |
| API Type         | RESTful JSON APIs    |
| Testing Tool     | Postman              |

---

## 📦 Dependencies Used
Referenced from `pom.xml`, the following dependencies are included:

| Group ID                   | Artifact ID                   | Scope     |
|----------------------------|-------------------------------|-----------|
| org.springframework.boot   | spring-boot-starter-web       | compile   |
| org.springframework.boot   | spring-boot-starter-data-jpa  | compile   |
| org.springframework.boot   | spring-boot-starter-security  | compile   |
| org.springframework.boot   | spring-boot-starter-test      | test      |
| org.postgresql             | postgresql                    | runtime   |
| org.projectlombok          | lombok                        | optional  |

---

## 🧱 System Architecture
The application follows a clean monolithic layered architecture:

1. **Controller Layer** – Handles incoming HTTP requests and API routing.
2. **Service Layer** – Encapsulates business logic.
3. **Repository Layer** – Handles database interaction using Spring Data JPA.
4. **Model Layer** – Contains the domain entities.
5. **Configuration Layer** – Manages security and application-level configs.

---

## ☁️ Cloud Infrastructure
| AWS Service               | Description                                               |
|---------------------------|-----------------------------------------------------------|
| Elastic Beanstalk         | Application deployment with auto-scaling capabilities     |
| Amazon RDS (PostgreSQL)   | Managed relational database service with high availability|
| Amazon ECR                | Container image repository for versioned deployments     |
| Amazon ECS                | Container orchestration for scalable service management   |

---

## 📊 API Specification
| Endpoint                            | Method | Description                    | Response Type         |
|-------------------------------------|--------|--------------------------------|------------------------|
| `/jobPosts`                         | GET    | Retrieve all job listings      | JSON array of jobs     |
| `/jobPost/{postId}`                 | GET    | Get job post by ID             | Single job JSON        |
| `/jobPosts/keyword/{keyword}`      | GET    | Search jobs by keyword         | Filtered job list      |
| `/jobPost`                          | POST   | Create new job listing         | Created job JSON       |
| `/jobPost`                          | PUT    | Update existing job listing    | Updated job JSON       |
| `/jobPost/{postId}`                | DELETE | Delete job listing by ID       | Success message        |
| `/load`                             | GET    | Initialize system with sample data | Confirmation message |

---

## 📂 Folder Structure
```plaintext
com.telusko.springbootrest
├── config         # Security/configuration classes
├── controller     # REST API controllers
├── model          # Entity classes
├── repo           # Spring Data repositories
├── service        # Business logic
└── SpringBootRestApplication.java  # Main app entry point
```
---
