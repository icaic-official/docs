---
layout: default
title: Technical Appendix
nav_order: 4
---

# Technical Appendix

**Updated: 17 November 2026.**

This appendix applies to **both the Individual Contest and the Team Contest**. Each team receives the same resources and limits as one individual contestant.

## 1. Platform and Development Environment

| Component | Specification |
| --- | --- |
| Contest platform | Provides task statements, datasets, solution submission, final submission selection, and evaluation scores. |
| Operating system | Ubuntu 26.04 LTS |
| Main development environment | JupyterLab 4.6, accessed through the internal contest network, with GPU access on the training and evaluation machines. |
| Python | Python 3.13 |

## 2. Available Python Packages

The listed version families may change following installation and GPU compatibility testing. Final package versions will be published before the contest. Within each contest, all participants use the same software environment.

| Category | Package | Version family |
| --- | --- | --- |
| Core AI/ML | `torch` | 2.14 |
| Core AI/ML | `torchvision` | 0.29 |
| Core AI/ML | `torchaudio` | 2.11 |
| Core AI/ML | `transformers` | 5.17 |
| Core AI/ML | `accelerate` | 1.15 |
| Core AI/ML | `peft` | 0.21 |
| Core AI/ML | `trl` | 1.13 |
| Core AI/ML | `scikit-learn` | 1.9 |
| Core AI/ML | `xgboost` | 3.4 |
| Core AI/ML | `lightgbm` | 4.7 |
| Core AI/ML | `catboost` | 1.2 |
| Core AI/ML | `sentence-transformers` | 6.0 |
| Core AI/ML | `datasets` | 5.0 |
| Core AI/ML | `evaluate` | 0.4 |
| Core AI/ML | `spacy` | 3.8 |
| Core AI/ML | `nltk` | 3.10 |
| Core AI/ML | `gensim` | 4.4 |
| Data processing | `numpy` | 2.5 |
| Data processing | `pandas` | 3.0 |
| Data processing | `scipy` | 1.18 |
| Data processing | `polars` | 1.44 |
| Data processing | `pyarrow` | 25.0 |
| Data processing | `h5py` | 3.16 |
| Computer vision | `opencv-python-headless` | 5.0 |
| Computer vision | `Pillow` | 12.3 |
| Computer vision | `scikit-image` | 0.26 |
| Computer vision | `albumentations` | 2.0 |
| Visualization | `matplotlib` | 3.11 |
| Visualization | `seaborn` | 0.13 |
| Visualization | `plotly` | 7.1 |
| Utilities/training | `tqdm` | 4.70 |
| Utilities/training | `joblib` | 1.6 |
| Utilities/training | `tensorboard` | 2.21 |
| Utilities/training | `pytorch-lightning` | 2.6 |
| Utilities/training | `pydantic` | 2.13 |
| Utilities/training | `pyyaml` | 6.0 |
| Development | `jupyterlab` | 4.6 |

The Python standard library may also be used. Installing additional packages during the contest is prohibited. **TensorFlow and Keras are unavailable.**

## 3. Hardware Resources and Pretrained Models

### 3.1. Laptops

Each individual contestant or team receives **one Ubuntu laptop without a GPU**. In the Team Contest, all three contestants share the laptop.

### 3.2. Training and Evaluation Machines

Training and evaluation use **Amazon EC2 `g4dn.2xlarge`** instances:

| Resource | Specification |
| --- | --- |
| GPU | 1 NVIDIA T4 |
| GPU memory | 16 GB nominal (approximately 15 GiB) |
| CPU | 8 vCPUs |
| System memory | 32 GiB |
| Local instance storage | 225 GB NVMe SSD |

Each individual contestant or team has a dedicated GPU allocation for development.

### 3.3. Pretrained Models

There are no pretrained models provided for the contest.

## 4. Offline Resources

Required datasets and documentation are provided within the contest environment. Offline documentation is available through DevDocs for all listed packages.

## 5. Submission and Evaluation

| Limit | Rule |
| --- | --- |
| Evaluation runtime | Maximum **10 minutes per evaluation run**, unless the task statement explicitly states otherwise |
| Submissions | Maximum **15 submissions per task per individual contestant or team** |
| Upload size | **100 MB hard limit per submission**; tasks may set lower limits |

**Notes:**

- Multiple submissions may be queued concurrently.
- Runtime limits use wall-clock time and include training, model loading, preprocessing, and inference within the evaluation run.
- Submitted files are fixed at submission time; later edits do not affect them.
- Task statements specify submission requirements and evaluation procedures.
