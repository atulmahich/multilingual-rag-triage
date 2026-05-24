# multilingual-rag-triage
# 🌍 Multilingual AI Support Triage (RAG Pipeline)
**🟢 Live Interactive Demo:** [Test the application here]([YOUR_HUGGING_FACE_SPACE_URL](https://huggingface.co/spaces/Atulkumar001/Multilingual-Support-Triage/settings))

An automated Retrieval-Augmented Generation (RAG) pipeline designed to resolve customer support tickets across multiple languages without requiring manual translation.
# Multilingual AI Support Triage (RAG Pipeline)

An automated Retrieval-Augmented Generation (RAG) pipeline designed to resolve customer support tickets across multiple languages without requiring manual translation. 

## 📌 The Business Problem
European tech startups spend thousands of hours manually routing and translating customer support tickets. Traditional keyword-search knowledge bases fail when a user speaks a different language than the internal documentation.

## 💡 The Solution
This pipeline ingests unstructured support tickets in any language, performs cross-lingual semantic search against an English knowledge base, and utilizes an LLM to generate an accurate, technical response in the customer's native language. 

## 🛠️ Tech Stack
* **Data Engineering:** `Pandas`, Hugging Face `datasets`
* **Semantic Search:** `SentenceTransformers` (Multilingual MiniLM), Cosine Similarity
* **LLM Orchestration:** `huggingface_hub` (Meta-Llama-3-8B-Instruct)
* **Language:** Python

## 🧠 System Architecture
1. **Ingestion & Cleaning:** Raw data is pulled and normalized using Pandas, dropping duplicates and structuring metadata.
2. **Vectorization:** Cleaned historical resolutions are mapped into a 384-dimensional semantic space.
3. **Cross-Lingual Retrieval:** Incoming foreign-language queries are embedded and matched to the closest English resolution vector using cosine similarity.
4. **Generation:** Llama-3 synthesizes the retrieved internal document into a polite, customer-facing email in the original language.

## 🚀 How to Run Locally
1. Clone the repository:
  git clone [https://github.com/yourusername/multilingual-rag-triage.git](https://github.com/yourusername/multilingual-rag-triage.git)
2. Install dependencies:
  pip install -r requirements.txt
3. Export your Hugging Face Token:
  export HF_TOKEN="your_token_here"
4. Run the pipeline:
  python main.py


1. Clone the repository:
```bash
   git clone [https://github.com/yourusername/multilingual-rag-triage.git](https://github.com/yourusername/multilingual-rag-triage.git)
