# Physics Simulation Project

This project involves a simple physics simulation of mass points connected by springs. The system can display viscous damping, with or without gravity. We use a simple Euler method to update the position and velocity of each mass point over time.

The simulation is displayed as an animation, where each point and its connections are updated for each frame. In addition, you can visualize the final state of the system with a static plot showing the position of each point and its connections.

The resulting animation can be saved as an HTML file. An example simulation can be seen in the animation.html file

## Dependencies

This project requires the following Python libraries:
- Numpy
- Matplotlib
- IPython

## Usage

1. Configure the physical parameters of the system at the beginning of the script. This includes the mass of each point (`m`), the stiffness of the springs (`k`), the rest length of the springs (`L`), the gravitational acceleration (`g`), and the viscous damping coefficient (`γ`).

2. Run the script to execute the simulation. This will display an animated plot of the system evolving over time, followed by a static plot of the system in its final state.

3. The resulting animation can be saved as an HTML file by uncommenting the last two lines of the script.

## Classes and Functions

- `Point`: A class representing a point in the simulation. Each point has an x-coordinate and a velocity.

- `Spring`: A class representing a spring in the simulation. Each spring is connected to two points.

- `update_positions_and_velocities(points, springs, dt)`: A function to update the positions and velocities of the points over a small time step `dt`.

- `get_animation(points, springs)`: A function to create an animation of the simulation. This function calls `update_positions_and_velocities` for each frame of the animation.

## Example

```
# Define the system
m = 0.001 # Point mass [kg]
k = 1e3 # Spring stiffness [kg/s2]
L = 0.01 # Rest length [m]
γ = 0 # or γ = 0.005 Viscous damping coefficient [kg/s] (simulate both)
g = 9.81 # Gravity acceleration [m/s2]

# Run the simulation
ani = get_animation(points, springs)

# Save the animation to an HTML file
with open("animation.html", "w") as f:
    f.write(ani.to_jshtml())
```

## Notes

- The system is initialized with all points at rest.
- The simulation uses a simple Euler method to update the system. This method is not energy-conserving and may exhibit numerical instability for large time steps or stiff systems.
- This code is a basic starting point for more complex physics simulations and can be modified to include other forces, constraints, or interactions between points.