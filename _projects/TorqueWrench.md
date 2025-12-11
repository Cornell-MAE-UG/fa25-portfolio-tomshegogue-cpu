---
layout: project
title: Torque Wrench Design and Analysis
description: My design of a 3/8 inch drive instrumented torque wrench rated for 600 in-lbf
technologies: [Autodesk Fusion, ANSYS]
---

Let me show you my design and analysis of a 3/8 inch drive instrumented torque wrench rated for 600 in-lbf!

CAD model with dimensions: 
![Torque Wrench CAD Photo]({{ "assets/images/Dimensions1.png" | relative_url }})
![Torque Wrench CAD Photo]({{ "assets/images/Dimensions2.png" | relative_url }})


We used Structural Steel for our design. Structural Steel has a Young's Modulus of 30e6 psi. Structural steel also has a high yield stress which prevents inelastic deformation and a high ultimate strength which prevents fracture.


![Force Photo]({{ "assets/images/Force.png" | relative_url }})
For our FEM Analysis, a 30 lb load (600/L) was applied in the +x direction on the highlighted blue face.


![Constraint Photo]({{ "assets/images/Clamped.png" | relative_url }})
Boundary conditions were applied to the blue-highlighted faces of our FEM model. By setting displacement to zero in each direction, we were able to fix those faces of the drive.



Normal strain contours (in the strain gauge direction) from FEM:
![Normal Strain Contour Photo]({{ "assets/images/NormalStrainContour1.png" | relative_url }})
![Normal Strain Contour Photo]({{ "assets/images/NormalStrainContour2.png" | relative_url }})
![Normal Strain Contour Photo]({{ "assets/images/NormalStrainContour3.png" | relative_url }})



Contour plot of maximum principal stress from FEM:
![Principle Stress Contour Photo]({{ "assets/images/PrincipleStressContour1.png" | relative_url }})
![Principle Stress Contour Photo]({{ "assets/images/PrincipleStressContour2.png" | relative_url }})


FEM Calculation Results:
Max normal stress- 29359 psi
Load point deflection- 0.169 in
Strain at gauge 1- 178.6 microstrains
Strain at gauge 2- -178.9 microstrains


Using the FEM strains at the gauge location and assuming a full-bridge with GF=2, the torque wrench sensitivity at the rated torque of 600 in-lbf is approximately 0.36 mV/V.

Strain Gauge Selection:
Type: linear, single-axis foil strain gauge for bending
Resistance: 350 Ω, gauge factor GF ≈ 2.0
Active grid length: ~3 mm ≈ 0.12 in
Active grid width: ~2 mm ≈ 0.08 in
Overall backing size: ~5 mm × 3 mm ≈ 0.20 in × 0.12 in

