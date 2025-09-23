---
title: "Diffusion Spline-Based Navigation Policy in Dynamic Environments"
collection: projects
date: 2024-02-02
paper: false
layout: archive
permalink: /projects/2024-semester-project
excerpt: 'This project investigated the use of denoising diffusion probabilistic models (DDPMs) for spline-based robot navigation in two-dimensional environments with single or multiple, static or dynamic obstacles.'
header:
    teaser: /projects/2024-semester-project/semester-project-cover.jpg
---

Abstract
-------
This semester project investigates the use of denoising diffusion probabilistic mod- els (DDPMs) for spline-based robot navigation in two-dimensional environments with single or multiple, static or dynamic obstacles. All obstacles are modeled as bounding boxes with known dimensions. Furthermore, the control points of all obstacle trajectories are assumed to be known precisely at all times.

Expert demonstrations are employed for model training, and the trained policy is evaluated using various metrics that are relevant to real-world applications. The performance of the diffusion model is assessed against an existing optimization- based planner and a neural network-based planner.

The findings reveal that diffusion models are fundamentally feasible for spline-based navigation and are able to retain multi-modal solutions. Their performance in terms of obstacle collision rates is comparable to existing techniques, however they exhibit suboptimal computational performance compared to alternative planners.
