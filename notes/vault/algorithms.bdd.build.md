---
id: 5mnar9u03uhl8gicbb51btt
title: Build
desc: ''
updated: 1651148037455
created: 1651143513498
---
*Build* is the stupid version of creating a BDD. So what build does is that it leverages [[the unique table|algorithms.bdd.mk]] that Mk maintains. So in other words *Build* uses Mk. 

*Build* tries to recursively create the BDD with the Shannon Expansion.
Build takes in an expression which in these examples are denoted as $t$. What it then does is that it pulls out one variable at a time from the expression. So it takes the first variable and applies the shannon expansion.

![](/assets/images/2022-04-28-13-04-34.png)

So as you can see it first tries to set the $x$ variable to true(1) and then it tries to set it to false(0).


# The Algorithm
![](/assets/images/2022-04-28-13-08-24.png)

## Explanation 
So the *Build* algorithm starts from variable 1 as you can see at line 9. It takes in an expression called $t$. What the algorithm then first starts to test at line 2 is that, if the current index is larger than the amount of variables that we have, then we test the expression that we have at line 3 and return the result of it.

Else we continue at line 5 and line 6. This is here where we apply the shannon expansion. So by using the shannon expansion we start to build the negative and the positive cofactor. $v0$ and $v1$ is ids of the nodes for the negative and postive cofactor of the current node that we are trying to create.

When $v0$ and $v1$ is found we try to create a new node with the Mk at line 6 and return the id of that node.

In order to illustrate this we use the following example:

### Example of construction of a BDD based on an expression

In order to set the environment we have initialized it to say that we have 3 variables. But as you can see that expression only uses two, namely $x_2$ and $x_3$.

So $n=3$.

The expression that we want to create a BDD for is the following:
$$
x_2 \lor x_3
$$

![](/assets/images/2022-04-28-13-25-48.png)

![](/assets/images/2022-04-28-13-41-01.png)

So what happens here is that we are a variable 1 and try to go to the negative cofactor, however as we do not have $x_1$ in our expression then nothing changes in our expression so it stays the same ($x_2 \lor x_3$, 2) except that we now try to test variable two with the negative cofactor so we move to ($0 \lor x_3$, 3). Now that we are at variable 3 we try to create a new node for that by first testing the negative cofactor this leads us to the following ($0 \lor 0$, 4). Since variable 4 is greater than the amount variables we then test the expression ($0 \lor 0 = 0$ or false. 

![](/assets/images/2022-04-28-13-48-23.png)

Then we try to test the positive cofactor for variable 3(i.e. line 5 in *Build*). Here you can see that we have a case where $x_3$ or variable 3 has a low that gives node id 0 and a high where the node id is 1. So it now tries to create a new node with mk where $Mk(3, 0, 1)$ this creates the node id 2(Remember that the first node that we create after Mk has been initialized is 2) which it returns in the recursive call to the low of variable 2($x_2$).

![](/assets/images/2022-04-28-13-57-52.png)
![](/assets/images/2022-04-28-13-57-59.png)

So now the postive cofactor of $x_2$ is the next thing we want to find.

![](/assets/images/2022-04-28-13-59-35.png)

Here it tries the same thing again that it sets the $x_2$ variable to true(($1 \lor x_3$, 3)). And then it tries to test both the negative and positive cofactor of $x_3$ again. Since the evaluation of the expression for variable 3 in both low and high returns 1. Then the $Mk(3,1,1)$ returns 1 because it would otherwise have been a redundant test.

So now that we have both negative and positive cofactor we can create a new node with $Mk(2, 2, 1)$ which returns a new node id, 3.
It has then created the following bdd in the Mk table:

![](/assets/images/2022-04-28-14-03-09.png)

Saying that if $x_2$ at node id 3 is false then it goes to node id 2 and evaluates that. Else if $x_2$ at node id 3 is true then it goes to node id 1 which is true.

![](/assets/images/2022-04-28-14-06-50.png)

It then tries the positive cofactor for variable 1 but since the other half of generates the same then an insert into Mk would be like $Mk(1, 3, 3)$. Since this is redundant for Mk then build returns the node id of 3. which is the following generated BDD:

![](/assets/images/2022-04-28-14-09-08.png)

# Running time
Is $O(n^2)$ because the size of variables is deciding how many we need to assign when creating the BDD for a particular expression. 