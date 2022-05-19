---
id: s8pyld6pi0tatjqr2u7ksnu
title: Construction of ROBDD (Reduced Ordered Binary Decision Diagram)
desc: ''
updated: 1652990322664
created: 1647197226440
---
Here we talk about how to construct a binary decision tree.
There are different ways to construct a ROBDD. One approach could be to just construct an OBDD, and then continue to reduce it.

But we are going to cover a more appealing approach. 

# Terminology
First we need to set some terminology:

- Nodes are represented as numbers: $0,1,2 \dotsc$ with 0 and 1 reserved as terminal nodes. 
- The variables in the ordering $x_1 < x_2 < \dots < x_n$
- ROBDD is stored in a table: $T : u \to (i,l,h)$ which maps a node $u$ to its three attributes $var(u) = i$, $low(u) = l$, and $high(u) = h$

![](./assets/images/2022-03-13-20-01-17.png)

# Algorithms to build ROBDD´s
Here we will walk through some of chapter 4th ideas to construct a ROBDD[^1]

## Mk
Here it tries to create somekind of inverse table of $T$ called $H$.

The inverse table of $T(u) = (i, l, h)$, if and only if, $H(i,l,h) = u$ 

Table $T$ can determine the node by providing the id $u$ in constant time. And the inverse table $H$ can with the node give the id in constant time.

Here are the two operations needed on the two tables:

![](./assets/images/2022-03-13-20-07-01.png)

![](./assets/images/2022-03-17-10-10-45.png)

The following function $MK[T,H](i,l,h)$ searches the table $H$  for a node with variable index i and low-, high-branches $l,h$ and returns a matching node if one exists. Otherwise it creates a new node $u$, inserts it into $H$ and returns the identity of it. 

The running time of *MK* is $O(1)$ due to assumptions on the basic operations on $T$ and $H$.

#### Algorithm of MK

![](./assets/images/2022-03-17-10-11-38.png)

## Build
Here is a picture showing how *Build* to compute the ROBDD:

![](./assets/images/2022-03-13-20-20-32.png)

The running time of *Build* is bad. The running time is $O(2^n)$. This is due to variable ordering with $n$ variables there will always be generated on the order of $2^n$ calls.

So what it is going to do is that it recursively builds the BDD.
However the two terminal cases is being added first.

![](./assets/images/2022-03-17-10-28-42.png)

#### Algorithm of Build
![](./assets/images/2022-03-17-10-29-29.png)

## Apply
What we are trying to do now is that we want to represent every internal node as BDD. In other words we are trying to create an expression tree. In the lecture we are also calling this a *Multi-Rooted BDD*.

![](./assets/images/2022-03-17-10-43-44.png)
>**Note:** that every node is its own BDD

So now we are trying to create a function (i.e. ´Apply´) in order to construct this tree:

![](./assets/images/2022-03-17-10-45-41.png)

### Properties
![](./assets/images/2022-03-17-10-51-01.png)

### Algorithm
So the algorithm works as the following:

![](./assets/images/2022-03-17-10-48-21.png)

#### Algorithm of APPLY

![](./assets/images/2022-03-13-20-23-20.png)

---
[^1] It will only cover chapter 4.1, 4.2, and 4.3