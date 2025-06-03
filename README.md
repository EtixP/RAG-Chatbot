# RAG-Chatbot (Streamlit UI) — Dockerized

This is a Retrieval-Augmented Generation (RAG) chatbot with a Streamlit-based web interface. The app is containerized using Docker and can be run locally or in any containerized environment.

---

## Features

- PDF ingestion and chunking
- SentenceTransformer + FAISS vector search
- Gemini API (Google Generative AI) for answering questions
- Streamlit UI for easy interaction

---

## Run with Docker

You can run the chatbot directly using Docker:

1. **Pull the Docker image**

```bash
docker pull ghcr.io/etixp/chatbot-env:latest

2. **Create a .env file**

Create a file named .env in the current directory with your Gemini API key:
```env
GOOGLE_API_KEY=your_gemini_api_key_here

