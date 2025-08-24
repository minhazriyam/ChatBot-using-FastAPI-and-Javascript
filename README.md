# 🤖 Minhaz's ChatBot

A simple yet professional **chatbot web app** powered by **FastAPI** on the backend and **Groq’s Llama 3.3** model for responses.  
The frontend is a sleek neon-glass styled chat interface built with vanilla **HTML, CSS, and JavaScript**.

---

## ✨ Features

- **FastAPI backend** with CORS enabled
- **Groq Llama 3.3-70b** for conversational responses
- **Modern UI**: neon-glass chat bubbles, subtle watermark branding
- **Real-time chat** with smooth scroll and input handling
- **Clear chat** functionality
- **Frontend + backend decoupled** (works locally or can be deployed separately)

---

## 📂 Project Structure

.
├── backend/
│ └── main.py # FastAPI app serving /chat endpoint
│
├── frontend/
│ ├── index.html # Chat UI
│ ├── style.css # Neon-glass styling
│ └── script.js # Chat logic (send, append, clear)
│
├── .env # Environment variables (GROQ_API_KEY)
└── README.md
.


---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/minhaz-chatbot.git
cd minhaz-chatbot
```

### 2. Backend (FastAPI)
Create a virtual environment
```bash
cd backend
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows
```

Install dependencies
```bash
pip install fastapi uvicorn groq python-dotenv
```
Environment variables
Create a .env file in the backend folder:
```bash
GROQ_API_KEY=your_groq_api_key_here
```
Run the backend
```bash
uvicorn main:app --reload
```
By default, the backend runs at:
👉 http://127.0.0.1:8000

### 3. Frontend (HTML/CSS/JS)
Just open frontend/index.html in your browser.
It will send requests to the FastAPI backend on http://127.0.0.1:8000/chat.

## Usage
* Start the FastAPI server (uvicorn main:app --reload).
* Open index.html in your browser.
* Type a message and hit send ✈️.
* The bot will reply using Groq Llama 3.3-70b.

## Preview


## Customization
* **Watermark Logo**: Adjust watermark size & opacity in style.css under .chatbox::before.
* **Bot Avatar**: Controlled in script.js (class bot-chat-logo). Can be disabled or resized via CSS.
* **Model**: Change model in main.py (model="llama-3.3-70b-versatile").

## License
MIT License — feel free to use, modify, and share.

