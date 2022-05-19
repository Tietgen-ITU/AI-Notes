---
id: 9bfriqmx7mv7lzih7cxkc09
title: 3. Binary Decision Diagrams
desc: ''
updated: 1652990321364
created: 1646570651244
---
It is first important to note the following for the if-then-else operator:

![](./assets/images/2022-03-06-13-49-35.png)
![](./assets/images/2022-03-06-13-54-13.png)

We call $t$ for the *test expression*.

This gives us a new normal form called [[If-then-else Normal Form (INF)|books.a97.normalForms#if-then-else-normal-form-inf]].

# Bindary decision diagram (BDD)
*OBDD = Ordered Binary Decision Diagram*

Here is an example of a BDD:

![](./assets/images/2022-03-06-14-13-26.png)

Notice the difference between the figure 2 and figure 3. The amount of nodes has been reduced from 9 to 6.

![](./assets/images/2022-03-06-14-15-27.png)
![](./assets/images/2022-03-06-14-15-46.png)

If all identitical nodes are shared and all redundant tests are eliminated then the OBDD is said to be reduced i.e. ROBDD.
![](./assets/images/2022-03-06-14-18-26.png)

ROBDD has a convenient lemma around a property called canonicity:

![](./assets/images/2022-03-06-14-09-28.png)
