# ✈️ Autonomous AI Travel Planner

An intelligent AI-powered travel planner that generates personalized travel itineraries using Retrieval-Augmented Generation (RAG), FastAPI, FAISS vector database, and Streamlit.

This system retrieves real travel information from a custom knowledge base and generates realistic travel plans including daily itinerary, budget estimation, hotel suggestions, and travel tips.

# 🚀 Features

🧠 AI-powered itinerary generation using RAG

📅 Day-wise structured travel plan

💰 Budget estimation and breakdown

🏨 Hotel suggestions (Luxury / Mid / Budget)

📍 Uses real travel data from knowledge base

⚡ FastAPI backend for scalable API

🎨 Streamlit frontend with modern UI

🔎 FAISS vector search for semantic retrieval

📖 Travel tips and recommendations

# 🧠 How It Works (RAG Pipeline)

Travel data is stored in tourism_india.txt

Text is split into smaller chunks

Each chunk is converted into embeddings using Sentence Transformers

Embeddings are stored in FAISS vector database

User query is converted into embedding

Relevant travel data is retrieved using vector similarity search

LLM generates itinerary based on retrieved context

Final response is sent to frontend and displayed

This ensures accurate, realistic, and context-aware travel plans.

# 🏗️ Project Architecture

User Input (Streamlit UI)
↓
FastAPI Backend (/query endpoint)
↓
RAG Pipeline
↓
FAISS Vector Search
↓
Retrieve travel knowledge
↓
LLM generates itinerary
↓
Response returned to frontend

# 🛠️ Tech Stack
## Frontend

Streamlit

Python

## Backend

FastAPI

Python

## AI / RAG

Groq LLM

Sentence Transformers

FAISS Vector Database

## Database (Optional)

SQLite

📂 Project Structure
ai_travel_planner/
│
├── backend/
│   ├── database/
│   │   ├── db.py
│   │   └── dep.py
│   │
│   ├── models/
│   │   ├── pydantic.py
│   │   └── table.py
│   │
│   ├── services/
│   │   └── rag.py
│   │
│   ├── routes/
│   │   └── routes.py
│   │
│   └── main.py
│
├── frontend/
│   └── app.py
│
├── data/
│   └── tourism_india.txt
└── README.md

# ⚙️ Installation
Clone Repository
git clone https://github.com/YOUR_USERNAME/ai_travel_planner.git
cd ai_travel_planner

Create Virtual Environment
python -m venv .venv

Activate Virtual Environment
Windows
.venv\Scripts\activate

Mac / Linux
source .venv/bin/activate

Install Dependencies
pip install -r requirements.txt

▶️ Run Backend (FastAPI)
cd backend
uvicorn main:app --reload


Backend runs at:

http://127.0.0.1:8000

▶️ Run Frontend (Streamlit)
cd frontend
streamlit run app.py


Frontend runs at:

http://localhost:8501

🔐 Environment Variables

Set your Groq API key securely:

GROQ_API_KEY=your_api_key_here

# 📊 Example Output

The system generates:

Best Time to Visit

Estimated Budget

Day-wise itinerary

Budget breakdown

Travel tips

Hotel suggestions

# 🌍 Deployment

Backend deployment options:

Render

Railway

AWS

Frontend deployment options:

Streamlit Cloud

# 🎯 Use Cases

AI Travel Planner

Tourism Recommendation System

GenAI Portfolio Project

RAG Learning Project

Intelligent Travel Assistant

# 👩‍💻 Author

## Stanisya Reeni
## MCA Student
