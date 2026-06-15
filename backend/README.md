# EVIC PAY Backend

> NestJS API for the EVIC PAY Proof of Concept (PoC)

---

## Overview

The EVIC PAY Backend provides the API layer for the Proof of Concept developed during the hackathon.

Its purpose is to orchestrate the business logic required to demonstrate hybrid cross-border payments, including payment initiation, intelligent routing, settlement simulation and ledger reconciliation.

This backend is not intended for production use and operates exclusively within the scope of the EVIC PAY PoC.

---

## Sprint 2 Objectives

The objectives of Sprint 2 are to establish the backend foundation and the local development environment.

### Deliverables

* NestJS backend initialised;
* Docker support configured;
* PostgreSQL integration prepared;
* Docker Compose integration completed;
* Frontend and backend connected through the development environment.

---

## Technology Stack

### Framework

* NestJS
* TypeScript
* Node.js 22

### Database

* PostgreSQL 17

### Infrastructure

* Docker
* Docker Compose

---

## Project Structure

```text
backend/
├── src/
├── test/
├── Dockerfile
├── nest-cli.json
├── package.json
├── tsconfig.json
└── README.md
```

---

## Local Development

### Prerequisites

* Node.js 22+
* Docker Desktop
* Docker Compose
* Git

---

## Running the Backend with Docker

From the repository root:

```bash
docker compose up --build
```

Expected services:

```text
evicpay-frontend
evicpay-backend
evicpay-postgres
```

---

## Running the Backend Locally

Navigate to the backend folder:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run start:dev
```

The API will be available at:

```text
http://localhost:3001
```

---

## PostgreSQL Configuration

Development credentials:

```text
Host: postgres
Port: 5432

Database: evicpay
Username: evicpay
Password: evicpay
```

These credentials are intended exclusively for local development.

---

## Environment Variables

The backend expects the following variables:

```env
NODE_ENV=development

DATABASE_HOST=postgres
DATABASE_PORT=5432

DATABASE_NAME=evicpay
DATABASE_USER=evicpay
DATABASE_PASSWORD=evicpay
```

---

## Planned Modules

The following modules will be implemented in subsequent sprints.

### Ledger Module

Responsible for:

* Account balances;
* Debit and credit entries;
* Reconciliation.

---

### Payments Module

Responsible for:

* Payment initiation;
* Payment retrieval;
* Transaction status.

---

### Routing Engine

Responsible for selecting the most appropriate settlement rail.

Initial rules include:

* Brazil → PIX;
* Portugal → SEPA;
* Transactions above €5,000 flagged for AML review.

---

### Settlement Module

Responsible for simulating settlement operations through:

* PIX Mock;
* SEPA Mock;
* Stablecoin adapters.

---

## Planned API Endpoints

### Payments

```http
POST /payments
GET /payments
GET /payments/:id
```

### Balances

```http
GET /balances
```

---

## Sprint 2 Validation Checklist

* [ ] Backend initialised;
* [ ] Dockerfile created;
* [ ] PostgreSQL container running;
* [ ] Docker Compose operational;
* [ ] Backend reachable on port 3001;
* [ ] Frontend connected to the development environment.

---

## Recommended Git Commits

```bash
git commit -m "chore: initialize NestJS backend"

git commit -m "chore: add PostgreSQL and backend services to Docker Compose"

git commit -m "chore: establish local development environment"
```

---

## Disclaimer

This backend is part of a hackathon Proof of Concept and does not process real financial transactions or customer funds.

It is intended solely for experimentation, validation and demonstration purposes.

---

## Next Steps

Sprint 3 will focus on implementing the first EVIC PAY business capabilities:

* Ledger persistence;
* Payments module;
* Routing engine;
* REST APIs;
* PostgreSQL integration through the application layer.


## Documentation

- Frontend: `frontend/README.md`
- Backend: `backend/README.md`
