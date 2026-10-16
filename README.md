**#Live Link --->** https://enterprise-rag-knowledge-assistant.netlify.app/

# Enterprise RAG Knowledge Assistant

An AI-powered **Retrieval-Augmented Generation (RAG)** application that enables users to interact with enterprise documents using natural language. The system combines **Large Language Models (LLMs)** with **vector similarity search** to deliver accurate, context-aware responses from uploaded documents.

---

## Features

- Document ingestion and preprocessing
- Intelligent document chunking
- Embedding generation using LangChain
- Vector storage with ChromaDB
- Semantic document retrieval
- Retrieval-Augmented Generation (RAG)
- Multi-query retrieval
- Prompt engineering
- Conversational memory
- REST API support
- Docker-ready deployment

---

## Tech Stack

### Programming Language
- Python

### AI & LLM
- LangChain
- OpenAI / Azure OpenAI *(update according to your implementation)*
- Prompt Engineering

### Vector Database
- ChromaDB

### Backend
- FastAPI

### Deployment
- Docker

---

## Project Architecture

```
                User Query
                     │
                     ▼
              FastAPI Backend
                     │
                     ▼
          Prompt Engineering Layer
                     │
                     ▼
              LangChain Pipeline
                     │
         ┌───────────┴───────────┐
         │                       │
         ▼                       ▼
    ChromaDB               Large Language Model
(Vector Retrieval)      (OpenAI/Azure OpenAI)
         │                       │
         └───────────┬───────────┘
                     ▼
            Context-Aware Response
```

---

## Project Structure

```
Enterprise-RAG-Knowledge-Assistant/
│
├── app/
│   ├── api/
│   ├── services/
│   ├── retriever/
│   ├── prompts/
│   ├── embeddings/
│   └── utils/
│
├── data/
│
├── vectorstore/
│
├── notebooks/
│
├── requirements.txt
├── Dockerfile
├── README.md
└── .env.example
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/Enterprise-RAG-Knowledge-Assistant.git
cd Enterprise-RAG-Knowledge-Assistant
```

---

### Create Virtual Environment

```bash
python -m venv venv
```

Windows

```cmd
venv\Scripts\activate
```

Linux / macOS

```bash
source venv/bin/activate
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

### Configure Environment Variables

Create a `.env` file.

Example:

```env
OPENAI_API_KEY=your_key

LANGCHAIN_API_KEY=your_key

CHROMA_DB_PATH=./vectorstore

MODEL_NAME=gpt-4o-mini
```

---

## Running the Project

Start the FastAPI server

```bash
uvicorn app.main:app --reload
```

Application will run at

```
http://localhost:8000
```

Swagger Documentation

```
http://localhost:8000/docs
```

---

## Workflow

1. Upload enterprise documents.
2. Documents are split into semantic chunks.
3. Chunks are converted into embeddings.
4. Embeddings are stored inside ChromaDB.
5. User submits a question.
6. Relevant context is retrieved.
7. LangChain augments the prompt.
8. LLM generates a context-aware answer.

---

## Sample Use Cases

- Enterprise Knowledge Assistant
- HR Policy Search
- Company Documentation Chatbot
- Legal Document Search
- Technical Documentation Assistant
- Research Assistant

---

## Skills Demonstrated

- Retrieval-Augmented Generation (RAG)
- Large Language Models (LLMs)
- Prompt Engineering
- Semantic Search
- Vector Databases
- LangChain
- FastAPI
- REST APIs
- Docker Deployment

---

## Future Improvements

- Multi-agent workflow
- Azure OpenAI integration
- Model Context Protocol (MCP)
- Hybrid Search (BM25 + Vector Search)
- Authentication & RBAC
- Kubernetes deployment
- Streaming responses
- Conversation analytics

---

## Screenshots

Add screenshots here.

Example:

```
assets/

├── architecture.png

├── chat-ui.png

├── swagger-api.png
```
## License

This project is released under the MIT License.
