---
title: "SimpleSim.jl"
collection: projects
date: 2024-11-01
paper: false
layout: archive
permalink: /projects/SimpleSim
excerpt: 'A minimalist Julia toolbox for modular dynamical systems simulation and for control systems design with support for continuous-time, discrete-time and realistic hybrid systems.'
header:
    teaser: /projects/2024-simplesim/simplesim-cover.jpg
---

## Abstract

`SimpleSim.jl` is a minimalist Julia package for modular dynamical systems simulation and for control systems design.
It can simulate continuous-time and discrete-time dynamical systems and supports mixed ("hybrid") systems.
Timing issues are deconflicted by `SimpleSim.jl` automatically, ensuring precise timing of all systems in the simulation.
In addition to standard simulations, `SimpleSim.jl` provides a few helpful features such as zero-crossing detection and reproducible random variables.

`SimpleSim.jl` does not export any types.
The interface almost solely consists of the function `simulate` and a agreed-upon model structure.
This super light interface results in most design decisions left up to the user.
At the same time `SimpleSim.jl` does not compromise on functionality and offers a feature-rich simulation framework.

Click [here](https://github.com/janneshb/SimpleSim.jl) for the GitHub repository or [here](https://janneshb.github.io/SimpleSim.jl/) for the full documentation.

<!--
## Examples

Below, two illustrative examples of how easy it is to simulate systems in `SimpleSim.jl` are given.
The [full documentation](https://janneshb.github.io/SimpleSim.jl/) of the package provides a few more very detailed examples.

### Controlled Inverted Pendulum on a Cart

For the controlled pendulum, three systems are needed:
* inverted pendulum (CT system)
* controller (DT system)
* feedback loop (CT system)

The inverted pendulum itself is modeled as two nonlinear differential equations,
one for the position of the cart and one for the angle of the pendulum.

```
function fc_inv_pendulum(x, u, p, t)
    # state vector: [z, z', θ, θ']
    # F(t) = u(t)
    dz = x[2]
    θ = x[3]
    dθ = x[4]

    # nonlinear differential equations:
    # | m*ddz - m*l^2*ddθ*cos(θ) + m*l^2*dθ*dθ*sin(θ) = u
    # | l*ddθ - g*sin(θ) = ddz*cos(θ)
    #
    ddz = (u / p.m - p.g * sin(θ) * cos(θ) - p.l * p.l * dθ * dθ * sin(θ)) / (1 + cos(θ) * cos(θ))
    ddθ = (ddz * cos(θ) + p.g * sin(θ)) / p.l
    return [dz, ddz, dθ, ddθ]
end

yc_inv_pendulum(x, u, p, t) = [x[3], x[4]]

inverted_pendulum = (
    p = (g = 9.81, l = 0.5, m = 0.3),
    xc0 = [0.0, 0.0, deg2rad(5.0), 0.0],
    uc0 = 0.0,
    fc = fc_inv_pendulum,
    yc = yc_inv_pendulum,
)
```

### Bouncing Ball
-->

## Citing

If you used `SimpleSim.jl` in research and you are preparing a publication, please use the following BiBTeX entry:

```
@software{SimpleSim,
    author = {H{\"u}hnerbein, Jannes},
    title = {{SimpleSim.jl: A minimalist Julia toolbox for modular dynamical systems simulation}},
    url = {https://github.com/janneshb/SimpleSim.jl},
    version = {0.1.2},
    year = {2024},
    month = {04},
}
```
