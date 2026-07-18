---
title: "Optimistic vs Pessimistic Uncertainty Model Unfalsification"
collection: projects
date: 2025-12-10
paper: false
tags: [Conference Paper, IEEE CDC, Optimization, Control]
coauthors: [Jad Wehbeh, Eric C. Kerrigan]
layout: archive
permalink: /projects/2025-optimistic-pessimistic-unfalsification
excerpt: "We present a novel, input-output data-driven approach to uncertainty model unfalsification. I presented the paper at the 2025 IEEE Conference on Decision and Control (CDC) in Rio de Janeiro, Brazil."
header:
    teaser: /projects/2025-optimistic-pessimistic-unfalsification/opt-pess-teaser.png
---

This paper builds on the results of <a href="/projects/2024-masters-thesis">my Master's thesis</a> and was presented at the <a href="https://cdc2025.ieeecss.org/" target="_blank" rel="noopener noreferrer">2025 IEEE Conference on Decision and Control (CDC)</a> in Rio de Janeiro, Brazil.

In robust control, a controller is modified based on an uncertainty model to ensure stability and, optionally, constraint satisfaction despite worst-case disturbances.
Data-driven approaches are commonly used to identify such an uncertainty model.
However, since the true nature of uncertainties ultimately remains unknown, the notion of *identifying* an uncertainty model is misleading: no amount of data can fully reflect system uncertainty.
Following philosopher Karl Popper's notion of falsifiability, we therefore look for ways to *unfalsify* an uncertainty model instead, i. e. systematically challenging it with the available data to gain confidence in its validity.

The paper proposes two complementary formulations of this problem.
The **optimistic** approach determines the smallest uncertainties that could explain the given data, while the **pessimistic** approach finds the largest possible uncertainties suggested by the data.
The pessimistic problem is revealed to be a semi-infinite program, which we solve using the local reduction algorithm. We also show that the optimistic and pessimistic approaches are mathematical duals: the optimistic uncertainty model constitutes a strict lower bound, falsifying all less conservative models, while the pessimistic model can be taken as a loose upper bound.

Both approaches were tested using an uncertain linear model with data from a simulated nonlinear pendulum-on-a-cart system  simulated, with the Julia package <a href="/projects/SimpleSim">SimpleSim.jl</a>.
The experiments confirm the theory: the optimistic objective grows monotonically as more data is added, and the pessimistic solution upper-bounds the optimistic one.

## Links

- <a href="https://doi.org/10.1109/CDC57313.2025.11312677" target="_blank" rel="noopener noreferrer">Paper on IEEE Xplore (DOI: 10.1109/CDC57313.2025.11312677)</a>
