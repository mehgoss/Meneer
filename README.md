# Meneer

---

#📘Meneer — Your Smart South African School Assistant


---

📌 #Overview

Meneer is a mobile app designed to help South African learners (Grades 8–12) improve school performance by combining:

✅ Offline CAPS-aligned daily lessons and quizzes

✅ AI-powered question answering (photo or typed input)

✅ Real-time interactive exam mode with instant feedback

✅ Progress tracking and personalized learning recommendations



---

🎯 #Key Features

Feature	Offline	Online

CAPS Lessons by Grade and Subject	✅	✅
Practice Quizzes	✅	✅
AI “Ask a Question” (photo or typed)	❌	✅
Interactive AI Exam Mode	❌	✅
Progress Tracker	✅	✅
Optional Cloud Sync	❌	✅



---

🧱 #App Folder Structure

meneer-app/
├── src/
│   ├── components/
│   │   ├── LessonViewer.js
│   │   ├── QuizPlayer.js
│   │   ├── AskAI.js
│   │   ├── ExamMode.js
│   │   └── ProgressChart.js
│   ├── screens/
│   │   ├── GradeSelect.js
│   │   ├── SubjectSelect.js
│   │   ├── Dashboard.js
│   │   ├── LessonScreen.js
│   │   ├── QuizScreen.js
│   │   └── AskAIChatScreen.js
│   ├── data/
│   │   ├── lessons/
│   │   │   ├── grade8_math_term3.json
│   │   │   └── ...
│   │   └── subjects.json
│   ├── utils/
│   │   ├── storage.js
│   │   ├── aiAPI.js
│   │   └── ocrUtils.js
│   └── App.js
├── backend/
│   ├── main.py (FastAPI app)
│   ├── ai/
│   │   ├── evaluator.py
│   │   ├── explainer.py
│   │   └── question_generator.py
│   ├── ocr/
│   │   └── easyocr_engine.py
│   ├── models/
│   │   └── user_progress.db
├── assets/
│   ├── images/
│   └── audio/
├── README.md
├── package.json
└── requirements.txt


---

🛠️ #Tech Stack

Frontend

React Native (Expo)

AsyncStorage / SQLite for offline data

Axios for online API calls


#Backend

FastAPI for AI backend

EasyOCR or Tesseract for text extraction

SymPy for math problem solving

Hugging Face Transformers for NLP question answering

PostgreSQL or SQLite for user data



---

🧩 #Core Modules

LessonViewer: Load offline lesson content, show text/audio

QuizPlayer: Practice quizzes with instant offline marking

AskAI: Submit homework photos or typed questions, get AI-powered answers (online)

ExamMode: Interactive live exam with AI feedback and hints



---

🧪 #Sample Lesson JSON Format

{
  "title": "Linear Equations",
  "content": "To solve 2x + 4 = 10, subtract 4 from both sides...",
  "audio": "linear_eq.mp3",
  "quiz": [
    {
      "type": "mcq",
      "question": "What is x in 2x + 4 = 10?",
      "options": ["x=2", "x=3", "x=4", "x=6"],
      "answer": "x=3"
    }
  ]
}


---

🔗 #API Endpoints

Endpoint	Description

POST /ask-ai	Submit typed question
POST /upload-image	Submit homework photo for OCR + AI
POST /exam/start	Start interactive AI exam session
POST /exam/answer	Submit answer, get immediate feedback
GET /user/progress	Fetch user progress data



---

🔄 #User Experience Flow

Offline Mode

Select grade & subjects

Study daily lessons offline

Take quizzes & get instant scores offline


Online Mode

Use “Ask AI” to get help from homework photos or typed questions

Engage with interactive AI exams that give real-time feedback

Sync progress for parental and self-monitoring



---

✅ #Getting Started

Frontend

cd meneer-app
npm install
npx expo start

Backend

cd backend
pip install -r requirements.txt
uvicorn main:app --reload


---

📈 #Future Improvements

Voice-enabled AI tutor

Secure peer chat & study groups

Gamification (badges, XP, leaderboards)

Local language support (Setswana, Zulu, Xhosa)

Parental reporting dashboard



---

✊ #Vision

Meneer aims to make quality education accessible to all South African learners — whether they have internet or not — by combining proven CAPS curriculum with AI-powered personalized learning and support.


---



