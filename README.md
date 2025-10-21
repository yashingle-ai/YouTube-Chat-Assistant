# 🎬 VidSynth AI – YouTube Chat Assistant

> 🧠 Transform YouTube videos into key topics, structured notes, and an interactive chatbot using AI.

[![Streamlit App](https://img.shields.io/badge/Try%20it%20Live-Streamlit-brightgreen?logo=streamlit)](https://youtubechatassistant.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-Framework-blueviolet)](https://www.langchain.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 🚀 Live Demo  
🎯 **Try it now:** [https://youtubechatassistant.streamlit.app/](https://youtubechatassistant.streamlit.app/)

---

## 🧩 Overview

**VidSynth AI** (YouTube Chat Assistant) is an intelligent Streamlit application that:
- Extracts transcripts from any YouTube video.  
- Translates them into English (using Gemini AI).  
- Summarizes the content into concise notes.  
- Extracts the **5 most important topics** discussed.  
- Lets you **chat interactively** with the video using **RAG (Retrieval-Augmented Generation)**.  

All of this happens directly in your browser — no manual downloads or preprocessing needed.

---

## 🎥 Example Use Cases
✅ Get structured notes from lectures and tutorials.  
✅ Translate non-English videos into English notes.  
✅ Chat with long educational or documentary videos.  
✅ Quickly understand video content without watching the full thing.

---

## 🧠 Features

| Feature | Description |
|----------|-------------|
| 🎧 **Transcript Extraction** | Fetches captions directly from YouTube videos. |
| 🌍 **Language Translation** | Translates transcript to English using Google Gemini. |
| 📝 **AI Notes Generation** | Creates structured, concise notes with headings and bullet points. |
| 🔍 **Topic Extraction** | Lists the 5 most important topics in the video. |
| 💬 **Chat With Video** | Uses RAG-based question answering over the transcript. |
| 🧱 **Chunking + Vector Store** | ChromaDB + Sentence Transformers embeddings for fast search. |

---

## 🏗️ Tech Stack

| Component | Technology Used |
|------------|----------------|
| Frontend | Streamlit |
| Backend | Python |
| AI Models | Gemini 2.5 Flash Lite (LLM), Sentence Transformers (Embeddings) |
| Vector Database | ChromaDB |
| Framework | LangChain |
| Deployment | Streamlit Cloud |

---

## ⚙️ Installation and Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/youtube-chat-assistant.git
cd youtube-chat-assistant
```

### 2️⃣ Create and Activate a Virtual Environment
```bash
python -m venv venv
venv\Scripts\activate      # on Windows
source venv/bin/activate   # on macOS/Linux
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Add Environment Variables
Create a `.env` file in the project root with your Google Gemini API key:

```
GOOGLE_API_KEY=your_google_gemini_api_key_here
```

*(Gemini key is free to generate at [Google AI Studio](https://aistudio.google.com/))*

---

## ▶️ Run the App Locally
```bash
streamlit run app.py
```

Then open the local URL (usually `http://localhost:8501`) in your browser.

---

## 🧠 How It Works

1. **Transcript Extraction** → Fetches text from YouTube using `youtube-transcript-api`.  
2. **Translation** → Converts non-English text to English via Gemini.  
3. **Chunking** → Splits transcript into overlapping chunks using `RecursiveCharacterTextSplitter`.  
4. **Embeddings** → Uses `HuggingFaceEmbeddings` (`all-MiniLM-L6-v2`) to vectorize text.  
5. **Vector Storage** → Stores and retrieves relevant chunks via **ChromaDB**.  
6. **RAG-based Chat** → Uses Gemini to answer user queries based on retrieved context.

---

## 📁 Project Structure

```
youtube-chat-assistant/
│
├── app.py                      # Main Streamlit application
├── supporting_functions.py      # Core logic and helper functions
├── requirements.txt             # Dependencies
├── .env.example                 # Example environment file
├── README.md                    # Project documentation
└── assets/                      # (optional) images or icons
```

---

## 🧩 Requirements

Make sure your `requirements.txt` includes:

```
streamlit
python-dotenv
youtube-transcript-api
langchain
langchain-core
langchain-community
langchain-text-splitters
langchain-chroma
chromadb
sentence-transformers
huggingface-hub
google-generativeai
langchain-google-genai
pysqlite3-binary
```

---

## 🖼️ UI Preview

| Sidebar | Notes | Chat |
|----------|-------|------|
| ![Sidebar](https://github.com/your-username/youtube-chat-assistant/assets/sidebar.png) | ![Notes](https://github.com/your-username/youtube-chat-assistant/assets/notes.png) | ![Chat](https://github.com/your-username/youtube-chat-assistant/assets/chat.png) |

*(Add screenshots here once available)*

---

## 🤝 Contributing
Contributions are welcome!  
1. Fork the repository  
2. Create a new branch (`feature/new-feature`)  
3. Commit your changes  
4. Open a pull request  

---

## 🧾 License
This project is licensed under the [MIT License](LICENSE).

---

## 🌐 Author

👤 **Yash Ingle**  
🎓 B.Tech, Artificial Intelligence, SVNIT Surat  


---

## 💫 Acknowledgements
- [LangChain](https://www.langchain.com/)  
- [Streamlit](https://streamlit.io/)  
- [Google Gemini](https://aistudio.google.com/)  
- [Sentence Transformers](https://www.sbert.net/)  
- [YouTube Transcript API](https://pypi.org/project/youtube-transcript-api/)

---

✨ **Live App:** [https://youtubechatassistant.streamlit.app/](https://youtubechatassistant.streamlit.app/)  
🎉 *Experience AI-powered understanding of YouTube videos instantly!*
````
