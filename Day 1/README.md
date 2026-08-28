# Mini RAG Chatbot

An end-to-end Retrieval-Augmented Generation (RAG) chatbot designed to parse PDF documents and deliver contextual question-answering. This implementation runs completely local open-source models (Hugging Face + FAISS) inside Google Colab without requiring external API keys.

---

## 📌 Project Overview

This project implements a complete 7-stage RAG pipeline inside a Jupyter/Colab notebook (`Mini_RAG_Chatbot.ipynb`):

1. **PDF Text Extraction**: Parse uploaded PDF documents using `PyPDFLoader`.
2. **Text Chunking**: Segment extracted text into manageable chunks using `RecursiveCharacterTextSplitter`.
3. **Embeddings Generation**: Generate semantic dense vectors locally using `sentence-transformers/all-MiniLM-L6-v2`.
4. **Vector Database**: Store and index vectors using `FAISS` for fast similarity search.
5. **Context Retrieval**: Search top-$k$ relevant text chunks based on user query embeddings.
6. **Prompt Engineering**: System instructions to prevent LLM hallucinations and enforce context reliance.
7. **LLM Question Answering**: Generate final answers using the open-access model `Qwen/Qwen2.5-1.5B-Instruct`.

---

## 📁 Repository Structure

```text
mini-rag-chatbot/
│
├── Mini_RAG_Chatbot.ipynb    # Main end-to-end RAG pipeline notebook
├── README.md                 # Project overview and setup instructions
├── requirements.txt          # Project Python dependencies
├── sample_data/
│   └── sample_document.pdf   # Input PDF (e.g., U.S. Financial Report)
└── screenshots/
    └── rag_demo.png          # Screenshot of successful QA pipeline execution