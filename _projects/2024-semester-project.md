---
title: "Diffusion Spline-Based Navigation Policy in Dynamic Environments"
collection: projects
date: 2024-02-02
paper: false
tags: [Thesis, Machine Learning, Robotics]
layout: archive
permalink: /projects/2024-semester-project
excerpt: 'This project investigated the use of denoising diffusion probabilistic models (DDPMs) for spline-based robot navigation in two-dimensional environments with single or multiple, static or dynamic obstacles.'
header:
    teaser: /projects/2024-semester-project/semester-project-cover.jpg
---

In my semester thesis at the <a href="https://rsl.ethz.ch/" target="_blank" rel="noopener noreferrer">Robotic Systems Lab</a> at ETH Zurich, I investigated whether denoising diffusion probabilistic models (DDPMs) can be used for spline-based robot navigation in two-dimensional environments with single or multiple, static or dynamic obstacles.

Diffusion models have shown impressive results in generative tasks, and one of their properties that make them interesting for robotics is that they can retain multi-modal solutions.
I. e., when there are several equally valid ways around an obstacle, the model does not have to collapse onto just one of them.
This project explored whether that promise holds up for spline-based navigation.

All obstacles are modeled as bounding boxes with known dimensions, and the control points of all obstacle trajectories are assumed to be known precisely at all times. The diffusion policy is trained on expert demonstrations and evaluated using various metrics that are relevant to real-world applications. Its performance is assessed against an existing optimization-based planner and a neural network-based planner.

The findings show that diffusion models are fundamentally feasible for spline-based navigation and are able to retain multi-modal solutions. Their obstacle collision rates are comparable to the existing techniques; however, their computational performance falls short of the alternative planners.
