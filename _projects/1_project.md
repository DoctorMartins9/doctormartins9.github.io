---
layout: page
title: Human Motion Estimation and Filtering
description: Robust pose filtering, multiview tracking, and sparse-sensor motion inference.
img: /assets/img/4.jpg
importance: 1
category: work
related_publications: true
---

This research track groups the papers in `papers/project_1` around robust human motion estimation under noisy, partial, or distributed observations.
The common thread is making motion pipelines stable enough for real-time use, from learned kinematic filters to multiview tracking and sparse wearable sensing.

Representative papers in this track include:

- 2024: {% cite Martini2024_flk %}
- 2024: {% cite Bozzini2024 %}
- 2024: {% cite bozzini2024late %}
- 2025: {% cite martini2025denoising %}
- 2026: {% cite martini2025cometh %}
- 2026: {% cite pompanin2026 %}

Current focus areas:

- real-time denoising for 3D pose estimation
- multiview estimation and tracking of humans
- sparse visual-inertial sensing for upper-limb motion
- edge-ready motion-analysis pipelines

Papers currently stored in this folder:

- [FLK: A filter with learned kinematics for real-time 3D human pose estimation (2024)]({{ '/papers/project_1/2024_FLK.pdf' | relative_url }})
- [A real-time diffusion-based filter for human pose estimation on edge devices, IROS (2024)]({{ '/papers/project_1/2024_IROS.pdf' | relative_url }})
- [Late Breaking Results: A real-time diffusion-based filter for human pose estimation on edge devices, DAC (2024)]({{ '/papers/project_1/2024_LBR_DAC.pdf' | relative_url }})
- [Denoising and completion filters for human motion software: A survey with code (2025)]({{ '/papers/project_1/2025_CSR.pdf' | relative_url }})
- [Upper-Limb Pose Estimation from Sparse Body-Worn Visual-Inertial Sensors, preprint (2025)]({{ '/papers/project_1/2025_SPL-preprint.pdf' | relative_url }})
- [COMETH: Convex optimization for multiview estimation and tracking of humans (2026)]({{ '/papers/project_1/2026_COMETH.pdf' | relative_url }})
