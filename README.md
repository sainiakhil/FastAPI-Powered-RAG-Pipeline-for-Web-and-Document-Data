# RAG-Powered Content Processing and Chat Service with FastAPI
## Project Overview
This project implements a Retrieval-Augmented Generation (RAG) pipeline for processing web content and PDF files, enabling context-aware question-answering using FastAPI. The system integrates embeddings, a vector database, and a language model to deliver concise and relevant responses to user queries.

## Key Features
1. Content Processing:
-    Extracts text from web URLs and PDF files.
- Chunks and embeds content using Sentence Transformers.
- Stores embeddings in ChromaDB for efficient retrieval.
  
2. Contextual Chat Service:
- Performs similarity search over embedded chunks for relevant context.
- Generates answers using the Qwen-2.5-3B-Instruct model from the retrieved content.
  
3. Interactive UI:
- Built a user-friendly interface with HTML and JavaScript for easy interaction.

## Tech Stack
- Backend: FastAPI
- Embeddings: Sentence Transformers
- Language Model: Qwen-2.5-3B-Instruct (via Hugging Face Transformers)
- Vector Database: ChromaDB
- Frontend: HTML, JavaScript
- Dependencies: PyPDF2, BeautifulSoup, Requests, PyTorch, ngrok

## Endpoints
1. Serve UI:
-    GET /
-    Provides the user interface for interacting with the service.

2. Process Web Content:
-   POST /process-url
-   Input: JSON with a valid URL.
-   Action: Extracts, chunks, and stores content in the vector database.
  
3. Process PDF Content:
-  POST /process-pdf
-  Input: PDF file.
Action: Extracts, chunks, and stores PDF content.

4. Chat with Processed Content:
-    POST /chat
-    Input: Query and Source ID.
-    Action: Retrieves relevant context and generates a response.

## How It Works
1. Text Extraction:
-    Extracts content from user-provided URLs or PDF files.
  
2. Chunking and Embedding:
-    Breaks down content into manageable chunks (500 tokens).
-    Generates embeddings using Sentence Transformers.
  
3. Vector Storage:
-    Embeddings and chunks are stored in ChromaDB.

4. Similarity Search and Generation:
-    Performs a similarity search on the query embedding.
-    Retrieves top chunks, integrates context, and generates responses using Qwen-2.5-3B.

