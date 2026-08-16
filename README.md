# Research Paper Assistant using RAG

An end-to-end Retrieval-Augmented Generation (RAG) system that enables users to ask questions about a research paper, retrieve relevant sections from the document, and generate grounded answers using a large language model.

The project uses the **"Attention Is All You Need"** research paper as the knowledge source and combines document retrieval, semantic embeddings, vector search, and LLM-based generation.

## Problem Statement

Research papers can be long and technically dense, making it difficult to quickly locate specific information.

This project builds a research-paper assistant that can:

- Load and process a research paper
- Split the document into meaningful chunks
- Convert document chunks into semantic embeddings
- Store embeddings in a vector database
- Retrieve relevant information for a user query
- Generate answers using only retrieved context
- Provide source page references
- Summarize the complete research paper
- Extract major topics from the paper
- Evaluate retrieval and generation quality

## Knowledge Source

The system uses the research paper:

**Attention Is All You Need**

The PDF contains **15 pages** and was loaded using PyMuPDF. :contentReference[oaicite:1]{index=1}

## RAG Architecture

```text
Research Paper PDF
        ↓
PDF Document Loader
        ↓
Text Splitting
        ↓
52 Document Chunks
        ↓
Sentence-BERT Embeddings
        ↓
ChromaDB Vector Database
        ↓
MMR Retriever
        ↓
Relevant Context
        ↓
Groq LLM
        ↓
Grounded Answer
        ↓
Source Pages
