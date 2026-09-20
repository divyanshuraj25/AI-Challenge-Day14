# 🔍 Day 14: Semantic Search Engine with FAISS & Vector Embeddings

This repository demonstrates the architecture of a high-performance **Semantic Search Engine** powered by **FAISS (Facebook AI Similarity Search)** and dense vector embeddings, evaluated against a lexical keyword-matching baseline.

---

## 🚀 Key Features Built
- **50-Document Knowledge Base:** Spanning technology, health, finance, gastronomy, and nature domains.
- **Dense Embedding Generation:** Compact continuous vector representation using transformer architecture (`all-MiniLM-L6-v2`, 384 dimensions).
- **FAISS Vector Index:** Built an `IndexFlatIP` (normalized inner product / cosine similarity) index holding all 50 float32 document coordinates.
- **Side-by-Side Benchmark:** Ran 10 real-world queries comparing intent-based vector retrieval against word-overlap lexical search.
- **Production Architecture Trade-off Analysis:** Documented indexing latency, query speed, memory footprint, and hybrid search paradigms.

---

## 📊 Keyword Search vs Semantic Search (Sample Findings)
- **Vocabulary Mismatch Victory (Semantic):** Query *"How to treat muscular exhaustion and fatigue?"* accurately retrieved *"Cold plunge water immersion speeds up athletic recovery after heavy exercise"* despite zero keyword overlap.
- **Exact Token Precision (Keyword):** Query *"PostgreSQL relational database"* retrieved exact system specifications without semantic drift.
