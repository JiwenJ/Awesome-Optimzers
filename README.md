# Awesome Optimizers List

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/JiwenJ/Awesome-Optimzers?style=flat-square&logo=github)](https://github.com/JiwenJ/Awesome-Optimzers/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](./LICENSE)
[![Papers](https://img.shields.io/badge/Papers-36-b31b1b.svg?style=flat-square&logo=arxiv&logoColor=white)](./data/optimizers.csv)
[![Code Links](https://img.shields.io/badge/Code%20Links-34-2ea44f.svg?style=flat-square&logo=github)](./data/optimizers.csv)
[![Reference Import](https://img.shields.io/badge/Reference%20Import-195-ff8c00.svg?style=flat-square&logo=bookstack&logoColor=white)](./data/reference_catalog.csv)
[![Coverage](https://img.shields.io/badge/Years-2022--2026-6f42c1.svg?style=flat-square&logo=bookstack&logoColor=white)](./data/optimizers.csv)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/JiwenJ/Awesome-Optimzers/pulls)

Here is a curated list of modern optimizers and their corresponding papers, codebases, and practical advantages.

Current scope:

- Start from `2022`
- Order by time in reverse chronological order
- Focus on deep learning and LLM-related optimizers
- `GitHub` is optional; entries without a public implementation are still included

> Main curated table: [data/optimizers.csv](./data/optimizers.csv)
>
> Supplementary reference import: [data/reference_catalog.csv](./data/reference_catalog.csv)
> This file contains `195` additional `2022+` optimizer-related entries imported from the reference materials, including papers without public code links.

| Optimizer Name | Paper | Date | GitHub | Advantages |
| --- | --- | --- | --- | --- |
| Spectral Sphere Optimizer (SSO) | [Controlled LLM Training on Spectral Sphere](https://arxiv.org/abs/2601.08393) | 2026-01 | [Unakar/Spectral-Sphere-Optimizer](https://github.com/Unakar/Spectral-Sphere-Optimizer) | Enforces spectral constraints on both weights and updates, improving stability and outperforming AdamW and Muon in reported LLM pretraining runs. |
| SPlus | [A Stable Whitening Optimizer for Efficient Neural Network Training](https://arxiv.org/abs/2506.07254) | 2025-06 | [kvfrans/splus](https://github.com/kvfrans/splus) | Uses stable whitening-style preconditioning to cut both gradient steps and wall-clock time in reported transformer training runs. |
| Dion | [Dion: Distributed Orthonormalized Updates](https://arxiv.org/abs/2504.05295) | 2025-04 | [microsoft/dion](https://github.com/microsoft/dion) | Distributed orthonormalized updates that retain Muon-style gains while lowering large-scale training overhead. |
| D-Muon | [Muon is Scalable for LLM Training](https://arxiv.org/abs/2502.16982) | 2025-02 | [MoonshotAI/Moonlight](https://github.com/MoonshotAI/Moonlight) | Scales Muon-style orthogonalized updates to distributed LLM training and reports strong compute-efficiency gains over AdamW. |
| Scion | [Training Deep Learning Models with Norm-Constrained LMOs](https://arxiv.org/abs/2502.07529) | 2025-02 | [LIONS-EPFL/scion](https://github.com/LIONS-EPFL/scion) | Norm-constrained LMO updates improve stability, memory efficiency, and hyperparameter transfer across model sizes. |
| Muon | [Muon: An optimizer for the hidden layers of neural networks](https://kellerjordan.github.io/posts/muon/) | 2024-12 | [KellerJordan/Muon](https://github.com/KellerJordan/Muon) | Uses orthogonalized matrix updates for hidden-layer weights and is commonly paired with AdamW for embeddings and heads. |
| Cautious Optimizers | [Cautious Optimizers: Improving Training with One Line of Code](https://arxiv.org/abs/2411.16085) | 2024-11 | [kyleliang919/C-Optim](https://github.com/kyleliang919/C-Optim) | A one-line cautious mask that can make AdamW-, Lion-, and momentum-style optimizers more stable and robust. |
| MARS | [MARS: Unleashing the Power of Variance Reduction for Training Large Models](https://arxiv.org/abs/2411.10438) | 2024-11 | [AGI-Arena/MARS](https://github.com/AGI-Arena/MARS) | Injects variance reduction into AdamW-, Lion-, and Shampoo-style updates and reports clear GPT-2 training gains. |
| ADOPT | [ADOPT: Modified Adam Can Converge with Any β2 with the Optimal Rate](https://arxiv.org/abs/2411.02853) | 2024-11 | [iShohei220/adopt](https://github.com/iShohei220/adopt) | A drop-in Adam-family variant with stronger convergence guarantees and improved practical stability. |
| SOAP | [SOAP: Improving and Stabilizing Shampoo using Adam](https://arxiv.org/abs/2409.11321) | 2024-09 | [nikhilvyas/SOAP](https://github.com/nikhilvyas/SOAP) | Blends Shampoo-style preconditioning with Adam-style moment updates for stronger large-batch optimization. |
| AdEMAMix | [AdEMAMix](https://arxiv.org/abs/2409.03137) | 2024-09 | [apple/ml-ademamix](https://github.com/apple/ml-ademamix) | Mixes long-horizon EMA information into AdamW and improves training efficiency for large language models. |
| Adam-mini | [Adam-mini](https://arxiv.org/abs/2406.16793) | 2024-06 | [zyushun/Adam-mini](https://github.com/zyushun/Adam-mini) | Reduces optimizer memory by sharing update statistics across parameter groups while preserving AdamW-like quality. |
| SF-AdamW (Schedule-Free) | [The Road Less Scheduled](https://arxiv.org/abs/2405.15682) | 2024-05 | [facebookresearch/schedule_free](https://github.com/facebookresearch/schedule_free) | Removes explicit learning-rate schedules and simplifies tuning while keeping AdamW-style behavior. |
| MicroAdam | [MicroAdam](https://arxiv.org/abs/2405.15593) | 2024-05 | [IST-DASLab/MicroAdam](https://github.com/IST-DASLab/MicroAdam) | Compresses Adam-style state updates to reduce memory pressure while keeping competitive convergence. |
| FAdam | [FAdam: Adam is a natural gradient optimizer using diagonal empirical Fisher information](https://arxiv.org/abs/2405.12807) | 2024-05 | [lessw2020/fadam_pytorch](https://github.com/lessw2020/fadam_pytorch) | Uses diagonal empirical Fisher preconditioning to make Adam behave more like a lightweight natural-gradient optimizer. |
| AGD | [AGD: an Auto-switchable Optimizer using Stepwise Gradient Difference for Preconditioning Matrix](https://arxiv.org/abs/2312.01658) | 2023-12 | [intelligent-machine-learning/dlrover](https://github.com/intelligent-machine-learning/dlrover/tree/master/atorch/atorch/optimizers) | Auto-switches preconditioning based on stepwise gradient differences to balance adaptivity and efficiency. |
| AdaLOMO | [AdaLomo: Low-memory Optimization with Adaptive Learning Rate](https://arxiv.org/abs/2310.10195) | 2023-10 | [OpenLMLab/LOMO](https://github.com/OpenLMLab/LOMO) | Extends LOMO with adaptive learning rates for memory-constrained full-parameter LLM fine-tuning. |
| AdaPlus | [AdaPlus](https://arxiv.org/abs/2309.01966) | 2023-09 | [guanleics/AdaPlus](https://github.com/guanleics/AdaPlus) | Adds Nesterov momentum and finer stepsize control on top of AdamW-style optimization. |
| CoRe | [CoRe Optimizer: An All-in-One Solution for Machine Learning](https://arxiv.org/abs/2307.15663) | 2023-07 | [ReiherGroup/CoRe_optimizer](https://github.com/ReiherGroup/CoRe_optimizer) | Proposes a single optimizer intended to work robustly across tasks with less hyperparameter retuning. |
| Adam+CM | [Promoting Exploration in Memory-Augmented Adam using Critical Momenta](https://arxiv.org/abs/2307.09638) | 2023-07 | [chandar-lab/CMOptimizer](https://github.com/chandar-lab/CMOptimizer) | Adds critical momenta to Adam-style updates to encourage exploration and help escape sharp or poor minima. |
| CAME | [CAME: Confidence-guided Adaptive Memory Efficient Optimization](https://arxiv.org/abs/2307.02047) | 2023-07 | [yangluo7/CAME](https://github.com/yangluo7/CAME) | Reduces optimizer-state cost for large models while preserving the benefits of adaptive optimization. |
| LOMO | [Full Parameter Fine-tuning for Large Language Models with Limited Resources](https://arxiv.org/abs/2306.09782) | 2023-06 | [OpenLMLab/LOMO](https://github.com/OpenLMLab/LOMO) | Fuses gradient computation and parameter updates to enable low-memory full-parameter LLM fine-tuning. |
| Prodigy | [Prodigy](https://arxiv.org/abs/2306.06101) | 2023-06 | [konstmish/prodigy](https://github.com/konstmish/prodigy) | A parameter-free optimizer derived from D-Adaptation that reduces or removes learning-rate tuning. |
| DoWG | [DoWG Unleashed: An Efficient Universal Parameter-Free Gradient Descent Method](https://arxiv.org/abs/2305.16284) | 2023-05 | [AMorporkian/DoWG](https://github.com/AMorporkian/DoWG) | A universal parameter-free gradient method that extends DoG-style step-size adaptation with stronger empirical performance. |
| Sophia | [Sophia](https://arxiv.org/abs/2305.14342) | 2023-05 | [Liuhong99/Sophia](https://github.com/Liuhong99/Sophia) | A practical stochastic second-order optimizer for language-model pretraining with modest overhead. |
| WSAM | [Sharpness-Aware Minimization Revisited: Weighted Sharpness as a Regularization Term](https://arxiv.org/abs/2305.15817) | 2023-05 | [intelligent-machine-learning/dlrover](https://github.com/intelligent-machine-learning/dlrover/tree/master/atorch/atorch/optimizers) | Revisits SAM with weighted sharpness to improve generalization while keeping optimization practical. |
| UAdam | [UAdam: Unified Adam-Type Algorithmic Framework for Non-Convex Stochastic Optimization](https://arxiv.org/abs/2305.05675) | 2023-05 | - | Unifies Adam-type methods in one framework and studies convergence behavior under a broad non-convex stochastic setting. |
| FOSI | [FOSI: Hybrid First and Second Order Optimization](https://arxiv.org/abs/2302.08484) | 2023-02 | [hsivan/fosi](https://github.com/hsivan/fosi) | Combines first-order optimizers with second-order curvature information for faster convergence on difficult objectives. |
| DoG | [DoG is SGD's Best Friend: A Parameter-Free Dynamic Step Size Schedule](https://arxiv.org/abs/2302.12022) | 2023-02 | [formll/dog](https://github.com/formll/dog) | Provides a parameter-free dynamic step-size schedule that makes SGD-style optimization far less tuning-sensitive. |
| Lion | [Symbolic Discovery of Optimization Algorithms](https://arxiv.org/abs/2302.06675) | 2023-02 | [google/automl/lion](https://github.com/google/automl/tree/master/lion) | Uses sign-based momentum updates to offer a lightweight alternative to AdamW. |
| D-Adaptation | [D-Adaptation](https://arxiv.org/abs/2301.07733) | 2023-01 | [facebookresearch/dadaptation](https://github.com/facebookresearch/dadaptation) | Learning-rate-free optimization for SGD, Adam, and AdaGrad variants with less manual tuning. |
| VeLO | [VeLO: Training Versatile Learned Optimizers by Scaling Up](https://arxiv.org/abs/2211.09760) | 2022-11 | [google/learned_optimization](https://github.com/google/learned_optimization/tree/main/learned_optimization/research/general_lopt) | A learned optimizer trained at scale to transfer across tasks and architectures better than small learned optimizers. |
| Amos | [Amos](https://arxiv.org/abs/2210.11693) | 2022-10 | [google-research/jestimator](https://github.com/google-research/jestimator) | Introduces scale-aware adaptive decay and weight decay for Adam-style optimization. |
| AdaNorm | [AdaNorm](https://arxiv.org/abs/2210.06364) | 2022-10 | [shivram1987/AdaNorm](https://github.com/shivram1987/AdaNorm) | Stabilizes adaptive optimization by correcting gradient-norm scaling behavior. |
| Adan | [Adan: Adaptive Nesterov Momentum Algorithm](https://arxiv.org/abs/2208.06677) | 2022-08 | [sail-sg/Adan](https://github.com/sail-sg/Adan) | Uses adaptive Nesterov momentum to speed up and stabilize deep-model training. |
| GradaGrad | [Grad-GradaGrad? A Non-Monotone Adaptive Stochastic Gradient Method](https://arxiv.org/abs/2206.06900) | 2022-06 | - | Proposes a non-monotone adaptive stochastic gradient method aimed at improving practical convergence over monotone variants. |

## Notes

- This list is paper-first; public implementations are linked when available.
- Some entries link to the most canonical public implementation rather than a dedicated repo.
- The README table stays curated for readability; broader reference-only coverage lives in [data/reference_catalog.csv](./data/reference_catalog.csv).
- Broad survey repos such as `APRIL-AIGC/Awesome-Optimizer` also include optimizer-adjacent methods; this table keeps the main list focused on optimizers and optimizer families used for training.
- `Muon` and `D-Muon` are listed separately: the original `Muon` entry uses the canonical 2024 write-up, while `D-Muon` refers to the 2025 scalable LLM-training paper.
- Cross-check for missing modern entries was done against [APRIL-AIGC/Awesome-Optimizer](https://github.com/APRIL-AIGC/Awesome-Optimizer), [boshallen/Awesome-Optimizers](https://github.com/boshallen/Awesome-Optimizers?tab=readme-ov-file#awesome-optimizers), [AidinHamedi/Optimizer-Benchmark](https://github.com/AidinHamedi/Optimizer-Benchmark), and [Benchmarking Optimizers for Large Language Model Pretraining](https://arxiv.org/abs/2509.01440).
- New entries should be added in reverse chronological order.
