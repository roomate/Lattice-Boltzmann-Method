# Lattice Boltzmann Method

The Lattice Boltzmann Method (or LBM for short) is a numerical method dedicated to the simulation of fluids. 
This method became quite popular during the last decades for at least two reasons.

It is important to keep in mind that Vanilla CFD methods are usually quite challenging to fully grasp, as they are very complex and
computationally demanding. They implicitely rely on state-of-the-art numerical analysis and software engineering as it entails
to solve coupled kinetics and thermodynamics Partial Differential Equations (PDEs) in a given domain. Standard sophisticated numerical schemes with
this objective are Hybrid High Order (HHO) or Compatible Discrete Operator (CDO) schemes for example.

In this context, the LBM is advantageous by its simplicity. It is not computationally very expensive, easily parallelizable, and the resolution algorithm is quite simple, 
only a few steps. While most methods try to solve Navier-Stokes equations (recall this terminology also incorporates continuity and thermodynamics equations), the LBM focus on only one single equation, derived
from Statistical Physics: the Boltzmann equation. You might know that from Boltzmann equation arises an infinite cascad of equations known as the BBGKY hierarchy.
In particular, the key point is that one can recover Navier-Stokes equations via the Chapman-Enskog development, which assumes the dimensionless Knudsen number is very small.
Hence, the LBM is dedicated to solve only one, yet very complicated, equation whose unknown is the distribution function, a multi-variate function of
2D+1 variables, where D is the space dimension.