# AI/ML Projects — Hands-on Portfolio

Practical AI/ML projects built from scratch using open-source models on Google Colab (free GPU).

## Projects

### 1. QLoRA Fine-Tuning — Coding Assistant
Fine-tuned Qwen2.5-1.5B-Instruct on a custom dataset of 8 coding Q&A examples using QLoRA.

**What I did:**
- Built a training dataset with a consistent code + explanation style
- Configured a LoRA adapter (r=8) targeting attention layers (q_proj, v_proj)
- Diagnosed underfitting after 3 epochs, retrained for 15 epochs (loss dropped from ~2.1 to ~0.5)
- Verified style transfer on held-out questions using disable_adapter() comparison

**Stack:** Python, Hugging Face Transformers, PEFT, Google Colab (T4 GPU)

---

### 2. RAG Pipeline + Hallucination Checking
Built a Retrieval-Augmented Generation system that answers questions from a document store — and says "I don't know" when the answer isn't available.

**What I did:**
- Embedded 8 documents using sentence-transformers (all-MiniLM-L6-v2, 384-dim embeddings)
- Built a FAISS vector index for fast meaning-based search
- Connected retrieval to Qwen2.5 generation with a grounding prompt
- Verified hallucination resistance: model said "I don't know" for questions outside the knowledge base

**Stack:** Python, sentence-transformers, FAISS, Hugging Face Transformers, Google Colab

---

## Key Skills Demonstrated
- QLoRA fine-tuning on open-source LLMs
- RAG pipeline design and evaluation
- Hallucination detection and grounding
- Iterative debugging (diagnosing underfitting, fixing and retesting)

## About
Built as part of a structured AI/ML learning track targeting Applied AI / Forward Deployed Engineer roles.
---

### 3. MCP Travel Agent — Multi-Tool AI Agent

A multi-tool AI agent using Claude's tool-use API (the pattern that powers MCP). Ask one travel question and Claude automatically calls three tools — weather checker, flight cost estimator, currency converter — then combines all results into one natural answer.

**What I built:**
- `convert_currency` — converts between USD, INR, EUR, GBP, JPY
- `get_weather` — returns weather for major cities
- `estimate_flight_cost` — estimates flight cost between cities
- Agent loop — `while stop_reason == "tool_use"` keeps firing tools until Claude has everything it needs

**Stack:** Python, Claude Haiku API, Tool Use / MCP pattern, Google Colab

**File:** `mcp_travel_agent.ipynb`

---

## Key Skills Demonstrated
- QLoRA fine-tuning on open-source LLMs
- RAG pipeline design and evaluation
- Hallucination detection and grounding
- Multi-tool AI agent development with MCP pattern
- Iterative debugging (diagnosing underfitting, fixing and retesting)
