# CognitoMark: High-Fidelity Exam Portal

> A state-of-the-art, real-time examination platform designed for precision, reliability, and an exceptional user experience.
> This portal features advanced telemetry, granular behavior tracking, and a premium administrative dashboard to ensure a seamless and secure testing environment.

---

## 📸 Screenshots

- 🧑‍🎓 Student Exam Interface
- 🛠 Admin Dashboard
- 📊 Telemetry & Monitoring View

📁 Place your images inside a /screenshots folder in the root of your repository.

## 🚀 Key Features Overview

CognitoMark provides a robust and intelligent examination experience for both students and administrators.

### Real-Time Administration

- Instant updates & dynamic dashboards
- Monitor exams with high responsiveness

### Advanced Telemetry & Tracking

- High-fidelity click tracking
- Integrity monitoring & behavior insights

### Premium User Experience

- Intuitive UI & responsive design
- Custom components & vibrant interface

## 🛰 Real-Time Administration Capabilities

Administrators can oversee the examination process with clarity and control.

- Live Updates: Notifications for registrations, exam starts, and submissions via Socket.IO
- Dynamic Dashboard: Automatic refreshing of Students & Sessions tabs
- Empty States: User-friendly messages for empty data scenarios
- Navigation Insights: Tracks transitions between questions (Previous/Next)
- Reset Workflow: Secure admin session reset with password confirmation

## 🧠 Advanced Telemetry & Tracking

A sophisticated telemetry system captures and categorizes every interaction.

- High-Fidelity Click Tracking: Logs all clicks, including background interactions
- Granular Categorization: Logs clicks by Header, Integrity Monitor, Stress Bar, Question Area, Navigation
- Sequential Answering: Forces logical question flow
- Integrity Monitor: Detects tab switching, minimizing, fullscreen exit
- Fullscreen Enforcement: Auto fullscreen exam mode & violation logging

## 💎 Premium User Experience

Designed for focus, clarity, and visual excellence.

- Vibrant UI: Dark-mode theme with glassmorphism & modern typography
- Custom Components: Premium confirmation modals & dropdowns
- Responsive Navigation: Collapsible sidebar with smooth micro-animations
- CSV Exports: Export session & per-question data

## 🧰 Technical Stack

### Frontend

- Next.js (Turbopack)
- React
- Socket.IO Client
- Axios

### Backend

- Express.js
- Socket.IO
- Mongoose ODM
- JWT Authentication

### Database

- MongoDB
- Timeseries logging for telemetry

## ✅ Scoring & Evaluation System

- Admin Answer Key: Supports MCQ & text answers
- Auto Scoring: Automatic scoring on submission
- Per-Question Results: Correct/incorrect indicators
- Session Score: Total score stored & displayed

## 📁 Project Structure

```
frontend/
 ├── src/app          → Next.js pages & layouts
 ├── src/screens      → Student login, exam UI, admin dashboard
 ├── src/components   → Reusable UI components
 └── src/api          → API client wrappers

backend/
 ├── src/controllers  → Business logic
 ├── src/db           → DB setup & telemetry logging
 └── src/sockets      → Real-time event handling
```

## ⚙️ Getting Started

### Prerequisites

- Node.js v24.12+
- npm / pnpm / yarn

### 1️⃣ Clone Repository

```
git clone https://github.com/CognitoMark/CognitoMark.git
```

### 2️⃣ Setup Backend

```
cd backend
npm install

# create .env based on .env.example
npm run dev
```

### 3️⃣ Setup Frontend

```
cd frontend
npm install

# create .env based on .env.example
npm run dev
```

## 🔐 Environment Variables

### Backend (.env)

```
PORT=5000
JWT_SECRET=your_secret
CLIENT_ORIGIN=http://localhost:3000
MONGODB_URI=your_mongodb_connection
```

### Frontend (.env)

```
NEXT_PUBLIC_API_URL=http://localhost:5000
NEXT_PUBLIC_SOCKET_URL=http://localhost:5000
```

## 📊 Telemetry Flow & Security

The platform tracks user actions from exam selection to submission while ensuring strict security.

### Security & Integrity Features

- JWT Protection: Secures admin routes
- SSR Safety: Protects client storage access
- Sequential Guard: Ensures ordered answering
- Reset Behavior: Clears sessions & telemetry while preserving exams