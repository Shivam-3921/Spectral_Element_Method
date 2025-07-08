# Spectral Element Method in 1D

This project implements the **Spectral Element Method (SEM)** in one dimension for solving partial differential equations (PDEs), particularly the **advection-diffusion-reaction** and **Poisson-type problems**. The implementation emphasizes high-order accuracy using Legendre-Gauss-Lobatto (LGL) nodes and explores both theoretical and numerical aspects of SEM and its numerical integration variant (SEM-NI).

## Overview

The Spectral Element Method is a high-order finite element method that employs global polynomial approximations within each element. SEM achieves exponential convergence for smooth solutions, making it highly efficient for problems with regular behavior.

The notebook included in this repository:
- Formulates the SEM in 1D using a Galerkin-based variational approach.
- Constructs Lagrange interpolating polynomials on LGL nodes.
- Assembles the stiffness and mass matrices using appropriate quadrature rules.
- Solves an example problem with a known exact solution.
- Compares the numerical solution with the analytical solution and studies error convergence.

## Key Features

- **Legendre-Gauss-Lobatto quadrature** for accurate and efficient integration.
- Support for varying polynomial degrees and number of elements.
- Error analysis in both L_2 and H_1 norms.
- Demonstration of **spectral convergence** by increasing polynomial order.

## Repository Contents

- `Spectral_Element_Method_in_1D.ipynb`: Main implementation notebook including derivations, matrix assembly, and convergence studies.
- `Spectral_Element_Method_project_report.pdf`: Detailed report covering mathematical background, implementation steps, convergence theory, and results.
