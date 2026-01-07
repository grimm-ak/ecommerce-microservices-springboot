Ecommerce Microservices Backend (Spring Boot)

A production‑style microservices‑based e‑commerce backend built using Java and Spring Boot, designed to demonstrate scalable backend architecture, service isolation, and inter‑service communication.This project focuses on backend engineering principles rather than UI, and closely follows patterns used in real‑world distributed systems.

📌 Key Features

Microservices architecture with independent services

API Gateway for centralized routing

Product, Order, Inventory, and Notification services

RESTful APIs with clear separation of concerns

Containerized infrastructure using Docker Compose

Asynchronous communication (Kafka where applicable)

Database persistence using Spring Data JPA / MongoDB

🏗 Architecture Overview

Client
  │
  ▼
API Gateway
  │
  ├── Product Service
  ├── Order Service
  ├── Inventory Service
  └── Notification Service

Each service:

Is a standalone Spring Boot application

Has its own database

Can be developed, deployed, and scaled independently

🛠 Tech Stack

Language: Java 17

Framework: Spring Boot, Spring Cloud

API: REST (JSON)

Databases: MySQL, MongoDB

Messaging: Kafka

Build Tool: Maven

Containerization: Docker & Docker Compose

📂 Project Structure

api-gateway/
product-service/
order-service/
inventory-service/
notification-service/
docker-compose.yml

▶ How to Run Locally

This project is designed to run in a Docker‑based environment.

Prerequisites

Java 17+

Maven

Docker & Docker Compose

Steps

# Build all services
mvn clean install

# Start infrastructure and services
docker-compose up -d

Verify Services

API Gateway: http://localhost:8080

Product Service: http://localhost:8081

Order Service: http://localhost:8082

Inventory Service: http://localhost:8083

📡 Sample API Endpoints

Create Product

POST /api/products
Content-Type: application/json

{
  "name": "iPhone",
  "price": 999.99
}

Place Order

POST /api/orders
Content-Type: application/json

{
  "skuCode": "iphone_15",
  "quantity": 1
}

🔍 Design Highlights

Clear Controller → Service → Repository layering

Database transactions and consistency handling

Inter‑service communication via REST / messaging

Fault‑tolerant design with service isolation

Scalable and extensible architecture

🧪 Testing

Unit testing support using Spring Boot Test

APIs can be tested via Postman or curl

Swagger UI can be enabled per service (if configured)

📄 License

This project is licensed under the MIT License.

See the LICENSE file for details.

👤 Author

Aman Kumar SinghGitHub: https://github.com/grimm-ak

📌 Note for Recruiters

This project is intentionally backend‑focused to demonstrate system design, microservices architecture, and Java/Spring expertise. Frontend is omitted by design.
