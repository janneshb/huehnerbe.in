---
title: "Vacci Nation &mdash; Modeling the Outbreak of an Influenza Strain in a Population with Different Belief Groups"
date: 2019-12-02
collection: projects
paper: false
tags: [Coursework, Optimization, Control, Game Theory, Simulation]
coauthors: [Nicolas Antunes Morgado, Benjamin Gundersen, Julius Siebenaller]
layout: archive
permalink: /projects/2019-vacci-nation
excerpt: 'We modeled the outbreak of an influenza strain for a community that consists of two belief groups regarding vaccination ("trusters" and "skepticals"). The disease spreads according to an SIVR-model taking into account the game theory based vaccination decisions of the individual agents.'
header:
    teaser: /projects/2019-vacci-nation/vacci-nation-cover.png
---

In this course project, we modeled the outbreak of an influenza strain in a community that is split into two belief groups regarding vaccination ("Trusters" and "Skepticals") who perceive the cost of getting vaccinated differently.

Whether an outbreak takes hold in a community depends not only on the disease itself, but also on the vaccination decisions of the individuals in it. We wanted to understand how the composition of a community affects vaccine uptake and, ultimately, the course of an epidemic.

Each belief group forms a sub-community modeled as a small-world network, and the networks are combined into one population. The disease spreads according to an SIVR model, driven by the infection rate and the decisions of the individual agents. Each agent follows a simple game-theoretic model to decide whether to vaccinate, weighing its cost of vaccination against a regularly updated outbreak forecast over a given time horizon.

On top of this baseline, we studied how different distributions of the two groups change the outbreak, and how the agent-specific parameters affect the outcome.

The results are in line with, and confirm, previous research. Most notably, vaccine uptake levels turned out to be much more sensitive to the share of Trusters in the community than to the cost ratios within the individual groups.

## Links

- <a href="/files/2019-vacci-nation/Report_Vacci-Nation.pdf" target="_blank" rel="noopener noreferrer">Full report (PDF)</a>
