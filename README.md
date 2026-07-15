# 🎓 EduSimplify AI

**An AI learning assistant that lets you chat with any PDF.**  
Upload a document, ask questions in natural language, and get precise answers from the content — powered by **IBM Granite LLM** and **RAG (Retrieval-Augmented Generation)**.

[![Python](https://img.shields.io/badge/python-3.10+-blue.svg)](#)
[![FastAPI](https://img.shields.io/badge/fastapi-backend-green)](#)
[![React](https://img.shields.io/badge/react-frontend-blueviolet)](#)
[![IBM Watson](https://img.shields.io/badge/IBM-watsonx-orange)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 🚀 Features

- 📄 **Upload any PDF** – notes, textbooks, research papers  
- 🤖 **Ask questions in natural language** – get answers instantly  
- 📚 **Answers only from the document** – no hallucination  
- ⚡ **FastAPI backend** with async processing  
- 🎨 **React frontend** built with Vite  
- 🧠 **IBM Granite Foundation Model** (Granite 3.3) via watsonx.ai  
- 📑 **Automatic PDF chunking** for better context retrieval  
- 🔍 **RAG pipeline** – retrieves relevant chunks before answering  

---

## 🛠 Tech Stack

| Layer       | Technology                          |
|-------------|--------------------------------------|
| **Frontend** | React.js, Vite, CSS                 |
| **Backend**  | FastAPI, Python                     |
| **AI/ML**    | IBM watsonx.ai, Granite 3.3, LangChain (or custom RAG) |
| **PDF Processing** | PyMuPDF (fitz)               |
| **Deployment** | (you can add: Docker, Render, etc.) |

---

## 📸 Screenshots

*(Your existing screenshots can be pasted here – they're great!)*

**Upload & Chat Interface**  
<img width="1920" height="1080" alt="upload" src="https://github.com/user-attachments/assets/5b269f58-c72b-43cb-9022-56c040623669" />

**Question & Answer**  
<img width="1920" height="1080" alt="qna" src="https://github.com/user-attachments/assets/672c9897-f30d-4624-bd70-1089672c547c" />

**Chat History**  
<img width="1920" height="1080" alt="history" src="https://github.com/user-attachments/assets/acb908e8-315a-42a1-bdc5-a3ff66af82f6" />

**Document View**  
<img width="1920" height="1080" alt="docview" src="https://github.com/user-attachments/assets/2307c3fe-5c70-4d1d-9159-2b27ac5fd3b4" />

**Backend Logs**  
<img width="662" height="630" alt="backend" src="https://github.com/user-attachments/assets/fdee6277-a5dd-438e-9d1d-fefec51eedd6" />

---

## 📖 How it works

```mermaid
flowchart LR
    A[User uploads PDF] --> B[PyMuPDF extracts text]
    B --> C[Text split into chunks]
    C --> D[Chunks embedded & stored in vector DB]
    E[User asks a question] --> F[Question embedded]
    F --> G[Retrieve most relevant chunks]
    G --> H[Prompt = question + chunks]
    H --> I[IBM Granite generates answer]
    I --> J[Answer displayed in UI]
