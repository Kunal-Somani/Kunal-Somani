<div align="center">

# Kunal Somani

**B.E. Robotics & Artificial Intelligence** — Thapar Institute of Engineering & Technology  
**B.S. Data Science & Applications** — Indian Institute of Technology Madras

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/kunal-somani-227373344)
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:kunal120222@gmail.com)

</div>

---

Pre-final year undergrad working at the intersection of robotics, computer vision, and autonomous systems. I build things that run on actual hardware: multimodal ML pipelines, edge AI systems, agentic backends, and production-grade open-source tooling.

**Open Source:** Merged contributor at JdeRobot/RoboticsAcademy with 16 PRs. Fixed deployment script bugs in `run_academy.sh` and `develop_academy.sh`, refactored the Hardware Abstraction Layer, resolved an FP16 precision crash in the Object Detection pipeline, and added 52 unit tests across 5 test classes.

**Research at Thapar ELC (Summer 2025):** Multimodal CNN+DNN for Parkinson's early detection. Fused MPU9250 tremor signals with voice recordings via late fusion, improving combined model accuracy from 88% to 91%.

**Computer Vision:** Toll fraud detection system built on HOG features and LinearSVC. 24K+ images, 97% accuracy on multi-axle vehicle classification. Published writeup on Medium.

**Robotics Research (ongoing):** Audio-Visual-Thermal fusion architecture for autonomous SAR in visually degraded environments, under Dr. Ankit Soni at Thapar, using Isaac Sim and ROS 2 Humble.

---

## Featured Projects

| Project | Description | Stack |
|---|---|---|
| [Parkinson's Early Detection](https://github.com/eshaansingla/ParkinsonsEarlyPrediction) | Multimodal early detection fusing MPU9250 IMU tremor signals with voice recordings. CNN on extracted voice features (88% accuracy), DNN on tremor data combined via late fusion weighting to reach 91%. Includes a custom ESP32 hardware data collection pipeline from sensor to model inference. | TensorFlow · Keras · Librosa · Parselmouth · scikit-learn · SoundDevice |
| [Axon Core](https://github.com/Kunal-Somani/axon-core) | Tri-modal AI assistant with a Gemini-powered semantic router dispatching queries across three paths: personal knowledge retrieval via Qdrant and local Gemma, OS-level tool execution with a user confirmation handshake, and general conversation. Next.js frontend with a FastAPI orchestrator, fully containerized. | FastAPI · LangChain · Qdrant · Ollama · Gemini · Next.js · Docker · SQLAlchemy |
| [its-ok-gemini](https://github.com/Kunal-Somani/its-ok-gemini) | Autonomous SDLC agent that takes a natural language brief, generates full application code via Gemini, creates a GitHub repository, and deploys to GitHub Pages without human intervention. Handles iterative revision rounds by cloning its own deployed code and applying surgical updates. Includes a Prometheus metrics layer, async task orchestration via background workers, and a WebSocket-based live status feed. | FastAPI · Gemini API · GitPython · Docker · GitHub API · SQLAlchemy · Alembic · Prometheus |
| [LLM Quiz Solver](https://github.com/Kunal-Somani/llm-quiz-solver) | Recursive autonomous agent for dynamic data analysis. Playwright handles JS-heavy DOMs and client-side rendering, feeds extracted context to GPT-4o-mini for just-in-time Python code synthesis, and executes the generated code in a sandboxed environment. Implements multi-step recursive task traversal with authentication state preserved across the chain. | FastAPI · Playwright · GPT-4o-mini · Docker · Pandas · BeautifulSoup |
| [Toll Fraud Detection](https://github.com/Kunal-Somani/tiet-ucs532p-bteam) | Classical CV pipeline for detecting fake FASTag usage at toll plazas. 3780-dimensional HOG feature vectors, LinearSVC trained on 24K+ images, 97% accuracy on multi-axle truck classification. Includes a cross-modal centroid tracker, misclassification error analysis, and a simulated audit pipeline. | OpenCV · scikit-learn · HOG · LinearSVC · Seaborn · Matplotlib |

---

## Active Research

| Project | Description | Status |
|---|---|---|
| [Canary Rover](https://github.com/Kunal-Somani/canary-rover) | Autonomous mine inspection rover. PPO-trained locomotion in PyBullet (200K timesteps), ROS 2 sensor nodes for IMU, LiDAR, and BLDC encoders, full 3D visual simulation in NVIDIA Isaac Sim 5.1 with live sensor feeds, and SLAM via slam_toolbox and RTAB-Map. Crack detection, gas leak sensing, spark-proof chassis. Team of 5. | Ongoing — Capstone |
| [MRI Reconstruction](https://github.com/Kunal-Somani/MRI_Reconstruction) | Dual-branch physics-guided deep learning framework for accelerated MRI reconstruction. A learned gating network routes k-space information adaptively, removing the need for anatomy labels at inference. Achieves +1.78% SSIM over single-branch baselines at 112ms per inference and 302 GFLOPs on an RTX 4060. | Ongoing |
| Audio-Visual-Thermal SAR | Multimodal fusion architecture for autonomous search and rescue in visually degraded environments. Three sensing modalities fused for robust SLAM and object detection, under Dr. Ankit Soni at Thapar. | Ongoing |
| AI Personal Assistant | Multimodal personal assistant exploring Mamba and beyond-transformer architectures as an alternative to the standard FAISS/RAG+LLM pattern. Speech, text, and document input modes. | In progress |

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

Currently exploring: Physics-guided deep learning for medical imaging · RL-based autonomous navigation · Beyond-transformer sequence architectures · Multimodal sensor fusion for SAR

</div>
