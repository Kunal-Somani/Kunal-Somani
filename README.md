<div align="center">

# Kunal

### Robotics & AI · Edge Intelligence · Autonomous Agents

**B.E. Robotics & Artificial Intelligence** — Thapar Institute of Engineering & Technology  
**B.S. Data Science & Applications** — Indian Institute of Technology Madras

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/kunal-somani-227373344)
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:kunal120222@gmail.com)

</div>

---

## About Me

Pre-final year undergrad at the intersection of robotics, computer vision, and autonomous systems. I build things that actually work on hardware — multimodal ML pipelines, edge AI systems, agentic backends, and production-grade open-source contributions.

- **Research:** Multimodal CNN+DNN for Parkinson's early detection — improved combined model accuracy from 88% to 91%+ *(Thapar ELC, Summer 2025)*
- **Open Source:** Core-contributor at JdeRobot with 16 merged PRs; active contributions at Kubeflow/CNCF and RuxaiLab
- **CV/ML:** Toll Fraud Detection system — 24K+ images, 97% accuracy on multi-axle trucks *(Medium article published)*
- **Robotics Research:** Audio-Visual-Thermal fusion for autonomous SAR under Dr. Ankit Soni, Thapar — using Isaac Sim + ROS 2 Humble
- **Capstone:** Canary Rover — autonomous mine inspection robot with SLAM, RL navigation, crack detection, and gas leak sensing

---

## Open-Source Contributions

| Organisation | Repository | Contribution | Status | Period |
|---|---|---|---|---|
| JdeRobot | Robotics Academy | Fixed `BumperNode` unnecessary variable assignment, HAL refactor, deployment script fixes (getopts, Docker Compose V2, preflight checks), removed duplicate `detection_network.py`, 52 unit tests, docstrings across 4 backend modules | 16 PRs Merged | Feb 2026–Present |
| Kubeflow / CNCF | docs-agent | Fixed 10.14s asyncio event loop starvation via `run_in_executor()`; eliminated 2–4s per-query latency with SentenceTransformer singleton; `MAX_TOOL_DEPTH` recursion guard; `ZeroDivisionError` fixes in KFP chunking pipelines | 6 PRs Open | Feb 2026–Present |
| RuxaiLab | sentiment-analysis-api · facial-sentiment-analysis-api | Centralized logger factory; f-string anti-pattern fixes in audio/transcript services; whitespace-only input bypassing ML model validation; `ZeroDivisionError` fix in MVP pipeline; dynamic CLI video loading | 6 PRs Open | Feb 2026–Present |

---

## Featured Projects

| Project | Description | Stack |
|---|---|---|
| [**Axon Core**](https://github.com/Kunal-Somani/axon-core) | Unified multi-modal intelligence API with dynamic LLM routing across 3 processing units — RAG via FAISS+Ollama, tool-use via Gemini, and general chat. Step-Back Query Generation for hallucination reduction. Secure execution handshake requiring user confirmation before subprocess calls. | FastAPI · LangChain · FAISS · Ollama · Gemini |
| [**its-ok-gemini**](https://github.com/Kunal-Somani/its-ok-gemini) | Autonomous SDLC agent — receives a natural language task brief, generates full application code via LLM, creates a GitHub repo, and deploys live to GitHub Pages without human intervention. Handles iterative revision rounds by cloning its own deployed code and making surgical updates. | FastAPI · Gemini API · GitPython · Docker · GitHub API |
| [**Financial Analyst Agent**](https://github.com/Kunal-Somani/financial-analyst-agent) | Dual-tool agentic system with dynamic reasoning to select between a custom SQL executor and a PGVector RAG retriever. Synthesized results delivered to Telegram via live API integration. | n8n · Gemini 2.5 Pro · PostgreSQL · pgvector · Docker |
| [**Autonomous Agent Portfolio**](https://github.com/Kunal-Somani/n8n-agents-project) | 4 autonomous agents — GitHub issue triage, scheduled ArXiv research digest, live Hacker News sentiment analysis with per-story just-in-time RAG, and unstructured-text-to-Google-Sheets extraction. Handles 500+ items and 25+ API calls per run with strict schema enforcement. | n8n · Gemini Flash · Ollama · REST APIs |
| [**LLM Quiz Solver**](https://github.com/Kunal-Somani/llm-quiz-solver) | Recursive multi-agent system with dynamic DOM analysis via Playwright, JIT Python code synthesis via LLM, and multi-step traversal with state maintained across authentication boundaries. Deployed on Render via Docker. | FastAPI · GPT-4o · Playwright · Docker |
| [**Parkinson's Early Detection**](https://github.com/eshaansingla/ParkinsonsEarlyPrediction) | Multimodal early detection system fusing MPU9250 IMU tremor signals and voice recordings. CNN for voice (88% accuracy) + DNN for tremor, combined via late fusion weighting — achieving 91% accuracy. Built custom data collection pipeline from ESP32 hardware to model inference. | TensorFlow · Keras · Librosa · Parselmouth · scikit-learn |
| [**Toll Fraud Detection**](https://github.com/Kunal-Somani/tiet-ucs532p-bteam) | Classical CV pipeline for detecting fake FASTag usage at toll plazas. 24K+ images, 3780-dim HOG feature vectors, LinearSVC — 97% accuracy on multi-axle trucks. | OpenCV · scikit-learn · HOG · LinearSVC |

---

## Active Research & Projects

| Project | Description | Status |
|---|---|---|
| Audio-Visual-Thermal SAR | Multimodal fusion architecture for autonomous search & rescue in visually degraded environments. Fusing 3 modalities for robust SLAM and object detection. | Ongoing — under Dr. Ankit Soni, Thapar |
| Canary Rover | Autonomous mine inspection rover — crack detection, gas leak sensing, dust suppression, anti-theft GPS, SLAM via RPLiDAR+IMU, RL-trained navigation, spark-proof body. Hardware in build phase. | Ongoing — Capstone |
| Brain & Knee MRI Reconstruction | AI architecture to accelerate MRI scan result generation, replacing slow mathematical-only methods. | In progress |
| AI Assistant (RAGless) | Multimodal personal AI assistant exploring Mamba and beyond-transformer architectures to replace FAISS/RAG+LLM approach. Speech, text, and document modes. | In progress |

---

## Tech Stack
(unchanged)

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
