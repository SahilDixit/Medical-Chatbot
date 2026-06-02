# Medical-Chatbot
#  Medical Chatbot using RAG, Groq, and Pinecone

A Retrieval-Augmented Generation (RAG) based Medical Chatbot that answers medical questions using information retrieved from a medical knowledge base. The application uses LangChain for orchestration, Hugging Face embeddings for semantic search, Pinecone as the vector database, and Groq-hosted Llama models for fast inference.

##  Features

* PDF-based medical knowledge ingestion
* Automatic document chunking and preprocessing
* Semantic search using vector embeddings
* Pinecone vector database integration
* Groq-powered LLM responses
* Retrieval-Augmented Generation (RAG) pipeline
* Source-aware question answering
* Fast and scalable architecture

##  Tech Stack

* Python
* LangChain
* Groq (Llama 3.3 70B)
* Pinecone
* Hugging Face Embeddings
* Sentence Transformers
* PyPDF
* Jupyter Notebook

## Project Structure

Medical-Chatbot/
│
├── data/
│   └── Medical_book.pdf
│
├── research/
│   └── trials.ipynb
│
├── src/
│   ├── __init__.py
│   ├── helper.py
│   └── prompt.py
│
├── static/
├── templates/
│
├── app.py
├── main.py
├── store_index.py
│
├── requirements.txt
├── pyproject.toml
├── setup.py
├── README.md
├── LICENSE
└── uv.lock

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

Create a virtual environment:

```bash
uv venv medical-chatbot-env --python 3.11
```

Activate it:

```bash
medical-chatbot-env\Scripts\activate
```

Install dependencies:

```bash
uv pip install -r requirements.txt
```

##  Environment Variables

Create a `.env` file in the project root:

```env
PINECONE_API_KEY=your_pinecone_api_key
GROQ_API_KEY=your_groq_api_key
```

##  Data Processing Pipeline

1. Load medical PDF documents
2. Extract document text
3. Split text into chunks
4. Generate embeddings using Hugging Face
5. Store embeddings in Pinecone
6. Retrieve relevant chunks based on user queries
7. Generate responses using Groq Llama models

##  Embedding Model

```text
sentence-transformers/all-MiniLM-L6-v2
```

* Embedding Dimension: 384
* Lightweight and efficient
* Suitable for semantic search applications

##  Retrieval Pipeline

```text
User Query
    ↓
Embedding Generation
    ↓
Pinecone Similarity Search
    ↓
Top-k Relevant Chunks
    ↓
Groq LLM
    ↓
Final Response
```

##  Example Query

```text
What is Acromegaly and Gigantism?
```

##  Future Improvements

* Streamlit frontend
* Conversation memory
* Multi-document retrieval
* Medical citation support
* Hybrid search (BM25 + Vector Search)
* Docker deployment

##  Author

Sahil Dixit

Electrical and Electronics Engineering
BITS Pilani, Hyderabad Campus



```
```
