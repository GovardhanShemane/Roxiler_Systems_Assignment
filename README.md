# RateMyStore - Full Stack Web Application

**Welcome to RateMyStore!** This is a full stack web application built using ReactJS (frontend), Express.js (backend), and PostgreSQL (database). It enables users to discover, rate, and review stores with role-based access for different types of users.

## 🔍 Overview

RateMyStore provides a unified platform where:

* **Normal Users** can register, browse stores, and submit/edit ratings.
* **Store Owners** can view who rated their stores and track the average rating.
* **System Administrators** can manage users, stores, and platform statistics.

## 🚀 Features

### ✅ General

* Role-based login & dashboards
* Secure JWT authentication
* Password management with bcryptjs
* Responsive UI (TailwindCSS)
* Filtering & sorting in tables

### 🛠️ System Administrator

* Add/manage users (Admin/Normal/Store Owner)
* Add/manage stores
* Dashboard with stats: total users, stores, ratings
* View/search users and stores with filters

### 👤 Normal User

* Register/Login
* Browse, search, and rate stores (1-5 stars)
* Update previously submitted rating
* Change password

### 🏬 Store Owner

* Login
* View users who rated their store
* See average store rating
* Update password

## ⚙️ Tech Stack

### Frontend

* ReactJS
* Redux Toolkit
* React Router DOM
* TailwindCSS
* Axios

### Backend

* Node.js + Express.js
* PostgreSQL
* Sequelize ORM
* JWT for Authentication
* bcryptjs
* dotenv + CORS

## 🔧 Prerequisites

* Node.js (v18+)
* npm (v9+)
* PostgreSQL
* Backend server running at `http://localhost:5000/api`

## 📦 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/rate-my-store.git
cd rate-my-store
```

### 2. Install Dependencies

```bash
cd backend
npm install
cd ../frontend
npm install
```

### 3. Environment Variables

Create a `.env` file in `frontend/` with:

```
REACT_APP_API_URL=http://localhost:5000/api
```

### 4. Run Application

```bash
# Start backend
cd backend
npm run start

# Start frontend
cd ../frontend
npm run start
```

## 🧪 Available Scripts

```bash
npm start        # Dev server
npm run build    # Build for production
```

## 📋 Functionality Summary

### Registration/Login

* Fields: Name, Email, Address, Password
* Role-based redirection after login

### Admin Dashboard

* Add/view users and stores
* Apply filters (Name, Email, Role)
* View ratings and stats

### Normal User Dashboard

* List/search stores
* Rate or update ratings

### Store Owner Dashboard

* View users who rated their store
* View average rating

### Profile/Logout

* Update password securely
* Logout clears localStorage token

## 📌 API Endpoints Used

```
- POST /auth/login
- POST /auth/register
- PUT /users/update-password
- GET /users/stores
- POST /users/ratings
- PUT /users/ratings/:id
- GET /admin/dashboard
- POST /admin/users
- POST /admin/stores
- GET /admin/users
- GET /admin/stores
- GET /admin/users/:id
- GET /owner/dashboard
```

## ✅ Form Validations

* **Name:** 20-60 chars
* **Address:** Max 400 chars
* **Password:** 8-16 chars, 1 uppercase, 1 special char
* **Email:** Valid email format

## 🤝 Contributions

Open to suggestions, improvements, and pull requests! Please maintain code clarity and comment where needed.

## 📄 License

MIT License
