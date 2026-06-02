
# 👤 User CRUD API

A RESTful API for managing users built with **Node.js**, **Express**, and **MongoDB (Mongoose)**.

> **Internship Project** — Week 1, Project 1 | Syntecxhub Back-End Development Internship 

---

## 🚀 Features

- Full **CRUD** operations for a User resource
- Input **validation** with meaningful error messages
- Proper **HTTP status codes** for every response
- **Duplicate email** detection
- Clean MVC folder structure (Models, Controllers, Routes)
- Global **error handling** middleware

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Runtime | Node.js |
| Framework | Express.js |
| Database | MongoDB Atlas |
| ODM | Mongoose |
| Environment | dotenv |
| Dev Tool | Nodemon |

---

## 📁 Folder Structure

```
Syntecxhub_User_CRUD_API/
├── config/
│   └── db.js            # MongoDB connection
├── controllers/
│   └── userController.js # CRUD logic
├── middleware/
│   └── errorHandler.js  # Global error handler
├── models/
│   └── User.js          # Mongoose schema
├── routes/
│   └── userRoutes.js    # API routes
├── .env                 # Environment variables
├── .gitignore
├── package.json
└── server.js            # Entry point
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/Shubhanjali801/backend_syntaxhub/Syntecxhub_User_CRUD_API.git
cd Syntecxhub_User_CRUD_API
```

### 2. Install dependencies
```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the root directory:
```env
PORT=5000
MONGO_URI=your_mongodb_atlas_connection_string
```

### 4. Run the server
```bash
# Development (with auto-reload)
npm run dev

# Production
npm start
```

Server will start at `http://localhost:5000`

---

## 📡 API Endpoints

Base URL: `http://localhost:5000/api/users`

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/users` | Create a new user |
| GET | `/api/users` | Get all users |
| GET | `/api/users/:id` | Get a single user by ID |
| PUT | `/api/users/:id` | Update a user by ID |
| DELETE | `/api/users/:id` | Delete a user by ID |

---

## 📋 Request & Response Examples

### ➕ Create User — `POST /api/users`

**Request Body:**
```json
{
  "name": "Shubhanjali",
  "email": "shubh@example.com",
  "age": 21,
  "phone": "9876543210"
}
```

**Response `201 Created`:**
```json
{
  "success": true,
  "data": {
    "_id": "664abc123...",
    "name": "Shubhanjali",
    "email": "shubh@example.com",
    "age": 21,
    "phone": "9876543210",
    "createdAt": "2026-06-03T10:00:00.000Z",
    "updatedAt": "2026-06-03T10:00:00.000Z"
  }
}
```

---

### 📋 Get All Users — `GET /api/users`

**Response `200 OK`:**
```json
{
  "success": true,
  "count": 2,
  "data": [ ... ]
}
```

---

### 🔍 Get User by ID — `GET /api/users/:id`

**Response `200 OK`:**
```json
{
  "success": true,
  "data": { ... }
}
```

**Response `404 Not Found`:**
```json
{
  "success": false,
  "message": "User not found"
}
```

---

### ✏️ Update User — `PUT /api/users/:id`

**Request Body (partial update supported):**
```json
{
  "age": 22
}
```

**Response `200 OK`:**
```json
{
  "success": true,
  "data": { ... }
}
```

---

### 🗑️ Delete User — `DELETE /api/users/:id`

**Response `200 OK`:**
```json
{
  "success": true,
  "message": "User deleted successfully"
}
```

---

## ✅ HTTP Status Codes Used

| Code | Meaning |
|------|---------|
| 200 | OK |
| 201 | Created |
| 400 | Bad Request / Validation Error |
| 404 | Not Found |
| 500 | Internal Server Error |

---

## 🧪 Testing

Test all endpoints using [Postman](https://www.postman.com/) or any API client.

Import the base URL: `http://localhost:5000/api/users`

---

## 👩‍💻 Author

**Shubhanjali**
B.Tech Information Technology — IIIT Allahabad
Syntecxhub Back-End Development Intern

---

## 📄 License

This project is built for internship/learning purposes.