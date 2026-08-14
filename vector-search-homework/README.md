# Vector & Hybrid Search

Same lesson-page knowledge base as the text search homework, this
time embedded and searched by meaning rather than keyword.

## What's here

- Embedding text with a lightweight ONNX `Embedder` (the ONNX
  runtime version of `all-MiniLM-L6-v2` — no PyTorch/CUDA needed)
- Similarity search by dot product, computed by hand and via
  minsearch's `VectorSearch`
- Batch-encoding chunked lesson content into a vector matrix
- Combining keyword search and vector search results with
  Reciprocal Rank Fusion (RRF) — the top-ranked result after fusion
  wasn't the top result in *either* search method individually; it
  won by ranking well in both

## Setup
```bash
uv add onnxruntime tokenizers numpy tqdm minsearch gitsource
uv add --dev huggingface-hub jupyter
uv run python download.py
```

## Run
Open `hw.ipynb`.