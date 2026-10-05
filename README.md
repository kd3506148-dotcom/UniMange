# CampusHub — Real-Time University Management System

A production-style, real-time University Management Platform connecting **Students**, **Faculty**, and **Administrators** built on the **MERN** stack (MongoDB, Express, React, Node.js) with **Socket.IO**.

---

## 🛠️ Technology Stack

- **Frontend:** React 18, Vite, React Router DOM, Axios, Socket.IO Client, Recharts, Lucide React
- **Backend:** Node.js, Express.js, Socket.IO, JWT, bcryptjs, Mongoose, Morgan, CORS
- **Database:** MongoDB / MongoDB Atlas (with zero-config development engine)

---

## 📁 Project Architecture

```text
University Management System/
├── package.json                 # Root script runner
├── .gitignore                   # Version control exclusions
│
├── server/                      # Express + Node + Mongoose Backend
│   ├── config/                  # Database and server configs (db.js)
│   ├── controllers/             # API request handlers (healthController.js)
│   ├── middleware/              # Error handler and 404 middleware
│   ├── models/                  # Mongoose data schemas (SystemHealth.js)
│   ├── routes/                  # Express REST routes (healthRoutes.js)
│   ├── services/                # Business logic services
│   ├── utils/                   # Shared utility helpers
│   ├── validations/             # Input validation schemas
│   ├── .env                     # Server environment variables
│   ├── .env.example             # Template for environment configuration
│   ├── package.json             # Server dependencies & scripts
│   └── server.js                # Server entrypoint with Socket.IO & Express
│
└── client/                      # React 18 + Vite Frontend
    ├── public/                  # Static assets
    ├── src/
    │   ├── components/          # Reusable UI components (Header.jsx)
    │   ├── context/             # React context (SocketContext.jsx)
    │   ├── hooks/               # Custom hooks (useSocket.js)
    │   ├── layouts/             # Page layouts
    │   ├── pages/               # Application views (HealthCheckPage.jsx)
    │   ├── services/            # Axios API layer (api.js, healthService.js)
    │   ├── utils/               # Client helpers
    │   ├── App.jsx              # Root component
    │   ├── index.css            # Modern responsive stylesheet
    │   └── main.jsx             # React entrypoint
    ├── .env                     # Client environment variables
    ├── .env.example             # Template for client configuration
    ├── index.html               # Main HTML document
    ├── package.json             # Client dependencies
    └── vite.config.js           # Vite dev server and proxy configuration
```

---

## 🚀 Running the Project

### Prerequisites
- Node.js (v18+)
- npm

### 1. Start the Backend Server (Terminal 1)
```powershell
cd server
npm.cmd run dev
```
- Server URL: `http://localhost:5000`
- Health Endpoint: `http://localhost:5000/api/health`

### 2. Start the Frontend Application (Terminal 2)
```powershell
cd client
npm.cmd run dev
```
- Frontend URL: `http://localhost:5173`

---

## 🔄 Verified End-to-End Pipeline

```text
React Form
    ↓
Axios POST /api/health/ping
    ↓
Express Route & Controller
    ↓
Mongoose ODM Validation
    ↓
MongoDB Persistence
    ↓
Socket.IO Broadcast Event
    ↓
React State Update (Real MongoDB Document Rendered)
```
