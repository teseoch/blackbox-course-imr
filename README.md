# Back-Box Analysis: From Theory to Practice

[Teseo Schneider](https://cs.nyu.edu/~teseo/)

Refer to the [website](https://teseoch.github.io/blackbox-course-imr/) for the full description.

## Abstract
The numerical solution of partial differential equations (PDEs) is ubiquitous in engineering applications, for the simulation of elastic deformations, fluids, and other physical phenomena.

The finite element method (FEM) is the most commonly used discretization of PDEs due to its generality and rich selection of off-the-shelf commercial implementations. Ideally, a PDE solver should be a "black box": the user provides as input the domain boundary, boundary conditions, and the governing equations, and the code returns an evaluator that can compute the value of the solution at any point of the input domain. This is surprisingly far from being the case for all existing open-source or commercial software, despite the research efforts in this direction and the large academic and industrial interest.

To a large extent, this is due to treating meshing and FEM basis construction as two disjoint problems. The FEM basis construction may make a seemingly innocuous assumption (e.g., on the geometry of elements), that lead to exceedingly difficult requirements for meshing software.

This state of matters presents a fundamental problem for applications that require fully automatic, robust processing of large collections of meshes of varying sizes, an increasingly common situation as large collections of geometric data become available. Most importantly, this situation arises in the context of machine learning on geometric and physical data, when one can run large numbers of simulations to learn from, as well as problems of shape optimization, which require solving PDEs in the inner optimization loop on a constantly changing domain.

The first part of the course introduces the finite element method and recent advancements toward an integrated pipeline, considering meshing and element design as a single challenge, leading to a black-box pipeline that can solve simulations on 10 thousand in the wild meshes, without any parameter tuning.

The second part demonstrates the effectiveness the black-box pipeline through practical examples in structural mechanics using state-of-the-art, easy-to-use, open-source Python libraries.