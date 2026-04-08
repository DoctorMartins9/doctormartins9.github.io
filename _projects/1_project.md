---
layout: page
title: Human Motion Estimation and Filtering
description: A research line on robust human motion intelligence, from noisy pose refinement to sparse sensing and multiview tracking.
img: /assets/img/4.jpg
importance: 1
category: work
related_publications: true
---

This project is about making human motion data trustworthy when the raw signal is anything but clean. Camera-based pose estimation is fast and flexible, but in real environments it is also fragile: joints jitter, limbs disappear behind occlusions, frames are dropped, and the body that comes out of the model is often less coherent than the one that was actually moving. The central question here is how to recover motion that remains believable, stable, and useful even when the observation is partial, noisy, or distributed across different devices.

The answer runs through time as much as through geometry. Instead of treating each frame as an isolated prediction, this line of work models movement as a continuous process with structure, memory, and physical limits. Temporal filtering reduces instability, biomechanical constraints keep the body plausible, and lightweight inference strategies make refinement possible even on edge hardware where latency matters. The goal is not simply to smooth trajectories, but to preserve the meaning of motion while removing the noise that makes it unreliable.

From there, the project widens its scope. One direction explores what can be reconstructed when sensing is intentionally sparse, combining a few body-worn inertial units with a minimal visual stream to recover upper-limb movement without heavy setups or intrusive markers. Another direction scales the same philosophy to multi-view environments, where information arrives from distributed cameras and must be fused into a single motion estimate that stays coherent across viewpoints. In both cases, the challenge is the same: use just enough structure, optimization, and prior knowledge to turn limited observations into dependable motion intelligence.

What ties the whole project together is a practical ambition. These methods are designed for settings where human motion is not an abstract benchmark, but a signal that supports decision-making in healthcare, ergonomics, rehabilitation, and human-centered automation. The broader aim is to make motion analysis robust enough to leave controlled lab conditions and become a real tool in the environments where people actually move.

<div style="display: none;" aria-hidden="true">
{% cite Martini2024_flk %}{% cite Bozzini2024 %}{% cite bozzini2024late %}{% cite martini2025denoising %}{% cite martini2025cometh %}{% cite pompanin2026 %}
</div>
