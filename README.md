# Zain Asad

### Scientific Software & Applied AI Engineer
**Scientific Software · Computer Vision · ML Systems · Laboratory Automation · Edge AI**

I’m a Senior Microbiology Analyst whose work has increasingly moved into software engineering, laboratory automation and applied machine learning.

I build systems that take scientific problems from **workflow understanding → architecture → implementation → model development → deployment → real-world use**.

My professional work includes operational laboratory software used in ISO 17025 workflows, barcode and LIMS integrations, scientific calculation tools, audit and traceability systems, computer-vision deployment platforms and ML-assisted colony counting.

I’m particularly interested in building AI that solves real scientific and operational problems rather than AI for its own sake.

---

## Featured Engineering Projects

### SatellaDet
**Open-source PyTorch object detection framework**

SatellaDet is a lightweight, anchor-free object detection framework designed for small-object detection and CPU-friendly ONNX deployment.

I built the framework to have direct control over the full detection pipeline rather than relying entirely on an existing object-detection framework.

**Key features**
- Custom PyTorch detector architecture
- Lightweight split-transform-fuse backbone
- Multi-scale P2 / P3 / P4 detection
- Anchor-free LTRB box regression
- Shared decoupled classification and regression towers
- CIoU regression loss
- Focal BCE classification loss
- EMA training weights
- Per-class precision, recall, F1, mAP50 and mAP50-95
- Count-oriented evaluation metrics
- Custom SatellaScore checkpoint selection
- YOLO-format dataset support
- 640, 960 and 1280 input resolutions
- ONNX export and verification
- CPU-oriented deployment design

**Stack:** Python · PyTorch · ONNX · NumPy · pytest

[View SatellaDet →](https://github.com/EphraimAsad/SatellaDet)

---

### Regulus / Sekhmet
**Computer vision and ML deployment for microbiology**

Regulus and Sekhmet form part of my work on ML-assisted microbiology colony counting.

The goal is not simply to train object-detection models, but to build the infrastructure required to make them usable and traceable inside a laboratory workflow.

**Regulus includes**
- PostgreSQL as the central system of record
- Model artefacts stored directly in PostgreSQL
- Model versioning and traceability
- ONNX inference
- Analyst review and correction
- Role-based permissions
- Persistent sessions
- Audit history
- Model-specific confidence thresholds
- Validation workflows
- Crash recovery
- Multi-user operation

**Sekhmet extends the workflow into**
- Camera-based plate capture
- Barcode and sample routing
- Colony detection and counting
- Multiple media-specific detection models
- Analyst-correctable inference
- Model-version audit traceability
- LIMS result export
- CPU-only inference

Current models include work on:
- TVC / PCA
- Campylobacter / mCCDA
- Enterobacteriaceae / VRBGA
- E. coli / TBX/TBG

Several models have achieved precision, recall and mAP50 above 0.90 on validation data, with CPU inference suitable for laboratory deployment.

**Stack:** Python · PyTorch · ONNX Runtime · PostgreSQL · Computer Vision · SQL

> Regulus and Sekhmet contain internal laboratory workflow components and are not fully public repositories.

---

### Satella Runner
**Android edge-AI inference for object detection**

Satella Runner is a native Android application for deploying ONNX object-detection models directly onto mobile hardware.

Rather than treating mobile inference as a simple model wrapper, I built the application around the practical problems that appear when computer vision leaves the development workstation.

**Current capabilities**
- Native Android / Kotlin implementation
- Jetpack Compose interface
- CameraX integration
- Gallery-image inference
- Full-resolution camera inference
- Live camera inference
- ONNX Runtime Android
- Support for compatible external ONNX detectors
- 1280 × 1280 model support
- Live camera zoom / magnification
- Zoom-assisted image capture
- Shared preprocessing across capture and live inference
- Image orientation correction
- Centre-square cropping
- RGB → float32 NCHW preprocessing
- Detection decoding and non-maximum suppression
- Frame dropping to prevent live-inference backlog
- Persistent model sessions
- Local inference benchmarking
- Mean / median / P95 latency measurements
- Cross-platform parity debugging
- Export of preprocessed tensors and raw model outputs for comparison against desktop inference

The project is particularly useful for testing whether the same detection model behaves consistently between workstation and edge/mobile environments.

**Stack:** Kotlin · Android · Jetpack Compose · CameraX · ONNX Runtime · Room · DataStore

---

### BactAI-D
**Hybrid AI system for bacterial identification**

BactAI-D explores phenotype-based bacterial identification using a combination of deterministic microbiology logic, machine learning and retrieval-backed explanation.

The system accepts natural-language phenotype descriptions and converts them into structured microbiological features before combining multiple identification approaches.

**Architecture**
- Rule-based phenotype parser
- Extended biochemical parser
- ML-assisted parser
- XGBoost genus classification
- Deterministic reference-database matching
- Adaptive ranking
- Species-level matching
- Retrieval-backed explanations
- Local Ollama inference
- Deterministic fallback when LLM output is unavailable or inappropriate
- Flask API
- React frontend

A genus classifier was developed across approximately 140 bacterial genera and achieved 95.1% accuracy on its evaluation set.

**Stack:** Python · XGBoost · Flask · React · FAISS · Hugging Face · Ollama

[View BactAI-D →](https://github.com/EphraimAsad/BactAI-D)

---

### Iapetus
**Predictive food microbiology platform**

Iapetus is an experimental predictive microbiology platform for exploring microbial growth, uncertainty and shelf-life risk.

The current version focuses on *Listeria monocytogenes* and combines machine-learning prediction with kinetic modelling.

**Features**
- ML-based microbial growth curves
- Kinetic growth modelling
- Monte Carlo uncertainty simulation
- P10 / P50 / P90 estimates
- Threshold exceedance probability
- Sensitivity analysis
- Risk-driver ranking
- Automated decision-support outputs
- Local LLM summaries
- Deterministic fallback
- FastAPI backend
- React frontend
- GitHub Actions CI

The current dataset is synthetic-first and the platform is intended for exploratory modelling rather than regulatory shelf-life validation.

**Stack:** Python · CatBoost · FastAPI · React · Monte Carlo Simulation · Ollama

[View Iapetus →](https://github.com/EphraimAsad/Iapetus)

---

# Professional Engineering

Alongside my role as a Senior Microbiology Analyst, I design, develop and maintain software used in operational laboratory workflows.

## FireAccess
**Laboratory confirmation-management platform**

FireAccess is an operational system built around microbiological confirmation workflows.

It supports approximately **30,000 confirmation records and associated label operations per month** across around **30 confirmation routes**, with approximately **25 laboratory users**.

Functionality includes:
- Parent/child confirmation records
- Barcode-driven workflows
- Automated thermal label generation
- Media batch tracking
- Analyst traceability
- Confirmation lifecycle management
- Multi-stage microbiology workflows
- Automated backup and recovery
- Result logic
- Audit-oriented record handling

The system was developed to remove repetitive manual handling while preserving laboratory traceability.

**Stack:** Microsoft Access · VBA · SQL · Barcode Integration · Thermal Printing

---

## CampyEnum
**Campylobacter enumeration software**

CampyEnum was developed to simplify and standardise Campylobacter enumeration workflows.

**Capabilities**
- Barcode-driven sample entry
- ISO 10272-2 weighted enumeration calculations
- Incomplete-sample handling
- Automated laboratory labels
- LIMS export
- Audit history
- Backup / archive workflows

The system was formally adopted as a controlled laboratory program within the ISO 17025 quality system.

**Stack:** TypeScript · React · Electron · SQL · Laboratory Informatics

---

## Additional Laboratory Automation

I have also developed smaller automation and analytical tools covering:

- SQL/LIMS reporting
- automated result comparisons
- Pseudomonas workflow automation
- Excel/VBA workflow tools
- sample-result transformation
- confirmation-result processing
- automated reporting
- label generation
- analyst timestamps and traceability
- DET mapping and workflow routing

My focus is usually the same: identify repetitive or error-prone work and replace it with a system that is faster, traceable and easier for analysts to use.

---

# Additional Machine Learning Work

## Satella Language Models

I publish language-model experiments and fine-tuned models through Hugging Face.

My work has included:
- Supervised fine-tuning
- LoRA / QLoRA
- DPO
- Reasoning and coding datasets
- Long-context training
- GGUF quantisation
- Evaluation harnesses
- Local deployment
- Mixture-of-Experts models

Projects include models based on Qwen3 and Qwen3.5 architectures, including Satella-30B-A3B and smaller Satella variants.

[View my Hugging Face profile →](https://huggingface.co/EphAsad)

---

## Mortality VAE

I also built a reproducible machine-learning analysis exploring sex differences in mortality across England and Wales between 1915 and 2015.

The project uses variational autoencoders to learn low-dimensional latent structures in age- and cause-specific mortality patterns.

Work included:
- PyTorch VAE implementation
- historical data harmonisation
- latent-space interpretation
- sex-specific modelling
- temporal robustness analysis
- latent dimensionality analysis
- synthetic decoding
- publication-quality visualisation
- reproducible analytical pipelines

[View the project →](https://github.com/EphraimAsad/VAE-Of-Mortality)

---

# Core Technologies

### Languages
`Python` `TypeScript` `JavaScript` `Kotlin` `SQL` `VBA`

### Machine Learning
`PyTorch` `ONNX Runtime` `XGBoost` `CatBoost` `scikit-learn` `Transformers` `Hugging Face` `Unsloth`

### Computer Vision
`Object Detection` `Small-Object Detection` `Model Evaluation` `ONNX Deployment` `Edge AI`

### Backend & Data
`FastAPI` `Flask` `PostgreSQL` `SQLite` `SQLAlchemy`

### Frontend & Applications
`React` `Electron` `Jetpack Compose` `Android` `CameraX`

### Engineering
`Git` `GitHub Actions` `Docker` `pytest` `Vitest` `Playwright` `CI/CD`

### Scientific & Laboratory Systems
`ISO 17025` `LIMS Integration` `Barcode Workflows` `Audit Trails` `Laboratory Automation` `Predictive Microbiology`

---

# What I Like Building

I’m most interested in problems where software, machine learning and domain knowledge have to work together.

Examples include:

- scientific software
- laboratory automation
- computer vision
- edge and local AI
- ML deployment systems
- predictive modelling
- scientific decision-support software
- model validation and traceability
- AI for life sciences and diagnostics

I particularly enjoy taking an idea beyond the model or prototype stage and building the surrounding system needed for people to actually use it.

---

# Publications & Research

### BactAI-D
**BactAI-D: Hybrid, Confidence-Aware AI for Phenotype-Based Bacterial Identification**

Zenodo  
DOI: `10.5281/zenodo.18089381`

### Mortality Modelling
**Decomposing Sex Differences in Mortality Across Age and Cause in England and Wales, 1915–2015**

Interpretable latent-variable modelling of long-term mortality patterns using variational autoencoders.

---

# Background

**BSc (Hons) Biology**  
Sheffield Hallam University, 2021

Current professional background:
- Food microbiology
- Water microbiology
- Environmental microbiology
- Microbiological confirmation
- Enumeration
- Laboratory quality systems
- Scientific software development
- Laboratory automation

---

## Links

- **GitHub:** [github.com/EphraimAsad](https://github.com/EphraimAsad)
- **Hugging Face:** [huggingface.co/EphAsad](https://huggingface.co/EphAsad)
- **LinkedIn:** [linkedin.com/in/zain-asad-1998eph](https://linkedin.com/in/zain-asad-1998eph)

---

I’m interested in opportunities across **Scientific Software Engineering, Applied AI, Machine Learning, Computer Vision and Laboratory Automation**, particularly where scientific understanding and engineering need to meet.
