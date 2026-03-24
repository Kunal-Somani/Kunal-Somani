<div align="center">

# Kunal

### Robotics & AI · Edge Intelligence · Autonomous Agents

**B.E. Robotics & AI** — Thapar Institute of Engineering & Technology  
**B.S. Data Science & Applications** — IIT Madras

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/kunal-somani-227373344)
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:kunal120222@gmail.com)

</div>

---

## About Me

I'm a pre-final year undergrad pursuing a rare dual degree in **Robotics & AI** (Thapar) and **Data Science** (IIT Madras), working at the intersection of physical systems and machine intelligence.

My work lives in two worlds: getting deep learning models to run on hardware with real-time constraints, and building AI agents that think, route, and act autonomously. I care about systems that are not just intelligent in theory, but that actually work when deployed — on edge devices, in production APIs, and in open-source codebases.

- **Research:** Built an IoT + voice multimodal pipeline for early Parkinson's detection (>95% classification accuracy)
- **Robotics:** Engineered HIL testing and kinematic control systems for 2 custom robots at MARS Society
- **Open Source:** 7 merged PRs at **JdeRobot**; active contributions at **Kubeflow/CNCF**, **RuxaiLab**, and **GFOSS**
- **Focus:** Edge AI deployment, LLM-driven autonomous agents, ROS 2 middleware, and production RAG architectures

---

## Open-Source Contributions

**JdeRobot — Robotics Academy** `ROS 2 · Python · Bash · Docker` — 7 PRs Merged *(Feb 2026–Present)*

| PR | What it fixed |
|---|---|
| #3571 | Docs: typos and grammar in README |
| #3572 | Refactor: PEP8 `is None` enforcement across HAL + Frequency templates; validated with live Gazebo exercise recordings |
| #3620 | Fix: broken `getopts` string, Docker Compose V2 detection, missing preflight checks, `curl` error handling in `run_academy.sh` |
| #3634 | Fix: undefined `Help` function call, incorrect Docker Compose V2 check, unquoted variables in `develop_academy.sh` |
| #3635 | Fix: FP16 precision crash in Object Detection pipeline via dynamic PyTorch tensor allocation for CPU environments |
| #3637 | Refactor: HAL memory identity evaluations; resolved 100+ linter warnings |
| #3638 | Tests: 35 unit tests across 5 test classes covering views, filesystem, exceptions, path traversal security |

**Kubeflow / CNCF — docs-agent** `FastAPI · asyncio · Milvus · LangChain` — 6 PRs Open *(Mar 2026–Present)*
- Fixed 10.14s asyncio event loop starvation — offloaded Milvus vector search to `run_in_executor()`
- Eliminated 2–4s per-query latency by promoting SentenceTransformer (~400MB) to module-level singleton
- Added `MAX_TOOL_DEPTH=3` recursion guard preventing stack overflow on multi-hop LLM tool calls
- Fixed `ZeroDivisionError` crashes in both standard and incremental KFP chunking pipelines

**RuxaiLab — sentiment-analysis-api & facial-sentiment-analysis-api** `Flask · TensorFlow · OpenCV` — 6 PRs Open *(Feb 2026–Present)*
- Fixed malformed `logger.debug()` f-string calls silently dropping debug output; added 2 new `remove_audio` branch tests
- Fixed whitespace-only text bypassing input validation, reaching the ML model with no error returned
- Fixed `ZeroDivisionError` in MVP pipeline on empty prediction arrays; wired dynamic CLI video path into `cv2.VideoCapture()`

**GFOSS — ORION CubeSat Edge AI Payload** `YOLOv8 · Eclipse Zenoh · Jetson` *(Feb 2026–Present)*
- Architected live YOLOv8 computer vision pipeline on NVIDIA Jetson at 30+ FPS
- Engineered async Pub/Sub middleware via Eclipse Zenoh + Pydantic with 3.5ms telemetry latency on x86

---

## Featured Projects

| Project | Description | Stack |
|---|---|---|
| [**Axon Core**](https://github.com/Kunal-Somani/axon-core) | Unified multi-modal intelligence API with dynamic LLM routing across 3 specialized processing units (RAG, tool-use, conversational). Dual voice/text client with human-in-the-loop execution handshake for secure system commands. | FastAPI · LangChain · FAISS · Ollama · Gemini |
| [**Financial Analyst Agent**](https://github.com/Kunal-Somani/financial-analyst-agent) | Dual-tool agentic system with dynamic reasoning to select between a custom SQL executor and a PGVector RAG retriever. Delivers synthesized summaries to Telegram via live API integration. | n8n · Gemini 2.5 Pro · PostgreSQL · pgvector · Docker |
| [**its-ok-gemini**](https://github.com/Kunal-Somani/its-ok-gemini) | Autonomous SDLC agent that interprets a task brief, generates full application code via LLM, creates a GitHub repo, and deploys it live to GitHub Pages — including iterative code revision rounds. | FastAPI · Gemini API · GitPython · Docker · GitHub API |
| [**Autonomous Agent Portfolio**](https://github.com/Kunal-Somani/n8n-agents-project) | Suite of 4 autonomous agents handling CI/CD GitHub triage, scheduled research synthesis, live sentiment analysis, and structured data extraction with just-in-time RAG and XML/JSON pipeline management. | n8n · Gemini Flash · Ollama · REST APIs |

---

## Tech Stack

**Languages**  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)

**Robotics & Edge**  
![ROS 2](https://img.shields.io/badge/ROS_2-22314E?style=flat&logo=ros&logoColor=white)
![NVIDIA Jetson](https://img.shields.io/badge/NVIDIA_Jetson-76B900?style=flat&logo=nvidia&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-FF6600?style=flat&logoColor=white)
![Eclipse Zenoh](https://img.shields.io/badge/Eclipse_Zenoh-2C2255?style=flat&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-D97615?style=flat&logo=mathworks&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat&logo=nvidia&logoColor=white)

**AI & Computer Vision**  
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=PyTorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=TensorFlow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-111F68?style=flat&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat&logo=huggingface&logoColor=black)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)

**Backend & Databases**  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![Milvus](https://img.shields.io/badge/Milvus-00A1EA?style=flat&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-FF6D5A?style=flat&logo=n8n&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat&logoColor=white)

**DevOps & Infra**  
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=cloudflare&logoColor=white)
![Anaconda](https://img.shields.io/badge/Anaconda-44A833?style=flat&logo=anaconda&logoColor=white)

---

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Kunal-Somani&theme=dark&hide_border=true&include_all_commits=true&count_private=true)

![Streak Stats](https://nirzak-streak-stats.vercel.app/?user=Kunal-Somani&theme=dark&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Kunal-Somani&theme=dark&hide_border=true&include_all_commits=true&count_private=true&layout=compact)

</div>

---

<div align="center">

*Currently exploring: NVIDIA Isaac Sim · Advanced RAG architectures · Kubernetes orchestration*

</div>
