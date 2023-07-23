# Numerical Analysis with Python
This repository contains scripts for performing numerical analysis. The scripts demonstrate the implementation of numerical root finding (Newton-Raphson method applied on the Lotka-Volterra system) and numerical integration methods (Trapezoidal, Simpson, Midpoint, and Monte Carlo). 

## Contents
The repository includes two Python scripts:

1. `lotka_volterra.py` - This script numerically solves the Lotka-Volterra system using the Newton-Raphson method. The Lotka-Volterra system is a pair of first-order, non-linear, differential equations frequently used to describe the dynamics of biological systems in which two species interact, one as predator and the other as prey. It also includes 3D visualization for the Lotka-Volterra solutions, fox population growth, and rabbit population growth depending on R (prey population) and F (predator population).

2. `numerical_integration.py` - This script approximates a definite integral of a standard normal distribution over the interval from 0 to 5. It implements four different methods of numerical integration: Trapezoidal rule, Simpson's rule, Midpoint rule, and Monte Carlo method. It shows a log-log plot of the relative error of each method as a function of the number of subdivisions/intervals used.

## Requirements
To run these scripts, you need Python 3.x and the following libraries installed:
- NumPy
- Matplotlib
- Scipy