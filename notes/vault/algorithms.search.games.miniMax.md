---
id: pIgMNEQdG3vm0X0uedLMo
title: The Minimax algorithm
desc: ''
updated: 1645978622038
created: 1644834981118
---

This algorithm computes the minimax decisions from current state. It applies a recursive computation of the minimax values of each next successor state. 

![](/assets/images/2022-02-17-10-26-44.png)
![](/assets/images/2022-02-17-10-27-26.png)

It goes all the way down to the leaves of the tree and then the minimax values are backed up through the tree as the recursion unwinds. 

![](/assets/images/2022-02-14-11-43-51.png)

The same algorithm from the lecture slides:

![](/assets/images/2022-02-17-10-32-25.png)
>**Note:** That min and max value function calls each other. They shift in turns.

# Space and time complexity
This algorithm performs a complete depth-first exploration of the game tree. The maximum depth of the tree is $m$ and there are $b$ legal moves at each point. 

The algorithm time complexity of the minimax algorithm is $O(b^m)$

The space complexity is $O(bm)$ for an algorithm that generates all actions at once, or $O(m)$ for an algorithm that generates actions one at a time.

![](/assets/images/2022-02-17-10-41-54.png)

# What to do with multi-player games
We use the same algorithm, but uses a vector describing the max goal state for each player:

![](/assets/images/2022-02-17-10-44-13.png)


