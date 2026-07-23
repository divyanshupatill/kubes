# vProfile - Java Web Application

A multi-tier Java web application built with Spring MVC, deployed on Kubernetes with a complete CI/CD pipeline.

## Prerequisites

- JDK 17
- Maven 3
- MySQL 8
- Docker & Docker Compose
- Kubernetes Cluster (EKS/Kops)
- kubectl CLI

## Technologies

- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat 10
- MySQL 8
- Memcached
- RabbitMQ
- Elasticsearch

## CI/CD Pipeline

This project uses **GitHub Actions** for CI/CD:

1. **Build** — Compile Java app with Maven
2. **Test** — Run unit tests
3. **Checkstyle** — Code quality analysis
4. **Docker** — Build & push Docker image
5. **Deploy** — Deploy to Kubernetes cluster

## Database Setup

We use MySQL as the database backend.

SQL dump file location:
- `src/main/resources/db_backup.sql`

To import the dump into MySQL:
```bash
mysql -u <user_name> -p accounts < db_backup.sql
```

## Running Locally with Docker Compose

```bash
docker-compose up -d
```

## Kubernetes Deployment

```bash
kubectl apply -f kubedefs/
```
