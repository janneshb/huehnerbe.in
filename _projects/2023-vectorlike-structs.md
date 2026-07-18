---
title: "VectorlikeStructs.jl"
collection: projects
date: 2024-10-01
paper: false
tags: [Software, Julia]
layout: archive
permalink: /projects/VectorlikeStructs
excerpt: 'A Julia package enabling structs to behave like vectors. It is especially useful when working with large vectors that contain various quantities that need to be accessed individually.'
---

`VectorlikeStructs.jl` is a Julia package that lets structs behave like vectors — combining the numerical operations you expect from vectors with the convenient dot-indexing of structs.

## Background

The package is especially useful when working with complex state vectors in robotics. For example, the state of a 6DoF rigid body is defined by its position `p`, velocity `v`, orientation `q` and angular velocities `ω`. Combining these quantities into one long vector is awkward to work with: accessing the angular rate along the y-axis, for example, requires some thinking to determine the right index.

## Usage

Define a `@vectorlike` struct as follows:

```julia
@vectorlike struct SixDoFState
    p
    v
    q
    ω
end
```

Any `SixDoFState` now supports the common numerical operations you are used to from working with vectors, such as addition, matrix-vector multiplication and scalar multiplication. At the same time, you can still access the struct as you would expect: retrieving the y-axis component of the angular rate is as simple as `x.ω[2]`.

## Links

- <a href="https://github.com/janneshb/VectorlikeStructs.jl" target="_blank" rel="noopener noreferrer">GitHub repository</a>
