---
layout: project
type: project
image: img/onemin.png
title: "A Material Analysis of MoSe2"
date: 2025
published: true
labels:
  - Quantum Espresso
  - Julia
summary: "My group and I are interested in the properties of the material MoSe2 regarding to solar panel materials, and we discuss our calculations and the results."
---

Molebdynum Diselenide, a Transition-Metal Dichalcogenide (TMDC) is a byproduct in the production of layered deposition of thin film solar panels. Because of this, we are interested in the bandgap of monolayer and multilatyer MoSe2 as well as its other properties with regards to solar panel materials. In this project, we will discuss how we calculated these material properties by using the ab initio plane wave code Quantum Espresso and the ThreeBodyTB.jl package in Julia, and as well as some of the results we gathered.

Provided below is a little snippet from our code where we use this convert our crystal coordinates (that are cartesian coordinates) to fractional coordinates so that we can simulate and make crystals from a package in the Julia language called "ThreeBodyTB":

```
# Function to convert Cartesian coordinates to fractional coordinates
function cartesian_to_fractional(
    A::Matrix{Float64},
    cartesian_coords::Vector{Vector{Float64}}
) :: Matrix{Float64}
    # 1) Invert the lattice matrix
    A_inv = inv(A)
    
    # 2) Convert each Cartesian coordinate to fractional
    fractional_coords = [A_inv * v for v in cartesian_coords]
    
    # 3) Form a 2D matrix (rows = fractional coordinates)
    frac_matrix = hcat(fractional_coords...)'
    
    return frac_matrix
end
```
