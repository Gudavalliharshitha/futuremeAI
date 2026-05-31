# 🔮 FutureMe — Meet The Version Of You Who Already Made It

An elegant, premium, Apple-style AI-powered personal reflection product. A user enters details about their current life, goals, struggles, and future ambitions, and receives an emotionally intelligent, personalized strategic guidance plan from their future self. 

Built in **Nitish’s Founder Labs** with extreme visual excellence, micro-animations, glassmorphic dark-mode visuals, and an interactive real-time follow-up chat with the user's future identity, powered by the **Gemini 1.5 Flash API**.

---

## 🛠️ Tech Stack & Architecture

- **Frontend**: Clean Vanilla HTML5 + CSS3 + ES6 JavaScript. Fully responsive, leverages Outfit & Plus Jakarta Sans typography, sleek gradient backdrops, glassmorphism cards, inline validators, and smooth coordinate timelines.
- **Backend**: Node.js + Express API. Serves frontend static content directly, manages backend secure routes, and safely coordinates model parameters.
- **AI Model**: `@google/generative-ai` integrating `gemini-1.5-flash` with native strict JSON schemas.

---

## 📦 Project Structure

```
futureme/
├── backend/
│   ├── .env               # Local configuration file (ignored from git)
│   ├── .env.example       # Sample environment template
│   ├── package.json       # Backend npm configurations & script commands
│   └── server.js          # Express app with API endpoints & server setup
├── frontend/
│   ├── index.html         # Rich structural base with form, dynamic cards & chat
│   ├── script.js          # Advanced network fetches & interactive chat state machine
│   └── style.css          # Premium Apple styling & micro-animations
└── README.md              # Setup & documentation manual (This file)
```

---

## 🚀 Getting Started (Run Locally)

Get the application running in less than 60 seconds with this simple full-stack setup:

### Step 1: Install Backend Dependencies

Navigate to the `backend/` directory and run npm install:

```bash
cd backend
npm install
```

### Step 2: Configure your Gemini API Key

Open the `backend/.env` file and replace the placeholder value with your Google Gemini API key:

```env
GEMINI_API_KEY=AIzaSy...your_gemini_api_key...
PORT=5000
```

> **Note**: To obtain a Gemini API key, visit the [Google AI Studio Console](https://aistudio.google.com/).

### Step 3: Run the Application

Start the development server with live-reload support:

```bash
npm run dev
```

Alternatively, to run the production server:

```bash
npm start
```

### Step 4: Open in Browser

Open your browser and navigate to:
🔗 **[http://localhost:5000](http://localhost:5000)**

*Because the Express backend is configured to serve the static frontend directory, the entire product operates seamlessly on a single port. No CORS preflight issues or multiple terminals required.*

---

## 📡 API Reference

### 1. Generate Reflection Profile
- **Endpoint**: `POST /api/generate-futureme`
- **Request Body**:
  ```json
  {
    "name": "Nitish",
    "age": "23",
    "goal": "Build a successful AI startup",
    "struggle": "Lack of consistency",
    "oneYearVision": "Running a profitable AI company",
    "tone": "Brutally Honest"
  }
  ```
- **Response Format**:
  ```json
  {
    "success": true,
    "data": {
      "message": "A powerful 120-180 word message written by your future self speaking directly to you...",
      "futureIdentity": "A concise, empowering description of who you are becoming...",
      "nextMoves": [
        "Create a structured 90-minute timeblock for deep coding",
        "Build a simple tracking journal...",
        "Share progress publicly..."
      ],
      "habit": "Track your wasted time honestly for 7 days.",
      "warning": "Do not wait for motivation; execution is standard.",
      "mantra": "Action creates clarity."
    }
  }
  ```

### 2. Live Chat Integration
- **Endpoint**: `POST /api/chat-futureme`
- **Request Body**:
  ```json
  {
    "userProfile": {
      "name": "Nitish",
      "age": "23",
      "goal": "Build a successful AI startup",
      "struggle": "Lack of consistency",
      "oneYearVision": "Running a profitable AI company",
      "tone": "Brutally Honest"
    },
    "chatHistory": [
      {
        "role": "futureme",
        "message": "I'm here. We already crossed the gap to our goal..."
      },
      {
        "role": "user",
        "message": "Will I actually make it?"
      }
    ],
    "question": "What should I focus on this week?"
  }
  ```
- **Response Format**:
  ```json
  {
    "success": true,
    "reply": "A personal, sharp, and highly actionable reply from your future self..."
  }
  ```

---

## 🔮 Model Adaptability Matrix

Gemini's personality and responses dynamically shift based on the chosen tone:
- **Motivational**: Warm, inspiring, and supportive.
- **Brutally Honest**: Direct, sharp, and cutthroat on excuses.
- **Calm Mentor**: Wise, patient, grounded, and steady.
- **CEO Mode**: Strategic, executive, and highly focused on rapid execution metrics.

---

## 👨‍💻 Founder Lab AI Hacks Included

1. **Identity Prompting**: Programmed system instructions ensuring Gemini behaves purely as a future successful version, avoiding generic chatbot clichés.
2. **Strict JSON Schemas**: Employs structural guarantees in Node.js to eliminate JSON serialization errors during live demos.
3. **Chronological State Cache**: Frontend maintains conversation queues, maintaining deep context across multiple conversational exchanges.
