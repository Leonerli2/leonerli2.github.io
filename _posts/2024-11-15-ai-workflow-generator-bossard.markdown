---
layout: post
title: AI Workflow Generator - Automating Assembly Instructions
date: 2024-11-15 09:00:00 +0100
image: AIWorkflowGenerator.jpg
tags: [AI, Python, Automation, Exploration Lab]
---

During the ETH Exploration Lab, I developed an AI-powered tool at Bossard AG that automatically converts PDF assembly instructions into digital workflows for smart manufacturing stations.

## The Problem

Bossard's Smart Stations help factory workers by displaying step-by-step assembly instructions digitally. However, most companies already have assembly instructions as PDFs. Converting these PDFs into the digital format manually is extremely time-consuming - it can take hours per document and requires product experts to do it.

<div style="text-align: center; margin: 30px 0;">
  <img src="{{ site.baseurl }}/images/AIWorkflow1.png" alt="Bossard Smart Station showing assembly instructions" style="max-width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
  <p style="font-style: italic; color: #7F8C8D; margin-top: 10px;">Smart Station displaying digital assembly instructions</p>
</div>

This creates a major barrier: companies want to use smart stations, but the conversion effort stops them from adopting the technology.

## My Solution

I built an automated conversion pipeline that takes a PDF and outputs structured digital workflows ready for the Smart Stations. The system:

1. **Extracts text instructions** using AI multimodal models that understand document layout
2. **Detects and extracts images** from PDFs using computer vision models like YOLO
3. **Matches images to instructions** so each step shows the correct picture

The key insight was that context awareness is essential. Understanding how instructions and images relate both spatially and semantically was crucial for accurate matching, and even instruction extraction. A unified multimodal model approach with spatial awareness is way better than trying to combine outputs from separate models, although less flexible.

## What I Learned

**Real-world complexity**: PDFs from different companies vary wildly in quality and structure. Building something that works on clean test data is one thing, making it robust for real customer documents is much harder.

**User feedback is crucial**: I built a web application and tested it with actual Bossard customers. Their feedback showed both the potential and limitations, helping prioritize what to improve.

**Video mode prototype**: I also prototyped a feature where assembly experts can record themselves while explaining the process verbally. The AI extracts instructions from their speech and captures key frames - useful for documenting knowledge that doesn't exist in written form.

## Technologies Used

- **Python** for the entire pipeline
- **GPT-4o/Whisper API** for instruction extraction
- **Computer vision models** (YOLO, Docling, Mistral) for image detection and document layout understanding
- **Web application** for customer testing and feedback

## Impact

The tool successfully automates a previously manual, time-intensive process. While it doesn't work perfectly on all PDFs (quality and structure matter), it demonstrates that AI can significantly reduce the barrier to adopting smart manufacturing technology.

This project was my individual research component of the Exploration Lab and became a stepping stone in understanding how to apply AI to real industrial challenges.
