---
id: hdaOWm2idoClfidLApYBU
title: Tree
desc: ''
updated: 1644487660879
created: 1644317893343
---
A tree data structure consists of **nodes** and **leaves**. 
A tree data sructure can also be refered to as a *search tree* when the tree is structured in a specific manner that provides the ability to traverse down the tree to the specific instance of searching that it wants to solve.

A search tree has a **Root** which is the first node or top node. It is where you have a path to every node or leaf.


A **leaf** does not have any children. They do contain some value that it represents. Leaves are at the "edge" of a tree so to speak. You cannot traverse further down to another node when you have reached a leaf. 

A **node** is an extension of a leaf or can be. A node can also contain a value. However, it can also have children. Those children could be another node or a leaf. 

A set of all the leaf nodes that is available for expansion at any given point is called the frontier. 

Here is an example of a tree:
![](/assets/images/2022-02-08-12-12-05.png)

# Redundant Paths
According to the book then redundant paths is sometimes unavoidable.
>*"In other cases, redundant paths are unavoidable. This includes all problems where the actions are reversible, such as route-finding problems and sliding-block puzzles"*[^1]

A **loopy path** is special case of a redundant path where for example in the picture have "Arad" as a root which have "Timisoara" as a child which then has "Arad" as a child.

---
[^1] Book RN, Chapter 3.3 *Searching for solutions*, Page 77, line 1