# Depth First Search (DFS) – Shimaa

This folder contains:
- DFS code implementation
- Explanation of how DFS works
- DFS analysis and comparison measures

---

## ⭐ What is DFS?

DFS (Depth First Search) is a graph search algorithm that explores **one full branch deeply** before moving to another.

- Explores the **left-most / deepest path first**
- Uses a **stack**
- Performs **backtracking** when reaching a dead end
- Produces a **valid path**, but NOT the shortest or optimal one

---

## ⭐ Why DFS in the Drone Delivery Problem?

In the drone-delivery route:

- DFS helps check if the drone can reach **all delivery points**
- Ensures the **graph is connected**
- Finds a valid route, but NOT the best or shortest
- Not suitable for finding optimal or cost-efficient routes

---

## ⭐ How DFS Works

1. Start at the initial location  
2. Mark it as **visited**  
3. Move to the next unvisited neighbor  
4. Continue going **deeper**  
5. When reaching a dead end → **Backtrack**  
6. Try another branch  
7. Continue until all reachable nodes are visited or until the goal is found  

---

## ⭐ Python Implementation

def dfs(graph, start):
    visited = set()
    stack = [start]
    order = []

    while stack:
        node = stack.pop()  
        if node not in visited:
            visited.add(node)
            order.append(node)

            for neighbor in reversed(graph[node]):
                if neighbor not in visited:
                    stack.append(neighbor)

    return order

graph = {
    "A": ["B", "C"],
    "B": ["D", "E"],
    "C": ["F"],
    "D": [],
    "E": ["F"],
    "F": []
}

start_point = "A"
visited_order = dfs(graph, start_point)

print("DFS Visit Order:", visited_order)


## ⭐ Example Output

```
DFS Visit Order: ['A', 'C', 'F', 'B', 'E', 'D']
```

Meaning:

- DFS reached all delivery points  
- The path is **not optimal**  
- DFS confirms **connectivity only**  

---

## ⭐ Advantages

- Simple and easy to implement  
- Uses low memory  
- Good for checking connectivity  
- Works well in deep graphs  

---

## ⭐ Disadvantages

- Does NOT give shortest path  
- May explore deep wrong routes  
- Slower in large/deep graphs  
- Not suitable for weighted routes  

---

# ⭐ Comparison Measures for DFS

## 1. Execution Time
DFS can be moderately fast because it goes deep quickly,  
but in large graphs it may waste time exploring long incorrect paths.

---

## 2. Memory Usage
DFS uses very little memory because it only stores:
- The stack  
- The visited nodes  

---

## 3. Success Rate
DFS can reach the goal **if a path exists**.  
It may take a long or wrong route, but it eventually finds a path.

---

## 4. Solution Optimality
DFS does not produce an optimal route.  
It always returns the **first** path it finds, not the shortest or least-cost one.

---

## 5. Scalability
DFS does not scale well.  
When the graph grows deeper or larger, DFS may explore unnecessary long paths before backtracking.

---

