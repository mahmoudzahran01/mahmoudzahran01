### Mahmoud Zahran — AI/ML Engineer

I build production LLM systems for Arabic and English: retrieval and RAG, text-to-SQL agents, document AI, fine-tuning and GPU inference — with evaluation that decides what ships.

Currently **Software Engineer (AI) at [Qubit](https://qubit.sa)** (KAUST TAQADAM 2026 winner), an AI decision-intelligence platform for enterprise and government clients. MSc Computer Science, KAUST (GPA 3.9). BSc Computer Science, University of Maryland (Magna Cum Laude).

[LinkedIn](https://www.linkedin.com/in/mahmoudzahran01) · [Email](mailto:mahmoudzahran.2001@gmail.com) · Riyadh, Saudi Arabia

---

#### What I've shipped

- **Bilingual RAG** — Arabic/English retrieval with hybrid search and cross-encoder reranking at 88% Hit@5; kept Arabic dense-only after an ablation showed fusion hurt Arabic ranking.
- **Document AI** — benchmarked 10+ OCR engines and VLMs on Arabic documents, fine-tuned an Arabic text recognizer, shipped self-hosted extraction; key-value accuracy 32% → 95%.
- **Text-to-SQL agents** — tool-calling agents with dialect-aware SQL; a semantic profiler that lifted metric recall from 29% to 94%, and a bilingual benchmark that gates every model launch.
- **Grounding** — a fact-check layer that re-runs live SQL behind every figure in a generated report.
- **Agentic workflows** — an automation engine with loops, branches, HTTP nodes, run budgets and streaming; tests grown from 19 to 264.

*Production code is proprietary. The projects below are public; where an evaluation set is private, the repo says so.*

#### Projects

| Project | Result |
|---|---|
| **[Bilingual text-to-SQL model](https://github.com/mahmoudzahran01/bilingual-text-to-sql)** — QLoRA distillation of two larger teachers into a 4B model, synthetic pairs kept only when both teachers' SQL returned the same rows | Execution accuracy **56% → 86%**, eight significance-tested ablations, 2.5 GB INT4 build with no accuracy loss |
| **[LLM inference and GPU serving](https://github.com/mahmoudzahran01/llm-gpu-serving)** — vLLM on GPU Kubernetes (Helm, device plugin), OpenTelemetry tracing, SLO alerts | Prefix caching **13x** faster first token, speculative decoding **2.2x**, INT4 **3x** smaller and faster |
| **[Arabic–English retrieval models](https://github.com/mahmoudzahran01/arabic-english-retrieval-eval)** — fine-tuned bge-m3 and distilled [e5-base](https://huggingface.co/mzahran1/arabic-english-e5-base-retrieval) / [e5-small](https://huggingface.co/mzahran1/arabic-english-e5-small-retrieval-v2) embedders ([v2-m3](https://huggingface.co/mzahran1/arabic-english-bge-m3-retrieval)), a [reranker](https://huggingface.co/mzahran1/arabic-english-reranker-mminilm), calibrated LLM judges, pre-registered model selection, contamination audit, [technical report](https://github.com/mahmoudzahran01/arabic-english-retrieval-eval/blob/main/report/main.pdf) | Arabic→English MRR@10 **63 → 71** over bge-m3 (5 seeds); small models **+17 to +18** over their base; highest ≤300M score among 10 models on a 19-task Arabic benchmark; LLM-judge agreement κ **0.42 → 0.97** |

#### Open source

- **MTEB** (the standard embedding leaderboard): proposed **MTEB(ara)**, a 19-task Arabic benchmark built from a review of all 103 Arabic tasks ([issue #5845](https://github.com/embeddings-benchmark/mteb/issues/5845)); model registered in MTEB (PR [#5846](https://github.com/embeddings-benchmark/mteb/pull/5846), merged); found broken qrels in MLQA ara-deu and that 89% of MIRACL-Arabic dev queries are copies of TyDi-QA train questions.

#### Research

- **TACTIC** — co-first author, ICML 2025 GenBio Workshop ([paper](https://openreview.net/forum?id=pc9NrFL0CT)): multi-agent LLM and graph-autoencoder pipeline for cell-type annotation.
- **SPELL** — co-author, ICLR 2025 MLGenX Workshop ([paper](https://openreview.net/forum?id=Sh88LK85AR)): chain-of-thought prompting for zero-shot cell typing.
- **Frozen LLM Priors** — co-author, submitted to *Nature Biotechnology* ([code](https://github.com/mahmoudzahran01/frozen-llm-priors-spatial-transcriptomics)).

#### Skills

| Area | Tools and techniques |
|---|---|
| LLMs & agents | LangGraph, LangChain, tool calling, multi-agent systems, MCP, structured outputs, prompt engineering |
| Fine-tuning | PyTorch, Transformers, TRL (SFT, GRPO), PEFT (LoRA, QLoRA), distillation, synthetic data |
| Inference | vLLM, llama.cpp, speculative decoding, prefix caching, quantization (FP8, GPTQ, NVFP4, GGUF) |
| Retrieval | RAG, chunking, sentence-transformers, hard-negative mining, rerankers, Qdrant, hybrid search |
| Evaluation | LLM-as-judge, judge calibration, Ragas, hallucination detection, execution grading, A/B testing |
| LLMOps | Docker, Kubernetes, Helm, GPU scheduling, CI/CD, OpenTelemetry, Prometheus, Grafana |
| Document AI | Arabic NLP, OCR pipelines, PaddleOCR, Tesseract, pdfplumber, VLM-based OCR |
| Backend & data | Python, FastAPI, Pydantic, SQLAlchemy, sqlglot, pandas, PostgreSQL, ClickHouse, Redis |

Languages: Arabic (native), English (fluent).
