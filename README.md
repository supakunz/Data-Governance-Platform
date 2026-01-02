# Data Governance Platform (Demo Project)

> ⚠️ **Disclaimer**  
> This project is a **demonstration and anonymized version** inspired by real-world  
> production systems I previously built as a Full-stack Engineer.  
>  
> All names, workflows, architectures, and data models have been **generalized**  
> and **do not represent any proprietary system, real company, or real data**.

---

## 📌 Overview

A full-stack admin dashboard demonstrating **secure CRUD workflows**,  
**approval-based data management**, and **audit-friendly backend design**.

This project focuses on **system design, data governance, and full-stack engineering**  
rather than a specific business domain.

---

## 👨‍💻 My Role (Full-stack Engineer)

- Designed overall **system architecture and data flow**
- Built frontend UI using **React + TypeScript + TailwindCSS**
- Developed **RESTful APIs** with Node.js & Express
- Designed **PostgreSQL schemas** with request–approval workflows
- Implemented **JWT authentication & role-based authorization**
- Added **audit logging** for traceability
- Containerized the system using **Docker & Docker Compose**

---

## 🔥 Key Features

- 🔐 JWT authentication with role-based access control
- ✏️ Full CRUD operations with approval workflow
- 🕒 Request-based updates (pending / approved / rejected)
- 🧾 Audit logging for all critical actions
- 🔍 Advanced search, filtering, and pagination
- 📊 Interactive dashboards and charts
- 🎨 Responsive UI with TailwindCSS
- 🐳 Dockerized for local and production-like environments

---

## 🍀 Tech Stack

### Frontend
- React + TypeScript
- Vite
- TailwindCSS
- Axios

### Backend
- Node.js
- Express.js
- JWT (Authentication)
- Bcrypt (Password hashing)
- Helmet (Security headers)
- CORS

### Database
- PostgreSQL

### DevOps
- Docker & Docker Compose
- ESLint

---

## 🏗️ System Architecture

### High-Level Architecture

- Client → Server communication via **RESTful APIs**
- Server → Database interaction using **SQL-based CRUD**
- Clear separation between **presentation, business logic, and data layers**

> Architecture diagrams included in this repository are **simplified and anonymized**.

---

### Application Architecture

- Features are grouped by **functional responsibility**
- User-submitted changes are stored as **requests**
- Core domain data is updated **only after approval**
- Supports controlled data propagation and governance

---

### Backend Service Design

- **Request Layer**  
  Stores user-initiated changes in a dedicated request table

- **Review & Approval Layer**  
  Admins validate and approve or reject requests

- **Domain Update Layer**  
  Approved requests update core entities

- **Audit Layer**  
  All actions are recorded for traceability and debugging

This design ensures:
- Data consistency
- Controlled writes
- Clear history of changes

---

## 🗄️ Data & Workflow Design (Conceptual)

- One-to-many relationships between core entities
- Extensible attribute tables for flexible metadata
- Request–approval workflow before mutating core data
- Audit logs linked to both users and requests

> Entity names and schemas have been generalized for demonstration purposes.

---

## ❄️ Installation (Local / Demo)

### Prerequisites
- Node.js (v18+)
- PostgreSQL
- Docker & Docker Compose

#### Server Environment

Create a `.env` file in the `server` directory:

**On Local:**
```env
# Server
HOST=localhost:5173
PORT=5000

# Local PostgreSQL Database
DB_HOST=database
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=postgres
DB_NAME=request_model_test

# JWT Configs
JWT_SECRET=jipjipmoneydata_secret

# Environment for changing database
NODE_ENV=development
```

**3. Build and run with Docker Compose:**

```bash
# Development mode
docker-compose -f docker-compose.dev.yml up --build

# Production mode
docker-compose -f docker-compose.prd.yml up --build
```

**The application will be available at:**
- **Client:** `http://localhost:5173`
- **Server:** `http://localhost:5001`

---

## 📁 Project Structure

```
JJM_Admin/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── api/           # API integration
│   │   ├── components/    # Reusable components
│   │   ├── context/       # React context providers
│   │   ├── hooks/         # Custom React hooks
│   │   ├── icons/         # Icon assets
│   │   ├── layout/        # Layout components
│   │   ├── pages/         # Page components
│   │   └── lib/           # Utility libraries
│   └── package.json
│
├── server/                # Backend Node.js application
│   ├── src/
│   │   ├── configs/       # Configuration files
│   │   ├── controllers/   # Route controllers
│   │   ├── middleware/    # Custom middleware
│   │   ├── routes/        # API routes
│   │   ├── services/      # Business logic
│   │   └── utils/         # Utility functions
│   └── package.json
│
├── docker-compose.dev.yml
├── docker-compose.prd.yml
└── README.md
```

---

## 🔒 Security Features

- JWT-based authentication with secure token storage
- Password hashing with bcrypt
- Helmet middleware for HTTP security headers
- CORS configuration for API protection
- Environment variable management for sensitive data

---

## 🙋‍♂️ Contact

Developed by **Supakun Thata**
📧 Email: supakun@gmail.com
