---
layout: page
title: Human-Robot Collaboration and Industrial Safety
description: Real-time perception, robust tracking, and collision prediction for shared industrial workcells.
img: /assets/img/9.jpg
importance: 3
category: work
related_publications: true
---

This project is about giving industrial environments a better sense of anticipation. In shared workcells, safety is not only a matter of reacting quickly when a person and a robot get too close. It depends on understanding what is happening in the scene, how both actors are moving, and whether the current interaction is drifting toward a risky configuration before that risk becomes immediate.

That requires perception that is both rich and reliable. People have to be localized and tracked in spaces where occlusions are common, viewpoints are partial, and computation is often distributed across edge devices rather than concentrated on a single workstation. For that reason, the project treats sensing as an active part of safety: multi-camera setups, stable pose estimation, and robust motion filtering are not background components, but the foundation that makes any predictive layer believable.

On top of perception, the work adds a second kind of intelligence: reasoning about intent and process. Industrial robots often operate through recurring plans and structured sequences, which means that safety can improve when the system does more than extrapolate trajectories. By learning patterns of motion and combining them with human occupancy in the workspace, the project moves from monitoring to forecasting. The question shifts from “where is everyone now?” to “what is likely to happen next, and how early can we know it?”

The result is a vision of human-robot collaboration where safety is proactive rather than purely defensive. Instead of isolating people from automation, the aim is to support shared spaces in which interaction remains efficient, understandable, and trustworthy. In that setting, prediction is not an extra feature layered on top of perception, but the natural continuation of a system that has learned to read the workspace as it unfolds.

<div style="display: none;" aria-hidden="true">
{% cite geretti2022process %}{% cite boldo2024real %}{% cite Martini2024 %}{% cite geretti2025collision %}
</div>
