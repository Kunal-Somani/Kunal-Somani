<div align="center">

# Kunal

**B.E. Robotics and Artificial Intelligence** - Thapar Institute of Engineering and Technology  

**B.S. Data Science and Applications** - Indian Institute of Technology Madras  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/kunal-somani-227373344)
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:kunal120222@gmail.com)

</div>

---

Pre-final year undergrad building at the intersection of robotics, computer vision, and autonomous systems. My work runs on real hardware and real infrastructure: multimodal ML pipelines, edge AI systems, agentic backends, and production-grade open-source tooling.

**Open Source:** Active contributor at JdeRobot/RoboticsAcademy with 16 merged PRs. Resolved an FP16 precision crash in the Object Detection pipeline, fixed deployment script bugs across `run_academy.sh` and `develop_academy.sh`, refactored the Hardware Abstraction Layer, and shipped 52 unit tests across 5 test classes.

**Research at Thapar ELC (Summer 2025):** Multimodal CNN and DNN for Parkinson's early detection. Fused MPU9250 tremor signals with voice recordings via late fusion, pushing combined model accuracy from 88% to 91%.

**Computer Vision:** Toll fraud detection system built on HOG features and LinearSVC. 24K+ images, 97% accuracy on multi-axle vehicle classification.

**Robotics Research (ongoing):** Audio-Visual-Thermal fusion architecture for autonomous SAR navigation in visually degraded environments, under Dr. Ankit Soni at Thapar, using Isaac Sim and ROS 2.

---

## Featured Projects

| Project | Description | Stack |
|---|---|---|
| [Archon](https://github.com/Kunal-Somani/archon) | Production-deployable instruction-to-deployment backend. Hybrid RAG (Cohere dense + BM25 sparse, RRF fusion) retrieves context, Anthropic Tool Use generates schema-validated code, and a GitHub App deployer pushes live sites to GitHub Pages. FastAPI and Celery handle async execution; Redis Pub/Sub streams logs over WebSocket to a React and TypeScript dashboard; full observability via Prometheus, Grafana, and OpenTelemetry. | FastAPI - Celery - Redis - Cohere - Anthropic API - React - TypeScript - Vite - PostgreSQL - SQLAlchemy - Alembic - Prometheus - Grafana - OpenTelemetry - Docker |
| [Parkinson's Early Detection](https://github.com/eshaansingla/ParkinsonsEarlyPrediction) | Multimodal early detection fusing MPU9250 IMU tremor signals with voice recordings. CNN on voice features (88% accuracy) and DNN on tremor data combined via late fusion to reach 91%. Custom ESP32 hardware pipeline from sensor to model inference. | TensorFlow - Keras - Librosa - Parselmouth - scikit-learn - SoundDevice |
| [Axon Core](https://github.com/Kunal-Somani/axon-core) | Production-deployable fully local tri-modal AI assistant. A BART-MNLI zero-shot router dispatches across three paths: knowledge retrieval via Qdrant and local Gemma, OS-level tool execution with user confirmation, and general conversation. Hybrid RAG with MiniLM and BM25, reranked by a cross-encoder; GBNF-constrained sampling for tool calling. | FastAPI - LangChain - Qdrant - Ollama - Next.js - Docker - SQLAlchemy |
| [Helix](https://github.com/Kunal-Somani/helix-agent) | Production-deployable recursive autonomous web agent on the OODA loop. Playwright handles JS-heavy DOMs, Claude Tool Use synthesizes Python solutions just-in-time, RestrictedPython and SIGALRM sandbox execution, and HTTP submission loops until a terminal state. Durable jobs via ARQ on Redis; Prometheus, Loki, and Grafana cover observability. | FastAPI - Playwright - Claude API - ARQ - Redis - Prometheus - Loki - Grafana - Docker |
| [TruthTag: Toll-Audit](https://github.com/Kunal-Somani/TruthTag-Toll-Audit) | Classical CV pipeline cross-verifying RFID FASTag claims against physical vehicle geometry at toll plazas. 3780-dimensional HOG vectors, LinearSVC trained on 24K+ images, 97% accuracy on multi-axle classification. Cross-modal centroid tracker, MOG2 virtual tripwire, and a Streamlit audit dashboard. | OpenCV - scikit-learn - HOG - LinearSVC - NumPy - Streamlit - Seaborn - Matplotlib |

---

## Active Research

| Project | Description | Status |
|---|---|---|
| [Canary Rover](https://github.com/Kunal-Somani/canary-rover) | Autonomous mine inspection rover. PPO locomotion trained in PyBullet (200K timesteps), real-time ROS 2 sensor stack for IMU, LiDAR, and BLDC encoders, SLAM via slam_toolbox and RTAB-Map, and full 3D simulation in NVIDIA Isaac Sim 5.1. Capstone project, team of 5. | Ongoing -- Capstone |
| [MRI Reconstruction](https://github.com/Kunal-Somani/MRI_Reconstruction) | Dual-branch physics-guided framework for accelerated MRI reconstruction. Learned gating network routes k-space data adaptively without anatomy labels at inference. Achieves +1.78% SSIM over single-branch baselines at 112ms and 302 GFLOPs on an RTX 4060. | Paper authored |
| Audio-Visual-Thermal SAR | Multimodal fusion architecture for autonomous SAR in visually degraded environments. Thermal, acoustic, and visual modalities fused for robust SLAM and detection, under Dr. Ankit Soni at Thapar. | Review paper authored |

---

## Tech Stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)

**Robotics & Edge**
![ROS 2](https://img.shields.io/badge/ROS_2-22314E?style=flat&logo=ros&logoColor=white)
![NVIDIA Jetson](https://img.shields.io/badge/NVIDIA_Jetson-76B900?style=flat&logo=nvidia&logoColor=white)
![Isaac Sim](https://img.shields.io/badge/Isaac_Sim-76B900?style=flat&logo=nvidia&logoColor=white)
![PyBullet](https://img.shields.io/badge/PyBullet-306998?style=flat&logoColor=white)
![Stable Baselines3](https://img.shields.io/badge/Stable_Baselines3-4B8BBE?style=flat&logoColor=white)
![Gymnasium](https://img.shields.io/badge/Gymnasium-0052CC?style=flat&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-FF6600?style=flat&logoColor=white)
![Eclipse Zenoh](https://img.shields.io/badge/Eclipse_Zenoh-2C2255?style=flat&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-D97615?style=flat&logo=mathworks&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat&logo=nvidia&logoColor=white)

**AI & Computer Vision**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=PyTorch&logoColor=white)
![PyTorch Lightning](https://img.shields.io/badge/PyTorch_Lightning-792EE5?style=flat&logo=lightning&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=TensorFlow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-111F68?style=flat&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat&logo=huggingface&logoColor=black)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)
![Librosa](https://img.shields.io/badge/Librosa-000000?style=flat&logoColor=white)
![Parselmouth](https://img.shields.io/badge/Parselmouth-512BD4?style=flat&logoColor=white)
![einops](https://img.shields.io/badge/einops-FF6B6B?style=flat&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4878CF?style=flat&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)

**Backend & Databases**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-6BA3BE?style=flat&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)

**DevOps & Infra**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Anaconda](https://img.shields.io/badge/Anaconda-44A833?style=flat&logo=anaconda&logoColor=white)

---

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats-eight-theta.vercel.app/api?username=Kunal-Somani&theme=dark&hide_border=true&include_all_commits=true&count_private=true)

![Streak Stats](https://github-readme-streak-stats.herokuapp.com/?user=Kunal-Somani&theme=dark&hide_border=true)

</div>

---

<div align="center">

Currently working on: Physics-guided deep learning for medical imaging -- RL-based autonomous navigation -- Multimodal sensor fusion for SAR -- Beyond-transformer sequence architectures

</div>
