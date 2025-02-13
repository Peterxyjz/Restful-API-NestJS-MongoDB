# Restful-API-NestJS-MongoDB

## 📌 Overview

This project is a backend application built with NestJS and MongoDB, following best practices for modular development, authentication, authorization, and API structure.

## 🛠 Tech Stack

- **Backend:** NestJS
- **Database:** MongoDB (Mongoose ODM)
- **Authentication:** JWT, Passport.js
- **State Management:** Stateful & Stateless
- **API Documentation:** Swagger
- **Security:** Helmet, Rate Limiting
- **Deployment:** Docker

## 📂 Project Structure

```
├── src
│   ├── modules
│   │   ├── auth
│   │   ├── users
│   │   ├── company
│   │   ├── jobs
│   │   ├── resumes
│   │   ├── permissions
│   │   ├── roles
│   │   ├── subscribers
│   │   ├── mailer
│   │   ├── common
│   │   └── ...
│   ├── main.ts
│   ├── app.module.ts
│   ├── config
│   ├── filters
│   ├── guards
│   ├── pipes
│   ├── interceptors
│   └── utils
├── test
├── .env
├── Dockerfile
├── README.md
└── package.json
```

## 🚀 Features

### ✅ Database & Models

- Connect and configure MongoDB with NestJS
- Define and manage schemas using Mongoose
- Soft-delete functionality
- Query builder for optimized database queries

### ✅ Authentication & Authorization

- JWT-based authentication
- Role-based access control (RBAC)
- Passport.js integration for authentication strategies
- Global Guards for security

### ✅ RESTful API Development

- CRUD operations for Users, Companies, Jobs, and Resumes
- DTO (Data Transfer Object) for request validation
- Pipes and Interceptors for request/response transformation
- Versioned APIs for backward compatibility

### ✅ Security & Performance

- CORS configuration
- Rate limiting to prevent abuse
- Helmet for enhanced security
- API Health checks

### ✅ Additional Modules

- Email service with Node.js and NestJS Mailer
- Cron Jobs for automated email notifications
- Logging and debugging tools

## 📌 Setup Instructions

### 1️⃣ Prerequisites

- Node.js & npm/yarn
- MongoDB instance (local or cloud)
- Docker (optional)

### 2️⃣ Installation

```sh
# Clone the repository
git clone https://github.com/your-repo/nestjs-mongodb-backend.git
cd nestjs-mongodb-backend

# Install dependencies
npm install
```

### 3️⃣ Environment Configuration

Create a `.env` file in the root directory and set the necessary environment variables:

```env
PORT=3000
MONGO_URI=mongodb://localhost:27017/mydatabase
JWT_SECRET=your_secret_key
```

### 4️⃣ Run the Application

```sh
# Development mode
npm run start:dev

# Production mode
npm run build && npm run start
```

### 5️⃣ Run with Docker

```sh
# Build Docker image
docker build -t nestjs-backend .

# Run container
docker run -p 3000:3000 --env-file .env nestjs-backend
```

## 📖 API Documentation

API documentation is available via Swagger after running the application:

```
http://localhost:3000/api
```

## 🛠 Testing

```sh
# Run unit tests
npm run test

# Run end-to-end tests
npm run test:e2e
```

## 📌 Contributing

Contributions are welcome! Please submit a PR or open an issue if you find bugs or want to enhance features.

## 📜 License

This project is licensed under the MIT License.
