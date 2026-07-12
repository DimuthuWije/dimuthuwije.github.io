---
layout: page
title: "Low-cost Electric Fence Energizer"
description: "Fence energizer for low-cost wildlife protection applications"
img: assets/img/projects/FenceEnergizer.jpg
importance: 9
category: "Selected Projects"
related_publications: false
slug: "low-cost-electric-fence-energizer"
---

## Low-cost Electric Fence Energizer Development

This project involved analysing an electric fence energizer system as part of a SCoRe Lab research initiative focused on developing affordable technologies for human–elephant conflict mitigation.

The objective was to understand the circuit architecture of an existing commercial fence energizer and reconstruct its design approach to support the development of a lower-cost alternative for communities affected by elephant-related crop damage.

---

<div class="row justify-content-center">

    <div class="col-sm-8 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/FenceEnergizer.jpg" 
        title="Electric fence energizer system analysed during the project" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Electric fence energizer system analysed as part of a low-cost wildlife protection technology research project.
</div>

---

## Problem Context

Electric fences are widely used in Sri Lanka to reduce human–elephant conflict by protecting agricultural areas located near elephant habitats. However, commercially available fence energizers can be expensive, limiting accessibility for communities that rely on these systems for crop protection.

As part of a broader SCoRe Lab research initiative, this project explored the electrical architecture of a fence energizer system to support the development of a lower-cost alternative.

Understanding the internal operation of an existing energizer was necessary to identify the major circuit sections, component interactions, and design principles involved in generating controlled high-voltage pulses for electric fencing applications.

---

## PCB Analysis and Trace Identification

The fence energizer PCB was analysed to understand its electrical architecture and reconstruct the circuit design.

The PCB contained separate high-voltage and low-voltage sections. Images of the PCB were processed to identify component locations, copper routing, and electrical connections required for schematic reconstruction.

<div class="row justify-content-center">

    <div class="col-sm-8 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/FenceEnergizerPCBLV.jpg" 
        title="Fence energizer PCB used for circuit analysis" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Fence energizer PCB analysed during circuit reconstruction and design investigation.
</div>

---

<div class="row justify-content-center">

    <div class="col-sm-6 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/FenceEnergizerPCBBacklightFront.jpg" 
        title="Backlit front PCB image showing copper traces" 
        class="img-fluid rounded z-depth-1" %}

    </div>

    <div class="col-sm-6 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/FenceEnergizerPCBBacklightBack.jpg" 
        title="Backlit rear PCB image showing copper traces" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>


<div class="caption">
    Backlit PCB images used to identify hidden copper traces and component connections during circuit reconstruction.
</div>

---

## PCB Trace Reconstruction and Circuit Analysis

The PCB copper traces were manually traced to reconstruct the electrical connections between components.

Some connections were hidden beneath integrated circuits, requiring continuity measurements to identify the underlying electrical paths and complete the circuit reconstruction.

<div class="row justify-content-center">

    <div class="col-sm-10 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/FenceEnergizerTraceAnalysis.gif" 
        title="PCB trace identification using continuity measurements" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    PCB trace identification using continuity measurements to reconstruct hidden electrical connections.
</div>

---

## Schematic Reconstruction

After completing the PCB trace analysis, the circuit was reconstructed as a schematic using Multisim.

The schematic was organised to represent the different functional sections of the energizer, including the low-voltage control circuitry and high-voltage pulse generation stage.

<div class="row justify-content-center">

    <div class="col-sm-8 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/FenceEnergizerSchematic.png" 
        title="Reconstructed fence energizer schematic" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Reconstructed schematic developed from PCB trace analysis and component identification.
</div>

---

<div class="row justify-content-center">

    <div class="col-sm-6 mt-3 mt-md-0">

        {% include figure.liquid 
        path="assets/img/projects/FenceEnergizerHVLV.jpeg" 
        title="High-voltage and low-voltage sections of the energizer circuit" 
        class="img-fluid rounded z-depth-1" %}

    </div>

</div>

<div class="caption">
    Separation of high-voltage and low-voltage sections to analyse the functional architecture of the energizer system.
</div>

---

## Outcome

This project provided an understanding of the electrical architecture and design principles of an electric fence energizer system.

The reconstructed circuit provided a foundation for developing a low-cost alternative for electric fence applications and demonstrated practical experience in PCB analysis, circuit reconstruction, hardware investigation, and electronic system design.