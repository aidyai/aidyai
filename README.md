<div align="center">

# Idara Samuel Osu

**ML Engineer · Inference · MLOps · Agent Ochestration**

[![Email](https://img.shields.io/badge/idaraosusamuel@gmail.com-black?style=flat-square&logo=gmail&logoColor=white)](mailto:idaraosusamuel@gmail.com)
[![Twitter](https://img.shields.io/badge/@Osuaidy-black?style=flat-square&logo=x&logoColor=white)](https://twitter.com/Osuaidy)
[![Location](https://img.shields.io/badge/Nigeria-Remote-black?style=flat-square)]()

*Training, optimising, and shipping AI systems — from raw data to production inference.*  
*Founder of **USEM AI**: multilingual AI Agent for Zero-Resource Indigenous African languages, built end-to-end.*

</div>

<br>

👋 &nbsp;I'm Idara — ML Engineer from Nigeria, building AI for languages the world forgot to include  
🔭 &nbsp;Currently scaling **USEM AI** and teaching **Etimbuk** (my AI agent) her next language — Ibibio,Annang,Oro  
🌍 &nbsp;On a mission to make every indigenous African language speak through AI  
⚡ &nbsp;Fun fact: I love the Ancients — Isaac Newton and Nikola Tesla are my people  
📫 &nbsp;[idaraosusamuel@gmail.com](mailto:idaraosusamuel@gmail.com) &nbsp;·&nbsp; [@Osuaidy](https://twitter.com/Osuaidy)

<br>

## 🧠 Expertise

```
Training          PyTorch · HuggingFace Transformers · NLLB · Whisper · OrpheusTTS · Molmo · H100
Inference         TensorRT-LLM · CTranslate2 · vLLM · SGLang · ONNX · fp16 · int4 AWQ
Optimisation      KV Caching · In-flight Batching · PagedAttention · Dynamic Shape Profiles
MLOps             Vertex AI Pipelines · SageMaker Pipelines · KFP · DVC · MLflow · Evidently AI
Agents            LangChain · LangGraph · Multi-agent Orchestration · Tool Calling
Serving           FastAPI · SSE Streaming · SageMaker Endpoints · Serverless · Docker
Monitoring        BigQuery · CloudWatch · Prometheus · Grafana · Drift Detection · Auto-retrain
CI/CD & IaC       GitHub Actions · Terraform · EventBridge · SQS · ECR
Data              MongoDB · PostgreSQL · Supabase · Proprietary Data Pipelines
```

<br>

## 🔬 Work

**[USEM AI](https://github.com/aidyai/usem.ai)** — *Founder & ML Engineer · 2024–2026*

Built a production multilingual AI platform for Ibibio, Annang, Oro, and Ekid from nothing — proprietary datasets, model training on H100s, full inference stack, and a live agentic layer. Converted TTS/STT to TensorRT-LLM and NMT + Whisper to CTranslate2. Applied KV caching, in-flight batching, and quantization for real-time throughput. Shipped **Etimbuk** — a LangGraph agent routing across translation, TTS, STT, and creative writing with proactive WhatsApp/Telegram notifications. 100+ active users.

<br>

**[Auto Insurance Damage Inspection](https://github.com/aidyai/auto-insurance-vertex-ai-pipelines)** — *MLOps · GCP · Vertex AI*

Vision pipeline for vehicle damage classification and severity scoring. Fine-tuned **Molmo-2B** as the backbone; full pipeline containerised on Vertex AI with DVC dataset versioning and MLflow experiment tracking. TensorRT fp16 conversion with per-head output diff assertion. KFP conditional deployment gate blocks promotion if `accuracy < 0.85` or `macro F1 < 0.80`. Evidently AI drift monitoring on BigQuery inference logs triggers automated retraining when drift share exceeds 20%.

<br>

**[Production TTS — OrpheusTTS + TensorRT](https://github.com/aidyai/TTS-TensorRT-LLM-Sagemaker)** — *Inference Engineering · AWS · SageMaker*

OrpheusTTS → ONNX → TensorRT: encoder · decoder · HiFi-GAN vocoder, all fp16 with dynamic shape profiles. Sentence-chunked streaming via FastAPI SSE. SageMaker g5.xlarge deployment with 10% canary → smoke test → full traffic promotion in GitHub Actions. Async DNSMOS P.835 scoring on sampled outputs; RTF, TTFC, and GPU utilisation tracked via CloudWatch.

<br>

**[YouTube Summariser — Whisper + Mistral on One GPU](https://github.com/aidyai/Video-Summarizer---TensorRT-LLM)** — *Inference Engineering · AWS*

Whisper large-v3 and Mistral 7B, both TensorRT-LLM, co-deployed on a single A10G (24GB). Mistral quantized with int4 AWQ calibrated on CNN/DailyMail. PagedAttention + continuous batching + chunked context on the LLM. Videos over 10 minutes handled via SQS async queue. Prometheus tracks Whisper RTF, LLM TTFT, tokens/sec, and queue depth.

<br>

**[Churn Prediction — Postgres to SageMaker](https://github.com/aidyai/churn-sagemaker-pipelines)** — *MLOps · AWS · Supabase*

Full SageMaker Pipeline DAG: SQL feature engineering in a Processing Job → GPU-accelerated XGBoost with SHAP → Model Registry approval gate (`AUC ≥ 0.82`, `F1 ≥ 0.75`) → endpoint deployment with live Supabase feature fetch at inference time. EventBridge cron → Lambda → Evidently AI drift check on live database → automated pipeline retrigger on drift share ≥ 30%.

<br>

<div align="center">

*BSc Urban & Regional Planning · CGPA 4.35/5.0*

</div>
