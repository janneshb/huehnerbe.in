---
title: "Distributed Trajectory Planning for Multiple Autonomous Aerial Vehicles"
date: 2021-08-05
collection: projects
paper: false
tags: [Thesis, GNC, Optimization, Robotics]
layout: archive
permalink: /projects/2021-bachelors-thesis
excerpt: "In this project I used ALADIN to implement a distributed trajectory planner for multiple aerial vehicles (such as quadcopters) and compared it to more naïve approaches as well as the corresponding centralized planner."
header:
    teaser: /projects/2021-bachelors-thesis/bachelors-thesis-cover.png
---

In my Bachelor's thesis, I developed centralized and distributed trajectory planners for multiple autonomous aerial vehicles and compared their performance.

With an increasing number of vehicles featuring some degree of autonomy, possible interactions between agents must be taken into account to guarantee safe operation within a confined space. Distributed planning is one way to tackle this: instead of a single central planner computing trajectories for everyone, each agent solves part of the problem itself.

I first developed a centralized planning algorithm that generates safe trajectories for multiple <a href="https://arxiv.org/abs/2209.12048" target="_blank" rel="noopener noreferrer">CRS</a> EmboRockETH agents. I then cast this planner into distributed form and, based on the distributed optimization problem, implemented decentralized planners using ALADIN and round-robin scheduling.

The performance of all trajectory planners (centralized, distributed and the more naïve decentralized variants) was evaluated and compared using various problem setups.
