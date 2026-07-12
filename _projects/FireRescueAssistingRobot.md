---
layout: page
title: Fire Rescue Assisting Robot
description: Thermal Human Detection for Fire Rescue Robots
img: assets/img/projects/HuMomentThumbnail.gif
importance: 2
category: Selected Projects
related_publications: true
slug: fire-rescue
---

## Thermal Human Detection for Fire Rescue Robotics

This project explores thermal perception for human detection in smoke-filled environments, where conventional optical imaging systems are limited by poor visibility. A compact perception system was developed and evaluated for potential integration into fire rescue robotic platforms.

---

<div class="row justify-content-center">
    <div class="col-sm-6 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/HuMoment.gif"
        title="Thermal human detection demonstration"
        class="img-fluid rounded z-depth-1" %}

    </div>
</div>

<div class="caption">
    Real-time thermal human detection using the developed perception system.
</div>

---

## The Approach

The system was developed by evaluating different sensing approaches and selecting a compact thermal perception solution suitable for robotic applications. Computer vision techniques were applied to thermal data to detect human presence under challenging environmental conditions.

The developed approach was validated through live testing, including evaluation in a simulated smoke-filled environment to assess its suitability for fire rescue scenarios.

<div class="row justify-content-sm-center">

    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid 
        path="assets/img/projects/simulatedEnvironment.png" 
        title="Smoke-filled environment testing" 
        class="img-fluid rounded z-depth-1" %}
    </div>

    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid 
        path="assets/img/projects/FireRescueHardware.jpeg" 
        title="Embedded thermal perception system" 
        class="img-fluid rounded z-depth-1" %}
    </div>

</div>

<div class="caption">
    Simulated smoke-filled environment used for system evaluation and embedded perception hardware.
</div>

---

This work was later extended into a conference manuscript submitted to the IEEE International Conference on Electrical Engineering and Emerging Technologies (ICEEET), 2026.

{% cite wijesiriwardene2026human %}