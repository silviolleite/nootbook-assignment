# Agentic Router — Notebook Assignment

Extension of the [Agentic Router notebook](https://github.com/hamzafarooq/multi-agent-course/blob/main/modules/Module_3_Production_Agentic_RAG_AI_Systems/001.%20Agentic%20Router.ipynb) with two additions:

- **Part 1 (required):** Sub-query division with concurrent routing and citation synthesis.
- **Bonus:** RBAC-aware semantic caching with FAISS.

## Requirements

- Python 3.10+
- `git` on PATH — the pre-built Qdrant collections (`Agentic_RAG/qdrant_data`) are sparse-cloned from the course repo on first run.

## Setup

Install dependencies:

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

Set API keys via `.env`:

```bash
cp .env-example .env
# edit .env with your keys
```

Or export them directly:

```bash
export OPENAI_API_KEY="sk-..."
export TAVILY_API_KEY="tvly-..."
```

## Running

```bash
jupyter notebook agentic_router.ipynb
```

The Qdrant data is downloaded automatically on first run, locally or on **Google Colab**.

## Notebook structure

| Section | Description |
|---|---|
| 1. Internet Tool | Tavily-based web search |
| 2. Router | LLM-based query classification |
| 3. Qdrant | Vector DB setup |
| 4. Embeddings | `nomic-ai/nomic-embed-text-v1.5` |
| 5. RAG Generator | Retrieval + grounded response |
| 6. Agentic RAG | Single-query orchestrator |
| 7. RBAC | Role-based access control |
| Part 1 | `agentic_rag_multi` — sub-query division |
| Bonus | `RoleAwareSemanticCache` + `secure_agentic_rag_cached` |
| Self-Check | `run_self_check()` — 6 assertions |
