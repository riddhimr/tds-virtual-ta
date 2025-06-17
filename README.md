# TDS Virtual TA

This is a Retrieval-Augmented Generation (RAG) system that answers questions about the TDS course using a FastAPI backend.

## Features
- Semantic search using OpenAI embeddings (via AIPipe proxy)
- Multimodal query support (text + image)
- Chunked and indexed discourse & markdown content
- Context-aware LLM responses with source links

## Setup

```bash
git clone https://github.com/<your-username>/tds-virtual-ta.git
cd tds-virtual-ta
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
cp .env.example .env  # Add your AIPipe API Key here
uvicorn app:app --reload --host 0.0.0.0 --port 8000
