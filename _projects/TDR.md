---
layout: page
title: "Low-cost Time-Domain Reflectometer"
description: "Low-cost TDR for electric fence fault detection"
img: assets/img/projects/TDRThumbnail.jpg
importance: 8
category: "Selected Projects"
related_publications: false
slug: "low-cost-time-domain-reflectometer"
---

## Low-cost Time-Domain Reflectometer for Electric Fence Fault Detection

This project involved the development of a low-cost Time-Domain Reflectometer (TDR) as part of a research initiative focused on improving electric fence maintenance for human–elephant conflict mitigation.

The objective was to investigate a low-cost approach for locating discontinuities in electric fence wiring by analysing signal reflections along transmission lines, reducing reliance on expensive commercial measurement equipment.

---

<div class="row justify-content-center">

    <div class="col-sm-8 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/TDRModelFence.jpg" 
        title="Electric fence monitoring concept for elephant conservation applications" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Electric fence monitoring concept motivating the development of a low-cost fault detection approach.
</div>

---

## Problem Context

Electric fences are widely used in Sri Lanka to reduce human–elephant conflict by protecting agricultural areas located near elephant habitats. However, maintaining these systems is challenging because fence lines can extend over several kilometres across remote areas.

A single break or fault in the fence can significantly reduce its effectiveness, as the sections beyond the fault location may no longer receive the required electrical energy. Such damage can occur due to elephant activity, environmental conditions, or physical deterioration of the fence structure.

Locating these faults manually requires inspection of long fence sections, which can be time-consuming and resource intensive. This project explored the use of time-domain reflectometry as a potential low-cost diagnostic approach, where signal reflections along the fence wire can be analysed to identify cable discontinuities and estimate fault locations.

---

## Time-Domain Reflectometer Design

A low-cost pulse generation circuit was designed and implemented to create fast-edge electrical pulses for transmission through a cable.

The prototype was based on a Schmitt-trigger inverter architecture using a 74AC14 hex inverter IC, capacitors, and resistive components. The generated pulse was connected to the test cable and measurement equipment through a BNC splitter, allowing reflected signals to be observed using an oscilloscope.

<div class="row justify-content-center">

    <div class="col-sm-8 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/TDRSchematic.png" 
        title="Time-domain reflectometer circuit schematic" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Circuit design of the low-cost time-domain reflectometer prototype.
</div>

---

## Circuit Simulation and Prototype Development

The circuit operation was first verified through simulation before building the physical prototype.

The simulated output was used to verify pulse generation and expected signal behaviour before implementing the hardware prototype.

<div class="row justify-content-center">

    <div class="col-sm-8 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/TDRSim.png" 
        title="Multisim simulation of the TDR circuit" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Simulation of the low-cost TDR circuit before hardware implementation.
</div>

---

## Experimental Validation

The prototype was tested using a coaxial cable to observe reflected signals produced by the cable termination.

The incident pulse and reflected pulse were captured using an oscilloscope, and the measured time difference between them was used to estimate the distance to the cable termination based on signal propagation delay.

<div class="row justify-content-center">

    <div class="col-sm-6 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/TDRPrototype.png" 
        title="Physical implementation of the TDR prototype" 
        class="img-fluid rounded z-depth-1" %}

    </div>

    <div class="col-sm-6 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/TDROscilloscope.png" 
        title="Oscilloscope measurement showing signal reflection" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Physical prototype and oscilloscope measurements showing signal reflection behaviour during experimental validation.
</div>

---

## Outcome

The prototype demonstrated the capability of a low-cost time-domain reflectometer to measure signal reflections and estimate cable characteristics.

This work explored a hardware-based sensing approach for electric fence fault diagnosis, combining circuit design, signal measurement, simulation, and experimental validation to evaluate the feasibility of low-cost fault detection.