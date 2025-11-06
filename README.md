# Independent Study: GPU Power Profiling for Scalene

![Project Screenshot / Architecture Diagram]
*(A great image here would be a screenshot of a terminal showing the Scalene profiler's output, or a graph of GPU power usage you generated. You can upload this image to the repo and link it.)*

## 1. Project Overview

This was an independent study project I completed as part of my Master's in Computer Science. The goal was to extend Scalene, a high-performance CPU and memory profiler for Python, to also track and report GPU power usage. This is critical for understanding the true energy cost and efficiency of deep learning models.

## 2. The Problem & Goal

High-performance profilers like Scalene could show CPU and memory usage, but as AI/ML workloads move to GPUs, there was a blind spot in energy-efficiency analysis. Developers couldn't easily see how their model's architecture or batch size impacted GPU power draw.

My goal was to research and implement a method to access GPU power metrics and integrate this new data stream into Scalene's existing reports with negligible performance overhead.

## 3. Tech Stack

* **Primary Language:** Python
* **Core Tools:** Scalene (profiler), NVIDIA Management Library (NVML)
* **Models Profiled:** Mask R-CNN, various PyTorch models

## 4. Project Status: Case Study

This repository serves as a **case study and summary** of my independent research. The work involved modifying the open-source Scalene profiler (an existing, complex codebase) to add new functionality.

As this was a proof-of-concept for academic research, the focus was on the **analysis and integration method** rather than a production-ready code package. The original, messy development code is archived privately.

## 5. My Contributions & Key Features

As an independent researcher, I was responsible for the entire project from concept to implementation:

* **Researched** and identified the NVIDIA Management Library (NVML) as the correct interface for querying GPU hardware statistics.
* **Developed** a Python module that efficiently samples GPU power consumption and memory usage in real-time.
* **Architected** the integration of this module into the Scalene profiler's main data collection loop, ensuring the new profiling added negligible overhead.
* **Validated** the tool by running it against complex deep learning models like Mask R-CNN to identify performance and power bottlenecks.

## 6. Challenges & What I Learned

The biggest challenge was "profiling the profiler." It was critical that my new feature didn't slow down the program being measured. This project taught me a huge amount about systems-level programming, performance analysis, and how to work within a large, existing codebase. I also gained a deep understanding of how AI/ML models utilize hardware resources.
