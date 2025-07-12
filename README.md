# AI_classroom

# 📚 EduSync – AI-Powered Smart Classroom Platform

EduSync is an intelligent, web-based classroom system designed to enhance the online learning experience using artificial intelligence. It includes role-based access, AI chat assistance, auto-generated quizzes, class management, and real-time classroom tools.

---

## 🚀 Features

### 🧑‍🏫 Teachers
- Create and manage classrooms
- Upload notes and materials
- Use AI to summarize notes or generate quizzes
- View student submissions and scores

### 👩‍🎓 Students
- Join classrooms and view materials
- Interact with the AI teaching assistant
- Take quizzes and view results
- Participate in live classes

### 🤖 AI Assistant
- Answer class-related questions
- Summarize content
- Generate quizzes based on notes

---

## 🛠️ Tech Stack

| Layer     | Tech                                |
|-----------|-------------------------------------|
| Frontend  | HTML, TailwindCSS, JavaScript       |
| Backend   | Node.js, Express.js, MongoDB        |
| Auth      | JWT (Role-based: Student, Teacher)  |
| AI        | OpenAI GPT-3.5 API (chat, quiz, summary) |
| Models    | Mongoose schemas (`User`, `Classroom`) |

---

## 📂 Folder Structure (Key Files)

```
EduSync/
│
├── models/
│   ├── User.js              # User schema with role
│   └── Classroom.js         # Classroom schema with teacher & student refs
│
├── routes/
│   ├── auth.js              # Register/login APIs
│   ├── classroom.js         # CRUD and fetch classrooms
│   └── ai.js                # Chat, quiz and summary API routes
│
├── middleware/
│   └── auth.js              # JWT token verification
│
├── server.js                # Express entry point
├── .env                     # API keys and secrets
└── index.html               # UI for classroom and AI chat
```

---

## 🔐 Roles & Access Control

| Role     | Permissions                                           |
|----------|-------------------------------------------------------|
| Teacher  | Create/update/delete only their own classrooms & assignments |
| Student  | View classrooms, take quizzes, interact with AI       |
| Guest    | View only                                             |

---

## 🧪 API Overview

### Authentication
- `POST /api/auth/register` – Register user (email, password, role)
- `POST /api/auth/login` – Login and receive JWT

### Classroom
- `GET /api/classroom/` – List all classrooms for user
- `POST /api/classroom/` – Create classroom (teacher only)

### AI Features
- `POST /api/ai/chat` – Ask the chatbot a question
- `POST /api/ai/summarize` – Summarize uploaded text
- `POST /api/ai/quiz` – Generate a 5-question quiz from notes

---

## 📦 Installation & Setup

1. Clone the repo:
```bash
git clone https://github.com/BlessyCatherine/AI_classroom.git
cd AI_classroom
```

2. Install backend dependencies:
```bash
npm install
```

3. Set up `.env` file:
```
JWT_SECRET=your_jwt_secret_key
OPENAI_API_KEY=your_openai_api_key
MONGO_URI=your_mongodb_connection_string
```

4. Run the server:
```bash
node server.js
```

5. Open `index.html` in browser to access the UI.

---

## 🌐 Live Demo

_(Add your deployment link here, e.g., Firebase, Render, or Vercel)_

---

## 📌 Future Improvements

- Voice command support using Web Speech API
- Assignment submission and grading system
- Integrated video conferencing
- Notifications and email alerts

---

## 👥 Team

- [Blessy Catherine] – Full Stack Developer

---

## 📄 License

MIT License

---

> “Teaching is more effective when powered by intelligent tools.”
Update full README content
