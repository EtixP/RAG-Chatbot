# RAG-Chatbot (Streamlit UI) — Dockerized

This is a Retrieval-Augmented Generation (RAG) chatbot with a Streamlit-based web interface. The app is containerized using Docker and can be run locally or in any containerized environment.

---

## Features

- PDF ingestion and chunking
- SentenceTransformer + FAISS vector search
- Gemini API (Google Generative AI) for answering questions
- Streamlit UI for easy interaction

---

## API Key

This app uses the Gemini API from Google Generative AI. You must provide your own API key via a .env file.

Get your key here: https://makersuite.google.com/app/apikey

---

## Data

The container includes a pre-built FAISS index and metadata. If you'd like to reprocess your own PDFs:

- Mount your local data/ folder to the container.
- Rebuild the index before running the app.

---

## Run with Docker

You can run the chatbot directly using Docker:

1. **Pull the Docker image**
```
docker pull ghcr.io/etixp/chatbot-env:latest
```
2. **Create a .env file**
   
Create a file named .env in the current directory with your Gemini API key:
```
GOOGLE_API_KEY=your_gemini_api_key_here
```
3. **Run the Container**
```
docker run -p 8501:8501 --env-file .env ghcr.io/etixp/chatbot-env:latest
```
4. **Open the Webpage**
```
http://localhost:8501
```



