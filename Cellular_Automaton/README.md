
# Vertex Model for Simulating Growth and Division of Cells

## Description
This Python project models growth and division of cells in a tissue by simulating a Cellular Automaton. It captures the fundamental properties of biological cells: growth, division, and the mechanical interactions with their surroundings. The program simulates an array of cells and their evolution over time. It starts with a predefined number of cells, each cell grows, and once it reaches a certain size, it divides, creating a new cell.

## Dependencies
- numpy
- matplotlib
- IPython

## Installation
No specific installation procedure is required for this project. You only need to have Python (version 3.6 or later) installed on your machine along with the required libraries.

## Usage
The simulation parameters can be modified directly in the script:
- `Nc`: the initial number of cells in each direction.
- `D`: the initial diameter of each cell.
- `K`, `T`, `gamma`, `h`, `n`: constants used in the simulation.
- `display_interval`: the interval at which to update the display of the simulation.
- `grow_c_i`: indices of the cells that grow.
- `grow_speed`: the speed at which the cells grow.
- `l_min`: minimum length for a cell edge before it gets removed.

## Implementation Details
The implementation includes the following classes:
- `Vertex`: Represents a vertex in the simulation. Each cell is represented by a polygon whose corners are vertices. The vertices store the forces acting on them and are used to update the position of the cells.
- `Cell`: Represents a cell in the simulation. A cell has a list of vertices that make up its shape. It can calculate its area, perimeter and divide into two cells.

The main script initializes the cells and vertices, merges shared vertices, adds randomness to the initial positions of the vertices, calculates the initial target areas for each cell and runs the main loop that updates the positions and velocities of the vertices, and handles cell growth and division.

## Contributing
If you want to contribute to this project, please open a GitHub issue to discuss what you would like to change.

## License
This project is open-source. Feel free to use, modify and distribute the code.

