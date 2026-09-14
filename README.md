<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0b0f1a,50:1a2740,100:2d6cdf&height=190&section=header&text=Thanigai%20Singaravelan&fontSize=42&fontColor=ffffff&fontAlignY=34&desc=AI%20Researcher%20%C2%B7%20LLM%20Systems%20%C2%B7%20GPU%20Inference&descSize=16&descAlignY=54" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&pause=1200&color=2D6CDF&center=true&vCenter=true&width=560&lines=Retrieval-augmented+generation+at+the+edge;Profiling+LLMs+until+they+stop+being+memory-bound;MSc+Artificial+Intelligence+%E2%80%94+Distinction;Currently+learning+CUDA+the+hard+way" alt="typing" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-than--tsv-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/than-tsv/)
[![Email](https://img.shields.io/badge/Email-reach%20out-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:thanigaisinga@gmail.com)
[![Location](https://img.shields.io/badge/United%20Kingdom-1a2740?style=for-the-badge&logo=googlemaps&logoColor=white)](#)
![Profile views](https://komarev.com/ghpvc/?username=ThanigaiSingaravelan&style=for-the-badge&color=2d6cdf&label=VISITORS)

</div>

---

<img align="right" width="300" src="https://github-readme-stats.vercel.app/api?username=ThanigaiSingaravelan&show_icons=true&hide_border=true&include_all_commits=true&title_color=2d6cdf&icon_color=2d6cdf&hide_title=true" />

### `~/whoami`

**AI Researcher @ Thanwise Ltd.** I work on LLM systems — retrieval architectures, prompt pipelines, and getting models to run fast on the hardware that's actually available rather than the hardware in the paper.

Before research: ~18 months at **TCS** shipping ML into live supply-chain systems for Diageo and Pando.

Before that: **MSc Artificial Intelligence & Mobile Robots**, De Montfort University — Distinction, 76 average, 85 on the dissertation.

<br clear="right"/>

---

## 🎯 Current focus

```text
inference/     quantisation · mixed precision · KV-cache behaviour · batch scheduling
retrieval/     chunking strategy · embedding pipelines · reranking · eval harnesses
finetuning/    LoRA / PEFT adapters on HuggingFace Transformers
multimodal/    prototyping + benchmarking against published baselines
kernels/       CUDA C/C++ and Triton — self-directed, moving into real projects
```

Day to day: train, fine-tune and deploy LLM and diffusion models on GPU infrastructure; profile latency, throughput and memory footprint; turn research prototypes into components that survive production traffic.

---

## 🧪 Featured — LLAMAREC

<div align="center">

### [**Cross-Domain Recommendation via Locally-Deployed Llama 3**](https://github.com/ThanigaiSingaravelan/llamrec)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Llama](https://img.shields.io/badge/Llama%203%20%2F%203.1-0467DF?style=flat-square&logo=meta&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![HuggingFace](https://img.shields.io/badge/🤗%20Transformers-FFD21E?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

*MSc dissertation · Distinction · 85/100*

</div>

> Cross-domain recommendation normally means shipping user histories to a third-party API. LLAMAREC keeps inference entirely local — the recommendation quality without the privacy cost, and explainable, because the model emits its reasoning alongside the ranking.

| Layer | Implementation |
|:--|:--|
| **Serving** | Ollama, fully local — Llama 3 8B / 70B and 3.1 8B |
| **Retrieval** | RAG over multi-domain user histories — books · film · TV · music |
| **Prompting** | Three strategies, head-to-head: standard, few-shot, chain-of-thought |
| **Data** | Amazon review corpus → vectorised NumPy/Pandas pipeline → batched embeddings |
| **Eval** | Reproducible harness across cold-start and warm-start segments |

<details>
<summary><b>⚙️ Engineering notes</b></summary>

<br/>

- Inference profiled across GPU and mixed CPU/GPU configurations; mapped the trade surface between parameter count, quantisation level and prompt strategy on both consumer and workstation cards.
- **70B at local precision is memory-bound long before it is compute-bound.** Most of the tuning work turned out to be memory layout and batching, not FLOPs.
- Prompt strategy and model size are not independent axes — chain-of-thought recovers a meaningful slice of what the smaller models give up, which changes the cost calculus entirely.
- Cold-start is where the LLM approach earns its keep: no interaction history to collaborative-filter over, but plenty of semantic signal to reason from.

</details>

---

## 🛠 Stack

<div align="center">

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL%20%2F%20PL%2FSQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

**Deep learning & GPU**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-FFD21E?style=for-the-badge)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

**Platforms**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Azure](https://img.shields.io/badge/Azure%20AZ--104-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![ROS](https://img.shields.io/badge/ROS-22314E?style=for-the-badge&logo=ros&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</div>

**Techniques** — multi-GPU LLM inference · model & data parallelism · mixed-precision training · quantisation · performance profiling · memory optimisation · LoRA fine-tuning · RAG · prompt engineering · SLAM · sensor fusion · 3D reconstruction

---

## 💼 Track record

<details open>
<summary><b>Tata Consultancy Services</b> — Assistant Systems Engineer · <i>Jul 2022 – Dec 2023</i></summary>

<br/>

- ML algorithms in Python/PyTorch for supply-chain forecasting and inventory planning — **~15% cost reduction** on targeted workflows for Diageo and Pando
- End-to-end pipelines on multi-core CPU and GPU-backed environments; high-volume datasets, tuned batch sizes, vectorised ops, memory layout for throughput
- Integrated models into live planning, warehouse and transportation systems across distributed infrastructure
- Owned incident analysis for ML-driven modules in production — root-cause work on both performance and correctness regressions

</details>

<details>
<summary><b>Success Point Overseas Education Consultancy</b> — Systems Design Engineer · <i>Jan 2022 – Jun 2022</i></summary>

<br/>

- Automated customer-analytics processing pipelines
- Algorithmic optimisation improving key brand metrics by **~20%**

</details>

<details>
<summary><b>Elsewhere in the toolbox</b></summary>

<br/>

- C++ and Python for mobile robotics — real-time perception, SLAM, sensor fusion, with attention to data structures and tight inner loops
- CNNs and transformers built from the ground up; object detection and 3D reconstruction coursework
- Extending personal projects toward custom CUDA kernels and Triton-based optimisation

</details>

---

## 🎓 Education & credentials

<table>
<tr>
<td width="50%" valign="top">

**MSc Artificial Intelligence and Mobile Robots**
De Montfort University · **Distinction** (avg 76)

`Neural Systems & NLP — 78`
`Research Methods — 77`
`Fuzzy Logic & Evolutionary Computing`
`Dissertation — 85`

</td>
<td width="50%" valign="top">

**BTech Information Technology**
Anna University · **First Class with Distinction**

Generative AI (Professional) · IBM Artificial Intelligence · Azure AZ-104 · Deep Learning & ML (NPTEL) · Computer Vision & Image Processing · ROS · Agile Scrum & Kanban

</td>
</tr>
</table>

---

<div align="center">

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ThanigaiSingaravelan&layout=compact&hide_border=true&langs_count=8&title_color=2d6cdf" height="150" />
<img src="https://streak-stats.demolab.com?user=ThanigaiSingaravelan&hide_border=true&ring=2d6cdf&fire=2d6cdf&currStreakLabel=2d6cdf" height="150" />

<br/><br/>

**Open to conversations about inference optimisation, RAG design, or anything where AI research meets systems engineering.**

[![Say hello](https://img.shields.io/badge/Say%20hello-2d6cdf?style=for-the-badge&logo=minutemailer&logoColor=white)](mailto:thanigaisinga@gmail.com)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2d6cdf,50:1a2740,100:0b0f1a&height=110&section=footer" width="100%" />

</div>
