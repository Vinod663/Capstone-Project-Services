# Capstone Project - Services

* **Student Name:** Vinod Niloshana Fernando
* **Student Number:** 241711104
* **Slack Handle:** @Vinod(Vinod Fernando)
* **GCP Project ID:** dark-furnace-506710-f7

---

## Project Description
This repository contains the backend domain microservices for the Capstone Project, encompassing the `student-service`, `program-service`, and `enrollment-service`. These services handle core business logic, database transactions (PostgreSQL and MongoDB), and file storage integrations (Google Cloud Storage). They are designed to register with the Eureka Service Registry and fetch configurations from the centralized Config Server.

## Technology Stack
* **Framework:** Next.js (v16.1.6)
* **UI Library:** React (v19.2.3)
* **Styling:** Tailwind CSS (v4) & shadcn/ui components
* **Form Handling:** React Hook Form integrated with Zod validation
* **Language:** TypeScript
* **Package Manager:** pnpm
* **Deployment:** Google Cloud Run

## Setup / Getting Started Instructions

**1. Prerequisites**
* Node.js installed locally.
* `pnpm` installed globally (`npm install -g pnpm`).

**2. Installation**
Clone the repository and install the required dependencies:
```bash
git clone https://github.com/Vinod663/Capstone-Project-Services.git
cd Capstone-Project-Services
pnpm install