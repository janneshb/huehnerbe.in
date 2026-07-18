---
title: "Uncertainty Model Unfalsification via Semi-Infinite Programming and Local Reduction"
collection: projects
date: 2024-11-11
paper: false
tags: [Thesis, Optimization, Control]
layout: archive
permalink: /projects/2024-masters-thesis
excerpt: "In this project, I present a novel, input-output data-driven approach to uncertainty model identification. This project served as the final project for my Master's degree at ETH Zurich."
header:
    teaser: /projects/2024-uncertainty-model-unfalsificaion/master-thesis-teaser-2.png
---

In my Master's thesis, written at Imperial College London under the supervision of Prof. Eric Kerrigan as the final project of my degree at ETH Zurich, I developed a novel input-output data-driven approach to uncertainty model identification.

The true bounds and distributions of a system's uncertainties ultimately remain unknown — no amount of data can pin them down exactly. So instead of trying to identify *the* uncertainty model, this thesis asks a more modest question: what minimal concrete statements can be made based on an uncertain system model and the available input-output data? We refer to this as *unfalsifying* an uncertainty model.

I took two complementary unfalsification approaches. The **optimistic** approach determines the smallest uncertainties that could explain the given data, while the **pessimistic** approach finds the largest possible uncertainties. The pessimistic problem turns out to be a semi-infinite program, which is solved using the local reduction algorithm. The thesis also shows that the optimistic and pessimistic approaches are mathematical duals of each other.

The proposed techniques were applied to a numerical example using constraint-tightening model predictive control, comparing the performance of various uncertainty models. All tests use input-output data from a nonlinear system with an uncertain linear model.

The optimistic approach often yields satisfactory performance and constraint satisfaction while keeping computational complexity low, though no guarantees can be formulated. The pessimistic approach leads to more conservative robust controllers and, under the right assumptions, guarantees robustness at the cost of increased computational complexity.
