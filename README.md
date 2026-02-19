✈️ Autonomous AI Travel Planner
An Intelligent RAG-Powered Travel Itinerary Generator using FastAPI, Streamlit, and Vector Search
📌 Overview

The Autonomous AI Travel Planner is an AI-powered web application that generates personalized, realistic travel itineraries based on user preferences such as destination, number of days, trip type, and budget.

This project leverages Retrieval-Augmented Generation (RAG) to retrieve real travel information from a custom knowledge base and combines it with the power of Large Language Models (LLMs) to produce accurate, structured, and context-aware travel plans.

Unlike traditional itinerary generators, this system uses semantic search over travel guides, ensuring that the generated itinerary is grounded in real data and avoids hallucinated information.

This project demonstrates the practical implementation of modern AI system design including:

RAG pipeline

Vector databases

FastAPI backend architecture

Streamlit frontend development

API integration

AI application deployment

🎯 Objectives

The primary objectives of this project are:

Build an intelligent AI travel planning system

Implement Retrieval-Augmented Generation using vector search

Create a scalable backend using FastAPI

Design a clean and interactive frontend using Streamlit

Provide realistic itinerary generation grounded in real travel data

Demonstrate modern AI system architecture for portfolio and production use

🚀 Key Features
🧠 AI-Powered Itinerary Generation

Generates structured day-wise travel plans based on:

Destination

Trip duration

Budget

Trip type (Family, Solo, Adventure, Couple, Relaxation)

📅 Structured Travel Planning

Provides detailed itinerary including:

Morning activities

Afternoon activities

Evening activities

💰 Budget Estimation

Includes complete financial breakdown:

Accommodation cost

Food and activity cost

Transportation cost

Total estimated cost

Comparison with user's budget

🏨 Hotel Recommendations

Suggests hotels based on knowledge base data:

Luxury hotels

Mid-range hotels

Budget hotels

📖 Travel Tips

Provides useful travel recommendations including:

Safety tips

Seasonal advice

Cultural etiquette

Packing suggestions

🔎 Retrieval-Augmented Generation (RAG)

Uses vector search to retrieve real travel data before generating itinerary.

This ensures:

Accurate responses

Reduced hallucinations

Context-aware planning

🎨 Interactive Web Interface

Built using Streamlit with:

Modern UI design

Sidebar input system

Tab-based itinerary viewing

Clean layout

⚡ Scalable FastAPI Backend

Backend handles:

Query processing

Vector search

LLM integration

Response generation

🧠 System Architecture
User Input (Streamlit Frontend)
            │
            ▼
FastAPI Backend API (/query endpoint)
            │
            ▼
RAG Pipeline
            │
            ├── Load travel knowledge base
            ├── Convert to embeddings
            ├── Store in FAISS vector database
            │
            ▼
Semantic Search retrieves relevant travel data
            │
            ▼
LLM generates itinerary using retrieved context
            │
            ▼
Response returned to frontend
            │
            ▼
Displayed to user

🛠️ Technology Stack
Frontend

Streamlit

Python

HTML/CSS styling (via Streamlit markdown)

Backend

FastAPI

Python

AI and Machine Learning

Groq LLM API

Sentence Transformers

FAISS Vector Database

Data Storage

Text knowledge base (.txt files)

SQLite (optional database support)

Deployment Tools

GitHub

Render (Backend hosting)

Streamlit Cloud (Frontend hosting)

📂 Project Structure
ai_travel_planner/
│
├── backend/
│   │
│   ├── main.py
│   ├── routes/
│   │   └── routes.py
│   │
│   ├── rag/
│   │   └── rag.py
│   │
│   ├── models/
│   │
│   └── database/
│
├── frontend/
│   └── app.py
│
├── data/
│   └── tourism_india.txt
│
├── requirements.txt
│
└── README.md

📖 How Retrieval-Augmented Generation Works

Traditional LLM systems generate responses purely based on training data, which can result in hallucinated or inaccurate information.

This project uses Retrieval-Augmented Generation to improve accuracy.

Process:

Travel data is stored in text format

Data is split into chunks

Each chunk is converted into embeddings

Embeddings are stored in FAISS vector database

User query is converted into embedding

Most relevant chunks are retrieved

LLM uses retrieved data as context

Accurate itinerary is generated

This ensures factual and reliable responses.

▶️ Running the Application
Start Backend
cd backend
uvicorn main:app --reload


Backend runs at:

http://127.0.0.1:8000

Start Frontend
cd frontend
streamlit run app.py


Frontend runs at:

http://localhost:8501

🔐 Environment Variables

Set your API key securely:

GROQ_API_KEY=your_api_key_here


Never expose API keys publicly.

📊 Example Output

The system generates:

Best Time to Visit: October to February
Estimated Budget: ₹25,000

Day-wise itinerary
Budget breakdown
Travel tips
Hotel recommendations

🌍 Deployment

Backend deployment options:

Render

Railway

AWS EC2

Frontend deployment options:

Streamlit Cloud

📈 Future Enhancements

Possible improvements include:

User authentication system

Save trip history

Google Maps integration

Multi-country travel support

PDF export functionality

Hotel booking integration

Flight price integration

Chat-based travel assistant

Real-time weather integration

🎓 Learning Outcomes

This project demonstrates knowledge of:

Retrieval-Augmented Generation

Vector databases

FastAPI backend development

Streamlit frontend development

API integration

AI system architecture

Full-stack AI application development

👩‍💻 Author

Stanisya Reeni
MCA Student
AI and GenAI Enthusiast