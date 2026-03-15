### This repository contains an implementation of various **Artificial Intelligence** search and reinforcement learning algorithms, focusing on shortest path problems under constraints and Markov Decision Processes (MDP).

### Project Structure

* **Assignment1.ipynb**: The main Jupyter Notebook containing the implementation of search algorithms (Uniform Cost Search, A*) and reinforcement learning tasks (Value Iteration, Policy Iteration, Q-Learning).
* **G.json**: Adjacency list representing the graph structure.
* **Coord.json**: Node coordinates for heuristic calculations in A* search.
* **Dist.json**: Edge distances between nodes.
* **Cost.json**: Energy costs associated with traveling between nodes.

---

### Part 1: Search Algorithms

The first part of the project implements pathfinding algorithms on a map of New York City (NYC), incorporating energy constraints.

#### 1. Uniform Cost Search (Dijkstra's)

Solves a relaxed version of the shortest path problem without energy constraints.

* **Algorithm**: Uninformed best-first search that expands nodes in increasing order of cumulative distance.
* **Guarantee**: Guaranteed to find the mathematically shortest path.

#### 2. Shortest Path with Energy Budget

Finds the shortest path from a start node to a target node while ensuring the total energy cost does not exceed a predefined budget.

#### 3. A* Search

Optimizes the search using heuristics to find the shortest path with energy constraints efficiently.

---

### Part 2: Markov Decision Processes (MDP)

The second part focuses on solving stochastic environments using Reinforcement Learning techniques.

#### 1. Value Iteration (VI)

An iterative algorithm that computes the optimal state-value function ($V^*$) and subsequently the optimal policy ($\pi^*$).

* **Process**: Iteratively updates state values based on the Bellman optimality equation until convergence.

#### 2. Policy Iteration (PI)

Alternates between **Policy Evaluation** (computing the value of the current policy) and **Policy Improvement** (updating the policy to be greedy with respect to the new values).

#### 3. Monte Carlo Control (Model-Free)

Learns the optimal policy through sampled experience without requiring a transition model.

* **Approach**: Uses episode returns to estimate the action-value function $Q(s, a)$.

#### 4. Q-Learning (Temporal Difference)

An off-policy TD control algorithm that learns the optimal action-value function independently of the agent's behavior.

* **Updates**: Updates $Q$-values per step based on the maximum predicted future reward.

---

### Key Visualizations

The project includes several visualizations to analyze algorithm performance:

* **Runtime Comparisons**: Box plots and line plots comparing the execution times of Value Iteration vs. Policy Iteration.
* **Policy Grids**: Visual representations of the optimal routes discovered by agents in a GridWorld environment.

### Requirements

* `numpy`
* `matplotlib`
* `heapq`
* `json`
