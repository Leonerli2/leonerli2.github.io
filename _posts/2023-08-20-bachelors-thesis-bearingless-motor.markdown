---
layout: post
title: Bearingless Motor Design - Swissmem Award Winner
date: 2023-08-20 10:00:00 +0100
image: DoubleBearinglessOutrunner.jpg
tags: [Motor Design, Control Systems, Award, Research]
---

I'm proud to share that my Bachelor's thesis, "Design and Commissioning of a Double Bearingless Outrunner Motor for Fluid Manipulation," was awarded the prestigious **Swissmem Best Thesis Award 2023** in the industry sector drive technology. 

## What is a Bearingless Motor?

Bearingless motors are a fascinating class of electric machines that combine motor functionality with magnetic levitation. Unlike traditional motors that require mechanical bearings, bearingless motors use electromagnetic forces to both rotate and levitate the rotor. This eliminates mechanical wear, enables operation in sterile environments, and allows for contactless pumping applications.

## The Challenge

In collaboration with Levitronix, a Swiss leader in bearingless motor technology, I worked on a novel dual-motor configuration specifically optimized for fluid manipulation applications. The concept was straightforward but technically demanding: combine two commercial bearingless outrunner motors into a single integrated system with enhanced mechanical performance.

The key challenge? Ensuring both motors contribute equally to the torque generation. Without proper torque distribution, one motor could be overloaded while the other underperforms, leading to inefficient operation or even mechanical stress. Additionally regarding the stability, longer rotors are generally harder to stabilize compared to disk-like rotors. Therefore my task was to develop the control strategy and hardware integration to make two motors work seamlessly as one while staying stable.

## Technical Approach

### System Integration

The core innovation involved:
- **Dual-Motor Configuration**: Integrating two existing bearingless outrunner motors in a stacked configuration
- **Torque Distribution Control**: Developing a controller to ensure both motors generate equal torque under all operating conditions
- **Communication Architecture**: Establishing reliable data exchange between motor controllers for coordinated operation
- **Mechanical Design**: Designing the rotor and stator assemblies to accommodate the dual-motor setup
- **Stability**: Guarantee stability even in fluid manipulation applications

## Results and Recognition

The dual-motor system successfully achieved its design goals:
- **Balanced Torque Distribution**: Both motors contributing equally under all operating conditions
- **Coordinated Operation**: Seamless communication and control between motor units
- **Enhanced Performance**: Improved mechanical characteristics compared to single-motor configuration
- **Reliable Integration**: Stable operation throughout commissioning and testing

The **Swissmem Best Thesis Award** recognized this work for its practical innovation in system integration and its relevance to industrial fluid manipulation applications.

## Key Learnings

This thesis taught me the value of system-level thinking in complex engineering projects. The experience emphasized:

1. **Integration Complexity**: Combining existing technologies into a cohesive system presents unique challenges beyond individual component design
2. **Load Distribution**: Ensuring balanced operation across multiple actuators requires careful control design
3. **Industry Collaboration**: Working with commercial hardware within confidentiality constraints while achieving research goals
4. **Practical Problem-Solving**: Sometimes the best solution is smart integration rather than reinventing existing technology

## Technologies Used

- **Simulation**: MATLAB/Simulink for control design and system modeling
- **Programming**: C/C++ for torque distribution control implementation
- **Hardware**: Integration with existing motor controllers and power electronics

## Project Demonstration

Watch the dual bearingless outrunner motor system in action:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; margin: 20px 0;">
  <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
          src="https://www.youtube.com/embed/dcOowOVzIVc"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
  </iframe>
</div>


The experience gained from this thesis, particularly in coordinated motor control and system integration, continues to influence my work in embedded systems and precision control applications.
