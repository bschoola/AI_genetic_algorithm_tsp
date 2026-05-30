# Genetic Algorithm - Travelling Salesman Problem (TSP)

An **AI / GenAI study project** implementing a Genetic Algorithm to solve the classic Travelling Salesman Problem (TSP).

## About

The Travelling Salesman Problem consists of finding the shortest route that visits all cities exactly once and returns to the starting point. Since it is an NP-hard problem, genetic algorithms are an efficient approach to find good solutions in reasonable time.

The simulation runs in real time via Pygame, displaying the evolution of the best route each generation.

## How It Works

The algorithm follows the classic evolutionary cycle:

1. **Initialization** — generates a random population of routes
2. **Fitness Evaluation** — calculates the total distance of each route (shorter = better)
3. **Selection** — chooses parents with probability inversely proportional to distance
4. **Crossover (OX)** — applies Order Crossover to combine genes from both parents
5. **Mutation** — swaps two adjacent genes with a configurable probability
6. **Elitism** — preserves the best individual from each generation

## Project Structure

```
├── tsp.py                  # Entry point — main loop with Pygame visualization
├── genetic_algorithm.py    # Genetic algorithm logic (selection, crossover, mutation)
├── draw_functions.py       # Rendering functions (cities, paths, chart)
├── demo_crossover.py       # Crossover operator demonstration
├── demo_mutation.py        # Mutation operator demonstration
├── benchmark_att48.py      # ATT48 dataset (classic benchmark with 48 cities)
└── requirements.txt        # Project dependencies
```

## Setup and Execution

### Requirements

- Python 3.12+

### Installation

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

### Run

```bash
python tsp.py
```

Press `Q` or close the window to exit.

## Configurable Parameters

In [tsp.py](tsp.py):

| Parameter | Default | Description |
|---|---|---|
| `N_CITIES` | 15 | Number of cities |
| `POPULATION_SIZE` | 100 | Population size |
| `MUTATION_PROBABILITY` | 0.5 | Mutation probability |

## Dependencies

| Library | Version | Purpose |
|---|---|---|
| pygame | 2.5.2 | Real-time visualization |
| numpy | 1.26.4 | Probability calculations |
| matplotlib | 3.8.4 | Chart rendering |


## Resources
From FIAP
https://github.com/FIAP/genetic_algorithm_tsp