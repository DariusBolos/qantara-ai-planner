
# 🌉 Qantara — The Art of Effortless Escape

**Qantara** is an intelligent, AI-driven trip planning application designed to simplify and personalize the way people explore the world. It generates custom itineraries, predicts budgets, optimizes routes, and offers real-time travel assistance using modern AI tools. Built with a microservice architecture, Qantara separates concerns into a **Spring Boot backend** for core CRUD operations and authentication, and a **Python FastAPI backend** for AI/ML logic.

---

## ✨ Features

### 🔐 Authentication
- JWT-based login/signup
- OAuth2 login (Google, GitHub, etc.)
- Role-based access control
- Secure token/session handling

### 📦 Core Backend (Spring Boot)
- Trip CRUD (Create, Read, Update, Delete)
- User management
- Preferences handling
- PostgreSQL database integration

### 🧠 AI Capabilities (Python FastAPI)
- **AI-Powered Itinerary Generator**  
  GPT-based NLP to create daily travel plans tailored to the user
- **Route Optimizer**  
  Suggests optimal travel routes using graph algorithms (Dijkstra/A*)
- **Budget Estimator**  
  Predicts trip costs using ML models (scikit-learn, XGBoost)
- **Chatbot Travel Assistant**  
  Conversational interface for travel questions and advice
- *(Optional)* **Image-Based Recommendations**  
  Suggest destinations from uploaded landmark images

### 🌐 Frontend (React + Tailwind)
- User-friendly interface
- Interactive maps with Mapbox or Leaflet
- Form-based trip customization
- Integrated chatbot assistant

---

## 🧱 Architecture Overview

```
Frontend (React + Tailwind)
        │
        ▼
Spring Boot Backend
 - User Auth (JWT + OAuth2)
 - Trip CRUD, PostgreSQL
        │
        ▼
Python FastAPI Backend (AI)
 - GPT Itinerary Generator
 - ML Budget Estimator
 - Route Optimizer
 - Chatbot Assistant
        │
        ▼
External APIs (OpenAI, Google Places, etc.)
```

---

## 🛠️ Tech Stack

### Frontend
- React (Vite or Next.js)
- TailwindCSS + ShadCN UI
- Mapbox or Leaflet.js
- Axios / React Query

### Backend (Spring Boot)
- Spring Boot 3
- Spring Security (JWT + OAuth2)
- PostgreSQL + JPA/Hibernate
- MapStruct (DTO mapping)

### AI Service (Python)
- FastAPI
- OpenAI API (GPT-4) / Hugging Face Transformers
- scikit-learn / XGBoost
- NetworkX (for routing algorithms)
- Google Places API

### Infrastructure
- Docker & Docker Compose
- Optional: Redis for caching
- Optional: RabbitMQ or gRPC for async communication

---

## 🔁 Inter-Service Communication

| From        | To        | Method |
|-------------|-----------|--------|
| Spring Boot | FastAPI   | REST   |
| Spring Boot | PostgreSQL| JDBC   |
| FastAPI     | OpenAI / Google APIs | REST |

---

## 🚀 Getting Started

### ⚙️ Spring Boot Backend

```bash
cd qantara-backend
./gradlew bootRun
```

- 📍 Runs at: `http://localhost:8080`
- Handles user management, authentication, preferences, and CRUD operations

---

### 🤖 Python AI Service

```bash
cd qantara-ai
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8001
```

- 📍 Runs at: `http://localhost:8001`
- Key AI Endpoints:
  - `POST /generate-itinerary`
  - `POST /optimize-route`
  - `POST /predict-budget`
  - `POST /chat`

---

### 🧑‍💻 Frontend (React)

```bash
cd qantara-frontend
npm install
npm run dev
```

- 📍 Runs at: `http://localhost:3000`
- Interactive UI for planning, customizing, and interacting with your trips

---

## 📐 Project Structure

```
qantara-frontend/      → React frontend
qantara-backend/       → Spring Boot service (auth + CRUD)
qantara-ai/            → FastAPI service (AI/ML logic)
```

---

## 🎓 Academic Value

This application is ideal for a Bachelor's thesis focused on:

- Real-world microservice architecture
- AI/NLP + ML integration in production
- Modern authentication (JWT + OAuth2)
- Human-AI interaction design
- Clean separation of concerns between services

---

## 🔮 Future Enhancements

- 🌍 Multilingual itinerary generation
- 🏨 Flight and hotel booking APIs
- 📓 User travel journal / blog
- ⭐ Travel review and rating system
- 📶 Offline PWA support

---

## 📄 License

MIT License – see [`LICENSE`](./LICENSE) for details.

---

## 🔗 Name Meaning

**Qantara** (قنطرة) means **“bridge”** in Arabic — symbolizing a connection between people and the places they dream of visiting, powered by AI.

> **Qantara — The Art of Effortless Escape.**
