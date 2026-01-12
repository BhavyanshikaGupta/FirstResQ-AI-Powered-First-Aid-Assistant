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

User inputs a symptom in natural language

Sentence-BERT encodes the query

Cosine similarity is computed against a curated first-aid dataset

The most relevant first-aid response is returned in real time

## 👥 Contributors

Vanshika Chauhan        https://www.linkedin.com/in/vanshika-chauhan-049574297/

Bhavyanshika Gupta      https://www.linkedin.com/in/bhavyanshika-gupta-8888bb284/

## 📄 License

This project is for educational and research purposes.

## Screenshots

### Home Page
<img width="1804" height="959" alt="image" src="https://github.com/user-attachments/assets/0dd1ab1e-7d50-4da3-8869-73b41d057bfa" />


### Chat Interface
<img width="1802" height="986" alt="image" src="https://github.com/user-attachments/assets/b689f469-cc91-42d8-8e0d-5eb909f04325" />


### Hardware Setup
<img width="572" height="753" alt="image" src="https://github.com/user-attachments/assets/188af82c-0cae-4687-aee2-8d035fe8ceca" />

