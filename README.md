# NewsNinja
### AI-Powered News & Reddit Audio Summarizer

NewsNinja is an end-to-end AI application that scrapes real-time News articles and Reddit discussions, generates broadcast-style summaries using Anthropic Claude, and converts them into high-quality MP3 audio using ElevenLabs.

Built with FastAPI, AsyncIO, LangGraph, and Streamlit.

# Features

Real-time News scraping

Reddit topic extraction

AI-generated broadcast-style summaries

High-quality MP3 audio generation

Fully async backend architecture

Retry + exponential backoff support

Clean Streamlit frontend

Modular and production-ready design

# System Architecture
Streamlit UI
      ↓
FastAPI Backend (Async)
      ↓
News Scraper + Reddit Scraper
      ↓
Anthropic Claude (Summary Generation)
      ↓
ElevenLabs TTS
      ↓
MP3 Audio Output

# Tech Stack
### Backend

FastAPI
AsyncIO
LangGraph
LangChain
Anthropic API
ElevenLabs SDK
Pydantic
Tenacity (Retry Logic)
AIOLimiter (Rate Limiting)

### Frontend

Streamlit

### Utilities

BrightData scraping
dotenv
Uvicorn

# Project Structure
```
NewsNinja/
│
├── backend.py
├── news_scraper.py
├── reddit_scraper.py
├── models.py
├── utils.py
├── streamlit_app.py
├── audio/
├── requirements.txt
└── README.md
```


### Start Backend
python backend.py

Runs at:

http://localhost:1234
### Start Frontend
streamlit run streamlit_app.py
### 📡 API Endpoint
POST /generate-news-audio
Request Body
{
  "topics": ["Artificial Intelligence"],
  "source_type": "both"
}
Response

Returns an MP3 audio file (audio/mpeg).

### 🧠 How It Works

User selects a topic in Streamlit

Backend scrapes News and/or Reddit

Data is processed and structured

Claude generates a broadcast-style summary

ElevenLabs converts text to speech

Audio file is returned to the user

### 📈 Engineering Highlights

Async scraping with rate limiting

Exponential retry mechanism

Multi-source aggregation

LLM-powered content transformation

Clean REST API design

Modular architecture

### 🔮 Future Improvements

Docker containerization

Redis caching

Background task queue

Cloud deployment (AWS / Render)

Streaming audio response

Multi-language support
