---
layout: post
title: Embedded Control System for Bio-Inspired Saccadic Camera Motion
date: 2025-01-15 12:00:00 +0100
image: EmbeddedControlSystem1.png
tags: [Embedded Systems, Motor Control, Military Applications, Hardware Design]
---

My Master's thesis represents the culmination of my academic journey at ETH Zürich, focusing on a cutting-edge application that bridges embedded systems, motor control, and defense technology. I developed a custom dual motor controller for high-performance Pan-Tilt Units (PTUs) specifically designed for optical drone detection in restricted airspace.

## The Challenge

Monitoring airspace for unauthorized drones is increasingly critical. Optical detection offers key advantages over radar & RF, making it a complimentary solution. However, detecting UAV's at long range requires zoom-capable optics with a narrow field of view. Deploying multiple fixed cameras in every direction becomes impractical as the zoom factor increases, making a single camera mounted on a PTU the more efficient solution.

The breakthrough lies in combining PTUs with event-based cameras (Dynamic Vision Sensors). Unlike traditional frame-based cameras, DVS cameras mimic the biological retina by recording asynchronous pixel intensity changes as discrete events. This provides high temporal resolution, low latency, wide dynamic range, and resilience to motion blur - perfect for detecting fast-moving targets.

But there's a problem: when a DVS camera rotates across a static environment, it generates massive amounts of artificial events from background movement. This makes it extremely difficult to separate genuine object motion (the drone) from background noise. The solution? Bio-inspired saccadic motion - rapid, precise camera repositioning that minimizes the time spent in motion, reducing artificial events while maintaining coverage.

## My Solution

An existing PTU prototype using off-the-shelf motor controllers couldn't achieve the required performance. The proprietary controller software restricted custom control algorithms, control cycle configuration, and critical parameters needed for saccadic motion tailored to DVS cameras.

The goal: achieve 180° camera rotations in under 200ms with minimal settling time and overshoot, while respecting actuator and thermal constraints.

The heart of the solution is a fully custom dual-motor controller with dedicated PCB and firmware. I developed an open-source control framework enabling Software-in-the-Loop (SIL) simulation for rapid design iteration and fine-tuning of control strategies specifically optimized for event-based vision.

## Technical Implementation

### Custom Hardware Design
The custom PCB integrates all motor control electronics:
- Dual BLDC motor drivers with thermal management
- High-precision absolute encoder interfaces
- Multi-protocol communication (Ethernet, CAN, USB)
- Comprehensive safety and fault detection mechanisms
- High-current sensing circuits for real-time monitoring

### Control Framework
I developed a complete SIL simulation pipeline in MATLAB/Simulink for controller design and validation before hardware deployment. The control system implements:
- Field-Oriented Control (FOC) for efficient BLDC motor operation
- Custom trajectory planning optimized for saccadic motion patterns
- Optimized PWM and control cycle frequencies for target performance
- Active velocity threshold control for any movement that may be required
- Scanning pattern optimization balancing physical capabilities with approach probabilities of UAV's

<div style="text-align: center; margin: 30px 0;">
  <img src="{{ site.baseurl }}/images/20251030_180132.png" alt="Custom dual motor driver PCB" style="max-width: 60%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #7F8C8D; margin-top: 10px;">Custom-designed dual motor driver PCB for PMSM control</p>
</div>

## Results

The custom motor controller successfully achieves the performance targets for saccadic motion with DVS cameras:
- **Rapid Saccades**: 180° rotations in under 200ms
- **Minimized Overshoot**: Optimized settling time reduces artificial DVS events
- **Flexible Control**: Open-source framework enables custom scanning patterns and control strategies
- **Robust Operation**: Comprehensive safety mechanisms prevent mechanical damage
- **Multi-Protocol Interface**: Seamless integration via Ethernet, CAN, or USB in the complete vision system

The project demonstrates how tailored motor control hardware and control policies can enable advanced vision systems. Combining DVS cameras with optimized saccadic PTU motion opens new possibilities for efficient, high-performance drone detection. Exactly the kind of cross-disciplinary challenge I find most engaging.

## Technologies Used

- **Microcontrollers**: STM32 (ARM Cortex-M7)
- **Development**: C/C++, FreeRTOS
- **Hardware**: Altium Designer for PCB layout
- **Simulation**: MATLAB/Simulink for control algorithm development
- **Testing**: Custom test benches and instrumentation

The experience gained from this thesis has been invaluable, reinforcing my desire to work on projects that require deep integration between software and hardware, where every millisecond counts.

## Project Demonstration

Here's a video demonstration of the system in action:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; margin: 20px 0;">
  <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
          src="https://www.youtube.com/embed/pGRusqv1apg"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
  </iframe>
</div>
