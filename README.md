# Minhaz's ChatBot (Web App Interface)

A sleek, modern chatbot web application with a **futuristic neon interface**.  
Built with plain **HTML, CSS, and JavaScript**, it connects to a backend API to handle real-time conversations.  
Designed to feel like a **professional web app** (not just a mobile-style chat).

---

## Features

-  **Responsive web interface** – works across desktop & mobile
-  **Futuristic neon UI** – glassmorphism, gradients, glowing effects
-  **Chat bubbles** for both user & bot
-  **Optional bot avatar** (small round logo beside messages)
-  **Watermark logo** in chat background for subtle branding
-  **Scroll & auto-focus** to keep the latest messages visible
-  **Clear chat button** to reset the conversation instantly
-  **Lightweight frontend** – no frameworks needed

---

##  Tech Stack

- **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Styling:** Custom CSS with glassmorphism + neon effects
- **Icons:** [Font Awesome](https://fontawesome.com)
- **Backend (example):** FastAPI / Flask / Node.js (you can connect any API that accepts JSON)

---

##  Project Structure

```bash
.
├── index.html       # Main UI
├── style.css        # Stylesheet (neon + watermark + responsive)
├── script.js        # Chat logic (append messages, fetch API)
├── logo.jpg         # Bot logo (used in header / watermark)
└── README.md        # Project documentation
```

##  Getting Started
1. Clone the repo

```bash
git clone https://github.com/your-username/minhaz-chatbot.git
cd minhaz-chatbot
```

2. Start a local server
(you can use Python or any static server)

```bash
# Using Python 3
python3 -m http.server 8080
```

3. Run the backend

By default, script.js sends POST requests here:
```bash
http://127.0.0.1:8000/chat
```

Make sure your backend API is running and accepts:
```bash
{ "message": "hello" }
```

and returns:
```bash
{ "reply": "Hi there! 👋" }
```

## Configuration

**API endpoint**: edit inside script.js
```bash
const response = await fetch("http://127.0.0.1:8000/chat", { ... });
```

**Bot avatar**:
In script.js → appendMessage():
* Keep the bot-chat-logo block → shows a small round avatar
* Remove/comment the block → text-only bot messages

**Watermark**:
Controlled via CSS in style.css:
```bash
.chatbox::before {
  background-image: url("logo.jpg");
  background-size: 480px auto;  /* adjust size */
  background-position: center center;
  opacity: 0.06;
}
```
## Screenshots
**Web APP UI**


## Future Improvements

* Dark/Light theme toggle
* Persistent chat history (localStorage or DB)
* Sidebar with conversation history
* Voice input / text-to-speech
* Deploy frontend + backend on cloud (Vercel, Netlify, or Render)
