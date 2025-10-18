# 🧠 Ask My Docs - A Local Generative AI Knowledge Assistant

## 📘 Overview

**Ask My Docs** is a project that demonstrates the fundamentals of **Generative AI**, **Retrieval-Augmented Generation (RAG)**, and **Model Context Protocol (MCP)** through an interactive chat interface.  

Users can upload PDF or text documents, and then chat with an AI assistant that references the uploaded materials to answer questions with contextual accuracy.  

This project is designed to provide a practical, end-to-end overview of modern AI architecture — from document ingestion and vector search to generative response synthesis — all running locally through a lightweight Streamlit interface.

---

## 🎯 Objectives

- Learn how to integrate **LLMs with external knowledge** via RAG  
- Understand how **MCP servers** modularize retrieval and external context  
- Experiment with **prompt engineering** for context injection  
- Build a simple but complete **AI-powered web app** using Streamlit  
- Deploy and test locally with your own documents

---

## ⚙️ Technologies Used

| Category | Tool / Library | Purpose |
|-----------|----------------|----------|
| **Language** | Python 3.10+ | Core development |
| **Frontend** | [Streamlit](https://streamlit.io/) | Interactive chat UI |
| **Backend** | [FastAPI](https://fastapi.tiangolo.com/) or Flask | API + MCP server |
| **LLM** | OpenAI API, Anthropic Claude, or [Ollama](https://ollama.ai/) | Generative response engine |
| **Vector Store** | [ChromaDB](https://www.trychroma.com/) | Store and retrieve embeddings |
| **Embeddings** | `text-embedding-3-small` or `sentence-transformers` | Encode document chunks |
| **Text Extraction** | `PyPDF2` or `pdfplumber` | Extract text from PDFs |
| **Data Handling** | `pandas`, `tiktoken`, `numpy` | Preprocessing and chunking |
| **MCP SDK** | [Model Context Protocol SDK](https://github.com/modelcontextprotocol/python-sdk) | Serve context via protocol |
| **Optional** | `langchain` | Helper for retrieval and prompt chaining |

---

## 🧠 How It Works

1. **Upload Documents**
   - The user uploads one or more PDF or text files.
   - Text is extracted, split into chunks (~500 tokens), and embedded.

2. **Store in Vector Database**
   - Each chunk is embedded and stored in ChromaDB with metadata.

3. **Query and Retrieve**
   - The user submits a question.
   - The query is embedded, and the MCP server retrieves top-k relevant chunks.

4. **Contextual Response Generation**
   - The retrieved text + user question is passed into a prompt template.
   - The LLM generates a grounded answer using the provided context.

5. **Chat Interface**
   - Streamlit displays chat bubbles for user and AI.
   - Optionally shows which document snippets were used.

---

