# Capstone Project - Services

* **Student Name:** Vinod Niloshana Fernando
* **Student Number:** 241711104
* **Slack Handle:** @Vinod(Vinod Fernando)
* **GCP Project ID:** dark-furnace-506710-f7

---

## Project Description
This repository contains the backend domain microservices for the Capstone Project, encompassing the `student-service`, `program-service`, and `enrollment-service`. These services handle core business logic, database transactions (PostgreSQL and MongoDB), and file storage integrations (Google Cloud Storage). They are designed to register with the Eureka Service Registry and fetch configurations from the centralized Config Server.

## Technology Stack
* **Language:** Java 26
* **Framework:** Spring Boot (v4.1.0)
* **Cloud Infrastructure:** Spring Cloud (v2025.1.2)
    * Spring Cloud Netflix Eureka Client
    * Spring Cloud Config Client
* **Databases:** PostgreSQL & MongoDB
* **File Storage:** Google Cloud Storage
* **Build Tool:** Maven
* **Deployment:** Google Cloud Platform (Compute Engine) via PM2

## Setup / Getting Started Instructions

### 1. Prerequisites
* Java 26 (JDK) installed locally.
* Maven installed locally.
* Access credentials/permissions for the GCP project (`dark-furnace-506710-f7`).

### 2. Installation
Clone the repository and install the required dependencies:

```bash
git clone https://github.com/Vinod663/Capstone-Project-Services.git
cd Capstone-Project-Services
mvn clean package -DskipTests
```

### 3. Database Connection (Cloud SQL Proxy)
Before starting the services, establish a secure tunnel to the GCP databases using the Cloud SQL Auth Proxy:

```bash
./cloud-sql-proxy dark-furnace-506710-f7:asia-southeast1:postgres-vm dark-furnace-506710-f7:asia-southeast1:mysql-vm --private-ip &
```

### 4. Building the Services
Use the parent POM to build all microservices simultaneously:

```bash
mvn clean package -DskipTests
```

*(To build a single service, navigate into its folder — e.g., `cd student-service` — and run the same command).*

### 5. Running the Application
In a production or VM environment, the services are managed via PM2 to ensure zero-downtime reloads and automatic restarts. Start or reload the ecosystem:

```bash
pm2 reload ecosystem.config.js
```

To monitor the startup logs and verify successful database and GCP bucket connections:

```bash
pm2 logs
```