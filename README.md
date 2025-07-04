# 🧠 Chess QA Agent (RAG-Based)
A Retrieval-Augmented Generation (RAG) AI agent that answers questions about chess using a hybrid of semantic search and generative AI.

## 🧩 Tech Stack
- Vector Store: Pinecone

- Embedding Model: all-MiniLM-L6-v2 (Hugging Face Transformers)

- LLM Backend: Google Gemini API

- Frameworks: Python, FastAPI/Flask (optional), Langchain (optional)

## ⚙️ How It Works
### Data Ingestion:

- Parse chess-related content (books, articles, PGNs).

- Generate embeddings via all-MiniLM-L6-v2.

### Indexing:

- Store vector embeddings in Pinecone with metadata.

### Query Flow:

- User inputs a natural language chess question.

- Embed the query using the same MiniLM model.

- Search Pinecone for top-k relevant chunks.

- Pass retrieved context + query to Gemini via a prompt template.

- Return generated answer to the user.
