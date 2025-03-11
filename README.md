# Simulated-Annealing
## Member and Contact
* Diego Maldonado Castro  | thebrogrrs@gmail.com | diegomaldonadocastro1805@gmail.com
## License
GNU General Public License v3.0
## Affilation
Final project for the 2025-2 High-performance computing class, designed and developed at the Universidad Nacional Autonoma de México(UNAM), at the Escuela Nacional de Estudios Superiores (ENES Morelia). A project carried out by a student of the Bachelor's Degree in Technologies for Information in the Sciences.
## Introduction
Simulated Annealing is a probabilistic technique used to find the global minimum of an objective function by escaping local minima.

## Justification

This proyect aims to paralelize neighbor making and evaluation. By parallelizing this we can fasten the process at which Simulated Annealing, converges to the final temperature, thus ending the cycle and finding the best solution up until now. 
## Hypothesis

Simulated Annealing can be parallelized thus decreasing time of at which the algorihm performs in high density search spaces.
## General Objetive 

The goal is to adapt Simulated Annealing.
## Particular Objectives
* Parallelize neighbor evaluation.
* Reduce algorithm time duration.

## Simulated-Annealing pesudo-code

1. Initialize the system:
   
    a. Set an initial solution (state) S
    b. Set an initial temperature T
    c. Set a cooling schedule (e.g., T = T * alpha, where alpha is less than 1)
    d. Set a stopping condition (e.g., maximum iterations or minimum temperature)

3. Repeat until stopping condition is met:
   
    a. Generate a neighbor solution S' from the current solution S
    b. Compute the energy difference ΔE = E(S') - E(S), where E is the objective function
    c. If ΔE < 0 (new solution is better), accept S' as the current solution
    d. If ΔE >= 0 (new solution is worse), accept S' with probability exp(-ΔE / T)
    e. Update the temperature: T = T * alpha (reduce the temperature)

5. Return the best solution found.


