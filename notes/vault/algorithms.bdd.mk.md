---
id: c2vhezaryuajhfnzdlenozm
title: Mk - MakeNode - Unique Table Representation
desc: 'This is a data structure in order to ensure that we do not create BDDs with the same variable'
updated: 1651739084749
created: 1651141254129
---
In terms of terminology we have the following:

![](/assets/images/2022-04-28-12-22-28.png)

In short what the Mk algorithm does is to make a RBDD (Reduced Binary Decision Diagram).
Mk has two tables in the data structure.

#### Table: T
T is the table that can quickly lookup the node id(identifier) and get the variable index(i) what the node points to if it goes to low(l) and what it points to if it goes to high(h).

![](/assets/images/2022-04-28-12-35-49.png)

#### Table: H
H is the table that maps the variable index, low, and high to a specific unique node identifier.
The H table is the inverse of table T.

![](/assets/images/2022-04-28-12-35-58.png)

# Running time of Mk data structure
The running time of the data structure is in constant time, so $O(1)$. That is because this could e.g. be two hashtables.

# The algorithm
![](/assets/images/2022-04-28-12-34-08.png)

## Explanation
At the first line Mk performs a redundancy test. That is if the low and high points to the same node then just return the low node. Because there is no reason to make a new node.
> This is also called a uniqueness test

At line 2 it checks if it already contains a node that has the same variable index, low node, and high node. If so it returns that node that it already contains in line 3. Keep in mind that it is the unique node id that it returns.

If we get to line 4 then it means that it is neither a redundant node and we do not exists in our table already. That means that we create a new node in table T which gives us a new node id $u$. We use that node id to insert it into the H table at line 5, and the we return the new node id in line 6.

### General rules with Mk
So in Mk when it is being initialized it reserves the node ids 0 and 1 to low and high respectively. This means that the first node that is being created after initialization in the table would then be 2 and so on...

![](/assets/images/2022-04-28-12-52-16.png)