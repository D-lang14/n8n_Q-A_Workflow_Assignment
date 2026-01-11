# n8n_Q-A_Workflow_Assignment

## Problem
Manually looking up answers in PDFs caused delays and inconsistent outcomes.
Developing an interactive "Ask Me Anything" system for documents with little human involvement was the aim.

## Solution
Designed a compact n8n workflow that:
- Triggers on user questions
- Retrieves relevant text chunks from PDF using semantic search
- Generates concise, document-grounded answers using LLM
- Produces structured Q&A output staying within document content

## Workflow Overview
- **Trigger**: HTTP Request (user question input)
- **Data Processing**: PDF text extraction and chunking
- **Decision Logic**: Semantic similarity search for relevant chunks
- **Output**: Short answer strictly limited to retrieved document content

## Key Design Decisions
- Chose HTTP trigger for interactive "Ask Me Anything" interface
- Used semantic retrieval (RAG principles) to ground answers in document
- Structured single-path workflow for simplicity and reliability
- Limited response scope to prevent LLM hallucinations

## Limitations & Improvements
- Current workflow handles single PDF documents
- Future improvements include multi-document support, vector database integration, and citation tracking

## Tech Stack
- n8n
- PDF parsing nodes
- LLM API (for answer generation)
- Semantic search/embedding
- JSON

