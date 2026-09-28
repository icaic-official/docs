---
layout: default
title: Syllabus
nav_order: 2
---

# Syllabus

**Updated: 28 September 2026.**

## 1. Foundational Mathematics and Programming

- Linear algebra
- Calculus
- Probability
- Statistics and estimation
- Numerical computation
- Discrete mathematics and graphs
- Python programming
- NumPy and array manipulation
- Pandas and structured data
- Visualization

## 2. Artificial Intelligence Foundations

| Topic | Expected competency |
| --- | --- |
| Intelligent agents | Agents, environments, observations, actions, goals, utility, rationality, and the perception-action loop. |
| Search | Uninformed and heuristic search; completeness, optimality, computational complexity, and the design and evaluation of heuristics. |
| Adversarial search | Reason about competing actions, evaluate game states, reduce unnecessary exploration, and balance search depth against compute cost. |
| Constraint satisfaction | Represent variables, domains, and constraints; find feasible assignments and reduce the search space. |
| Planning | State-space planning, action models, goals, planning graphs, and the relation between planning and search. |
| Knowledge representation and logic | Propositional and first-order logic, inference, rule systems, ontologies, and limitations of symbolic representations. |
| Probabilistic reasoning | Represent dependencies between random variables, perform exact or approximate inference, and update beliefs from sequential observations. |
| Decision theory | Expected utility, risk, value of information, and decisions under uncertainty. |
| Multi-agent systems and game theory | Cooperation, competition, equilibria, basic mechanism design, and decentralized decision making. |

## 3. Machine Learning Foundations and Practice

| Topic | Expected competency |
| --- | --- |
| Prediction tasks | Model continuous targets and class probabilities; understand feature transformations, decision boundaries, residuals, model complexity, and interpretation. |
| Data preparation and feature engineering | Handle missing values, scale inputs, encode categorical data, construct informative features, and build preprocessing and model pipelines. |
| Information theory and learning objectives | Measure uncertainty, information shared between variables, and differences between distributions; relate these quantities to learning objectives. |
| Statistical estimation and uncertainty | Estimate model parameters and predictive uncertainty, incorporate prior knowledge, and account for uncertainty when comparing multiple hypotheses. |
| Optimization | Use gradients to update model parameters, choose how much data to use per update, and diagnose convergence and numerical stability. |
| Regularization | Control model complexity and overfitting through training constraints, data variation, and validation-based model selection. |
| Hyperparameter optimization | Explore hyperparameter settings, allocate search budgets, and decide when to stop trials using validation results. |
| Validation and model evaluation | Separate training, validation, and test data; respect group structure, prevent leakage, isolate the effects of changes, and reproduce experiments. Select metrics for classification, ranking, and regression; assess calibration and subgroup errors. |
| Class imbalance and cost-sensitive learning | Account for unequal class frequencies and error costs when preparing data, defining objectives, and selecting decision thresholds. |
| Semi-supervised and weakly supervised learning | Learn from combinations of labeled, unlabeled, and imperfectly labeled data; assess the reliability of supervision and resulting predictions. |
| Domain shift and generalization | Covariate shift, label shift, domain adaptation, invariance, and robust validation. |
| Efficient data pipelines | Caching, batching, parallel loading, memory mapping, sparse data, and profiling time and memory use. |

## 4. Classical Statistical Learning

| Topic | Expected competency |
| --- | --- |
| Similarity-based prediction | Predict from similar examples; choose distance measures, account for feature scale, and balance local detail against computational cost. |
| Tree-based models and ensembles | Partition feature spaces, control model complexity, handle missing values, and combine predictions from multiple models; assess interpretability and robustness. |
| Margin-based and kernel methods | Understand separation margins, nonlinear similarity functions, decision boundaries, and scaling considerations. |
| Probabilistic classifiers | Model class probabilities and feature distributions, assess assumptions about dependencies, and interpret predictive uncertainty. |
| Clustering | Group similar examples, choose similarity measures and grouping assumptions, handle noise, and assess cluster quality. |
| Dimensionality reduction | Select or transform features into compact representations; assess retained information and the limits of low-dimensional visualizations. |
| Anomaly and novelty detection | Model expected behavior, score departures from it, and select detection thresholds using suitable validation data. |

## 5. Neural Networks and Deep Learning

| Topic | Expected competency |
| --- | --- |
| Feedforward networks | Layered computation, nonlinear representations, approximation capability, and network capacity. |
| Activations and losses | Choose activation functions and training objectives suited to the target and output constraints; understand their effects on gradients and prediction errors. |
| Neural network training and diagnosis | Compute gradients through computational graphs, update parameters, and control update sizes; vary training difficulty or sequence length, and diagnose instability and forgetting using learning curves, gradient behavior, and controlled experiments. |
| PyTorch and CPU/GPU execution | Tensor manipulation, datasets and data loaders, modules, losses, optimizers, training loops, evaluation mode, checkpointing, random seeds, device placement, batch sizes, mixed precision, and memory management. |
| Initialization and normalization | Choose initial parameters and normalize inputs or internal representations; understand their effects on gradient flow and training stability. |
| Embeddings and pooling | Learn representations for text, images, audio, and categorical data; aggregate variable-sized inputs into useful representations. |
| Convolutional networks | Local feature extraction, shared parameters, spatial resolution, receptive fields, and applications to images and time series. |
| Recurrent sequence models | Maintain and update hidden state, process variable-length sequences, and understand how gradients behave over long dependencies. |
| Attention and transformers | Attention-based interactions between inputs, position information, visibility constraints, information flow between layers, and training stability. |
| Reconstruction-based representation learning | Learn compact representations by reconstructing inputs; assess reconstruction quality, robustness to corrupted inputs, and generative use. |
| Transfer learning and fine-tuning | Reuse pretrained representations, prepare adaptation data, and choose which parameters to update under memory and compute constraints; assess transfer quality and loss of previously learned capabilities. |
| Self-supervised representation learning | Construct supervision from data, learn useful similarities and invariances, and evaluate representations on downstream tasks. |

## 6. Reinforcement Learning and Sequential Decision Making

| Topic | Expected competency |
| --- | --- |
| Multi-armed bandits | Balance exploration and exploitation, use uncertainty to guide action selection, and assess cumulative performance relative to the best action. |
| Markov decision processes and value functions | States, actions, transitions, rewards, policies, returns, discounting, and episodic or continuing tasks; relate state and action values to future rewards. |
| Planning with known dynamics | Evaluate and improve policies using known transitions and rewards; understand convergence and computational trade-offs. |
| Value estimation from experience | Estimate future returns from complete or partial trajectories, combine observed rewards with current value estimates, and understand estimation bias and variance. |
| Learning control policies | Improve action selection from experience, distinguish data collected by the current policy from data collected by other policies, and manage exploration. |
| Function approximation and deep RL | Approximate values or policies with neural networks, reuse collected experience, and diagnose instability caused by changing targets and correlated data. |
| Policy optimization | Optimize expected return directly, use value estimates to guide policy updates, reduce update variance, and balance improvement against policy stability. |
| Reward design | Define rewards for goals and constraints, handle sparse feedback, and recognize unintended incentives. |
| Imitation, offline, and model-based RL | Learn from demonstrations or fixed datasets, account for limited data coverage, learn environment dynamics, and plan with imperfect models. |
| RL evaluation and reproducibility | Evaluate across multiple random seeds and episodes; compare return distributions, sample efficiency, and training stability. |
| Multi-agent reinforcement learning | Cooperative and competitive settings, non-stationarity, centralized training, and decentralized execution. |

## 7. Computer Vision

| Topic | Expected competency |
| --- | --- |
| Image processing and augmentation | Pixels, channels, color spaces, spatial resolution, input scaling, and controlled image transformations that preserve valid labels. |
| Image classification | Train and adapt classifiers to assign image-level labels using pretrained image representations. |
| Object detection | Localize and classify objects, represent bounding boxes, handle duplicate predictions, and evaluate localization and recognition quality. |
| Image segmentation | Assign labels to pixels and distinguish object instances; choose suitable training objectives and evaluate region overlap and boundary quality. |
| Generative vision | Learn image distributions, condition generation on inputs, produce samples, and understand limitations of generation quality and evaluation. |
| Video and temporal vision | Frame sampling, temporal pooling, motion features, sequence models, and video classification. |

## 8. Natural Language Processing, Speech, and Audio

| Topic | Expected competency |
| --- | --- |
| Text preprocessing and tokenization | Sentence, word, and subword tokenization, vocabularies, padding, masking, and sequence-length handling. |
| Text representations and encoders | Frequency-based and learned text representations, contextual information, similarity measures, sequence aggregation, and adaptation to downstream tasks. |
| Text classification and sequence labeling | Assign labels to documents or individual tokens; handle label dependencies and align token predictions with the original text. |
| Language modeling and sequence-to-sequence learning | Predict text from preceding or surrounding context, map input sequences to output sequences, assess predictive likelihood, and apply models to translation and summarization. |
| Retrieval and semantic search | Dense and sparse retrieval, embeddings, similarity, reranking, and retrieval evaluation. |
| Audio and signal representations | Waveforms, sampling rate, resampling, framing, time-frequency representations, and normalization. |
| Speech and audio models | Use provided models to recognize, transcribe, or interpret speech and other audio; prepare inputs and evaluate outputs for the task. |

## 9. Foundation Models and Large Language Models

| Topic | Expected competency |
| --- | --- |
| Prompting and context management | Design instructions and examples, organize complex tasks, select relevant context, handle context limits, and evaluate prompt effectiveness. |
| Structured generation and decoding | Choose outputs from predicted distributions, balance diversity and reliability, enforce output constraints, validate and repair outputs, and define stopping criteria. |
| Preference and reinforcement-based adaptation | Learn from preferences and reward signals, optimize model behavior, and assess trade-offs between task performance and adherence to desired behavior. |
| Retrieval-augmented generation | Select and organize retrieved evidence for generation, ground responses in that evidence, and evaluate factual support and citation accuracy. |
| Tool use and agents | Function/tool calling, planning loops, memory, state tracking, environment feedback, and rule-constrained actions. |
| LLM evaluation | Assess output validity, factual accuracy, hallucination, robustness to prompt variations, human preferences, and contamination risks. |
| Inference efficiency | Reduce computation and memory use, process requests efficiently, reuse intermediate results, and balance sequence length, model size, latency, and output quality. |
| Multimodal foundation models | Joint text-image-audio inputs, modality encoders, fusion, prompting, and cross-modal evaluation; image-text similarity, retrieval, and classification using text descriptions. |
| LLM safety and security | Prompt injection, jailbreaks, data leakage, unsafe outputs, tool misuse, and defensive validation. |

## 10. Learning from Time Series, Sequences, and Sensor Data

| Topic | Expected competency |
| --- | --- |
| Sampling and preprocessing | Sampling frequency, windows, overlap, resampling, synchronization, variable-length sequences, event segmentation, filtering, detrending, outliers, and leakage-safe transformations. |
| Statistical and frequency-domain features | Summarize distributions, temporal dependence, periodicity, and signal energy to construct informative features. |
| Classical forecasting | Model trends, seasonality, and dependence on past observations; establish baseline forecasts and assess modeling assumptions. |
| Multi-step forecasting | Use multivariate input sequences to predict individual future values or output sequences; predict multiple steps jointly or feed predictions into later steps, and assess training and inference differences, error accumulation, and horizon selection. |
| Temporal validation and metrics | Respect chronology and event boundaries, evaluate across forecast periods, choose error measures suited to scale and horizon, and prevent leakage. |
| Anomaly and change-point detection | Identify unusual observations in temporal context and changes in behavior over time; distinguish isolated anomalies from sustained shifts. |
| Sequence similarity and alignment | Compare and align sequences while accounting for shifts in timing, phase, and speed; assess the suitability of similarity measures. |
| Learning from sensor and IMU data | Accelerometer/gyroscope data, axes, orientation effects, sensor fusion, activity recognition, and biometric verification. |

## 11. Contest Tasks

### What to Expect

- Tasks involve implementing and adapting solutions, training or using models, producing predictions, or choosing actions in interactive environments within the time and compute budget.
- A task may combine tabular data, images, text, audio, video, time series, sensor streams, or graphs.

### What Not to Expect

- Solving a task simply by applying an off-the-shelf model or method unchanged.
- Questions that depend on memorizing obscure library APIs.

## 12. Recommended Preparation Resources

These resources support preparation. The ICAIC topic tables above define the examinable scope; the recommended reading does not add requirements.

| Resource | Subject |
| --- | --- |
| *Artificial Intelligence: A Modern Approach* — Stuart Russell and Peter Norvig | Classical AI. |
| *The Elements of Statistical Learning* — Trevor Hastie, Robert Tibshirani, and Jerome Friedman | Statistical learning. |
| *Reinforcement Learning: An Introduction* — Richard S. Sutton and Andrew G. Barto | Reinforcement learning. |
| *Deep Learning* — Ian Goodfellow, Yoshua Bengio, and Aaron Courville | Deep learning. |

### Supplementary Resources

- Bishop, C. M., & Bishop, H. (2024). [*Deep Learning: Foundations and Concepts*](https://www.bishopbook.com).
- Murphy, K. P. (2022). [*Probabilistic Machine Learning: An Introduction*](https://probml.github.io/pml-book/book1.html).
- Murphy, K. P. (2023). [*Probabilistic Machine Learning: Advanced Topics*](https://probml.github.io/pml-book/book2.html).
- Jurafsky, D., & Martin, J. H. (2026). [*Speech and Language Processing: An Introduction to Natural Language Processing, Computational Linguistics, and Speech Recognition with Language Models*](https://web.stanford.edu/~jurafsky/slp3).
