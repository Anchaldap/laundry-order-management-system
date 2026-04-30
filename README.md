# laundry-order-management-system
Mini Laundry Order Management System with order tracking, billing, and dashboard (AI-first project using Node.js &amp; Express)
# 🧺 Mini Laundry Order Management System (AI-First)

## 📌 Overview

This project is a lightweight backend system designed for a dry cleaning store to manage daily orders efficiently. It allows users to create orders, track their status, calculate billing, and view basic business insights via a dashboard.

The system was built using an **AI-first approach**, leveraging tools like ChatGPT to accelerate development, debug issues, and improve code quality.

---

## 🚀 Features Implemented

### ✅ Order Management

* Create new laundry orders
* Automatically calculate total bill
* Generate unique Order IDs

### ✅ Order Status Tracking

Each order supports the following statuses:

* RECEIVED

* PROCESSING

* READY

* DELIVERED

* Update order status via API

### ✅ View & Filter Orders

* Fetch all orders
* Filter by:

  * Status
  * Customer name / phone number

### ✅ Dashboard Summary

* Total number of orders
* Total revenue generated
* Orders grouped by status

---

## 🛠️ Tech Stack

* **Backend:** Node.js, Express
* **Storage:** In-memory (Array)
* **Utilities:** UUID, CORS
* **API Testing:** Postman

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/laundry-system.git
cd laundry-system
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Run the Server

```bash
node server.js
```

Server will start on:

```
http://localhost:5000
```

---

## 📬 API Endpoints

### ➤ Create Order

**POST** `/orders`

```json
{
  "customerName": "Anchal",
  "phone": "9876543210",
  "garments": [
    { "type": "Shirt", "quantity": 2 },
    { "type": "Saree", "quantity": 1 }
  ]
}
```

---

### ➤ Get Orders

**GET** `/orders`

Filters:

```
/orders?status=RECEIVED
/orders?search=Anchal
```

---

### ➤ Update Order Status

**PATCH** `/orders/:id`

```json
{
  "status": "PROCESSING"
}
```

---

### ➤ Dashboard Summary

**GET** `/orders/dashboard/summary`

---

## 🤖 AI Usage Report (Important)

### 🔹 Tools Used

* ChatGPT (primary)
* GitHub Copilot (optional)

---

### 🔹 How AI Helped

* Generated initial Express server structure
* Created API routes and logic
* Helped design order schema and pricing logic
* Assisted in debugging API issues
* Suggested improvements for filtering and dashboard logic

---

### 🔹 Sample Prompts Used

1.

```
Create a Node.js Express API for an order management system with create, update, and list functionality.
```

2.

```
Add filtering by status and search by phone number in an Express API.
```

3.

```
Write a function to calculate total billing for garments with different prices.
```

4.

```
Fix a PATCH API that is not updating data correctly in Express.
```

---

### 🔹 What AI Got Wrong

* Initially missed validation for empty inputs
* Did not handle edge cases (invalid status updates)
* Basic filtering logic needed improvement
* No proper project structure in first response

---

### 🔹 Improvements Made Manually

* Added structured folder architecture
* Improved filtering logic (combined search + status)
* Added default status handling
* Cleaned and modularized code
* Ensured consistent API responses

---

## ⚖️ Tradeoffs

* ❌ Used in-memory storage instead of database (for speed)
* ❌ No authentication implemented
* ❌ No frontend UI included

---

## 🚀 Future Improvements

* Add MongoDB / SQL database
* Build frontend using React
* Add authentication (JWT-based)
* Add estimated delivery date feature
* Deploy on cloud (Render / Vercel)
* Add search by garment type

---

## 📸 Demo

* Postman Collection (attach link if available)
* Screenshots / Loom Video (optional but recommended)

---

## 🧠 Key Learnings

* AI can significantly speed up backend development
* Manual intervention is required for edge cases and structure
* Iterative prompting gives better results
* Clean architecture improves scalability

---

## 👤 Author

**Anchal Patel**
B.Tech IT Student
RKGIT

---

## ⭐ Final Note

This project focuses on **practical execution, AI leverage, and problem-solving ability**, rather than over-engineering.

---
