---
layout: page
title: COMETIC
description:  Enhancing Smartphone Eye Tracking with Cursor-Based Interactive Implicit Calibration
img: assets/img/COMETIC/title.jpg
importance: 1
category: Research Projects
---

2024  
*Chang Liu, Xiangyang Wang, Chun Yu, Yingtian Shi, Chongyang Wang, **Ziqi Liu**, Chen Liang, Yuanchun Shi*  
<br>
Limited accuracy of eye tracking on smartphones restricts its use. Existing RGB-camera-based eye tracking systems rely on extensive datasets, which could be improved by continuous fine-tuning using calibration data implicitly collected from user interactions. In this context, we propose COMETIC (Cursor Operation Mediated Eye-Tracking Implicit Calibration), which introduces a cursor-based interaction and utilizes the inherent correlation between cursor and eye movement.

<br>
**Publication:**  
- Enhancing Smartphone Eye Tracking with Cursor-Based Interactive Implicit Calibration*(CHI ’25)*.  

<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/cometic.mp4" autoplay="true" controls="true" width="100%" height="auto" %}
    </div>
</div>

<br>
## Eye Tracking on Smartphone 

Current smartphone eye tracking faces two main challenges: limited personalization for individual users and difficulty adapting to frequent posture changes. To address these issues, we developed a system that dynamically calibrates eye tracking through implicit user interactions, improving both accuracy and personalization.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/background.png" title="image" class="img-fluid rounded" %}
    </div>
</div>

<br>
## COMETIC  

By filtering valid cursor coordinates as proxies for gaze ground truth and fine-tuning the eye-tracking model with corresponding images, COMETIC enhances accuracy during interaction. Both filtering and fine-tuning utilize pre-trained models and can be further improved with personalized, dynamically updated data.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/teaser.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    The workflow of COMETIC (Cursor Operation Mediated Eye-Tracking Implicit Calibration)
</div>
<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/interaction.gif" title="image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/algorithm.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Interactions and Model Structures of COMETIC
</div>


<br>
## Data Collection Experiment  

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/apparatus_and_task.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    The Apparatus and Experimental Task
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/layout.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    The 3D-printed stand and the layout on screen
</div>
<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/apparatus.jpg" title="image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/experiment_layout.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    Apparatus and Layouts in the Experiment
</div>


<br>
## Evaluation  

Results show that COMETIC achieves an average eye-tracking error of 208.04 px (1.2 cm), representing a 49.64% improvement compared to the system without fine-tuning. The analysis reveals that filtering cursor points with an actual gaze distance between 250 and 300 px (1.44 to 1.73 cm) yields the best eye-tracking results.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/0829_video_to_gaze_error.png" title="image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/0829_cursor_video_to_distance_precision.png" title="image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/0829_cursor_video_to_distance_fp_error.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/0829_iter_gaze_error.png" title="image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/0829_iter_precision.png" title="image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/0829_iter_fp_error.png" title="image" class="img-fluid rounded" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/COMETIC/0829_iter_gaze_error_of_subject_tau_250.png" title="image" class="img-fluid rounded" %}
    </div>
</div>
