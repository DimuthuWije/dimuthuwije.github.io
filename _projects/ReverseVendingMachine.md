---
layout: page
title: Reverse Vending Machine
description: Automated Recycling System with Vision-Based Identification
img: assets/img/projects/RVMBanner.jpg
importance: 5
category: Selected Projects
related_publications: false
slug: reverse-vending-machine
---

## Automated Reverse Vending Machine System Concept

This project focused on the conceptual design and development of an automated reverse vending machine system for plastic bottle recycling. The system was designed to identify, validate, and sort recyclable bottles through a combination of computer vision, weight verification, embedded processing, and automated actuation.

The project was conducted as a research project at the University of Sri Jayewardenepura in collaboration with OREL Corporation (Pvt.) Ltd.

---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">

        <video
            controls
            preload="metadata"
            poster="/assets/img/projects/RVMThumbnail.png"
            class="img-fluid rounded z-depth-1"
            style="width:100%; aspect-ratio:16/9; background:#000;">

            <source src="/assets/video/RVM.mp4" type="video/mp4">

        </video>

    </div>
</div>

<div class="caption">
    Blender-based simulation of the proposed automated reverse vending machine concept.
</div>

---

## System Architecture and Workflow

The proposed system was designed to automate the bottle recycling process through an integrated perception, decision-making, and sorting pipeline.

The workflow incorporated bottle identification, database verification, weight-based validation, and actuator-controlled sorting into separate collection bins.

<div class="row justify-content-center">

    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid 
        path="assets/img/projects/RVMFlowChart.png" 
        title="Reverse vending machine system workflow" 
        class="img-fluid rounded z-depth-1" %}
    </div>

</div>

<div class="caption">
    System workflow developed for the proposed automated reverse vending machine, outlining bottle verification, weight validation, and automated sorting logic.
</div>

---

## Digital Prototype Development

A complete digital prototype was developed using Blender to evaluate the mechanical layout and demonstrate the automated bottle sorting concept before physical implementation.

The simulation included the bottle insertion process and the movement of bottles through the proposed sorting mechanism.

<div class="row justify-content-sm-center">

    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid 
        path="assets/img/projects/RVMCloseup.jpg" 
        title="Reverse vending machine digital prototype - View 1" 
        class="img-fluid rounded z-depth-1" %}
    </div>

    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid 
        path="assets/img/projects/RVMCloseup2.jpg" 
        title="Reverse vending machine digital prototype - View 2" 
        class="img-fluid rounded z-depth-1" %}
    </div>

</div>

<div class="caption">
    Blender-based digital prototype illustrating the mechanical layout and bottle sorting mechanism from multiple viewpoints.
</div>


---

## Vision-Based Bottle Identification

Initial experiments investigated camera-based identification approaches for automated bottle recognition.

A webcam-based perception system was developed to investigate bottle recognition using barcode identification as part of the proposed sensing pipeline.

<div class="row justify-content-sm-center">

    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid 
        path="assets/img/projects/RVMWebcamTesting.png" 
        title="Initial camera-based bottle identification testing" 
        class="img-fluid rounded z-depth-1" %}
    </div>

    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid 
        path="assets/img/projects/RVMBarcodeDetection.png" 
        title="Barcode detection experiment" 
        class="img-fluid rounded z-depth-1" %}
    </div>

</div>

<div class="caption">
    Initial computer vision experiments for automated bottle identification and barcode recognition.
</div>

---

## Embedded System Design

The proposed system architecture combined multiple hardware components to enable automated operation, including camera-based identification, weight verification, embedded processing, and actuator-based sorting.

The planned implementation included:

- Camera-based bottle identification
- Weight measurement using a load cell
- Embedded processing using a Raspberry Pi
- Servo-controlled sorting mechanism

The project demonstrated the design of a complete automated recycling workflow, from user interaction and perception to decision making and physical sorting.