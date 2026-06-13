# 🩺 FirstResQ – AI First Aid Assistant

FirstResQ is a full-stack AI-powered first aid assistant designed to provide **real-time, calm, and reliable emergency guidance** based on user-described symptoms. The system leverages **semantic NLP models** to map symptoms to appropriate first-aid instructions, ensuring quick and accurate responses during critical situations.

---

## 🚀 Features

- AI-powered symptom analysis** using Sentence Transformers (SBERT)
- Real-time chat-based first aid guidance**
- User authentication & session-based chat history**
- Voice interaction support** for hands-free usage
- Responsive frontend** built with modern UI components
- Guest access** without mandatory login
- Persistent chat storage** using SQLite

---

## 🛠️ Tech Stack

### Frontend
- React
- TypeScript
- Tailwind CSS
- Vite

### Backend
- Python
- Flask
- SQLAlchemy
- Sentence Transformers (SBERT)
- SQLite

---

## 📂 Project Structure
```bash
FirstResQ/
├── backend/ # Flask backend & AI model
│ ├── app.py
│ ├── first_aid_model/
│ ├── cleaned_first_aid.jsonl
│ └── requirement.txt
│
├── kid-aid-bot/ # React frontend
│ ├── src/
│ ├── public/
│ └── package.json
│
├── .gitignore
└── README.md

```

Backend Setup (Flask)
```bash
Copy code
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirement.txt
python app.py
```
Backend runs on:
```bash
http://127.0.0.1:5000
```

Frontend Setup (React)
```bash
cd kid-aid-bot
npm install
npm run dev
```
Frontend runs on:
```bash
http://localhost:8080
```

## AI Working

- User inputs a symptom in natural language
- Sentence-BERT encodes the query
- Cosine similarity is computed against a curated first-aid dataset
- The most relevant first-aid response is returned in real time

## 🔊 Raspberry Pi Voice Assistant Device

FirstResQ also supports a standalone Raspberry Pi–based voice assistant device, enabling hands-free first aid guidance without requiring a browser or smartphone.

The device captures user speech via a microphone, sends the transcribed text to the Flask backend over HTTP, and outputs the AI-generated first aid response through a speaker and on-screen display.

### 🧠 Device Capabilities

- Voice-based symptom input using microphone
- Real-time speech-to-text processing
- Server-based AI inference (lightweight edge device)
- Text & audio response output
- Works on local network with Flask server

### 🧰 Hardware Requirements

- Raspberry Pi (Pi 3 / Pi 4 recommended)
- USB Microphone
- Speaker or Headphones
- Display (optional, for text output)
- Raspberry Pi OS

### 🛠️ Device Software Stack

- Python 3
- SpeechRecognition
- Requests
- Pygame
- Google Speech API (via SpeechRecognition)

### 📡 Device–Server Communication Flow

- User speaks a symptom into the microphone
- Raspberry Pi converts speech → text
- Text is sent to Flask /chat/<session_id> API
- Backend processes input using SBERT similarity search
- First aid response is returned
- Raspberry Pi displays and speaks the response

### ▶️ Raspberry Pi Setup & Execution

```bash
sudo apt update
sudo apt install python3-pip portaudio19-dev
pip3 install SpeechRecognition requests pygame pyaudio
```

Update the server IP address in the script:

```bash
SERVER_URL = "http://<FLASK_SERVER_IP>:5000/chat/1"
```

Run the device client:

```bash
python3 raspcode.py
```

## 👥 Contributors

Vanshika Chauhan        https://www.linkedin.com/in/vanshika-chauhan-049574297/

Bhavyanshika Gupta      https://www.linkedin.com/in/bhavyanshika-gupta-8888bb284/

Piyush Thakur           https://www.linkedin.com/in/piyush-thakur-xlr


## 📄 License

This project is for educational and research purposes.

## Screenshots

### Home Page
<img width="1804" height="959" alt="image" src="https://github.com/user-attachments/assets/0dd1ab1e-7d50-4da3-8869-73b41d057bfa" />


### Chat Interface
<img width="1802" height="986" alt="image" src="https://github.com/user-attachments/assets/b689f469-cc91-42d8-8e0d-5eb909f04325" />


### Hardware Setup
<img width="572" height="753" alt="image" src="https://github.com/user-attachments/assets/188af82c-0cae-4687-aee2-8d035fe8ceca" />

