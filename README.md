

# Logistics Management System with Route Optimization

A backend-focused logistics management system built using **Node.js, Express, MongoDB**, and a lightweight **React** frontend.
The project focuses on **order lifecycle management**, **route optimization using graph algorithms**, and **clean REST API design**.

This project was designed to demonstrate **software engineering fundamentals**, **algorithmic problem-solving**, and **system design clarity**.

---

## 🚀 Key Features

### Backend (Core Focus)

* **Order Management System**

  * Create, update, track, and manage delivery orders
  * Well-defined order lifecycle (`CREATED → ASSIGNED → IN_TRANSIT → DELIVERED`)
* **Route Optimization**

  * Shortest-path based delivery routing using **Dijkstra’s Algorithm**
  * Distance-based cost and routing decisions
* **Pricing Engine**

  * Rule-based pricing using distance, package weight, and delivery type
* **Delivery Agent Assignment**

  * Greedy assignment of available agents based on proximity
* **Authentication & Authorization**

  * JWT-based authentication
  * Role-based access (Customer / Admin / Delivery Agent)
* **RESTful APIs**

  * Modular, well-structured API endpoints
  * Centralized error handling and validation
* **Database Seeding**

  * Preloaded sample data for cities, delivery hubs, agents, and orders

### Frontend (Minimal & Functional)

* Customer order placement and tracking
* Admin order overview
* Delivery agent status updates

---

## 🧠 Algorithms & Data Structures Used

### Route Optimization

* **Dijkstra’s Algorithm**

  * Used to compute the shortest delivery path between hubs
  * Time Complexity: **O(E log V)**
* **Graph Representation**

  * Cities and hubs modeled as nodes
  * Distances modeled as weighted edges

### Other Concepts

* **HashMaps** for constant-time lookup of orders and agents
* **Greedy Strategy** for delivery agent assignment
* **Enums** for order status consistency

---

## 🏗️ System Architecture

```
Logistics Management System
├── Backend (Node.js + Express)
│   ├── Authentication & Authorization
│   ├── Order Management
│   ├── Route Optimization Module
│   ├── Pricing Engine
│   ├── Delivery Agent Assignment
│   └── REST APIs
├── Frontend (React)
│   ├── Customer Dashboard
│   ├── Admin Panel
│   └── Delivery Agent View
└── Database (MongoDB)
    ├── Users
    ├── Orders
    ├── Delivery Hubs
    └── Agents
```

---

## 🛠️ Tech Stack

* **Backend**: Node.js, Express.js
* **Database**: MongoDB (Mongoose ODM)
* **Frontend**: React (basic UI)
* **Authentication**: JWT
* **Language**: JavaScript
* **Tools**: Git, Postman

---

## 📋 Prerequisites

* Node.js (v16 or higher)
* MongoDB (local or Atlas)
* npm
* Git

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/logistics-management-system.git
cd logistics-management-system
```

### 2. Backend Setup

```bash
cd backend
npm install
```

### 3. Environment Variables

Create a `.env` file inside `backend/`:

```env
PORT=3000
MONGO_URI=mongodb://localhost:27017/logistics_db
JWT_SECRET=your_secret_key
```

### 4. Seed Sample Data

```bash
node seedDatabase.js
```

### 5. Start the Server

```bash
npm start
```

### 6. Frontend (Optional)

```bash
cd frontend
npm install
npm start
```

---

## 📚 API Overview

### Health Check

```
GET /health
```

### Authentication

* `POST /api/auth/register`
* `POST /api/auth/login`
* `GET /api/auth/profile`

### Orders

* `POST /api/orders/create`
* `GET /api/orders`
* `GET /api/orders/:id`
* `PUT /api/orders/:id/status`

### Route & Pricing

* `POST /api/routes/optimize`
* `POST /api/pricing/calculate`

### Delivery Agents

* `GET /api/agents`
* `POST /api/agents/assign`

---

## 🧪 Testing

* Manual API testing using **Postman**
* Edge cases tested:

  * Invalid routes
  * No available delivery agents
  * Incorrect order transitions

---

## 📊 Sample Data

* 10+ cities
* Multiple delivery hubs
* Sample delivery agents
* Orders across different statuses

(All data is synthetic and used for demonstration.)

---

## 🧩 Design Decisions

* **MongoDB** chosen for flexible schema and fast iteration
* **Dijkstra’s algorithm** used for clarity and deterministic routing
* **REST APIs** for clean separation of concerns
* Focused scope to ensure **full ownership and explainability**

---

## 🔮 Future Improvements

* Add caching for frequently used routes
* Improve agent assignment using priority queues
* Introduce basic load balancing strategies
* Add automated unit tests

---

## 📄 License

MIT License

---

## ✅ Why This Project

This project was built to:

* Practice **backend system design**
* Apply **DSA concepts in real-world scenarios**
* Build an **interview-defensible** project suitable for **SDE roles**

---

