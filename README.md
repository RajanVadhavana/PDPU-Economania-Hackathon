# Automated Compliance Management System
**Project for Breach 2025 | Economania 2025**

Maintaining regulatory compliance in the financial sector is a moving target. With constant updates from bodies like SEBI, RBI, and IRDA, manual monitoring is no longer sustainable. We built this system to bridge the gap between shifting regulations and internal company policies using an automated, AI-driven approach.

---

## 📋 Overview
Financial institutions face significant risks, including heavy penalties and reputational damage, due to delays in processing regulatory circulars. Our solution automates the ingestion of these updates and provides an intelligent layer of analysis to ensure company policies remain aligned with current law.

### Core Features
* **Automated Regulatory Scraping:** Real-time monitoring and extraction of new circulars from official regulatory websites.
* **AI Policy Alignment:** Automated comparison between internal documentation and new mandates to identify discrepancies.
* **Risk Assessment:** A dedicated engine to detect compliance gaps and estimate potential penalty exposure.
* **Centralized Dashboard:** A visual interface providing a real-time "Compliance Score," audit trails, and instant risk notifications.
* **Interactive RAG Bot:** A specialized Chatbot (Retrieval-Augmented Generation) that allows compliance officers to query their own data and regulatory history using natural language.

---

## 🛠 Technical Implementation
Our approach moves beyond simple keyword matching. We utilize a multi-agent AI architecture to handle complex document processing:

* **Data Ingestion:** We use **Crawl4AI** to scrape unstructured data from official sources, ensuring the system stays updated without manual input.
* **Knowledge Base:** Documents are processed into embeddings and stored in a **FAISS Vector Database**, allowing for high-speed, semantic retrieval.
* **Agentic Workflow:** Using **Agno (formerly Phidata)** and **LangChain**, we've deployed specialized AI agents that collaborate to analyze policy documents against new guidelines.
* **RAG Pipeline:** The assistant uses a RAG (Retrieval-Augmented Generation) architecture to provide grounded, fact-based answers derived directly from the uploaded compliance documents.

---

## 🚀 Getting Started

### Prerequisites
* **Node.js** (v18 or higher)
* **Python** (v3.9 or higher)
* **MongoDB** (Local or Atlas)
* API Keys for: **DeepSeek/Llama** (via Groq/OpenRouter), **Cloudinary**, and **Crawl4AI**.

### Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/RajanVadhavana/PDPU-Economania-Hackathon.git](https://github.com/RajanVadhavana/PDPU-Economania-Hackathon.git)
   cd PDPU-Economania-Hackathon
2. **Backend Setup (FastAPI):**
    ```bash
    cd backend
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    pip install -r requirements.txt
    # Create a .env file and add your credentials
    python main.py
2. **Frontend Setup (Next.js):**
    ```bash
    cd frontend
    npm install
    # Add your Backend URL to the .env.local file
    npm run dev

Layer	Technologies Used
Frontend	Next.js (TypeScript), React, Streamlit (POC)
Backend	Node.js, Express, FastAPI
Database	MongoDB, Cloudinary, FAISS (Vector Store)
AI/LLMs	DeepSeek, Qwen, Gemma, Llama
Orchestration	Agno, LangChain, Crawl4AI

👥 The Team

This project was built and refined by:

    Dhyey Upadhyay
    Krish Vaghasia
    Nisarg Vashi
    Rajan Vadhavana
    Tanvi Madani

📈 Project Impact

By transitioning from manual audits to an automated system, financial institutions can significantly reduce the "window of risk" between a regulation being published and a policy being updated. This tool doesn't just find errors—it provides the insights necessary to fix them before they result in a penalty.
