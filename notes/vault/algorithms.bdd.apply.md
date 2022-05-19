---
id: riv9xhdfq8qg6keo67dgp2z
title: Apply
desc: ''
updated: 1651741891116
created: 1651148172859
---
Since build is not very efficient we want another method to try and build our BDDs with. 
What we want is to construct a BDD based of an expression tree:

![](/assets/images/2022-04-28-14-21-50.png)

So what we are going to construct is a multi-rooted BDD:

![](/assets/images/2022-04-28-14-24-52.png)

So in here every node corresponds to an expression. As you can see the $x_1$ variable now contains the operater (OP) *and*. So if $x_1$ is false then the whole statement of the $x_1 \land x_3$ goes to false(denoted by the dotted line from $x_1$ to node 0). If $x_1$ is true then $x_3$ has to be true in order for the whole statement to be true.

The unique table now contains many BDDs.

So Apply is trying to create that:

![](/assets/images/2022-04-28-14-27-00.png)

What *Apply* tries to do is to create a BDD by applying the negative cofactor and the postive cofactor to other expressions that the following operation should try and create. 

In the first expression:

![](/assets/images/2022-05-05-10-47-52.png)

What it does is that it tests the same variable and creates a new BDD with it. However, $x$ is not necessarily the same node. 

In terms of this expression:

![](/assets/images/2022-05-05-10-48-47.png)

It tries to create a new BDD with a variable $x$ and an expression $t$.

![](/assets/images/2022-04-28-14-32-11.png)

in this picture, the v and w is the number of the node. So the node Id. 
# The algorithm
![](/assets/images/2022-04-28-14-32-41.png)

At the first line we initialize $G$. What it does is that it remembers the result of previous calls of apply with the same nodes. If it already has computed the result before, it just looks it up and returns it.

Every time we have computed the BDD we then store it in the $G$ table(line 12).

## Example explanation
![](/assets/images/2022-05-05-11-03-24.png)

We start by calling apply with the operator *and* with nodeid 5 and 6($5 \land 6$)

![](/assets/images/2022-05-05-11-10-13.png)

What it does after is that it goes to line 9 and call the Mk with $u_1$ which is 5 and gets the low node for 5 and 6, which is 0 and 3. 