---
id: pIgMNEQdG3vm0X0uedLMo
title: The Minimax algorithm
desc: ''
updated: 1644835432780
created: 1644834981118
---

This algorithm computes the minimax decisions from current state. It applies a recursive computation of the minimax values of each next successor state. 

It goes all the way down to the leaves of the tree and then the minimax values are backed up through the tree as the recursion unwinds. 

![](/assets/images/2022-02-14-11-43-51.png)

This algorithm performs a complete depth-first exploration of the game tree. The maximum depth of the tree is $m$ and there are $b$ legal moves at each point. 

The algorithm time complexity of the minimax algorithm is $O(b^m)$

The space complexity is $O(bm)$ for an algorithm that generates all actions at once, or $O(m)$ for an algorithm that generates actions one at a time.

