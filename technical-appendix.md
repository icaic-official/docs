# Technical Appendix

**Updated: 18 September 2026.**

This appendix applies to **both the Individual Contest and the Team Contest**. Each team shares **one organizer-provided computer or laptop** and receives the same software environment, GPU allocation, and evaluation limits as one individual contestant. Submission quotas are per individual contestant in the Individual Contest and per team in the Team Contest.

## 1. Platform and Development Environment

| Component | Specification |
| --- | --- |
| Contest platform | The contest platform provides access to task statements and datasets, solution submission, final submission selection, and evaluation scores. |
| Operating system | Ubuntu 26.04 LTS |
| Main development environment | JupyterLab 4.6, accessed through the internal contest network, with GPU access for model training. |
| Offline editor | VSCode 1.138 on contestant laptops, without direct GPU access or AI assistance. |
| Python | Python 3.14 |
| Package versions | The provisional pins in section 2; the finalized contest image is identical for all contestants. |

Software versions are provisional pending installation and GPU compatibility validation. The finalized contest image will be published before the contest.

## 2. Available Python Libraries

The contest environment uses the following provisional package versions.

| Category | Package | Version |
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
| Computer vision | `opencv-python` | 5.0 |
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

## 3. AI Assistance

No LLM assistant is provided. LLM-based chat assistants, copilots, browser assistants, and AI coding agents are prohibited, including locally running assistants. External APIs are inaccessible and prohibited.

Task models and pretrained checkpoints may be used only as specified in section 4 and the task statement; their availability does not authorize their use as coding or chat assistants.

## 4. Hardware Resources and Pretrained Models

### 4.1. Laptops

Each individual contestant receives an Ubuntu laptop without a GPU; each team shares one such computer or laptop in the Team Contest. GPU training and execution take place through JupyterLab on the training and evaluation machines.

### 4.2. Training and Evaluation Machines

Training and evaluation use **Amazon EC2 `g6.xlarge`** instances. Each team receives the same compute allocation as one individual contestant:

| Resource | Specification |
| --- | --- |
| GPU | 1 NVIDIA L4 |
| GPU memory | 24 GB nominal (approximately 22 GiB) |
| CPU | 4 vCPUs |
| System memory | 16 GiB |
| Local instance storage | 250 GB NVMe SSD |

### 4.3. Pretrained Models

The approved pretrained-model list will be published later. Approved checkpoints and their required supporting files will be pre-cached in the contest environment. Contestants may use only models explicitly provided by the organizers. External model downloads are prohibited. Documentation for approved models will be available offline.

## 5. Network Access and Offline Resources

**There is no internet access during the contest.** Contestant laptops, training environments, and the grading system can access only internal contest services. There is no external website whitelist.

Required datasets, approved model files, and documentation are provided within the contest environment. External preparation resources are not accessible during the contest.

## 6. Evaluation Limits

| Limit | Rule |
| --- | --- |
| Notebook runtime | Maximum **10 minutes per submission**, unless the task statement explicitly states otherwise |
| Submissions | Maximum **15 submissions per task per individual contestant or team**, according to the contest |
| Submission accounting | All submissions count, including failed submissions, except those affected by a platform-side problem |
| Concurrent submissions | Permitted; submissions enter a queue and results appear when ready |
| End of contest | Submissions received before the contestant's deadline continue to run, including queued submissions, after the contest ends |

The runtime limit applies to each evaluation run of a submission, including any training, model loading, preprocessing, and inference performed within that run. It does not impose a cumulative 20-minute training budget on the contestant's development environment.

## 7. Additional Rules

- Access to networks outside the internal contest services is prohibited.
- Messaging, collaboration, and file-sharing services are prohibited.
- Attempts to bypass platform restrictions are prohibited.
- The approved pretrained-model list and finalized contest image will be published before the contest.