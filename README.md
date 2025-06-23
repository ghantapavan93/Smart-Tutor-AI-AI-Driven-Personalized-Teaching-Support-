# Smart-Tutor-AI-AI-Driven-Personalized-Teaching-Support-
![image](https://github.com/user-attachments/assets/5f79a0e8-036e-4187-930c-128b2ea17ad3)
Abstract
Smart Tutor AI leverages Retrieval-Augmented Generation (RAG) and Large Language Models (LLMs) to provide personalized, context-aware teaching support. By combining course-specific materials with advanced language modeling, the system addresses the hallucination problem of traditional LLMs, ensuring more factual, relevant, and helpful student support.

Pipeline Overview
Our architecture consists of the following steps (see the diagram above):

Data Collection

Source: Course documents (PPT, PDF, Python, CSV, DOCX, etc.)
Files are collected and stored for parsing.
Document Parsing

Tool: LlamaIndex
Documents are ingested, parsed, and preprocessed (text cleaning, chunking).
Embeddings

Tool: HuggingFace Transformers (all-MiniLM-L6-v2)
Text chunks are converted into vector embeddings.
Embeddings are stored in ChromaDB.
Similarity Search & Reranking

User queries are embedded.
Top-K relevant chunks are retrieved and re-ranked for context relevance.
LLM Response Generation

Model: Llama 3.1 7B/8B, running locally or via API (e.g., Ollama)
The LLM combines retrieved context with prompt engineering to generate responses.
Frontend

Streamlit UI for user interaction.
Chat interface for querying, response display, and feedback collection.
Evaluation

Human evaluation: Fluency, coherence, factuality, and relevance (Likert scale).
Automated evaluation: Evidently AI for context quality and faithfulness.
Real-time Evaluation: langfuse for real time evaluation tracing using LLM as Judge.
Features
Conversational Teaching Assistant Chatbot 24/7 Student Support: Engage in natural language conversations to clarify concepts, provide summaries, and answer questions directly from course-specific materials. Context-Aware Responses: Utilizes advanced retrieval-augmented generation (RAG) pipeline, ensuring answers are grounded in the latest course content.

Research Mode Multi-Format Document Upload: Students and instructors can upload and index various materials (PDFs, PPTX, DOCX, TXT) for enhanced Q&A. Article Integration: Add links of scholarly articles, research papers, and supplementary readings to the knowledge base for deeper learning and richer queries. Image Understanding: Upload relevant diagrams, screenshots, and visual course content. The system can extract text and context from images to support visual learning. YouTube & Video Support: Submit YouTube video links; transcripts and extracted audio content are indexed, enabling users to ask questions about lecture or tutorial videos.

Automated Quiz Generator On-Demand Quiz Creation: Generate quizzes to test understanding of uploaded course materials or user-selected topics. Adaptive Questions: Topic coverage can be adjusted; generates multiple-choice, short answer. Immediate Feedback: Provides instant grading and explanations.

Metadata Tagging & Smart Retrieval Automated Metadata Extraction: Each document, chunk, or resource is tagged with relevant metadata (source, upload date, topic/module, file type, etc.).

Material Download & Resource Sharing Downloadable Content: Users can download original or processed course materials, generated quizzes, and annotated notes directly from the chat interface.

Feedback & Continuous Improvement User Feedback Collection: Built-in thumbs up/down feedback on each answer to refine chatbot accuracy and performance. Human and Automated Evaluation: Combines user feedback with Evidently AI analysis to enhance faithfulness, relevance, and factuality of responses and Real time Evaluation using Langfuse.

Getting Started
Requirements
Python 3.9+
LlamaIndex
ollama
HuggingFace Transformers
ChromaDB
Streamlit
Evidently AI
Langfuse
Install dependencies:

pip install -r requirements.txt
About
With the rise of digital learning platforms, students rely on search engines and LLMs for quick information. However, these tools often return irrelevant results. Smart Tutor AI (STA) bridges this gap by providing professor-validated course materials, ensuring students receive precise and relevant content.

Topics
python natural-language-processing streamlit llm ollama rag-chatbot
Resources
 Readme
 Activity
Stars
 1 star
Watchers
 1 watching
Forks
 6 forks
Report repository
Releases
No releases published
Packages
No packages published
Contributors
9
@liteshperumalla
@Fardeen210
@google-labs-jules[bot]
@pavankalyano76
@dependabot[bot]
@ChristianBridge
@kaveti27022001
@kusalsai
@iamsudikshyadevkota
Languages
Jupyter Notebook
99.7%
 
Other
0.3%
Footer
© 2025 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Stat
