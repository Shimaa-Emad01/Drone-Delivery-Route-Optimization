**Drone Delivery Route Optimization Using AI Search Algorithms**

## 📌 Project Overview

This project implements and compares **six Artificial Intelligence search algorithms** to solve the **Drone Delivery Route Optimization Problem**.
The delivery environment is represented as a **weighted graph**, where each node is a delivery point and each edge represents a possible drone path.

The goal is to determine the **most efficient route** from the start location to the target location using different search techniques.

---

## 🚀 Algorithms Implemented

A diverse set of search paradigms were implemented by the team to ensure a comprehensive comparison:

| Algorithm Name                 | Paradigm                     | Responsible Team Member |
| :----------------------------- | :--------------------------- | :---------------------- |
| **Depth First Search (DFS)**   | Uninformed Search            | Shimaa                  |
| **Breadth First Search (BFS)** | Uninformed Search            | Hamza                   |
| **Uniform Cost Search (UCS)**  | Cost-Based Uninformed Search | Mariam                  |
| **Greedy Best-First Search**   | Heuristic Search             | Amira                   |
| **A* Search (A-Star)**         | Optimal Heuristic Search     | Ismail                  |
| **Genetic Algorithm (GA)**     | Evolutionary / Metaheuristic | Abdelrahman             |

---

## 🎯 Objectives & Evaluation Metrics

Each algorithm is evaluated using the following performance criteria:

* **Execution Time:** How fast the algorithm finds a route.
* **Memory Usage:** Amount of memory used during the search.
* **Solution Optimality:** How close the path cost is to the optimal route.
* **Scalability:** Performance as the graph grows in size and complexity.
* **Success Rate:** How consistently the algorithm produces a valid path.


## 🧪 Tech Stack

* **Programming Language:** Python 3.x
* **Version Control:** GitHub
* **Optional:** Matplotlib / NetworkX for graph visualization



## 📈 Key Findings (Summary)

* **A*** produced the most optimal paths consistently.
* **Greedy Search** was the fastest but not always optimal.
* **UCS** found optimal solutions for weighted graphs.
* **DFS & BFS** performed well on simple, unweighted graph structures.
* **Genetic Algorithm** gave near-optimal results on large/complex graphs.


## 👥 Team Members

| Member Name     | Contribution                                        |
| :-------------- | :-------------------------------------------------- |
| **Shimaa**      | DFS Implementation & Analysis                       |
| **Hamza**       | BFS Implementation & Analysis                       |
| **Mariam**      | UCS Implementation & Analysis                       |
| **Amira**       | Greedy Search Implementation & Analysis             |
| **Ismail**      | A* Search Implementation & Analysis                 |
| **Abdelrahman** | Genetic Algorithm Implementation & Final Comparison |
