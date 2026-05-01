# EduReach - Agentic College Chatbot Platform

EduReach is a comprehensive, AI-powered collegiate platform designed to enhance student engagement and streamline communication. It features an advanced Agentic Chatbot and an AI Voice Calling assistant (via Vapi) to handle admissions, general inquiries, counseling, and student life guidance.

## 🚀 Features

- **Agentic Chatbot:** Uses Langchain and Google Gemini to provide intelligent, context-aware responses based on a custom knowledge base.
- **Voice Assistant Integration:** Includes Vapi integration for real-time AI voice calling, allowing prospective students to interact via voice.
- **Modern User Interface:** Built with React, Vite, and Tailwind CSS to ensure a fully responsive, fast, and highly visual experience (Glassmorphism, dark/light themes, animations).
- **Secure Authentication:** JWT-based secure authentication with Bcrypt password hashing.
- **Robust Backend:** Express.js and Node.js server powered by a MongoDB database using Mongoose.
- **RAG Architecture:** Employs Retrieval-Augmented Generation for accurate college-specific answers using local document stores.

## 💻 Tech Stack

### Frontend (Client)
- **Framework:** React 19 with Vite
- **Styling:** Tailwind CSS v4, Lucide React (Icons)
- **Routing:** React Router DOM v7
- **HTTP Client:** Axios
- **Language:** TypeScript

### Backend (Server)
- **Environment:** Node.js (v24), Express.js
- **Database:** MongoDB (via Mongoose)
- **AI & LLM:** Langchain, Google GenAI (Gemini)
- **Voice API:** Vapi
- **Authentication:** JSON Web Tokens (JWT), bcryptjs
- **Language:** TypeScript (ts-node)

## 📁 Project Structure

```
EduReach-Agentic College Chatbot/
├── client/                 # Frontend React Application
│   ├── src/
│   │   ├── components/     # Reusable UI components (Navbar, ChatDrawer, CallPopup, etc.)
│   │   ├── context/        # React Context for state management
│   │   ├── pages/          # Full page views (HomePage, LoginPage, SignupPage)
│   │   ├── services/       # API integration layers
│   │   └── App.tsx         # Main Application Component
│   ├── index.html
│   ├── package.json
│   └── vite.config.ts
│
└── server/                 # Backend Node.js Application
    ├── src/
    │   ├── config/         # Database and app configurations
    │   ├── controllers/    # API endpoint logic
    │   ├── middleware/     # Express middlewares (Auth, Error handling)
    │   ├── models/         # MongoDB schemas
    │   ├── routes/         # Express route definitions (auth, chat, vapi)
    │   ├── services/       # Core business logic (RAG, Langchain)
    │   ├── app.ts          # Express app setup
    │   └── server.ts       # Server entry point
    ├── knowledge-base/     # Documents for the RAG chatbot
    └── package.json
```

## 🛠️ Prerequisites

Make sure you have the following installed:
- [Node.js](https://nodejs.org/) (v20+ recommended)
- [MongoDB](https://www.mongodb.com/) (Local or Atlas cluster)
- Git

## ⚙️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd "EduReach-Agentic College Chatbot"
   ```

2. **Install Server Dependencies:**
   ```bash
   cd server
   npm install
   ```

3. **Install Client Dependencies:**
   ```bash
   cd ../client
   npm install
   ```

## 🔐 Environment Variables

Create a `.env` file in the `server` directory with the following configuration:

```env
# Server Config
PORT=5000
CLIENT_URL=http://localhost:5173

# Database
MONGODB_URI=mongodb+srv://<your-username>:<your-password>@<cluster>.mongodb.net/?appName=<app-name>

# Security
JWT_SECRET=your_jwt_super_secret_key
JWT_EXPIRES_IN=7d

# Google Gemini API
GOOGLE_API_KEY=your_google_gemini_api_key

# Vapi (Voice AI) Configuration
VAPI_API_KEY=your_vapi_api_key
VAPI_ASSISTANT_ID=your_vapi_assistant_id
VAPI_PHONE_NUMBER_ID=your_vapi_phone_number_id
```

*(Note: Never commit your actual `.env` file to version control. Use `.env.example` as a template).*

## ▶️ Running the Application

### Start the Backend Server
```bash
cd server
npm run dev
```
*(Runs on `http://localhost:5000`)*

### Start the Frontend Client
Open a new terminal window:
```bash
cd client
npm run dev
```
*(Runs on `http://localhost:5173`)*

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License
This project is licensed under the MIT License.
