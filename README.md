# EVIC PAY

> **Global Financial Orchestration Platform** - Proof of Concept (PoC)
>
> Enabling cross-border payments through hybrid settlement rails using blockchain and traditional banking infrastructures.

---

## 📋 Overview

EVIC PAY is a Proof of Concept developed during a hackathon to demonstrate how traditional banking infrastructures and blockchain technologies can be orchestrated into a unified payment experience.

The platform explores the use of stablecoins as an intermediary settlement layer, enabling users to initiate cross-border payments using digital assets while automatically selecting the most suitable settlement rail.

### Initial Use Case: Portugal → Brazil
- Simulated BTC → USDC conversion
- Intelligent routing engine
- PIX settlement (Mock)
- Ledger reconciliation

---

## 🎯 Vision

Build a neutral financial orchestration layer capable of connecting:
- Banks & Payment Systems
- Stablecoins & CBDCs
- Compliance Orchestration
- Hybrid fiat and blockchain operations
- Open APIs for financial ecosystems

---

## 📁 Project Structure

```
evic-pay/
│
├── frontend/                          # Next.js React Frontend
│   ├── src/
│   │   ├── app/                       # Next.js App Router
│   │   │   ├── login/                 # Authentication pages
│   │   │   ├── dashboard/             # User dashboard
│   │   │   └── payments/              # Payment flows
│   │   │
│   │   ├── components/                # Reusable React components
│   │   │   ├── layout/                # Layout components
│   │   │   └── ui/                    # UI component library
│   │   │
│   │   ├── features/                  # Feature-specific logic
│   │   │   └── auth/                  # Authentication module
│   │   │
│   │   ├── store/                     # State management (Redux/Zustand)
│   │   │
│   │   └── services/                  # API & external service clients
│   │
│   ├── package.json
│   └── next.config.js
│
├── backend/                           # Backend API (Coming soon)
│   ├── src/
│   ├── tests/
│   └── package.json
│
├── docs/                              # Documentation
│   ├── architecture.md
│   ├── api-spec.md
│   └── setup-guide.md
│
├── infra/                             # Infrastructure & Deployment
│   ├── docker/
│   ├── kubernetes/
│   └── terraform/
│
├── README.md                          # This file
├── docker-compose.yml                 # Local development setup
└── .gitignore

```

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

The frontend will be available at `http://localhost:3000`

### Project Development Flow

**Portugal User** → **Digital Asset (BTC)** → **Simulated BTC → USDC Conversion** → **Routing Engine** → **PIX Settlement (Mock)** → **Recipient in Brazil** → **Ledger Reconciliation**

---

## 📦 Technology Stack

### Frontend
- **Framework**: Next.js 14+
- **UI Library**: React 18
- **Language**: TypeScript
- **Styling**: (TBD - Tailwind/CSS-in-JS)
- **State Management**: (TBD - Redux/Zustand/Context)

### Backend (Planned)
- **Runtime**: Node.js / Python / Go
- **API**: REST / GraphQL
- **Database**: PostgreSQL / MongoDB
- **Message Queue**: Redis / RabbitMQ

### Infrastructure
- **Containerization**: Docker
- **Orchestration**: Docker Compose / Kubernetes
- **IaC**: Terraform
- **Cloud**: (AWS / Azure / GCP - TBD)

---

## 🏗️ Architecture Layers

| Layer | Purpose | Components |
|-------|---------|-----------|
| **Presentation** | User Interface | Frontend (Next.js/React) |
| **Application** | Business Logic | Backend API, Payment Engine |
| **Integration** | External Services | Bank APIs, Blockchain RPC, Settlement Systems |
| **Data** | Persistence & Events | Databases, Event Streams, Ledger |
| **Infrastructure** | Deployment & Operations | Docker, Kubernetes, Monitoring |

---

## 🔐 Security Features (Planned)

- End-to-end encryption for payment data
- Multi-signature authorization for transactions
- Audit logging & compliance tracking
- KYC/AML integration points
- Rate limiting & DDoS protection

---

## 📊 Development Status

| Component | Status | Notes |
|-----------|--------|-------|
| Frontend UI | 🔨 In Progress | Next.js scaffold complete |
| Backend API | 📋 Planned | API specification pending |
| Payment Engine | 📋 Planned | Routing logic design phase |
| Settlement Integration | 📋 Planned | PIX integration mock ready |
| Documentation | 🔨 In Progress | Architecture docs pending |

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit changes: `git commit -m "feat: description"`
4. Push to branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📝 License

(To be defined)

---

## 📧 Contact & Support

For questions or support, please refer to the project documentation in `/docs`.

---

**Last Updated**: June 13, 2026
