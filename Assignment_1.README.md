MPI Random Walker Simulation
Overview
This project simulates a set of random walkers using the Message Passing Interface (MPI) for parallel processing in C. Each process manages a group of walkers that move within a defined range, passing them to neighboring processes when they exceed local bounds.

Features:
Each process initializes and moves NUM_WALKERS walkers.
Walkers take a random number of steps within their assigned range.
If a walker moves beyond its assigned range, it is passed to the next process using MPI_Send and MPI_Recv.
The last process wraps walkers back to the starting position.
Requirements
C Compiler (e.g., gcc)
MPI Library (e.g., MPICH, OpenMPI)
Compilation
To compile the program, use:

bash
Copy
Edit
mpic++ -o mpi_walkers mpi_walkers.cpp
