# Thanigai Singaravelan Senthil Kumar

**AI Researcher @ Thanwise Ltd** — LLM systems, retrieval architectures, and GPU-side inference performance.
MSc Artificial Intelligence & Mobile Robots (Distinction), De Montfort University.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-than--tsv-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/than-tsv/)
[![Email](https://img.shields.io/badge/Email-thanigaisinga@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:thanigaisinga@gmail.com)
![Location](https://img.shields.io/badge/UK-555?style=flat-square)

---

## Current focus

```
├── inference/        quantisation · mixed precision · KV-cache behaviour · batch scheduling
├── retrieval/        chunking strategy · embedding pipelines · reranking · eval harnesses
├── finetuning/       LoRA / PEFT adapters on HuggingFace Transformers
├── multimodal/       prototyping + benchmarking against published baselines
└── kernels/          CUDA C/C++ and Triton — currently self-directed, moving into projects
```

Day to day that means: train, fine-tune and deploy LLM and diffusion models on GPU infrastructure; profile latency, throughput and memory footprint; and turn research prototypes into components that hold up under production traffic.

---

## Featured: [LLAMAREC](https://github.com/ThanigaiSingaravelan/llamrec)

Cross-domain recommendation via locally-deployed Llama 3 — MSc dissertation, Distinction (85/100).

**Problem.** Cross-domain recommendation normally means shipping user histories to a third-party API. LLAMAREC keeps inference entirely local, so the recommendation quality is bought without the privacy cost — and it stays explainable, since the model emits its reasoning alongside the ranking.

**Architecture**

| Layer | Implementation |
|---|---|
| Serving | Ollama, local — Llama 3 8B / 70B and 3.1 8B |
| Retrieval | RAG over multi-domain user histories (books · film · TV · music) |
| Prompting | Three strategies compared head-to-head: standard, few-shot, chain-of-thought |
| Data | Amazon review corpus → vectorised NumPy/Pandas pipeline → batched embedding generation |
| Eval | Reproducible harness across cold-start and warm-start user segments |

**Engineering notes**
- Inference profiled across GPU and mixed CPU/GPU configurations; measured the trade surface between parameter count, quantisation level and prompt strategy on both consumer and workstation cards
- 70B at local precision is memory-bound well before it is compute-bound — most of the tuning work was memory layout and batching, not FLOPs
- Prompt strategy and model size are not independent: chain-of-thought recovers a meaningful slice of what the smaller models lose, which changes the cost calculus

`Python` · `PyTorch` · `Llama 3 / 3.1` · `Ollama` · `RAG` · `HuggingFace` · `NumPy` · `Pandas` · `Linux`

---

## Stack

**Languages** `Python` `C++` `C` `Java` `SQL` `PL/SQL`

**Deep learning** PyTorch (CUDA backend) · HuggingFace Transformers · LoRA fine-tuning · scikit-learn · NumPy · Pandas · Ollama

**Parallel & GPU** multi-GPU LLM inference · model and data parallelism · mixed-precision training · quantisation · performance profiling · memory optimisation

**Systems** algorithm design & analysis · graph algorithms · distributed systems · real-time systems · sensor fusion · SLAM · 3D reconstruction

**Platforms** Linux · Git · Docker · Azure (AZ-104) · ROS · Agile/Scrum

---

## Prior work

**Tata Consultancy Services** — Assistant Systems Engineer · Jul 2022 – Dec 2023

- ML algorithms in Python/PyTorch for supply-chain forecasting and inventory planning (Diageo, Pando) — ~15% cost reduction on targeted workflows
- End-to-end pipelines on multi-core CPU and GPU-backed environments; high-volume datasets, tuned batch sizes, vectorised ops, memory layout for throughput
- Integrated models into live planning, warehouse and transportation systems across distributed infrastructure
- Owned incident analysis for ML-driven modules in production — root-cause work on both performance and correctness regressions

**Success Point Overseas Education Consultancy** — Systems Design Engineer · Jan 2022 – Jun 2022
Automated customer-analytics processing; algorithmic optimisation improving key brand metrics ~20%.

---

## Also in the toolbox

- C++ and Python for mobile robotics: real-time perception, SLAM, sensor fusion — efficient data structures and tight inner loops
- CNNs and transformers from the ground up; object detection and 3D reconstruction coursework
- Extending personal projects toward custom CUDA kernels and Triton-based optimisation

---

## Education & certifications

**MSc Artificial Intelligence and Mobile Robots** — De Montfort University · Distinction (avg. 76)
Modules: Neural Systems & NLP (78) · Research Methods (77) · Fuzzy Logic & Evolutionary Computing · Project (85)

**BTech Information Technology** — Anna University · First Class with Distinction

Generative AI (Professional) · IBM Artificial Intelligence · Azure Administrator AZ-104 · Deep Learning & ML (NPTEL) · Computer Vision and Image Processing · ROS · Agile Scrum & Kanban

---


Open to talking about inference optimisation, RAG design, or anything where AI research meets systems engineering — [get in touch](mailto:thanigaisinga@gmail.com).
