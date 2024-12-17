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
  
3. nteractive UI:
- Built a user-friendly interface with HTML and JavaScript for easy interaction.
