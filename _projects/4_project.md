---
layout: page
title: Edge AI Systems, Verification, and Deployment
description: Efficient platforms, benchmarking, and adaptive video analytics for real-world perception.
img: /assets/img/10.jpg
importance: 4
category: work
related_publications: true
---

This project focuses on the part of AI that is often less visible, but decisive in practice: everything that has to work around the model for the model to matter. Real-world perception does not fail only because an algorithm is weak. It fails when data moves inefficiently across hardware, when robustness is assumed instead of measured, and when a deployed system cannot adjust as conditions drift away from the scenario it was trained for.

The first concern is efficiency at the system level. On embedded platforms, performance depends not just on network architecture but on how memory is shared, how CPU and accelerator cooperate, and how software components communicate inside larger robotic or cyber-physical stacks. A perception pipeline that looks good on paper can become unusable if latency, bandwidth, or energy overheads are handled poorly. This project treats those infrastructural details as part of the intelligence of the system, not as afterthoughts.

The second concern is trust. If perception is meant to support healthcare, industrial safety, or autonomous interaction, it has to be tested under the kinds of imperfections that happen outside curated benchmarks: occlusions, low-quality sensing, mismatched domains, and degraded computational settings. That is why verification and benchmarking are central here. The aim is to move from generic accuracy claims to a more realistic understanding of how and when a model remains dependable in the field.

The final concern is adaptation over time. Edge devices are increasingly capable, but they operate in environments that keep changing: lighting shifts, scenes evolve, users behave differently, and the data slowly drifts away from the assumptions baked into the original model. A useful edge-AI system therefore needs to do more than run efficiently once. It needs to decide when quality is slipping, learn with limited resources, and keep improving without constantly handing control back to the cloud.

Seen as a whole, this project is about building perception systems that can survive contact with reality. It connects low-level efficiency, rigorous validation, and lightweight adaptation into a single deployment mindset: models should not only be accurate, but measurable, maintainable, and capable of staying useful over time.

<div style="display: none;" aria-hidden="true">
{% cite de2021efficient %}{% cite aldegheri2024verification %}{% cite Boldo2024CASES %}
</div>
