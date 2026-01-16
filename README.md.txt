%%writefile README.md
# PropertyLoop RAG Chatbot

This project is a chatbot built using two provided CSV files:
- `holdings.csv`
- `trades.csv`

The chatbot answers questions strictly based on the provided files.  
If the answer is not found in the files, it returns:

**"Sorry can not find the answer"**

---

## ✅ Features
- CSV-based chatbot using Retrieval-Augmented Generation (RAG)
- Semantic search with FAISS vector database
- HuggingFace sentence-transformer embeddings
- Groq LLaMA model integration
- Safe fallback to prevent hallucinations
- Optional interactive UI using `ipywidgets`

---

## 📌 How it Works
1. CSV files are loaded using Pandas.
2. Data is converted into text format for retrieval.
3. Text is chunked and stored as embeddings in FAISS.
4. The chatbot retrieves relevant context and generates answers using the LLM.
5. If data is missing, it returns the fallback response.

---

## ▶️ How to Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
