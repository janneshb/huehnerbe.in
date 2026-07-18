---
title: "Distributed Primal-Dual Saddle Point Optimization Applied to Elevator Group Control Systems"
date: 2021-06-01
collection: projects
paper: false
tags: [Coursework, Optimization, Control]
coauthors: [Jeroen Buitendijk]
layout: archive
permalink: /projects/2021-advanced-topics-in-control
excerpt: 'We investigated the problem of elevator dispatching in large buildings by comparing different existing approaches to a custom distributed primal-dual saddle point optimization algorithm.'
header:
    teaser: /projects/2021-advanced-topics-in-control/atic-cover.jpg
---

For the course "Advanced Topics in Control" taught by Prof. Dörfler at ETH Zurich, we developed a novel distributed elevator dispatching algorithm and benchmarked it against established approaches.

Elevator group control, i. e. deciding which elevator serves which call in a large building, is usually handled by a central controller.
A distributed approach is attractive because it makes the system more robust to component failure: when one controller stops working, the unaffected elevators can simply continue operating.

We designed a novel dispatching algorithm based on distributed primal-dual saddle point optimization. To evaluate it, we benchmarked it against the ant colony optimization algorithm, which is well established in the literature, as well as two simple dispatching heuristics. All four algorithms were implemented and simulated in a self-developed elevator group control framework, using models of people flows in buildings that are well established in the literature.

The distributed controller outperforms the benchmark controllers for some building sizes and elevator system configurations.

## Links

- <a href="/files/2021-advanced-topics-in-control/Distributed Primal-Dual Saddle Point Optimization Applied to Elevator Group Control Systems.pdf" target="_blank" rel="noopener noreferrer">Full report (PDF)</a>
