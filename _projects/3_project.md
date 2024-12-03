---
layout: page
title:  AI-Assisted Art Training
description: AI for Enhancing Artistic Skill Development in Calligraphy and Painting
img: assets/img/AI-assisted/title.jpg
importance: 3
category: Research Projects
---

In professional art creation (e.g., calligraphy and painting), learning is costly and resource-limited, with top-tier resources scarce. While AIGC can generate artworks for aesthetic reference, it offers little guidance for developing creative skills.  
From a human-AI collaborative perspective, we aim for AI to not only generate but also "create" art like humans, guiding artistic skill learning. This project will develop a multimodal system to capture data like finger pressure and pen posture, create a professional dataset, and use representation learning to offer interactive, expert feedback.  

The project is currently in its early stages, with related research and the development of the data collection platform completed.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AI-assisted/overview.jpg" title="image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Research Direction and Context  

Given the complexity of art creation, we’ll begin with calligraphy practice. Through discussions with professional calligraphers, we’ve identified pen tip pressure and posture as key factors. Our goal is to focus on modeling the changes in pen tip pressure and pen posture during calligraphy practice for model training and instructional system development.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AI-assisted/copybook.jpg" title="image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Data Collection System Development  

Through research, we found that commercial products like the Apple Pencil can provide the necessary data, such as pen tip pressure and pen posture. Therefore, we plan to first validate the feasibility using data collected from the Apple Pencil. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AI-assisted/applepencil.jpg" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AI-assisted/penbrushfinetune.jpg" title="image" class="img-fluid rounded" %}
    </div>
</div>

We have developed a calligraphy practice app based on the Apple Pencil, which includes four different calligraphy templates. The app records key information during the user's writing process, such as touchpoint location, timestamps, pen tip pressure, pen tilt angle, and direction angle, in JSON format.

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AI-assisted/font.png" title="image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AI-assisted/interface.png" title="image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## Data Processing and Model Training 

After completing initial data alignment, filtering, and visualization, we plan to train a model to understand these sequential patterns using an autoregressive approach. Our initial plan is to train the model by masking certain data points and regenerating them. The project is currently ongoing, and further progress will be updated regularly.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AI-assisted/masking.png" title="image" class="img-fluid rounded" %}
    </div>
</div>