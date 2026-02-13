# 📄 DocChat AI  
### Multi-Agent Hybrid RAG System for Verified Document Intelligence

DocChat AI is an advanced **multi-agent Retrieval-Augmented Generation (RAG)** system designed to extract precise, source-grounded answers from long and complex documents.

Unlike traditional single-LLM chatbots, DocChat combines **hybrid retrieval, multi-agent reasoning, and verification-driven self-correction** to minimize hallucinations and ensure factual accuracy.

---

## 🚀 Key Features

- 📂 Upload and analyze long PDFs, reports, and structured documents  
- 🔍 Hybrid Retrieval (BM25 + Vector Search)  
- 🤖 Multi-Agent Architecture (Research + Verification Agents)  
- ✅ Hallucination Detection & Self-Correction Loop  
- 📊 Handles dense text, tables, and multi-document inputs  
- 🚨 Irrelevance detection for out-of-scope queries  
- 🌐 Interactive Gradio-based UI  

---
## 🛠️ Tech Stack

- **Docling** – Handles document ingestion, parsing, structured data extraction, and intelligent chunking of PDFs and complex documents (including tables and dense text).

- **LangGraph** – Orchestrates the multi-agent workflow, enabling structured state management and controlled collaboration between the Research Agent, Verification Agent, and self-correction loop.

- **ChromaDB** – Vector database used for storing embeddings and performing efficient semantic similarity search across document chunks.

- **LangChain (RAG Pipeline)** – Implements retrieval-augmented generation by integrating retrievers, prompt templates, and LLM-based reasoning into a unified pipeline.

- **Gradio** – Builds the interactive web interface for document upload, querying, and displaying verified responses.

- **IBM watsonx.ai** – Provides access to foundation models used for answer generation, reasoning, and verification within the multi-agent system.

## 🏗️ System Architecture

DocChat follows a **verification-driven multi-agent pipeline**:

### 1️⃣ Hybrid Retriever
- Combines **BM25 keyword search** and **vector embeddings**
- Retrieves the most relevant document chunks

### 2️⃣ Research Agent
- Analyzes retrieved content
- Generates initial document-grounded response

### 3️⃣ Verification Agent
- Cross-checks generated response against source chunks
- Detects hallucinations or unsupported claims

### 4️⃣ Self-Correction Mechanism
- Re-runs the research step if contradictions are detected
- Ensures factual consistency before final output

---
## 🎥 Demo Video

Click below to watch the project demo:

[▶️ Watch DocChat Demo](./docchat-demo.mp4)

In the demo video above, DocChat was tested with two documents. The first is the Google 2024 Environmental Report, a large document spanning 86 pages with numerous images and tables. The second is the DeepSeek-R1 Technical Report, which, while not as extensive as the first, still contains a significant number of diagrams and tables.

As demonstrated, DocChat accurately retrieves relevant answers from both documents. Below, you can see the extracted portions containing the correct information. You can also check these documents out yourselves to verify the information.

## 🧠 Why Not a Single LLM?

Traditional chatbots:
- Struggle with long documents  
- Misinterpret structured tables  
- Fabricate citations  
- Lack document-aware reasoning  

DocChat solves this with:
- Retrieval grounding  
- Multi-step validation  
- Agent-based reasoning  
- Explicit hallucination checks  

---


---

## ⚙️ Installation

```bash
git clone https://github.com/your-username/DocChat-AI.git
cd DocChat-AI
pip install -r requirements.txt

```
## ▶️ Run the Application

```bash
python app.py
```
## 📌 Use Cases

- Research paper analysis  
- Legal contract review  
- Technical documentation Q&A  
- Environmental and compliance reports  
- Multi-document comparison  

---

## 🎯 Learning Outcomes

This project demonstrates:

- Advanced RAG architecture design  
- Hybrid retrieval implementation  
- Multi-agent orchestration  
- Hallucination detection pipeline  
- Verification-based AI reasoning  
- Production-ready AI system structuring  
