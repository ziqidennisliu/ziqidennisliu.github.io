---
layout: page
title:  Cognitive Pen
description: A Pen-Based Multi-Physiological Signal Monitoring System
img: assets/img/cognitivepen/title.jpg
importance: 1
category: Fun Projects
---

2025  
*Ziqi Liu*
*Advisor: Yuntao Wang, Haipeng Mi*  

Continuous monitoring of physiological signals such as electrodermal activity (EDA) and photoplethysmography (PPG) is critical for assessing users’ psychological states in health and education contexts. However, acquiring high-quality signals remains challenging due to the sensitivity of sensor placement and motion artifacts.

This work presents a pen-based sensing device integrating EDA, PPG, and IMU sensors to enable unobtrusive and continuous physiological signal acquisition during natural handwriting interactions. The system’s applicability is validated in a cognitive load classification task, where results demonstrate that IMU-based filtering significantly enhances classification accuracy under motion.

This research offers a novel and practical solution for robust, low-burden psychological monitoring in everyday interactive contexts. The functional prototype and product design of this work have been collected by [Xinya College, Tsinghua University](https://www.xyc.tsinghua.edu.cn/en/), as an outstanding graduation project.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cognitivepen/first.png" title="image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Pen-based Sensing System Design  

Given the complexity of art creation, we’ll begin with calligraphy practice. Through discussions with professional calligraphers, we’ve identified pen tip pressure and posture as key factors. Our goal is to focus on modeling the changes in pen tip pressure and pen posture during calligraphy practice for model training and instructional system development.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cognitivepen/system.png" title="image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Hardware Design  

Through research, we found that commercial products like the Apple Pencil can provide the necessary data, such as pen tip pressure and pen posture. Therefore, we plan to first validate the feasibility using data collected from the Apple Pencil. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cognitivepen/structure.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cognitivepen/hardware1.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cognitivepen/Hardware.png" title="image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Algorism Design 

After completing initial data alignment, filtering, and visualization, we plan to train a model to understand these sequential patterns using an autoregressive approach. Our initial plan is to train the model by masking certain data points and regenerating them. The project is currently ongoing, and further progress will be updated regularly.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cognitivepen/motion_correlation.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cognitivepen/signalfiltering.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cognitivepen/algorism.jpg" title="image" class="img-fluid rounded" %}
    </div>
</div>