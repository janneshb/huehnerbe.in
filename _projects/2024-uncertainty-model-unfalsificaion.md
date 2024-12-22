---
title: "Uncertainty Model Unfalsification via Semi-Infinite Programming and Local Reduction"
collection: projects
paper: false
layout: archive
permalink: /projects/2024-masters-thesis
excerpt: 'In this project, I present a novel, input-output data-driven approach to uncertainty model identification. This project served as my Master\'s thesis'
header:
    teaser: /projects/2024-uncertainty-model-unfalsificaion/simplesim-cover.jpg
---

Abstract
-------

In this thesis, we present a novel, input-output data-driven approach to uncertainty model identification. As the true bounds and distributions of system uncertainties ultimately remain unknown, we depart from the goal of identifying the uncertainty model and instead look for minimal concrete statements that can be made based on an uncertain system model and available input-output data. We refer to this as unfalsifying an uncertainty model.

Two different unfalsification approaches are taken. The optimistic approach determines the smallest uncertainties that could explain the given data, while the pessimistic approach finds the largest possible uncertainties. The pessimistic problem is revealed to be a semi-infinite program, which is solved using the local reduction algorithm. It is also shown that the optimistic and pessimistic approaches to uncertainty model unfalsification are mathematical duals.

The proposed techniques are applied to a numerical example using constraint-tightening model predictive control and the performance of various uncertainty models is compared. In all tests, we use input-output data from a nonlinear system with an uncertain linear model. The findings reveal that the optimistic approach often yields satisfactory performance and constraint satisfaction while keeping computational complexity low, though no guarantees can be formulated. The pessimistic approach leads to more conservative robust controllers and, under the right assumptions, guarantees robustness albeit at the cost of increased computational complexity.

This project served as my Master's thesis.
