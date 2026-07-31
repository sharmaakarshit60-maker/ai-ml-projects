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
