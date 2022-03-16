---
id: 7xnmts9kqekluwo7dnaibw7
title: Implementing The ROBDD Operations
desc: ''
updated: 1647200018136
created: 1647199447573
---
Here small hints on implementing the different contruction algorithm. 

in order to use the table $H$ then it could be implemented as a hash-table using for instance the hash function:

$$
h(i, v0, v1) = pair(i, pair(v0, v1)) \; mod \; m
$$

The pairing function that maps the pairs of natural numbers to natural numbers and $m$ is a prime. A choise for the pairing function is:

![](/assets/images/2022-03-13-20-29-52.png)

This provides no collisions. 
In order to determine $m$ then the book suggests that it could be a very large number. 

#### Implementing table G
The table $G$ used in the *Apply* could be implemented as a two-dimensional array. However, it is better to use a hash-table.