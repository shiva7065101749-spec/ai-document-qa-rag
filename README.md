# AI Document Q&A App (RAG)

Upload a PDF and ask questions about it. Answers are generated from the document's content using Retrieval-Augmented Generation (RAG), with a local LLM, so no paid API key is needed.

## Tech Stack
- Python, Streamlit
- LangChain (PDF loading, text splitting)
- Hugging Face embeddings (all-MiniLM-L6-v2)
- ChromaDB (vector store)
- Ollama with DeepSeek-R1 (8B), running locally

## How It Works
1. Upload a PDF in the sidebar.
2. The PDF is split into chunks (500 characters, 50 overlap) and converted to embeddings.
3. The top 2 most relevant chunks are retrieved for each question.
4. The LLM answers using only the retrieved context.

## How to Run
1. Install Ollama and run: `ollama pull deepseek-r1:8b`
2. Install dependencies: `pip install streamlit langchain-community langchain-text-splitters chromadb sentence-transformers pypdf`
3. Start the app: `streamlit run app.py`

## Author
Shiva Kumar | linkedin.com/in/shiva-kumar-270b20245
