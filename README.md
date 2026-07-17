<div align="center">

<img src="assets/hero.svg" width="100%" alt="Kunal Somani — Robotics · AI · Open Source"/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-kunal--somani-0b0f14?style=flat&logo=linkedin&logoColor=22d3ee)](https://linkedin.com/in/kunal-somani-227373344)
[![Email](https://img.shields.io/badge/Email-kunal120222%40gmail.com-0b0f14?style=flat&logo=gmail&logoColor=f59e0b)](mailto:kunal120222@gmail.com)

</div>

I work on two sides of the same problem: **AI systems** (medical imaging, multimodal fusion, LLM tooling) and the **robots that run them** (ROS 2, RL locomotion, sim-to-real). Most of what's below either ships as open source or is headed to a paper.

> 🔒 A few research repos below are private until their papers are submitted or published — links will go live with the papers.

---

## Open Source

### [trajlens](https://github.com/Kunal-Somani/trajlens) — ruff for robot data
[![Stars](https://img.shields.io/github/stars/Kunal-Somani/trajlens?style=flat&logo=github&label=stars&color=f59e0b&labelColor=0b0f14)](https://github.com/Kunal-Somani/trajlens/stargazers)
[![Release](https://img.shields.io/github/v/release/Kunal-Somani/trajlens?style=flat&color=22d3ee&labelColor=0b0f14)](https://github.com/Kunal-Somani/trajlens/releases)
[![PyPI](https://img.shields.io/pypi/v/trajlens?style=flat&label=pypi&color=34d399&labelColor=0b0f14)](https://pypi.org/project/trajlens/)

Lints **and auto-repairs** [LeRobotDataset](https://github.com/huggingface/lerobot) datasets (v2.0–v3.0) against their own declared metadata — 16 checks across structural, semantic, temporal, statistical, and video categories, with terminal / JSON / HTML / SARIF reports that drop straight into CI. v0.2 adds `trajlens fix` (timestamp de-drift, stats recompute, episode reindex — dry-run by default, copy-on-write) and `trajlens web`, a CSP-hardened localhost dashboard. `pip install trajlens`. Validated by auditing a random sample of 100 public Hugging Face Hub datasets: two known upstream `lerobot` bugs were found in **~19%** and **~3%** of successfully linted datasets.

<a href="https://github.com/Kunal-Somani/trajlens"><img src="https://raw.githubusercontent.com/Kunal-Somani/trajlens/main/docs/assets/demo.gif" width="85%" alt="trajlens lint demo"/></a>

### [bodhirax](https://github.com/Kunal-Somani/bodhirax) — local-first LLM prompt eval studio
[![Release](https://img.shields.io/github/v/release/Kunal-Somani/bodhirax?style=flat&color=22d3ee&labelColor=0b0f14)](https://github.com/Kunal-Somani/bodhirax/releases)

A visual studio for testing and comparing LLM prompts across five providers (Ollama, OpenAI, Anthropic, Groq, Hugging Face) — runs entirely on your machine, keys never leave localhost. Four metrics: exact, fuzzy, local-embedding cosine, and LLM-judge. The zero-key local path goes from clone to a scored run in under five minutes.

<a href="https://github.com/Kunal-Somani/bodhirax"><img src="https://raw.githubusercontent.com/Kunal-Somani/bodhirax/main/docs/demo.gif" width="85%" alt="bodhirax prompt eval demo"/></a>

### Upstream contributions
| Project | Contribution |
|---|---|
| [NVIDIA/NemoClaw](https://github.com/NVIDIA/NemoClaw/pulls?q=is%3Apr+author%3AKunal-Somani) | Merged security-sensitive PR — least-privilege Gmail network-policy preset, workflow docs, and semantic policy tests; shipped in v0.0.79 |
| [deepset-ai/haystack](https://github.com/deepset-ai/haystack/pulls?q=is%3Apr+author%3AKunal-Somani+is%3Amerged) + [core-integrations](https://github.com/deepset-ai/haystack-core-integrations/pulls?q=is%3Apr+author%3AKunal-Somani+is%3Amerged) | 4 merged PRs in the Haystack LLM orchestration framework |
| [JdeRobot/RoboticsAcademy](https://github.com/JdeRobot/RoboticsAcademy/pulls?q=is%3Apr+author%3AKunal-Somani+is%3Amerged) | 16 merged PRs — fixed an FP16 crash in the object-detection pipeline, refactored the Hardware Abstraction Layer, shipped 52 unit tests |

---

## Research

| Work | Area | Status |
|---|---|---|
| [MRI Reconstruction](https://github.com/Kunal-Somani/MRI_Reconstruction) — dual-branch physics-guided deep learning; learned gating routes k-space adaptively, no anatomy labels at inference. +1.78% SSIM, 112 ms/slice | Medical imaging | Conference paper under review — IEEE SPL · Dr. Anurag Tiwari, TIET |
| [ThermoBridge](https://github.com/Kunal-Somani/thermobridge) 🔒 — bidirectional 3D MRI↔CT synthesis via Brownian-bridge diffusion with a learnable 3D anisotropic-diffusion mixer | Medical imaging | Paper in preparation · Dr. Anurag Tiwari, TIET |
| Multi-Modal Sensor Fusion for SLAM in Visually Degraded SAR Environments — pipeline-oriented survey of 55 systems (2011–2025) | SAR robotics | Survey submitted · Dr. Ankit Soni, TIET |
| SAR rover — simulated multi-modal (audio-visual-thermal) search-and-rescue platform 🔒 | SAR robotics | Journal paper #2, in progress · Dr. Ankit Soni, TIET |
| [Parkinson's early detection](https://github.com/eshaansingla/ParkinsonsEarlyPrediction) — CNN on voice + DNN on MPU9250 tremor, late fusion 88% → 91%, ESP32 sensor-to-inference pipeline | Multimodal ML | ELC summer research, TIET |

---

## Robotics

### [Canary Rover](https://github.com/Kunal-Somani/canary-rover) — autonomous mine-inspection scout · capstone
PPO-trained locomotion (200K timesteps, PyBullet) → ROS 2 sensor stack (IMU / RPLiDAR / 4× BLDC encoders) → full Isaac Sim 5.1 simulation with live sensor feeds. **Currently in sim-to-real transfer; physical rover roughly half built.** Team of 5.

<a href="https://github.com/Kunal-Somani/canary-rover"><img src="assets/canary_demo.gif" width="85%" alt="Canary Rover autonomous tunnel traversal in Isaac Sim"/></a>

### [object_finder](https://github.com/Kunal-Somani/object_finder) — map-less warehouse AMR · [▶ demo video](https://github.com/user-attachments/assets/c1a75752-a5f5-46bc-b5e6-5bc591ea847e)
ROS 2 Humble skid-steer robot that navigates without SLAM: FSM + PD wall-following on 360° LiDAR, HSV + depth target tracking, tested in the AWS Small Warehouse Gazebo world.

---

## Engineering Systems

| Project | Description |
|---|---|
| [Archon](https://github.com/Kunal-Somani/archon) | • Natural-language brief → live deployed site: hybrid RAG (Cohere dense + BM25, RRF fusion) feeds grammar-constrained code generation<br>• Celery async workers, Redis Pub/Sub live WebSocket logs, GitHub App deployer with short-lived tokens, full Prometheus/Grafana/OTel observability |
| [Axon](https://github.com/Kunal-Somani/axon-core) | • Fully local tri-modal assistant (text/speech/vision): BART-MNLI zero-shot router dispatches to knowledge RAG, confirmed OS tool execution, or chat<br>• Hybrid retrieval (Qdrant dense + BM25) reranked by a cross-encoder; GBNF grammar-constrained tool calls; zero external LLM APIs |
| [TruthTag](https://github.com/Kunal-Somani/TruthTag-Toll-Audit) | • Classical CV pipeline cross-verifying RFID FASTag claims against physical vehicle geometry: 3780-dim HOG features + LinearSVC, 97% accuracy on 24K+ images<br>• Cross-modal centroid tracker with MOG2 virtual tripwire, misclassification error analysis, and a Streamlit operator audit dashboard |
---

## Tech Stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

**Robotics & Simulation**
![ROS 2](https://img.shields.io/badge/ROS_2-22314E?style=flat&logo=ros&logoColor=white)
![Isaac Sim](https://img.shields.io/badge/Isaac_Sim-76B900?style=flat&logo=nvidia&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-FF6600?style=flat&logoColor=white)
![PyBullet](https://img.shields.io/badge/PyBullet-306998?style=flat&logoColor=white)
![Stable Baselines3](https://img.shields.io/badge/Stable_Baselines3-4B8BBE?style=flat&logoColor=white)
![Gymnasium](https://img.shields.io/badge/Gymnasium-0052CC?style=flat&logoColor=white)
![NVIDIA Jetson](https://img.shields.io/badge/Jetson-76B900?style=flat&logo=nvidia&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat&logo=nvidia&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-D97615?style=flat&logo=mathworks&logoColor=white)

**AI & Computer Vision**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=PyTorch&logoColor=white)
![PyTorch Lightning](https://img.shields.io/badge/Lightning-792EE5?style=flat&logo=lightning&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=TensorFlow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat&logo=huggingface&logoColor=black)
![Haystack](https://img.shields.io/badge/Haystack-1CBC9A?style=flat&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Librosa](https://img.shields.io/badge/Librosa-000000?style=flat&logoColor=white)

**Backend, Data & Infra**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)

---

## Activity

<div align="center">

<img height="170" src="https://github-readme-stats-liard-rho-19.vercel.app/api?username=Kunal-Somani&show_icons=true&include_all_commits=true&count_private=true&rank_icon=github&hide_border=true&bg_color=0b0f14&title_color=22d3ee&icon_color=f59e0b&text_color=c9d1d9&ring_color=22d3ee" alt="GitHub stats"/>
<img height="170" src="https://streak-stats.demolab.com?user=Kunal-Somani&hide_border=true&background=0b0f14&ring=22d3ee&fire=f59e0b&currStreakLabel=22d3ee&sideLabels=c9d1d9&currStreakNum=e6edf3&sideNums=e6edf3&dates=5b6b7d" alt="Streak"/>

<img width="94%" src="https://github-readme-activity-graph.vercel.app/graph?username=Kunal-Somani&bg_color=0b0f14&color=c9d1d9&line=22d3ee&point=f59e0b&area=true&area_color=22d3ee&hide_border=true" alt="Contribution graph"/>

</div>

<div align="center">
<sub>Now: physics-guided medical imaging · sim-to-real RL navigation · multimodal SAR fusion · robot-data tooling</sub>
</div>
