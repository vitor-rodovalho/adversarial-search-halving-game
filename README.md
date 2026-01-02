# 🎮 Halving Game: Adversarial Search & Optimization

[![Python](https://img.shields.io/badge/Python-3.12%2B-blue.svg)](https://www.python.org/)
![Game Theory](https://img.shields.io/badge/Area-Game%20Theory-green.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project presents a deep dive into Game Theory applied to the **Halving Game**, a zero-sum game of perfect information. The primary goal is to demonstrate the implementation of the **Minimax** algorithm, **Alpha-Beta Pruning** optimizations, and the critical impact of **Memoization** on the scalability of intelligent agents.



## 🧠 The Problem: Halving Game

Two players, $P(+1)$ (Maximizer) and $P(-1)$ (Minimizer), manipulate an integer $N$ until it reaches 0. The possible actions are:
* **Decrement:** $N = N - 1$
* **Division:** $N = \lfloor N / 2 \rfloor$

**Win Condition**: The player who receives the state $N = 0$ wins the match. In other words, the player who makes the move resulting in $N = 0$ **loses** the game.



## 📊 Statistical and Mathematical Analysis

The game's state space and optimal strategies were analyzed to understand the distribution of winning positions. Under perfect play (Minimax), the game is deterministic, meaning the winner is decided by the starting value of $N$.

Below is the visualization of the statistical distribution and the game's mathematical landscape:

![Statistical and Mathematical Analysis](assets/HalvingGame.png)

*The dashboard above illustrates the win distribution and the convergence of the win rate towards the theoretical mean.*



## 🚀 Technologies & Algorithms

* **Language:** Python 3.10+
* **AI Algorithms:**
    * **Minimax:** Exhaustive decision tree search.
    * **Alpha-Beta Pruning:** Optimization that reduces the search space by discarding irrelevant branches.
    * **Memoization (Dynamic Programming):** Transforming the search tree into a Directed Acyclic Graph (DAG), reducing complexity from exponential $O(b^d)$ to linear $O(N)$.
* **Visualization:** Matplotlib and Plotly (Interactive).



## 📈 Performance & Scalability

The optimized implementation achieved a performance gain exceeding **18,000x** compared to pure Minimax search for $N=200$.

| N | Pure Minimax (s) | Optimized Minimax (s) | Speedup (x) |
|---|---|---|---|
| 20 | 0.0011 | 0.0002 | 5.6x |
| 100 | 0.3421 | 0.0003 | 923.4x |
| 200 | 15.5736 | 0.0008 | **18,599.2x** |



## 🛠️ Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/vitor-rodovalho/adversarial-search-halving-game.git
    ```

2. Install dependencies, if needed:
    ```bash
    pip install matplotlib plotly
    ```

3. Run the notebook in Google Colab or locally via Jupyter.



---

## ⚠️ Language Note

Please note that the code comments are currently in **Portuguese**, as this project was originally developed for a university assignment.

## 📄 Author

Developed by **Vitor Hugo Rodovalho**.

---
   
