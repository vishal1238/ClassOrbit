<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0f1e,40:0d2137,80:0a4a6e,100:0891b2&height=220&section=header&text=ClassOrbit&fontSize=85&fontColor=ffffff&fontAlignY=40&desc=Live%20Class%20Platform%20%7C%20Real-Time%20Learning&descAlignY=62&descSize=22&animation=fadeIn" width="100%"/>

<br/>

[![React](https://img.shields.io/badge/React.js-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-1a1a2e?style=for-the-badge&logo=nodedotjs&logoColor=43d9a2)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-0a1628?style=for-the-badge&logo=mongodb&logoColor=47A248)](https://mongodb.com/)
[![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white)](https://socket.io/)
[![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=for-the-badge&logo=webrtc&logoColor=white)](https://webrtc.org/)

<br/>

> **The classroom, reimagined. Live video. Real-time chat. Role-based learning — all in one orbit.**

<br/>

</div>

---

## 🌐 What is ClassOrbit?

**ClassOrbit** is a full-stack live learning platform that brings instructors and students into the same virtual classroom — with **real-time video sessions**, **interactive chat**, and a **secure role-based system** that keeps every interaction structured, protected, and seamless.

Whether you're teaching a coding bootcamp or attending a live lecture, ClassOrbit delivers the real-time experience modern learning demands.

---

## 🚀 Core Features

<table>
<tr>
<td width="50%">

### 🎥 Live Video Sessions
Stream real-time classes with low-latency peer-to-peer video powered by **WebRTC**. No plugins. No downloads. Just open and connect.

</td>
<td width="50%">

### 💬 Real-Time Chat
Live in-class messaging via **Socket.io** keeps students engaged and questions answered — instantly, during the session.

</td>
</tr>
<tr>
<td width="50%">

### 🛡️ Role-Based Access Control
Two distinct roles — **Instructor** and **Student** — each with their own permissions, dashboards, and capabilities.

</td>
<td width="50%">

### 🔐 Secure Auth & Protected Routes
Full authentication with protected frontend routes and backend middleware to ensure only the right users access the right resources.

</td>
</tr>
<tr>
<td width="50%">

### 🗃️ Optimized MongoDB Schemas
Carefully structured and indexed database schemas for efficient queries and scalable data management.

</td>
<td width="50%">

### 📱 Responsive UI
Clean, responsive interface that works seamlessly across desktop and mobile — so learning never stops.

</td>
</tr>
</table>

---

## 🧭 Platform Flow

```
👤 Register / Login
        ↓
  ┌─────┴─────┐
  ▼           ▼
🎓 Instructor  📚 Student
  │              │
  ├─ Create Class ├─ Browse & Join Class
  ├─ Start Stream ├─ Watch Live Video
  ├─ Manage Chat  ├─ Send Messages
  └─ End Session  └─ Access Materials
        ↓
📊 Session History & Analytics
```

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend** | React.js | Component-based UI |
| **Backend** | Node.js + Express.js | REST API & server logic |
| **Database** | MongoDB | Persistent data storage |
| **Real-Time Video** | WebRTC | Peer-to-peer live streaming |
| **Real-Time Chat** | Socket.io | Bi-directional messaging |
| **Auth** | JWT + Middleware | Secure session management |

</div>

---

## 🏗️ Architecture Overview

```
┌──────────────────────────────────────────┐
│              React.js Frontend            │
│  ┌──────────┐  ┌──────────┐  ┌────────┐ │
│  │Auth Pages│  │Dashboard │  │  Class │ │
│  │  Login/  │  │Instructor│  │  Room  │ │
│  │ Register │  │ Student  │  │WebRTC  │ │
│  └──────────┘  └──────────┘  └────────┘ │
└────────────────────┬─────────────────────┘
                     │ HTTP / WebSocket
┌────────────────────▼─────────────────────┐
│          Node.js + Express.js             │
│  ┌──────────┐  ┌──────────┐  ┌────────┐ │
│  │   Auth   │  │  Class   │  │ Socket │ │
│  │Middleware│  │  Routes  │  │  .io   │ │
│  │JWT Verify│  │  RBAC    │  │Server  │ │
│  └──────────┘  └──────────┘  └────────┘ │
└────────────────────┬─────────────────────┘
                     │
┌────────────────────▼─────────────────────┐
│               MongoDB Atlas               │
│   Users │ Classes │ Sessions │ Messages  │
└──────────────────────────────────────────┘
```

---

## ⚡ Getting Started

### Prerequisites

- Node.js `v18+`
- MongoDB Atlas or local MongoDB instance

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/classorbit.git
cd classorbit
```

### 2. Install Dependencies

```bash
# Backend
cd server
npm install

# Frontend
cd ../client
npm install
```

### 3. Environment Variables

**`server/.env`**
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_jwt_key
CLIENT_URL=http://localhost:5173
```

**`client/.env`**
```env
VITE_API_URL=http://localhost:5000
VITE_SOCKET_URL=http://localhost:5000
```

### 4. Run the App

```bash
# Start backend (from /server)
npm run dev

# Start frontend (from /client)
npm run dev
```

Visit `http://localhost:5173` and start orbiting 🚀

---

## 📁 Project Structure

```
classorbit/
│
├── client/                       # React Frontend
│   ├── src/
│   │   ├── components/           # Shared UI components
│   │   ├── pages/
│   │   │   ├── auth/             # Login, Register
│   │   │   ├── instructor/       # Instructor dashboard
│   │   │   ├── student/          # Student dashboard
│   │   │   └── classroom/        # Live class room
│   │   ├── context/              # Auth & Socket context
│   │   ├── hooks/                # Custom hooks
│   │   └── utils/                # API calls, helpers
│   └── public/
│
├── server/                       # Express Backend
│   ├── models/
│   │   ├── User.js               # User schema (role-based)
│   │   ├── Class.js              # Class/session schema
│   │   └── Message.js            # Chat message schema
│   ├── routes/
│   │   ├── auth.js               # Auth routes
│   │   ├── classes.js            # Class management
│   │   └── users.js              # User management
│   ├── middleware/
│   │   ├── authMiddleware.js     # JWT verification
│   │   └── roleMiddleware.js     # RBAC enforcement
│   ├── socket/
│   │   └── socketHandler.js      # Socket.io events
│   └── server.js
│
└── README.md
```

---

## 👥 Role Capabilities

### 🎓 Instructor
- ✅ Create and schedule live classes
- ✅ Start / end video streaming sessions
- ✅ Moderate chat and participants
- ✅ Manage enrolled students

### 📚 Student
- ✅ Browse and join available classes
- ✅ Watch live video in real time
- ✅ Participate in session chat
- ✅ View past sessions & history

---

## 🔒 Security

- **JWT Authentication** — Stateless token-based auth with expiry
- **Role Middleware** — Every sensitive endpoint validates user role before execution
- **Protected Routes** — Frontend routes guard against unauthorized navigation
- **Input Validation** — Server-side validation on all incoming data

---

## 🤝 Contributing

```bash
# 1. Fork the repo
# 2. Create your branch
git checkout -b feature/amazing-feature

# 3. Commit your changes
git commit -m "feat: add amazing feature"

# 4. Push & open a PR
git push origin feature/amazing-feature
```

All contributions, bug reports, and suggestions are welcome!

---

## 📄 License

Distributed under the **MIT License**. See [LICENSE](LICENSE) for more information.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0891b2,50:0a4a6e,100:0a0f1e&height=130&section=footer" width="100%"/>

**Crafted with ❤️ by [Your Name](https://github.com/yourusername)**

*"Every great class starts with showing up. ClassOrbit makes sure you never miss one."*

<br/>

[![GitHub stars](https://img.shields.io/github/stars/yourusername/classorbit?style=social)](https://github.com/yourusername/classorbit)
&nbsp;
[![GitHub forks](https://img.shields.io/github/forks/yourusername/classorbit?style=social)](https://github.com/yourusername/classorbit)

</div>
