```
╭──────────────────────────────────────────────────────────────────╮
│                                                                  │
│   THANIGAI SINGARAVELAN SENTHIL KUMAR                            │
│   AI Researcher — LLM systems, retrieval, inference performance  │
│                                                                  │
╰──────────────────────────────────────────────────────────────────╯
```

AI Researcher at **Thanwise Ltd**. I build retrieval and inference systems around large language models, and spend most of my time finding out why they are slower than they should be.

```console
$ whoami --verbose
degree   MSc Artificial Intelligence          Distinction · avg 76
thesis   LLAMAREC                             85 / 100
models   Llama 3 8B · 70B · 3.1 8B            local, via Ollama
prior    TCS — supply chain ML                ~15% cost reduction
stack    Python · C++ · PyTorch · CUDA
located  United Kingdom
```

**[Email](mailto:thanigaisinga@gmail.com)** &nbsp;&nbsp; **[LinkedIn](https://www.linkedin.com/in/than-tsv/)** &nbsp;&nbsp; **[Portfolio](https://ThanigaiSingaravelan.github.io)**

<br />

## What I work on

Four threads, all pointing at the same question: how do you get a research result to run reliably on hardware someone can actually afford?

<table>
<tr>
<td width="50%" valign="top">

### Inference performance
Quantisation, mixed precision, batch scheduling and memory footprint. Profiling first, changing code second.

</td>
<td width="50%" valign="top">

### Retrieval architecture
Chunking strategy, embedding pipelines and evaluation harnesses that catch regressions before users do.

</td>
</tr>
<tr>
<td valign="top">

### Fine-tuning
LoRA adapters on HuggingFace Transformers, where adapting a smaller model beats reaching for a larger one.

</td>
<td valign="top">

### GPU kernels
CUDA C/C++ and Triton. Currently self-directed study, moving into the projects where it earns its place.

</td>
</tr>
</table>

<br />

## LLAMAREC &nbsp;·&nbsp; `85/100`

**[Cross-domain recommendation running entirely on local Llama 3](https://github.com/ThanigaiSingaravelan/llamrec)** — MSc dissertation, awarded Distinction.

Cross-domain recommendation usually means sending a user's entire history to a third-party API. LLAMAREC keeps every inference call on the machine: the same recommendation quality without the privacy cost, and the model explains its own ranking as it produces it.

| System | Implementation |
|:--|:--|
| **Serving** | Ollama, fully local — Llama 3 8B and 70B, plus 3.1 8B |
| **Retrieval** | RAG over multi-domain user histories: books, film, television, music |
| **Prompting** | Three strategies compared head-to-head — standard, few-shot, chain-of-thought |
| **Data** | Amazon review corpus through a vectorised NumPy/Pandas pipeline into batched embeddings |
| **Evaluation** | Reproducible harness covering both cold-start and warm-start user segments |

> ### At 70B, the bottleneck was never compute.
>
> Profiling across GPU and mixed CPU/GPU configurations, the model went memory-bound long before it saturated the arithmetic units. Most of the useful tuning turned out to be memory layout and batching — not the things I expected to be touching.

```
where the time actually went, Llama 3 70B, local

memory / bandwidth   ████████████████████████████████░░░░░░░░   saturated
compute              ██████████████░░░░░░░░░░░░░░░░░░░░░░░░░░   headroom left
```

<details>
<summary><b>Three other things that fell out of it</b></summary>

<br />

**Trade surface.** Mapped the relationship between parameter count, quantisation level and prompt strategy across consumer and workstation cards.

**Prompting isn't independent of size.** Chain-of-thought recovers a real slice of what the smaller models give up, which changes the deployment maths entirely.

**Cold-start is the payoff.** No interaction history to collaborative-filter over, but plenty of semantic signal left to reason from.

</details>

<br />

`Python` `PyTorch` `Llama 3 / 3.1` `Ollama` `RAG` `HuggingFace` `NumPy` `Pandas` `Linux`

<br />

## Experience

Research now, production before it — which is mostly why I care about the gap between the two.

<table>
<tr><td width="170" valign="top"><br /><code>Jul 2025 —<br />present</code></td><td valign="top">

### AI Researcher
Thanwise Ltd, United Kingdom

- Prototype and benchmark generative and multimodal approaches in Python and PyTorch against published baselines.
- Train, fine-tune and deploy LLM and diffusion models on GPU infrastructure, tuning inference latency, throughput and memory footprint through batching, mixed-precision execution and quantisation.
- Design RAG architectures, prompt pipelines and evaluation harnesses that carry research prototypes into production-grade components.
- Work with engineering and creative teams on architecture decisions, code review and profiling on accelerator hardware.

</td></tr>
<tr><td valign="top"><br /><code>Jul 2022 —<br />Dec 2023</code></td><td valign="top">

### Assistant Systems Engineer
Tata Consultancy Services, India

- Built ML algorithms in Python and PyTorch for supply-chain forecasting and inventory planning at Diageo and Pando, contributing a **~15% cost reduction** on the targeted workflows.
- Ran end-to-end pipelines on multi-core CPU and GPU-backed environments — high-volume datasets, tuned batch sizes, vectorised operations, memory layout for throughput.
- Integrated models into live planning, warehouse and transportation systems across distributed infrastructure.
- Owned incident analysis for ML-driven modules in production, doing root-cause work on both performance and correctness regressions.

</td></tr>
<tr><td valign="top"><br /><code>Jan 2022 —<br />Jun 2022</code></td><td valign="top">

### Systems Design Engineer
Success Point Overseas Education Consultancy, India

- Built automated data-processing systems for customer analytics, applying algorithmic optimisation that improved key brand metrics by **~20%**.
- Analysed market data and prototyped algorithmic solutions — early hands-on work in software design, profiling and iterative optimisation.

</td></tr>
</table>

<br />

## Stack

Tools I reach for without looking them up.

| | |
|:--|:--|
| **Languages** | Python, C++, C, Java, SQL, PL/SQL |
| **Deep learning** | PyTorch (CUDA backend), HuggingFace Transformers, LoRA fine-tuning, scikit-learn, NumPy, Pandas, Ollama |
| **GPU & parallel** | Multi-GPU LLM inference, model and data parallelism, mixed-precision training, quantisation, performance profiling, memory optimisation |
| **Systems** | Algorithm design and analysis, graph algorithms, distributed systems, real-time systems, sensor fusion, SLAM, 3D reconstruction |
| **Platforms** | Linux, Git, Docker, Microsoft Azure (AZ-104), ROS, Agile and Scrum |

<br />

## Education

<table>
<tr>
<td width="50%" valign="top">

### MSc Artificial Intelligence and Mobile Robots
De Montfort University, Leicester — **Distinction**

```
Project / dissertation      85
Neural Systems & NLP        78
Research Methods            77
Classification average      76
```

</td>
<td width="50%" valign="top">

### BTech Information Technology
Anna University, India — **First Class with Distinction**

Four years of fundamentals: data structures, algorithms, databases and systems programming, which is still the part I lean on most.

</td>
</tr>
</table>

<details>
<summary><b>Certifications</b></summary>

<br />

Generative AI (Professional) · IBM Artificial Intelligence · Microsoft Azure Administrator AZ-104 · Deep Learning & Machine Learning (NPTEL) · Computer Vision and Image Processing · Robot Operating System (ROS) · Agile Scrum & Kanban

</details>

<br />

## Tell me what's running slowly.

I'm happy to talk about inference optimisation, retrieval design, or anything sitting between AI research and systems engineering. Roles, collaborations and good questions all welcome.

```
→  thanigaisinga@gmail.com
→  linkedin.com/in/than-tsv
→  github.com/ThanigaiSingaravelan
```
