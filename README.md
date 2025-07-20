# llm-rag-failure-brave-containers

# Case Study: LLM Retrieval Failure on Brave's "Enable Containers" Flag

> **Author**: Yzz  
> **License**: Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 (CC BY-NC-ND 4.0) 
> **Purpose**: Research-only, not for commercial redistribution or derivative publication without consent.

---

## Summary

This case study explores a rare and insightful failure mode in retrieval-augmented language models (RAG-based LLMs). Specifically, it documents how Perplexity Labs' assistant failed to acknowledge a real, verifiable Brave Browser flag—`Enable Containers`—despite its existence in the browser binary and interface.

This error was not due to hallucination, but rather a **cascade failure involving retrieval latency, semantic misclassification, and internal suppression of speculative logic**.

---

## What Happened

- I queried the existence of `"Enable Containers"` in Brave.
- The assistant concluded the flag does not exist, suggesting alternative features (profiles, Docker, etc.).
- In reality, the `Enable Containers` flag **does exist** and allows for Firefox-like containerized tab browsing inside Brave.

This misclassification is not just an oversight—it reveals a deep failure vector in modern AI systems that rely on:
- Outdated or incomplete search indexes
- High-confidence filtering over low-confidence reasoning
- Literal interpretation suppression in the presence of ambiguity

---

## Target Audience

- AI researchers in retrieval, RAG pipelines, and safety tuning
- QA testers exploring edge-case model failures
- Observability engineers auditing hallucination boundaries
- Developers interested in browser security and experimental feature discovery

---

## 🧪 Reproduce the Bug

See [`04_reproduction_instructions.md`](case-study/04_reproduction_instructions.md)

---

## 📁 Contents

| File | Purpose |
|------|---------|
| `01_summary.md` | High-level overview |
| `02_prompt_trace.md` | Exact user input and assistant response |
| `03_failure_analysis.md` | Deep analysis of model behavior and root causes |
| `04_reproduction_instructions.md` | Guide to replicate the event |
| `05_implications.md` | What this teaches us about AI observability |
| `test-prompts/` | Input variations for testing other models |
| `assets/` | Screenshots and proof of the flag's existence |

---

## Attribution & Use

> This case was discovered, verified, and compiled by **Yzz**.  
> Please do not repackage or rebrand this research without permission.  
> This is a contribution to the open AI observability ecosystem.  

If used in academic or technical papers, please cite appropriately.

---
