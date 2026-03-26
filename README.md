# 🤖 AI Chatbot — Containerized LLM QA System

A ChatGPT-style AI chatbot with a beautiful dark UI, built with FastAPI + OpenAI, containerized with Docker.

## Features
- 💬 Real-time chat interface (like ChatGPT / Claude)
- 🔄 Full conversation memory (multi-turn)
- ✨ Typing indicator & smooth animations
- 🎨 Beautiful dark UI with suggestion prompts
- 🐳 Docker ready

## Run Locally

```bash
pip install -r requirements.txt
set OPENAI_API_KEY=your_key_here       # Windows
export OPENAI_API_KEY=your_key_here    # Mac/Linux
uvicorn app:app --reload
```
Open: **http://127.0.0.1:8000**

## Run with Docker

```bash
docker build -t llm-chatbot .
docker run -d -p 8000:8000 -e OPENAI_API_KEY=your_key_here llm-chatbot
```
Open: **http://localhost:8000**

## Change the Bot's Domain
Edit `SYSTEM_PROMPT` in `app.py` to make it domain-specific:
```python
SYSTEM_PROMPT = "You are a medical assistant. Only answer health-related questions..."
SYSTEM_PROMPT = "You are a coding tutor. Help students learn programming..."
SYSTEM_PROMPT = "You are a legal advisor. Answer questions about Indian law..."
```

## Tech Stack
- Python · FastAPI · OpenAI GPT-3.5 · Docker
