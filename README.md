# Bookflix

<p align="center">
  <strong>AI-Powered Digital Library, Book Rental & Reading Platform</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" />
  <img src="https://img.shields.io/badge/Material_UI-007FFF?style=for-the-badge&logo=mui&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker_Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" />
  <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" />
</p>

---

## 📌 Overview

Bookflix is a full-stack digital library platform that allows users to browse books, rent or purchase books, manage their personal library, read PDF books, access audio books, leave reviews, and receive AI-powered book recommendations.

The project consists of a React TypeScript frontend, a Node.js Express REST API, a PostgreSQL database, and a separate FastAPI-based recommendation service powered by collaborative filtering.

---

## ✨ Key Features

* 📚 Book browsing, search, pagination, and category filtering
* 🔐 JWT-based user authentication
* 👤 User profile and subscription management
* 🛒 Shopping cart and simulated payment flow
* 📖 Personal library management
* 🎧 Audio book access control
* 📄 PDF reading support
* ⭐ Book comments and rating system
* 🤖 AI-powered personalized book recommendations
* 🧠 Collaborative filtering recommendation service
* 🛠️ Admin dashboard for managing books, users, comments, and subscriptions
* 📄 Swagger / OpenAPI documentation for backend APIs
* 🐳 PostgreSQL database setup with Docker Compose

---

## 📸 Screenshots

### User Application

| Home Page                                                                                                                           | Book Detail                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://github.com/user-attachments/assets/b2d4765e-c1a9-4a29-8853-734455392427" alt="Bookflix Home Page" width="100%" /> | <img src="https://github.com/user-attachments/assets/180f63f5-4d6b-4249-adf1-eae729112f71" alt="Bookflix Book Detail" width="100%" /> |

| My Library                                                                                                                           | Recommendations                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://github.com/user-attachments/assets/b1749bc8-9eea-428c-82d2-a2755120a1c4" alt="Bookflix My Library" width="100%" /> | <img src="https://github.com/user-attachments/assets/c34ae207-b1ba-4465-a34c-3708ae122a20" alt="Bookflix Recommendations" width="100%" /> |

| Login                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://github.com/user-attachments/assets/5dc635ce-3817-4056-993c-7649a34f164f" alt="Bookflix Login" width="100%" /> |

---

### Admin Panel

| Admin Dashboard                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://github.com/user-attachments/assets/2da4b955-0f02-48ed-b598-0aca05bdea41" alt="Bookflix Admin Dashboard" width="100%" /> |

| Book Management                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://github.com/user-attachments/assets/54649d88-0ba4-4139-b061-0e48515aa021" alt="Bookflix Book Management" width="100%" /> |

| User Management                                                                                                                           | Subscription Management                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://github.com/user-attachments/assets/8a6b1a4a-8da6-4db1-bd20-d4556a592ba4" alt="Bookflix User Management" width="100%" /> | <img src="https://github.com/user-attachments/assets/b24520e6-9dfd-4572-a2a2-7b18b2ce68fa" alt="Bookflix Subscription Management" width="100%" /> |

| Comment Management                                                                                                                           |
| -------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://github.com/user-attachments/assets/2e2a2055-7501-4028-a0fb-33fba7766f6c" alt="Bookflix Comment Management" width="100%" /> |

---

## 🏗️ Architecture

```mermaid
flowchart TD
    A[React TypeScript Frontend] --> B[Node.js Express REST API]
    A --> C[FastAPI AI Recommendation Service]

    B --> D[(PostgreSQL Database)]
    C --> D

    C --> E[Collaborative Filtering Engine]
    E --> F[Cosine Similarity]
    E --> G[NMF Model]
    E --> H[Hybrid Recommendation Logic]

    B --> I[JWT Authentication]
    B --> J[Swagger API Docs]

    D --> K[Docker Compose PostgreSQL]
```

---

## 🤖 Recommendation System Flow

```mermaid
flowchart TD
    A[User Ratings & Comments] --> B[Prepare Dataset]
    B --> C[Create User-Item Matrix]

    C --> D[User Similarity]
    C --> E[Item Similarity]
    C --> F[NMF Model]

    D --> G[User-Based Recommendations]
    E --> H[Item-Based Recommendations]
    F --> I[Latent Factor Recommendations]

    G --> J[Hybrid Recommendation Score]
    H --> J
    I --> J

    J --> K[Filter Owned / Rented Books]
    K --> L[Return Personalized Recommendations]
```

---

## 🔐 Authentication Flow

```mermaid
sequenceDiagram
    participant User as User
    participant Frontend as React Frontend
    participant API as Express API
    participant DB as PostgreSQL
    participant JWT as JWT Service

    User->>Frontend: Submit login form
    Frontend->>API: POST /api/auth/login
    API->>DB: Validate user credentials
    DB-->>API: Return user
    API->>JWT: Generate token
    JWT-->>API: Access token
    API-->>Frontend: Return token and user data

    Frontend->>API: Authorized request with Bearer token
    API->>JWT: Validate token
    JWT-->>API: Token valid
    API-->>Frontend: Return protected resource
```

---

## 🗄️ Simplified Data Model

```mermaid
erDiagram
    USERS ||--o{ USER_BOOKS : owns
    USERS ||--o{ RENTALS : rents
    USERS ||--o{ READING_HISTORY : reads
    USERS ||--o{ COMMENTS : writes

    BOOKS ||--o{ USER_BOOKS : included_in
    BOOKS ||--o{ RENTALS : rented_as
    BOOKS ||--o{ READING_HISTORY : tracked_in
    BOOKS ||--o{ COMMENTS : receives

    ADMINS ||--o{ BOOKS : manages
```

---

## 🛠️ Tech Stack

### Frontend

* React
* TypeScript
* Vite
* Material UI
* React Router
* Axios
* Context API
* Redux Toolkit

### Backend

* Node.js
* Express.js
* PostgreSQL
* JWT Authentication
* bcrypt
* Swagger / OpenAPI
* CORS

### AI Service

* Python
* FastAPI
* SQLAlchemy
* pandas
* NumPy
* scikit-learn
* joblib
* Collaborative Filtering
* Cosine Similarity
* Non-negative Matrix Factorization

### Database & Infrastructure

* PostgreSQL
* Docker Compose
* SQL migrations
* Seed data

---

## 📂 Project Structure

```text
bookflix/
├── frontend/      # React TypeScript frontend
├── backend/       # Node.js Express REST API
├── ai_service/    # FastAPI recommendation service
└── README.md
```

### Frontend (`frontend/`)

React TypeScript application responsible for authentication pages, book listing, book detail pages, shopping cart, payment simulation, personal library, recommendation pages, user profile, and admin UI.

### Backend API (`backend/`)

Node.js Express REST API responsible for user authentication, book management, rental operations, reading progress, user library management, comments, subscriptions, admin operations, and Swagger API documentation.

### AI Service (`ai_service/`)

FastAPI service responsible for preparing recommendation data, creating user-item matrices, calculating user and item similarities, training recommendation models, and returning personalized book recommendations.

---

## 🌐 REST API Overview

### Authentication

* User register
* User login
* Forgot password
* Reset password

### Books

* List books
* Get book detail
* Filter books by category
* Rent book
* Update reading progress
* Check audio access

### Users

* Get profile
* Update profile
* Get user library
* Add books to library
* Remove books from library
* Manage subscription

### Comments

* Add comment
* Get book comments
* Get user comments
* Delete comment

### Admin

* Admin login
* Add, update, delete books
* Manage users
* Manage comments
* Manage subscriptions
* View dashboard statistics

Interactive API documentation is available through Swagger after running the backend:

```text
http://localhost:5000/api-docs
```

---

## 🤖 AI API Overview

The AI recommendation service exposes endpoints for model training and personalized recommendations.

### Main Endpoints

```text
POST /ai/train
GET  /ai/similar-users-recommendations/{user_id}
```

FastAPI documentation is available after running the AI service:

```text
http://localhost:8000/docs
```

---

## ⚙️ Local Development

### 1. Start PostgreSQL

```bash
cd backend
docker compose up -d
```

### 2. Start Backend API

```bash
cd backend
npm install
npm run dev
```

Backend runs on:

```text
http://localhost:5000
```

Swagger documentation:

```text
http://localhost:5000/api-docs
```

### 3. Start Frontend

```bash
cd frontend
npm install
npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

### 4. Start AI Service

```bash
cd ai_service
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

AI service runs on:

```text
http://localhost:8000
```

FastAPI documentation:

```text
http://localhost:8000/docs
```

---

## 🚀 Roadmap

### Completed

* React TypeScript frontend
* Express REST API
* PostgreSQL schema
* JWT authentication
* User profile management
* Book listing and filtering
* Personal library
* Cart and payment simulation
* Comment and rating system
* Admin dashboard
* Swagger documentation
* FastAPI AI recommendation service
* Collaborative filtering recommendation logic

### In Progress

* Repository cleanup
* README and documentation improvements
* Better installation documentation
* Screenshots and demo media
* API documentation separation

### Planned

* Production deployment
* CI/CD pipeline
* Improved recommendation explanations
* Better admin analytics
* More advanced search and filtering
* Cloud storage for PDF and audio assets
* Role-based authorization improvements
* Unit and integration tests

---

## 🔮 Future Vision

Bookflix aims to become a complete digital reading platform that combines book discovery, personal library management, subscription-based access, digital reading, audio books, and AI-powered recommendations.

The long-term goal is to improve the reading experience by helping users discover relevant books based on their interests, reading history, and community ratings.
