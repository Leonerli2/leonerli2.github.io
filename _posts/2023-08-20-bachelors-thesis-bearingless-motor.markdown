---
layout: post
title: Bearingless Motor Design - Swissmem Award Winner
date: 2023-08-20 10:00:00 +0100
image: DoubleBearinglessOutrunner.jpg
tags: [Motor Design, Control Systems, Award, Research]
---

I'm proud to share that my Bachelor's thesis, "Design and Commissioning of a Double Bearingless Outrunner Motor for Fluid Manipulation," was awarded the prestigious **Swissmem Best Thesis Award 2023** in the industry sector drive technology. This recognition validates the innovative approach and hard work that went into this challenging project.

## What is a Bearingless Motor?

Bearingless motors are a fascinating class of electric machines that combine motor functionality with magnetic levitation. Unlike traditional motors that require mechanical bearings, bearingless motors use electromagnetic forces to both rotate and levitate the rotor. This eliminates mechanical wear, enables operation in sterile environments, and allows for contactless pumping applications.

## The Challenge

In collaboration with Levitronix, a Swiss leader in bearingless motor technology, I tackled the design and commissioning of a double outrunner configuration specifically optimized for fluid manipulation applications. The key challenges included:

- **Complex Electromagnetic Design**: Simultaneous control of torque and levitation forces
- **Novel Outrunner Topology**: Implementing bearingless principles in an unconventional motor configuration
- **Precision Control**: Achieving stable levitation while maintaining smooth rotation
- **Fluid Dynamics**: Optimizing the design for pumping efficiency

## Technical Innovation

### Electromagnetic Design

The motor features a unique double outrunner configuration with:
- Dual rotor structure for independent torque and suspension control
- Optimized winding arrangements for force generation
- Finite Element Analysis (FEA) for electromagnetic optimization
- Minimized cross-coupling between torque and levitation systems

### Control System Development

I developed a comprehensive control system implementing:
- **Multi-input Multi-output (MIMO) Control**: Coordinating six degrees of freedom for complete rotor positioning
- **Real-time Sensing**: Position and current feedback loops running at kHz frequencies
- **Disturbance Rejection**: Handling fluid forces and external perturbations
- **System Identification**: Modeling the complex dynamics for controller tuning

### Hardware Integration

The project involved extensive hardware work:
- Custom power electronics for independent phase control
- Precision sensor integration for position measurement
- Thermal management for continuous operation
- Mechanical design considerations for the rotor and stator assembly

## Results and Recognition

The developed motor successfully demonstrated:
- **Stable Levitation**: Sub-millimeter position accuracy during operation
- **Smooth Rotation**: Ripple-free torque production across the speed range
- **Pumping Performance**: Efficient fluid manipulation capabilities
- **Reliability**: Extended testing without mechanical wear or maintenance

The **Swissmem Best Thesis Award** recognized this work for its combination of theoretical depth, practical implementation, and industrial relevance. This achievement reflects not just individual effort, but also the excellent supervision and support from ETH Zürich and Levitronix.

## Key Learnings

This thesis was my first deep dive into the intersection of electromagnetic design, control theory, and practical engineering. The experience taught me:

1. **Iterative Development**: The importance of rapid prototyping and testing cycles
2. **Theory Meets Practice**: How academic knowledge translates into real-world solutions
3. **Multidisciplinary Thinking**: Integrating electromagnetics, mechanics, and control
4. **Industry Collaboration**: Working effectively with industrial partners and their requirements

## Technologies Used

- **Simulation**: MATLAB/Simulink for control design
- **FEA**: Electromagnetic simulation for motor optimization
- **Programming**: C/C++ for embedded control implementation
- **Hardware**: STM32 microcontrollers, custom power electronics
- **Tools**: Oscilloscopes, power analyzers, and position sensors

## Project Demonstration

Watch the bearingless double outrunner motor in action:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; margin: 20px 0;">
  <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
          src="https://www.youtube.com/embed/dcOowOVzIVc"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
  </iframe>
</div>

This project solidified my passion for working on challenging problems that span multiple engineering disciplines. The recognition from Swissmem validates the approach and motivates me to continue pushing the boundaries of what's possible in drive technology.

Looking forward, the principles and techniques developed in this thesis continue to influence my work, especially in my current Master's thesis where precision motor control remains a central theme.
