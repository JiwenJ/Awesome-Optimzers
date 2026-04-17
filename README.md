# Awesome Optimizers List

Here is a curated list of modern optimizers and their corresponding papers, codebases, and practical advantages.

Current scope:

- Start from `2022`
- Order by time in reverse chronological order
- Focus on deep learning and LLM-related optimizers

> Structured data: [data/optimizers.csv](./data/optimizers.csv)

| Optimizer Name | Paper | Year | GitHub | Advantages |
| --- | --- | --- | --- | --- |
| Dion | [Dion](https://arxiv.org/abs/2504.05295) | 2025 | [microsoft/dion](https://github.com/microsoft/dion) | Distributed orthonormalized updates that retain Muon-style gains while lowering large-scale training overhead. |
| Muon | [Muon](https://arxiv.org/abs/2502.16982) | 2025 | [MoonshotAI/Moonlight](https://github.com/MoonshotAI/Moonlight) | Scales orthogonalized updates to LLM training and improves compute efficiency over strong AdamW baselines. |
| Cautious Optimizers | [Cautious Optimizers](https://arxiv.org/abs/2411.16085) | 2024 | [kyleliang919/C-Optim](https://github.com/kyleliang919/C-Optim) | A one-line cautious mask that can make AdamW-, Lion-, and momentum-style optimizers more stable and robust. |
| SOAP | [SOAP: Improving and Stabilizing Shampoo using Adam](https://arxiv.org/abs/2409.11321) | 2024 | [nikhilvyas/SOAP](https://github.com/nikhilvyas/SOAP) | Blends Shampoo-style preconditioning with Adam-style moment updates for stronger large-batch optimization. |
| AdEMAMix | [AdEMAMix](https://arxiv.org/abs/2409.03137) | 2024 | [apple/ml-ademamix](https://github.com/apple/ml-ademamix) | Mixes long-horizon EMA information into AdamW and improves training efficiency for large language models. |
| Adam-mini | [Adam-mini](https://arxiv.org/abs/2406.16793) | 2024 | [zyushun/Adam-mini](https://github.com/zyushun/Adam-mini) | Reduces optimizer memory by sharing update statistics across parameter groups while preserving AdamW-like quality. |
| Schedule-Free | [The Road Less Scheduled](https://arxiv.org/abs/2405.15682) | 2024 | [facebookresearch/schedule_free](https://github.com/facebookresearch/schedule_free) | Removes explicit learning-rate schedules and simplifies tuning without giving up strong performance. |
| MicroAdam | [MicroAdam](https://arxiv.org/abs/2405.15593) | 2024 | [IST-DASLab/MicroAdam](https://github.com/IST-DASLab/MicroAdam) | Compresses Adam-style state updates to reduce memory pressure while keeping competitive convergence. |
| AdaPlus | [AdaPlus](https://arxiv.org/abs/2309.01966) | 2023 | [guanleics/AdaPlus](https://github.com/guanleics/AdaPlus) | Adds Nesterov momentum and finer stepsize control on top of AdamW-style optimization. |
| CAME | [CAME: Confidence-guided Adaptive Memory Efficient Optimization](https://arxiv.org/abs/2307.02047) | 2023 | [yangluo7/CAME](https://github.com/yangluo7/CAME) | Reduces optimizer-state cost for large models while preserving the benefits of adaptive optimization. |
| Prodigy | [Prodigy](https://arxiv.org/abs/2306.06101) | 2023 | [konstmish/prodigy](https://github.com/konstmish/prodigy) | A parameter-free optimizer derived from D-Adaptation that reduces or removes learning-rate tuning. |
| Sophia | [Sophia](https://arxiv.org/abs/2305.14342) | 2023 | [Liuhong99/Sophia](https://github.com/Liuhong99/Sophia) | A practical stochastic second-order optimizer for language-model pretraining with modest overhead. |
| Lion | [Symbolic Discovery of Optimization Algorithms](https://arxiv.org/abs/2302.06675) | 2023 | [google/automl/lion](https://github.com/google/automl/tree/master/lion) | Uses sign-based momentum updates to offer a lightweight alternative to AdamW. |
| D-Adaptation | [D-Adaptation](https://arxiv.org/abs/2301.07733) | 2023 | [facebookresearch/dadaptation](https://github.com/facebookresearch/dadaptation) | Learning-rate-free optimization for SGD, Adam, and AdaGrad variants with less manual tuning. |
| Amos | [Amos](https://arxiv.org/abs/2210.11693) | 2022 | [google-research/jestimator](https://github.com/google-research/jestimator) | Introduces scale-aware adaptive decay and weight decay for Adam-style optimization. |
| AdaNorm | [AdaNorm](https://arxiv.org/abs/2210.06364) | 2022 | [shivram1987/AdaNorm](https://github.com/shivram1987/AdaNorm) | Stabilizes adaptive optimization by correcting gradient-norm scaling behavior. |
| Adan | [Adan: Adaptive Nesterov Momentum Algorithm](https://arxiv.org/abs/2208.06677) | 2022 | [sail-sg/Adan](https://github.com/sail-sg/Adan) | Uses adaptive Nesterov momentum to speed up and stabilize deep-model training. |

## Notes

- This list favors papers with public implementations.
- Some entries link to the most canonical public implementation rather than a dedicated repo.
- New entries should be added in reverse chronological order.
