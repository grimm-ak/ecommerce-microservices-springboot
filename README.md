# 🛒 E‑Commerce Microservices Platform

A **scalable, event‑driven microservices architecture** for an e‑commerce platform built using **Spring Boot** and **Spring Cloud**. This project demonstrates real‑world backend engineering practices such as service isolation, asynchronous communication, containerization, and API‑first design.

---

## 🚀 Features

* **Product Service**: Product catalog management using MongoDB
* **Inventory Service**: Real‑time inventory tracking backed by MySQL
* **Order Service**: Order processing with event‑driven architecture
* **Notification Service**: Email notifications for order lifecycle events
* **API Gateway**: Single entry point with centralized routing
* **Event‑Driven Architecture**: Apache Kafka for asynchronous communication
* **Containerized Setup**: Docker & Docker Compose for easy local deployment
* **API Documentation**: Integrated Swagger / OpenAPI for all services

---

## 🛠️ Tech Stack

* **Java**: 17+
* **Spring Boot**: 3.x
* **Spring Cloud**: 2023.x
* **Spring Data**: MongoDB & JPA
* **Messaging**: Apache Kafka
* **Databases**: MySQL, MongoDB
* **Containerization**: Docker & Docker Compose
* **API Spec**: OpenAPI 3.0
* **Build Tool**: Maven

---

## 📦 Prerequisites

* Java 17 or later
* Docker Desktop (with Docker Compose)
* Maven 3.9+
* Git

---

## 🚀 Quick Start

### 1️⃣ Clone the repository

```bash
git clone https://github.com/grimm-ak/ecommerce-microservices-springboot.git
cd ecommerce-microservices-springboot
```

### 2️⃣ Build the project

```bash
mvn clean install
```

### 3️⃣ Start all services

```bash
docker-compose up -d
```

This will start all services along with required infrastructure such as **Kafka**, **MySQL**, and **MongoDB**.

### 4️⃣ Verify running containers

```bash
docker-compose ps
```

---

## 🌐 Access Services

| Service              | URL                                            | Port |
| -------------------- | ---------------------------------------------- | ---- |
| API Gateway          | [http://localhost:8080](http://localhost:8080) | 8080 |
| Product Service      | [http://localhost:8081](http://localhost:8081) | 8081 |
| Inventory Service    | [http://localhost:8082](http://localhost:8082) | 8082 |
| Order Service        | [http://localhost:8083](http://localhost:8083) | 8083 |
| Notification Service | [http://localhost:8084](http://localhost:8084) | 8084 |

---

## 📚 API Documentation

Swagger UI is available for easy API exploration:

* **API Gateway (All Services)**: [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)
* **Product Service**: [http://localhost:8081/swagger-ui.html](http://localhost:8081/swagger-ui.html)
* **Inventory Service**: [http://localhost:8082/swagger-ui.html](http://localhost:8082/swagger-ui.html)
* **Order Service**: [http://localhost:8083/swagger-ui.html](http://localhost:8083/swagger-ui.html)

---

## 🧪 Running Tests

Run tests for all services:

```bash
mvn test
```

Run tests for a specific service:

```bash
cd <service-directory>
mvn test
```

---

## 🧩 Project Structure

```
.
├── api-gateway/           # API Gateway service
├── product-service/       # Product management service
├── inventory-service/     # Inventory management service
├── order-service/         # Order processing service
├── notification-service/  # Notification service
├── docker-compose.yml     # Docker Compose configuration
└── README.md              # Project documentation
```

---

## 🔄 Service Communication

* **Synchronous**: REST APIs over HTTP
* **Asynchronous**: Apache Kafka for event‑driven messaging

---

## 🔒 Configuration & Environment Variables

* Each service contains its own `application.yml`
* Environment‑specific overrides can be provided via `docker-compose.yml`
* Sensitive configuration is excluded via `.gitignore`

---

## 🐛 Debugging

To debug a specific service locally:

1. Stop the container:

```bash
docker-compose stop <service-name>
```

2. Run service in debug mode:

```bash
cd <service-directory>
mvn spring-boot:run \
  -Dspring-boot.run.jvmArguments="-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:5005"
```

3. Attach your IDE debugger to port **5005**

---

## 🧹 Clean Up

Stop and remove all containers, networks, and volumes:

```bash
docker-compose down -v
```

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Aman Kumar Singh**
GitHub: [https://github.com/grimm-ak](https://github.com/grimm-ak)

---

## 📌 Note for Recruiters

This repository focuses on **backend system design, microservices architecture, and Java/Spring expertise**.
Frontend/UI is intentionally omitted to emphasize backend scalability and engineering principles.
