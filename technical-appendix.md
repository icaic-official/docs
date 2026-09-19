# Technical Appendix

> [!CAUTION]
> **This appendix is not finalized.** Specifications and limits are provisional. The appendix will be finalized no later than one month before the contest.

**Updated: 19 September 2026.**

This appendix applies to **both the Individual Contest and the Team Contest**. Each team receives the same resources and limits as one individual contestant.

## 1. Platform and Development Environment

| Component | Specification |
| --- | --- |
| Contest platform | Provides task statements, datasets, solution submission, final submission selection, and evaluation scores. |
| Operating system | Ubuntu 26.04 LTS |
| Main development environment | JupyterLab 4.6, accessed through the internal contest network, with GPU access on the training and evaluation machines. |
| Offline editor | VSCode 1.138 on contestant laptops, without direct GPU access. |
| Python | Python 3.13 |

## 2. Available Python Libraries

The listed version families may change following installation and GPU compatibility testing. Final package versions will be published with the finalized contest image before the contest. The finalized image is identical for all contestants.

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

Each individual contestant or team receives **one Ubuntu laptop without a GPU**, shared by all three contestants in the Team Contest.

### 3.2. Training and Evaluation Machines

Training and evaluation use **Amazon EC2 `g6.xlarge`** instances:

| Resource | Specification |
| --- | --- |
| GPU | 1 NVIDIA L4 |
| GPU memory | 24 GB nominal (approximately 22 GiB) |
| CPU | 4 vCPUs |
| System memory | 16 GiB |
| Local instance storage | 250 GB NVMe SSD |

### 3.3. Pretrained Models

The approved pretrained-model list will be published before the contest. Approved checkpoints and their required supporting files will be pre-cached in the contest environment. Contestants may use only models explicitly provided by the organizers. Documentation for approved models will be available offline.

Task models and pretrained checkpoints may be used only as specified here and in the task statement. They may not be used as coding or chat assistants.

## 4. Offline Resources

Required datasets and documentation are provided within the contest environment.

## 5. Evaluation Limits

| Limit | Rule |
| --- | --- |
| Notebook runtime | Maximum **10 minutes per submission**, unless the task statement explicitly states otherwise |
| Submissions | Maximum **15 submissions per task per individual contestant or team** |
| Submission accounting | All submissions count, including failed submissions, except those affected by a platform-side problem |
| Concurrent submissions | Permitted; submissions enter a queue and results appear when ready |

Runtime limits are measured in wall-clock time. The per-submission limit applies to each evaluation run, including any training, model loading, preprocessing, and inference performed within that run.
