---
layout: page
title: Turning Phone-Surface Contacts into Probabilistic Landmarks for Indoor Localization
description: Submitted to Sensys '26
tag: • Indoor Localization, Smartphone Sensing, IMU, Ubiquitous Computing
img: assets/img/STEP/overview.png
importance: 2
category: Research Projects
---

2026  
*Xiangjie Tang, **Ziqi Liu**, Minhao Cui, Qijia Shao*

<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/STEP/overview.png" title="overview" class="img-fluid rounded" %}
    </div>
</div>
<br>

Fine-grained localization within everyday rooms is useful for context-aware mobile and ubiquitous applications (e.g., personal health), yet remains difficult without deployed sensing infrastructure. Smartphone Pedestrian Dead Reckoning (PDR) offers an attractive alternative by estimating relative motion from on-device motion sensors, but its error accumulates quickly without periodic correction. We present STEP, an indoor localization system that relies solely on IMU sensors and calibrates them in a closed loop. Its key insight is to leverage incidental phone-surface contact events from daily activities, recognizing the contacted surface materials so they can serve as probabilistic physical landmarks for improved PDR. To realize this, STEP first uses latent structural features to isolate the contact events, which are easily overwhelmed by other activities in low-sampling-rate IMU data. It then applies domain-adversarial and few-shot learning to recognize surface materials consistently across varying user behaviors. Finally, to handle environments with multiple objects of the same material, STEP introduces an adaptive particle filter that fuses PDR trajectories with material recognition probabilities. In experiments across 8 users, 2 environments, and 20 km of walking traces, STEP achieves a mean localization error of 8.88 m and 3.89 m in 2 scenarios, reducing error by 53.1% and 52.6% over PDR. These results show that sequences of uncertain contact observations can provide practical closed-loop correction for smartphone-based indoor localization.
