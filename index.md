---
layout: default
title: Large-scale 3D Semantic Occupancy Prediction on NuPlan-Occ for Autonomous Driving @ WACV 2026
description: Promoting Discriminative and Generative Methods for Dynamic Scene Understanding
---

:wave: Welcome to the **Large-scale 3D Semantic Occupancy Prediction Challenge** organized at :wave:
[<img class="rounded-rect" src="assets/imgs/wacv2026.png" width="420px" alt="WACV 2026"/>](https://wacv2026.thecvf.com)
{: .text-center}

**WACV 2026 Workshop / Challenge Info:** _TBA (date, venue, online link)_
{: .text-center}

[News](#news)
[Important Dates](#dates)
[Overview](#overview)
[Task](#task)
[Dataset](#dataset)
[Evaluation](#evaluation)
[Baseline](#baseline)
[Awards](#awards)
[Citations](#citations)
[Organizers](#organizers)

---

<div class="container">
  <img class="rounded-rect" src="assets/imgs/nuplan_occ/fig_01.PNG" alt="NuPlan-Occ overview figure"/>
</div>
{: .text-center}

<div class="container">
  <img class="rounded-rect" src="assets/imgs/nuplan_occ/fig_02.PNG" alt="OpenScene vs NuPlan-Occ comparison"/>
</div>
{: .text-center}

---

## :page_facing_up: **Paper** {#paper}

- **Paper & Dataset Curation (arXiv)**: https://arxiv.org/abs/2510.22973
- **Project / Code (UniScene v2)**: https://github.com/Arlo0o/UniScene-Unified-Occupancy-centric-Driving-Scene-Generation/tree/v2

## :tv: **Video** {#video}

#### Coming soon...

---

## :newspaper: **News** {#news}

- **TBA ---** :tada: Website is live!
- **TBA ---** :package: NuPlan-Occ dataset release & baseline code available.
- **TBA ---** :bar_chart: Evaluation server / leaderboard opens.

---

## :hourglass_flowing_sand: **Important Dates** {#dates}

- **TBA ---** Challenge **Opens** (Dev / Validation)
- **TBA ---** Challenge **Opens** (Final / Test)
- **TBA ---** Challenge Submission **Closes**
- **TBA ---** Winner Notification
- **TBA ---** Workshop @ **WACV 2026**

---

## 📌 **Overview** {#overview}

Semantic occupancy prediction is a cornerstone of 3D scene understanding in autonomous driving, providing dense, voxel-level semantic and geometric representations of dynamic environments. Despite recent advances, large-scale, high-resolution occupancy datasets remain scarce, limiting the development and evaluation of robust models.

This challenge introduces **NuPlan-Occ**, the largest publicly available semantic occupancy dataset to date, featuring **3.6 million frames** with high-resolution voxel annotations (**400 × 400 × 32**). Derived from the widely adopted NuPlan benchmark, NuPlan-Occ enables scalable training and evaluation of both discriminative and generative models for 3D scene understanding.

We invite researchers to develop and submit models for 3D semantic occupancy prediction, with the goal of advancing state-of-the-art performance in accuracy, scalability, and generalization.

<div class="container">
  <img class="rounded-rect" src="assets/imgs/nuplan_occ/fig_03.PNG" alt="Dataset comparison table"/>
</div>
{: .text-center}

---

## 🎯 **Task** {#task}

Participants are tasked with predicting **3D semantic occupancy grids** from **multi-view camera images**.

The occupancy grid is defined over a predefined spatial volume with 9 semantic classes including:

`vehicle, pedestrian, bicycle, traffic_cone, barrier, czone_sign, generic_object, background, empty`

**Two tracks are supported:**
- **Discriminative Track:** Predict occupancy from input images.
- **Generative Track:** Forecast occupancy sequences or complete partial scenes.

---

## 📊 **Dataset: NuPlan-Occ** {#dataset}

- **Source:** Built from the NuPlan dataset, with dense 3D semantic annotations.
- **Scale:** 19K scenes, 3.6M frames.
- **Resolution:** (400 × 400 × 32) voxels.
- **Annotations:** 10 semantic classes, with foreground/background separation.
- **Modalities:** Multi-view RGB images, LiDAR point clouds, BEV maps, and semantic occupancy grids.

### Access
- HuggingFace: https://huggingface.co/datasets/Arlolo0/Nuplan-Occupancy  
- GitHub: https://github.com/Arlo0o/UniScene-Unified-Occupancy-centric-Driving-Scene-Generation/tree/v2  
- Paper & Dataset Curation: https://arxiv.org/abs/2510.22973

<div class="container">
  <img class="rounded-rect" src="assets/imgs/nuplan_occ/fig_04.PNG" alt="Dense reconstruction and labeling pipeline"/>
</div>
{: .text-center}

---

## ⚙️ **Evaluation** {#evaluation}

**Primary Metric:** mean Intersection-over-Union (**mIoU**) across all semantic classes.

**Secondary Metrics:**
- Per-class IoU
- Precision & Recall

Evaluation code is released in the GitHub repository under the `SOP/` directory:  
https://github.com/Arlo0o/UniScene-Unified-Occupancy-centric-Driving-Scene-Generation/tree/v2/SOP/monoscene#3-evaluation

### 📝 Evaluation Guidelines
- **Validation Phase:** Participants can evaluate on a public validation set via our evaluation script.
- **Reproducibility:** Submitted code must include a README with training and inference instructions.
- **Paper Submission:** Top-performing teams will be invited to submit a short paper (4–6 pages) to the WACV 2026 workshop proceedings.

---

## 🏆 **Baseline & Benchmark** {#baseline}

We provide a reproduced baseline using **MonoScene** trained on **NuPlan-Occ miniset**:

| Metric | Value |
|---|---:|
| Precision | 48.99 |
| Recall | 42.54 |
| IoU | 29.49 |
| mIoU | 9.36 |

**Per-class IoU:**  
background: 29.0124, vehicle: 17.6694, bicycle: 0.4056, pedestrian: 6.4708, traffic_cone: 1.8878, barrier: 2.8173, czone_sign: 2.7924, generic_object: 13.8316

**Baseline Code & Pretrained Model:**  
Released in the GitHub repository under the `SOP/` directory.  
https://github.com/Arlo0o/UniScene-Unified-Occupancy-centric-Driving-Scene-Generation/tree/v2/SOP/monoscene

---

## 🏅 **Awards & Recognition** {#awards}

- 1st, 2nd, 3rd Place certificates and awards (sponsors TBD).
- Best Paper Award for the most innovative method.
- Top teams will be invited to present at the WACV 2026 workshop.
- Results will be published on the challenge website.

---

## 📚 **Recommended Readings & Citations** {#citations}

Participants are encouraged to cite the following works:

```bibtex
@inproceedings{li2025uniscene,
  title={Uniscene: Unified occupancy-centric driving scene generation},
  author={Li, Bohan and Guo, Jiazhe and Liu, Hongsi and Zou, Yin...u and Tan, Feiyang and Zhang, Chi and Wang, Tiancai and others},
  booktitle={Proceedings of the Computer Vision and Pattern Recognition Conference},
  pages={11971--11981},
  year={2025}
}

@article{li2025scaling,
  title={Scaling Up Occupancy-centric Driving Scene Generation: Dataset and Method},
  author={Li, Bohan and Jin, Xin and Zhu, Hu and Liu, Hongsi and... Kaiwen and Ma, Chao and Jin, Yueming and Zhao, Hao and others},
  journal={arXiv preprint arXiv:2510.22973},
  year={2025}
}
