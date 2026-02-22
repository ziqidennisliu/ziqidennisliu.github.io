---
layout: page
title: PreTap：Implicit Reachability Analysis and Tap Prediction for One-handed Mobile Interaction
description:  Submitted to ACM IMWUT 2026
tag: • Natural Interaction, Ubiquitous Computing, Mobile Devices, Personalization
img: assets/img/Pretap/headfig.jpg
importance: 1
category: Research Projects
---

2024  
***Ziqi Liu**, Ziyi Xu, Jinhe Wen, Xiangjie Tang, Qijia Shao*  

<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Pretap/headfig.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<br>
One-handed interaction on large-screen smartphones often leads to ergonomic discomfort and disruption, while existing solutions typically rely on explicit gestures, additional hardware, or static ergonomic models, limiting their deployability and adaptability. We present PreTap, an anticipatory system that predicts imminent tap regions and implicitly infers reachability from zero-permission inertial signals, enabling proactive interface adaptation during the pre-tap phase. 

Leveraging the proposed lightweight (180K-parameter) hybrid CNN–Attention architecture and unsupervised reachability analysis, PreTap characterizes user-specific unreachable regions from IMU motion signatures, achieving 93.47% unreachable coverage and 97.40% easy-zone coverage without explicit calibration. An empirical study (N=50) on commodity devices demonstrates high robustness: PreTap achieves an F1 score of 88.25% for proactive UI adaptation and 95.91% strategy accuracy, with an average prediction lead time of 220 ms. Furthermore, the proposed model exhibits high sample efficiency, adapting to individual motor and ergonomic signatures with only 3 minutes of interaction data. Our work demonstrates the potential of implicit motion sensing to create intelligent, reachability-aware interfaces that dynamically align with human motor intent.

