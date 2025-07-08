# Spectral Element Method in 1D

This project implements the **Spectral Element Method (SEM)** in one dimension for solving partial differential equations (PDEs), particularly the **advection-diffusion-reaction** and **Poisson-type problems**. The implementation emphasizes high-order accuracy using Legendre-Gauss-Lobatto (LGL) nodes and explores both theoretical and numerical aspects of SEM and its numerical integration variant (SEM-NI).

## Overview

The Spectral Element Method is a high-order finite element method that employs global polynomial approximations within each element. SEM achieves exponential convergence for smooth solutions, making it highly efficient for problems with regular behavior.

The notebook included in this repository:
- Formulates the SEM in 1D using a Galerkin-based variational approach.
- Constructs Lagrange interpolating polynomials on LGL nodes.
- Assembles the stiffness and mass matrices using appropriate quadrature rules.
- Solves an example problem with known exact solution:  
  \[
  -\Delta u + u = (\pi^2 + 1)\sin(\pi x), \quad u(0) = u(1) = 0
  \]
- Compares the numerical solution with the analytical solution and studies error convergence.

## Key Features

- **Legendre-Gauss-Lobatto quadrature** for accurate and efficient integration.
- Support for varying polynomial degrees \( N \) and number of elements \( NE \).
- Error analysis in both \( L^2 \) and \( H^1 \) norms.
- Demonstration of **spectral convergence** by increasing polynomial order.

## Repository Contents

- `Spectral_Element_Method_in_1D.ipynb`: Main implementation notebook including derivations, matrix assembly, and convergence studies.
- `Spectral_Element_Method_project_report.pdf`: Detailed report covering mathematical background, implementation steps, convergence theory, and results.

## Example Problem

We solve the boundary value problem:
\[
-\frac{d^2u}{dx^2} + u = (\pi^2 + 1)\sin(\pi x), \quad x \in (0,1), \quad u(0)=u(1)=0
\]
whose exact solution is \( u(x) = \sin(\pi x) \).

## Results

The method exhibits:
- **Third-order convergence** in the \( H^1 \) norm with \( N = 2 \),
- **Spectral (exponential) convergence** as \( N \) increases with fixed \( NE \),
- Sparse system matrices due to collocated quadrature and interpolation points.
