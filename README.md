# Idara Samuel Osu
### ML Engineer · Inference · MLOps · Agentic AI

`Nigeria` &nbsp;·&nbsp; `Remote` &nbsp;·&nbsp; `Open to Full-time`

---

> *"The languages of millions — trained, quantized, deployed."*  
> Founder of **USEM AI**: a production multilingual AI platform for indigenous African languages, built from raw data collection to live inference.

---

## ⚙️ Stack

| Domain | Tools |
|---|---|
| **Training** | PyTorch · HuggingFace Transformers · NLLB · Whisper · OrpheusTTS · H100 |
| **Inference Engineering** | TensorRT-LLM · CTranslate2 · vLLM · SGLang · ONNX · TorchScript |
| **Optimisations** | KV Caching · In-flight Batching · fp16 / int4 AWQ Quantization · Dynamic Shape Profiles |
| **MLOps** | Vertex AI Pipelines · SageMaker Pipelines · KFP · DVC · MLflow · Evidently AI |
| **Orchestration** | LangChain · LangGraph · Multi-agent · Tool Calling · Function Routing |
| **Serving** | FastAPI · SSE Streaming · SageMaker Endpoints · Serverless · Docker |
| **Monitoring** | BigQuery · CloudWatch · Prometheus · Grafana · Drift Detection · Auto-retrain Triggers |
| **CI/CD & IaC** | GitHub Actions · Terraform · EventBridge · SQS · S3 · ECR |
| **Data** | MongoDB · PostgreSQL · Supabase · Large-scale proprietary data pipelines |

---

## 🚀 Projects

---

### 🗣️ USEM AI — Multilingual AI Platform for Indigenous Languages
`Founder & ML Engineer` &nbsp;·&nbsp; `2024 – 2026` &nbsp;·&nbsp; `100+ active users`

End-to-end AI platform built for Ibibio, Annang, Oro, Ekid, and related languages — from raw data collection through production deployment.

- Built proprietary speech + text datasets for translation, TTS, and STT from scratch — no off-the-shelf corpus
- Fine-tuned and instruction-tuned an LLM for multilingual task-following; trained NMT on Meta's NLLB architecture
- Trained production TTS (OrpheusTTS) and STT models on H100s, evaluated against rigorous quality benchmarks
- Converted TTS/STT → **TensorRT-LLM**; NMT + Whisper → **CTranslate2** with timestamp support
- Applied **KV caching · in-flight batching · quantization** for real-time inference
- Architected **Etimbuk** — a LangGraph multi-tool agent routing across translation, TTS, STT, and creative writing with pedagogically structured output; proactive heartbeat notifications via WhatsApp and Telegram
- Deployed serverless with full **CI/CD, model versioning, and continuous delivery**

---

### 🔍 Auto Insurance Damage Inspection Pipeline
`MLOps Engineer` &nbsp;·&nbsp; `GCP · Vertex AI`

Vision model pipeline: damage type + severity + affected part — from raw images to monitored production endpoint.

- **EfficientNet-B4 multi-head model** (3 output heads) trained as containerised Vertex AI Pipeline components
- Dataset versioned with **DVC** (GCS remote); training tracked with **MLflow**
- **TensorRT fp16 conversion** via `torch_tensorrt` with per-head max-diff assertion (`< 0.05`) for correctness
- **KFP conditional deployment gate** — pipeline halts and registers model as `Rejected` if `accuracy < 0.85` or `macro F1 < 0.80`
- Deployed to Vertex AI endpoint (g2 GPU) with **10% canary → full traffic** promotion
- **Evidently AI** drift monitoring on BigQuery inference logs (image brightness, contrast, blur score, confidence) → automated Vertex Pipeline retrain trigger on drift share ≥ 20%

---

### 🎙️ Production TTS Deployment — OrpheusTTS + TensorRT
`Inference Engineer` &nbsp;·&nbsp; `AWS · SageMaker`

OrpheusTTS → ONNX → TensorRT engine pipeline with production streaming and monitoring.

- **Three-component TRT pipeline**: encoder · decoder · HiFi-GAN vocoder — all fp16 with dynamic shape profiles
- Correctness validated post-conversion: PyTorch vs TRT output diff asserted per head
- **Sentence-chunked streaming** via FastAPI SSE — latency vs. naturalness trade-off handled at sentence boundary
- SageMaker `g5.xlarge` (A10G) endpoint deployed via GitHub Actions: **10% canary → smoke test → 100% promotion**
- Production metrics: **RTF · DNSMOS P.835 · TTFC · GPU utilisation** via CloudWatch custom metrics
- DNSMOS scored async on 1-in-20 sampled outputs; alert fires if score drops below 3.2

---

### 📹 YouTube Video Summariser — Whisper + Mistral on Single GPU
`Inference Engineer` &nbsp;·&nbsp; `AWS · SageMaker`

Two TensorRT-LLM models (Whisper large-v3 + Mistral 7B) co-deployed on a single A10G (24GB VRAM).

- Whisper converted via `trtllm-build` (encoder + decoder engines, fp16, beam width 4)
- Mistral 7B quantized with **int4 AWQ** (calibrated on CNN/DailyMail) — lower perplexity than naive int8
- **PagedAttention + continuous batching + chunked context** enabled on LLM engine
- Streaming SSE summary: tokens yielded token-by-token with event loop yield between steps
- Videos > 10 min handled via **SQS async job queue** → S3 result store → polling endpoint
- Prometheus metrics: **Whisper RTF · LLM TTFT · tokens/sec · queue depth**

---

### 📊 Tabular ML — Churn Prediction: Postgres → SageMaker
`MLOps Engineer` &nbsp;·&nbsp; `AWS · Supabase`

Full MLOps lifecycle on tabular data: Supabase PostgreSQL → feature engineering → XGBoost → monitored production endpoint.

- SQL feature engineering (multi-table joins, derived features) in **SageMaker Processing Job**; live feature fetch from Supabase at inference time for real-time scoring
- **GPU-accelerated XGBoost** with `scale_pos_weight` for class imbalance; **SHAP** explainability logged per run
- **SageMaker Model Registry** approval gate: `AUC ≥ 0.82` and `F1 ≥ 0.75` required for `Approved` status
- Full **SageMaker Pipeline DAG**: ProcessingStep → TrainingStep → EvaluateStep → ConditionStep → RegisterStep → DeployStep
- **EventBridge (cron) → Lambda → Evidently AI** drift check on Supabase live data vs. training baseline → automated pipeline retrigger on drift share ≥ 30%
- Batch prediction endpoint (up to 1000 customers per call) with `high / medium / low` risk tier output

---

## 🎓 Education

BSc Urban & Regional Planning &nbsp;·&nbsp; **CGPA 4.35 / 5.0**

---

<p align="center"><i>Building AI for the languages that were never in the training data.</i></p>
