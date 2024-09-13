---
title: "VectorlikeStructs.jl"
collection: publications
paper: false
layout: archive
permalink: /projects/VectorlikeStructs
excerpt: 'A Julia package enabling structs to behave like vectors. It is especially useful when working with large vectors that contain various quantities that need to be accessed individually.'
---

This package is especially useful when working with complex state vectors in robotics.

For example, the state of a 6DoF rigid body is defined by its position `p`, velocity `v`, orientation `q` and angular velocities `ω`. Combining these values into one single vector can be complicated to work with. Accessing the angular rate along the y-axis, for example, requires some thinking to determine the right index in this long vector.

`VectorlikeStructs` lets you define a struct that supports numerical operations, such as addition, matrix vector multiplication and scalar vector multiplication, but preserves the convenient dot-indexing of structs.

Define a `@vectorlike` struct as follows:

```julia
@vectorlike struct SixDoFState
    p
    v
    q
    ω
end
```

Now, any `SixDoFState` supports the common numerical operations you are used to from working with vectors. But you can still access the struct as you would expect, too. Retrieving the y-axis component of the angular rate would be as simple as `x.ω[2]`.

Click [here](https://github.com/janneshb/VectorlikeStructs.jl) for the GitHub repository.
