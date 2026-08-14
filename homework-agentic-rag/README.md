# Text Search & Agentic RAG

Knowledge base: course lesson markdown pages (pulled directly from
GitHub at a pinned commit), not the FAQ dataset used in the lessons —
so no pre-written Q&A pairs to search against, only lesson prose.

## What's here

- Fetching lesson `.md` files from a GitHub repo at a specific commit
- Chunking long lesson pages into smaller, indexable pieces
- Indexing chunks with minsearch (`content` as text field, `filename`
  as keyword field)
- Adapting a RAG helper class written for a `question`/`answer`/
  `section` schema to work with `filename`/`content` instead
- Measuring how chunking reduces LLM input token usage vs. sending
  whole pages
- Making the pipeline agentic: giving the LLM a `search` tool and
  letting it decide when and what to search, instead of a fixed
  one-shot retrieval step

## Setup
```bash
uv add gitsource minsearch openai python-dotenv toyaikit
```
Requires an `OPENAI_API_KEY` in a `.env` file.

## Run
Open `homework_agentic_rag.ipynb`.