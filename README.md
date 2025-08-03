Protein Search for Targets on DNA: A Theoretical Approach
Author: Soumik Nath

Institution: Indian Institute of Science Education and Research (IISER) Bhopal

Supervisor: Dr. Rati Sharma

Project Duration: Summer Internship 2025

1. Overview
This project investigates the "speed-selectivity paradox" in protein-DNA interactions, a fundamental puzzle in molecular biology. The paradox arises because proteins must search for specific target sequences on DNA both quickly (requiring weak, non-specific binding) and accurately (requiring strong, stable binding).

The primary goal of this internship was to use a discrete-state stochastic model to analyze the protein search process, demonstrating how this approach can resolve the paradox where simpler continuum models fail.

Key Objectives:
Reproduce Key Results: Implement Monte Carlo simulations to model the stochastic hopping and sliding of a protein along a DNA chain.

Derive Analytical Theory: Work through the mathematical formalism of the Backward Master Equation (BME) to derive equations for the mean search time.

Compare and Validate: Plot and compare the results from the simulations against the analytical theory to validate the model.

Preliminary Study: Implement the Gillespie Algorithm to simulate Michaelis-Menten enzyme kinetics as an introduction to stochastic modeling.

2. Methodology
The project is built on a theoretical framework that models the protein's movement as a series of discrete steps.

A. The Model
The system is modeled as follows:

DNA: A one-dimensional lattice of L sites. One site, m, is the target.

Protein States: The protein can be in one of two states:

Bound to DNA: The protein is at a specific site i on the lattice.

Free in Solution: The protein is in the bulk solution (state 0).

Transition Rates:

u: Hopping rate to adjacent sites on the DNA (1D sliding).

k_off: Dissociation rate from DNA into the solution.

k_on: Association rate from the solution to any site on the DNA.

B. Analytical Solution
The Backward Master Equation (BME) was used to calculate the mean first-passage time (MFPT)—the average time for the protein to find the target for the first time. By setting up and solving a system of differential equations for the probability of finding the target from any starting position, we derived an analytical expression for the average search time (T_0).

C. Monte Carlo Simulations
To validate the analytical theory, a stochastic simulation was developed. The simulation tracks a single protein molecule as it randomly binds, slides, and unbinds from the DNA according to the defined transition rates. The time taken to reach the target site m is recorded, and the process is repeated thousands of times to calculate a reliable average search time.

3. Key Results and Discussion
The project successfully demonstrated that the discrete-state model resolves the speed-selectivity paradox and accurately predicts protein search dynamics.

Effect of Target Position: The search time is fastest when the target is located in the middle of the DNA chain due to symmetry. However, this effect diminishes significantly as the DNA length (L) increases.

Effect of DNA Length: For biologically realistic DNA lengths (e.g., L > 1000), the search time becomes largely independent of the target's specific location (unless it is at the very ends).

Model Validation: The results from the Monte Carlo simulations show excellent agreement with the predictions from the analytical BME-based theory, confirming the validity of our approach.

4. Future Work
The current 1D model can be extended to a more realistic 2D lattice to better represent the cellular environment.

Proposed 2D Model: The DNA is placed as a line in the center of a 2D grid representing the cytoplasm.

New Dynamics: When the protein dissociates from the DNA, it will perform a 2D random walk (diffusion) in the cytoplasm before eventually rebinding to the DNA.

Goal: This enhanced model will allow for a more accurate investigation of the role that 3D diffusion plays in the overall search process.

5. Repository Contents
Internship_Report.pdf: The full internship report with detailed derivations and discussion.

/Code: Contains the Python scripts for the Monte Carlo simulations and plotting.

gillespie_MM.py: Gillespie algorithm for Michaelis-Menten kinetics.

protein_search_simulation.py: Main simulation for the protein search on DNA.

/Plots: Figures and plots generated from the simulations and analytical calculations.
