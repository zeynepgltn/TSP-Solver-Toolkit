# Traveling Salesman Problem Algorithm Implementations

This repository contains various algorithm implementations for solving the Traveling Salesman Problem (TSP). The TSP is a classic optimization problem where the goal is to find the shortest possible route that visits each city exactly once and returns to the origin city.

## Algorithms Implemented

This project includes the following algorithms:

### Construction Heuristics
- **Nearest Neighbor**: A greedy approach that always visits the nearest unvisited city
- **Greedy Algorithm**: Another construction heuristic that builds a path by selecting the closest city at each step

### Improvement Heuristics
- **2-opt**: A local search algorithm that improves an existing route by swapping edges
- **Held-Karp Algorithm**: An implementation of a dynamic programming approach for TSP

### Metaheuristics
- **Simulated Annealing**: A probabilistic technique for approximating the global optimum
- **Ant Colony Optimization (ACO)**: A probabilistic technique inspired by the behavior of ants
- **Christofides Algorithm**: A heuristic algorithm that guarantees a solution that's at most 1.5 times longer than the optimal solution

## Test Cases

The algorithms have been tested on various datasets of different sizes:
- 51 cities
- 150 cities 
- 318 cities
- 3038 cities
- 14051 cities

## Implementation Details

All algorithms are implemented in Python, with the following dependencies:
- numpy
- matplotlib (for visualization)
- networkx (for the Christofides algorithm)
- math, time, random (standard libraries)

## Performance Comparison

| Algorithm | Cities | Time (s) | Total Distance |
|-----------|--------|----------|----------------|
| Held-Karp + 2-opt | 51 | 0.58 | 449.25 |
| Ant Colony Optimization | 51 | 3.54 | 468.04 |
| Christofides + 2-opt | 150 | 37.71 | 27899.07 |
| Ant Colony Optimization | 150 | 24.44 | 30922.63 |
| Simulated Annealing | 150 | 0.32 | 52041.52 |
| Nearest Neighbor + 2-opt | 318 | 2.87 | 45972.80 |
| Nearest Neighbor + 2-opt + SA | 318 | 6.32 | 48845.29 |
| Nearest Neighbor + 2-opt | 3038 | 2.25 | 172462.12 |
| Greedy | 14051 | 24.70 | 575715.88 |

## Usage

To run any of the algorithms, simply execute the corresponding Python script:

```bash
python nearest_neighbor_2opt.py
```

Or run the Jupyter notebooks included in the repository:

```bash
jupyter notebook Held-Karp-2-optyerelarama.ipynb
```

## Future Work

Future improvements to this project may include:
- Parallelization of computations
- Implementation of genetic algorithms
- Interactive visualization of routes
- Hybrid metaheuristics for improved solutions
- Support for asymmetric TSP instances

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- The TSP test data used in this project is derived from standard benchmark instances
- Special thanks to the open-source community for resources on TSP algorithms and implementation tips
