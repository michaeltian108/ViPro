# Adversarial Video Promotion Against Text-to-Video Retrieval

## Overview
We propose the first **video promotion** attack against Text-to-Video Retrieval (T2VR) to expose an overlooked vulnerability that may be abused for financial gain and widespread (mis)information. See our work at [ArXiv](https://arxiv.org/abs/2508.06964).

## Table of Contents
- [Introduciton](#introduction)
- [Features](#features)
- [Weights](#weights)
- [Update Log](#update-log)
- [To-do](#to-do)
- [Citation](#citation)

## Introduciton
In our work, we pioneer **Vi**deo **Pro**motion (ViPro) as the first attack to adversarially *promote* video ranks regarding selected queries. We further propose **Mo**dality **Re**finement (MoRe) to capture the intricate intra-/inter-modality interaction to boost transferability. MoRe contains: (1) **Temporal Clipping:** Video frames are clustered into video clips based on frame-to-frame similarity. (2) **Semantical Weighting:** For each clip and each query, we calculate its frame-to-frame similarity and frame-to-query similarity using cosine similarity between all frames x and all query tokens. Frames and queries with low similarity are suppressed by their corresponding weights during optimization. (3) **Clip-wise Optimization:** Perturbation are optimized as per clip before outputting the final perturbed video:

<img width="2437" height="811" alt="overview_v2" src="https://github.com/user-attachments/assets/694da61b-f62a-4b26-882e-e2ac2acff6e4" />

## Features
This project features:
1. 📚Mainstream Text-to-Video Retrieval (T2VR) datasets (MSR-VTT, ActivityNet, DiDeMo);
2. 💻Finetuning SOTA models (Cap4Video, DRL).
3. 👿Attacking models with Co-Attack, SGA, and ViPro(ours) under **White-box**, **Grey-box** and **Black-box** settings.
4. 🚀Evaluations under defenses including JPEG and Temporal shuffling.

We now release our checkpoints for reproducibility of the T2VR community. 
Full code will be released after acceptance.


## Weights
*Disclaimer: All open-weighted models are trained using code provided by the authors and we only share weights for reproducibility of T2VR related attacks/defenses.*
We express our sincere thank for the orignal work [DRL](https://github.com/foolwood/DRL) and [Cap4Video](https://github.com/whwu95/Cap4Video).
Using the open-sourced code, we trained both videos on MSR-VTT for our attacks and provided results on MSR-VTT below, click the name of the model for weights downloading:

| Model |  R@1 |  R@5 | R@10 | MR |
| :---- | :---- | :---- | :---- | :---- |
| DRL(Paper) | 47.60% | 73.40% | 81.90% | 2.00 |
| [DRL(Reproduced)](https://drive.google.com/file/d/1WV2ogaelAB3XoP5wxJpkeOq6bINhrdBt/view?usp=sharing) | 46.00% | 72.10% | 81.70% | 2.00 |
| Cap4Video(Paper) | 49.30% | 74.30% | 83.80% | 2.00 |
| [Cap4Video(Reproduceded)](https://drive.google.com/file/d/1D72TP7EElj_2dsb_Q-_z-ZyDj2HUvQiZ/view?usp=sharing) | 47.50% | 73.90% |  82.50% | 2.00 |

## To-do
- Full code will be released upon acceptance.
- ...

## Update Log

### v1.0.0 🎉 07/25/2025
- Initial realase of ViPro.

### v1.1.0 🎉 08/12/2025
- Weight checkpoints for DRL and Cap4Video open sourced.
- Added overview figures and details of our projects.
- Improved readability.

## Citation
If you find this work useful, please cite our paper:
```bibtex
@misc{tian2025adversarialvideopromotiontexttovideo,
      title={Adversarial Video Promotion Against Text-to-Video Retrieval}, 
      author={Qiwei Tian and Chenhao Lin and Zhengyu Zhao and Qian Li and Shuai Liu and Chao Shen},
      year={2025},
      eprint={2508.06964},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2508.06964}, 
}
```
