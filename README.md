# 🎓 Smart Tutor AI – Personalized Teaching Assistant  

**Institution:** University of North Texas

> Smart Tutor AI leverages Retrieval-Augmented Generation (RAG) and Large Language Models (LLMs) to provide context-aware, accurate, and personalized student support. It grounds every response in professor-validated course materials, addressing hallucination issues and aligning AI with academic integrity.

## 🚀 Key Features

- **Conversational AI Chatbot:**  
  24/7 teaching assistant with course-grounded responses from uploaded PDFs, PPTs, DOCX, and YouTube videos.

- **RAG-Based Contextualization:**  
  Uses advanced retrieval + reranking to ensure LLMs provide accurate, relevant information.

- **Multimodal Support:**  
  Supports image uploads, diagrams, and YouTube lectures—extracting and indexing their content.

- **On-Demand Quiz Generator:**  
  Auto-generates MCQs and short answers from uploaded content with instant grading.

- **Smart Metadata & Resource Tagging:**  
  Automatically tags files by topic, source, date, and type to enhance retrieval efficiency.

- **Feedback & Continuous Evaluation:**  
  Real-time feedback via Langfuse and automated scoring with Evidently AI.

---

## 🧠 Architecture Overview

### 🔸 Data Pipeline

1. **Document Ingestion**  
   - PDF, PPT, DOCX, TXT, CSV, YouTube links, images

2. **Parsing & Chunking**  
   - LlamaIndex for text cleaning and chunk generation

3. **Embeddings & Vector Storage**  
   - MiniLM embeddings stored in ChromaDB

4. **Query & Retrieval**  
   - FAISS or ChromaDB for similarity search + reranking

5. **LLM Response Generation**  
   - LLaMA 3.1 (7B/8B) via Ollama, combined with prompt engineering

6. **Frontend Interface**  
   - Streamlit-based chat interface, file uploads, quiz generation, downloads

7. **Evaluation & Monitoring**  
   - Langfuse (LLM-as-a-Judge), Evidently AI for trust and quality monitoring

---

## 🛠️ Tech Stack

| Component            | Tools/Frameworks                             |
|---------------------|----------------------------------------------|
| LLMs                | LLaMA 3.1, DistilGPT-2, GPT-4, Gemini 1.5     |
| Embedding Models    | all-MiniLM-L6-v2 (HuggingFace)               |
| Vector DB           | ChromaDB, FAISS (Pinecone optional)          |
| Document Indexing   | LlamaIndex                                   |
| Backend             | Flask, Python 3.9+                           |
| Frontend            | Streamlit                                    |
| Evaluation          | Langfuse, Evidently AI                        |
| Deployment          | Docker, Ollama, Vercel (optional)            |

---

## 📦 Installation

pip install -r requirements.txt
