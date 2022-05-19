---
id: jpzd5tndf6iyvqjm1ovclkr
title: Hill Climbing Algorithm
desc: ''
updated: 1651744378488
created: 1648715364905
---
These notes builds on top of this [[books.rn.chapter4#hill-climbing]].

The hill climbing algorithm is a greedy algorithm. This means that out of all of the options that are availble. It takes the best algorithm, whitout really concerning about the optimal solution for the goal.

# Algorithm
![](/assets/images/2022-03-31-10-30-52.png)

# Pros and cons
![](/assets/images/2022-03-31-10-32-54.png)

# Exploitation vs. Exploration
![](/assets/images/2022-03-31-10-33-21.png)

If i want to find the global maximum then then exploitation is not a good option. 

The thing is that between performance and exploiration there is the.

## Meta Heuristic 
Meta heuristic is something that finds some kind of balance between these. In [[lectures.lecture9.simulatedAnnealing]] it tries to simulate a heuristic which works the same way as annealing metal. So it starts by exploring then it moves to exploitation.

# Escaping Local Maxima
![](/assets/images/2022-03-31-10-33-44.png)

# Example: First-Choice Hill Climbing
![](/assets/images/2022-03-31-10-32-37.png)

