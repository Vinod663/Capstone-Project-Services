# Capstone Project - Frontend Web Application

* **Student Name:** Vinod Niloshana Fernando
* **Student Number:** 241711104
* **Slack Handle:** @Vinod(Vinod Fernando)
* **GCP Project ID:** dark-furnace-506710-f7

---

## Project Description
This is the frontend web application for the Capstone Project, providing a responsive interface to manage students, academic programs, and enrollments. It communicates with a centralized API Gateway that routes traffic to backend microservices (Student, Program, and Enrollment services) hosted on Google Cloud Platform.

*(Note for Evaluators: The public URL for this deployed Cloud Run application is located in the "About" section on the right-hand side of this GitHub repository).*

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
git clone https://github.com/Vinod663/Webapp.git
cd Webapp
pnpm install