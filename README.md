# Job_search_Model
This repository contains a simulation-based study of the McCall job-search model, extended with reinforcement learning (Q-learning) and Bayesian updating for unknown wage-offer distributions. The project compares classical dynamic programming methods with machine learning approaches to study convergence, reservation wages, and unemployment dynamics.

 **Project Contents**

Job Search Model (Search with Learning).ipynb
Main Jupyter notebook containing:

Model setup and parameterization

Method 1 – Value Function Iteration (VFI): Solves the Bellman equation to compute optimal reservation policies.

Method 2 – Reservation Wage Functional Equation (RWFE): Faster fixed-point iteration approach using operator mappings.

Offer Distribution Unknown Model: Extends the baseline by incorporating Bayesian belief updating over competing wage distributions.

Q-learning Implementation: Uses temporal-difference learning with an ε-greedy policy, Monte Carlo draws, and vectorized simulation.

Simulations & Plots: Demonstrates unemployment dynamics under different wage-offer distributions and learning setups.

**Methods Implemented**

Dynamic Programming Baseline

Bellman equation solved by VFI.

Visualizes convergence of value functions and reservation wages.

Q-learning with Temporal-Difference Updates

Implements an agent-based simulation with exploration–exploitation tradeoffs.

Compares learning outcomes against the dynamic-programming baseline.

Unknown Wage-Offer Distributions

Bayesian learning over Beta families of wage distributions.

Reservation Wage Functional Equation (RWFE) solved via operator iteration and bilinear interpolation.
