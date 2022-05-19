---
id: v9wh2uewteeps62zklg8p55
title: Exam
desc: 'These are some more explainatory notes for the exam'
updated: 1652990345980
created: 1652958356176
---
These notes are an accumulated version of all the notes.

# Heuristic
A heuristic is an estimate of how "far" you are from the goal state. This is used for a lot of different things. Especially path finding. 

## Valid heuristic
A valid heuristic is a heuristic where the goal node has a heuristic of 0 and that the heuristic is non-negative for all the other states.

#### Admissable Heuristic
Here are some of the things with an admissible heuristic:
- It should never overestimate the cost. This means that it should either be equal or under the real "distance"
  
#### Consistent Heuristic
A consistent heuristic is a heuristic where the heuristic between $n$ and $G$ is $h(n)$ is less than the real distance $c(n,a,n') + h(n')$. 

The function $c$ is a function that gives the cost of applying a specific action $a$ on the node in order to get to the next node.

So in mathematical terms a heuristic is consistent if:
$$
h(n) \leq c(n, a, n') + h(n') 
$$

This is where h(n') is the next node after applying the action of the cost. 
This is also called the inequality or sometimes the triangle inequality.

>**NOTE:** Just to add. If a node $a$ has a heuristic that is 13 then the distance between node $a$ and node $b$ (which is this c function) plus the heuristic from node $b$ to the goal has to be greater than or equal to 13 in order for that to be consistent. Remember this has to be true for all nodes. 

![](../assets/images/2022-02-10-11-41-45.png)

# Adversarial Search
This is some of the game AI logic specifying how to get the best possible chance of winning.

The notes about it is in here:
- [[Alpha-Beta|books.RN.Chapter6.alphaBetaPruning]]
- [[Minimax|algorithms.search.games.miniMax]]