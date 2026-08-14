# LLM Zoomcamp — Applied RAG & Search

Hands-on work from DataTalksClub's LLM Zoomcamp, covering the full RAG
pipeline built from scratch — keyword search, vector/semantic search,
hybrid retrieval, and agentic tool-calling — without relying on a
framework, to understand what's actually happening at each step.

## Contents

- [`homework-agentic-rag/`](./homework-agentic-rag) — **Text search & agentic RAG.**
  Keyword search over course lesson content with minsearch, document
  chunking, a RAG pipeline adapted from a Q&A schema to raw lesson
  text, token-usage measurement, and turning a fixed search→answer
  pipeline into an agentic one where the LLM decides when and what
  to search via tool-calling.

- [`vector-search-homework/`](./vector-search-homework) — **Vector & hybrid search.**
  Embedding text with a lightweight ONNX runtime (no PyTorch/CUDA),
  similarity search by dot product (by hand and via minsearch's
  `VectorSearch`), and combining keyword + vector search results
  with Reciprocal Rank Fusion (RRF).

- [`02-vector-Search/`](./02-vector-Search) — lesson notebooks from
  the vector search module (sentence-transformers, persistent
  storage, pgvector).

## Stack
Python, minsearch, ONNX Runtime, OpenAI API, toyaikit, uv

## Course
[DataTalksClub LLM Zoomcamp](https://github.com/DataTalksClub/llm-zoomcamp)