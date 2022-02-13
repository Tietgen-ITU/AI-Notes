---
id: Rj6hRTOdzg7bAyIuyapUG
title: Search Problem Definition
desc: ''
updated: 1644486024861
created: 1644483921942
---
![](/assets/images/2022-02-10-10-09-13.png)

# What Characterizes AI Search
- The search space is implicitly defined
- The search is goal directed
- The search space often grows exponentially with problem size
- Search actions are abstractrepresentations of real-world actions
  - Valid: can be composed to atomic actions 
  - Useful: "atomic" plans are easy such that states are decision points

# Assumptions about the search domain
![](/assets/images/2022-02-10-10-17-36.png)

# Search problem definition
![](/assets/images/2022-02-10-10-19-36.png)
>**Note:** the first three points form a graph called the state space. You can think of the first three steps of some sort of setup steps.

>**Note:** The $Goal(s)$ is function that determines if the specific state is the goal

A **Solution** is a sequence of actions that leads from $s_0$ to a goal state $a$.

An **optimal solution** is a path with minimum sum of action costs.
# Example: 8-Puzzle
![](/assets/images/2022-02-10-10-29-55.png)
![](/assets/images/2022-02-10-10-30-07.png)

# Example: 4-Queens
![](/assets/images/2022-02-10-10-40-23.png)
![](/assets/images/2022-02-10-10-34-48.png)



