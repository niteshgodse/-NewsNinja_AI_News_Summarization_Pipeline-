### NewsNinja
# AI-Powered News & Reddit Audio Summarizer

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
Backend

FastAPI

AsyncIO

LangGraph

LangChain

Anthropic API

ElevenLabs SDK

Pydantic

Tenacity (Retry Logic)

AIOLimiter (Rate Limiting)

Frontend

Streamlit

Utilities

BrightData scraping

dotenv

Uvicorn

# Project Structure
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
