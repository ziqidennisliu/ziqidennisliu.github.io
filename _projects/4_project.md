---
layout: page
title: Embroidery of Light
description: Luminescent Flexible Materials for Traditional Craftsmanship
tag: • Interaction Design, Product design
img: assets/img/Embroidery/title.jpg
importance: 2
category: Fun Projects
---

2024  
*Teamwork: **Ziqi Liu**, Yao Lu, Xuezhu Wang*  
*Advisor: Haipeng Mi*  
<br>
This work is part of a collaboration project with [Mercedes-Benz, Beijing](https://group.mercedes-benz.com/careers/about-us/locations/location-detail-page-5184.html). In this project, we explored the application forms and interaction design of emerging smart materials in automotive interiors, including textile sensors, smart materials, 4D materials, and dynamic materials.  

In this work, we explored the potential application of [a new type of flexible luminescent material](https://www.nature.com/articles/s41586-021-03295-8) in traditional **embroidery** techniques, as well as its possible uses in automotive cabin interactions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/overview.gif" title="example image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Pattern Design and Embroidery Sample

We designed three different types of patterns, including functional pattern, traditional embroidery pattern, traditional weaving pattern. Additionally, we created embroidery samples with flexible luminescent materials using traditional embroidery and weaving techniques.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/f1.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/f2.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/f3.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/f4.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/e1.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/e2.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/e3.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/e4.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/w2.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/w3.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/w4.png" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/w5.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Lighting Control and Circuit Implementation

Due to the requirement of alternating high-voltage, low-current conditions, we chose to connect the flexible luminescent material in series with a field-effect transistor (FET), with an ESP32 controller to control the brightness of the threads.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/circuit.jpg" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/circuit1.jpg" title="example image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Large-Format Interior Prototype Fabrication

We designed and created a glowing embroidered decoration for the interior of a Mercedes-Benz engineering vehicle, which was then installed in the actual vehicle for an effect preview. This served as a feasibility exploration for further exploring interactive features in the future.  
Due to confidentiality agreements, the final results cannot be displayed. However, here we present some images from the design process.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/design.png" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Sketches of the interior design of the Mercedes-Benz engineering vehicle.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/animation.gif" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Animation of the glowing embroidered decoration in the Mercedes-Benz engineering vehicle.
</div>


<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/install1.jpg" title="example image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Embroidery/install2.jpg" title="example image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Installation of the glowing embroidered decoration in the Mercedes-Benz engineering vehicle.
</div>

<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/embroidery.mp4" autoplay="false" controls="true" width="100%" height="auto" %}
    </div>
</div>
<div class="caption">
    The demonstration video
</div>
