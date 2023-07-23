# Molecular Dynamics Simulation Using Lennard-Jones Potential

This project presents a Python implementation of a molecular dynamics (MD) simulation using the Lennard-Jones potential. The simulation is performed for a collection of particles in a three-dimensional box with periodic boundary conditions. 

## Dependencies
The script uses the following Python packages:
- numpy
- matplotlib
- tqdm
- IPython

## Features
1. Lennard-Jones Potential: The Lennard-Jones potential is used to model the interaction between two particles. This potential energy function represents a simple model of the non-bonded interactions between a pair of neutral atoms or molecules.

2. Molecular Dynamics Simulation: The particles in the simulation are initialized with random velocities and are evolved over time according to the laws of classical mechanics.

3. Periodic Boundary Conditions: When a particle moves out of the box in the simulation, it enters from the opposite side due to the implementation of periodic boundary conditions. 

4. Visualization: The simulation is visualized using Matplotlib's 3D plotting capabilities. In addition, the temperature of the system is plotted over time.

5. Performance: The simulation uses a cell list algorithm to accelerate the computation of forces, and allows the option of using either square root computations or avoiding them for further speed gains.

## Usage
The script has several key parameters that you can adjust according to your needs:
- `N`: the number of particles in the simulation
- `dt`: the time step size
- `display_interval`: the number of steps between each frame of the animation
- `Lx`, `Ly`, `Lz`: the dimensions of the simulation box
- `m`, `eps`, `sig`: parameters of the Lennard-Jones potential

After setting these parameters, you can simply run the script to generate the animation of the MD simulation. The result is an MP4 video file `animation.mp4`.

## Future Enhancements
Future work on this project may include the addition of more complex interaction potentials, the inclusion of bonded interactions for simulating complex molecules, and further optimization to handle larger numbers of particles. 
