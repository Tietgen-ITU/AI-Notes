---
id: y8kmhbpie74fd94qaulzzvj
title: 2. Normal Forms
desc: ''
updated: 1646571905960
created: 1646569626775
---
# Disjunctive Normal Form (DNF)
Boolean expressions is in the *Disjunctive Normal Form*  if it consists of a disjunction of conjunctions of variables and negations of variables. So in other words if the boolean expression is in the following form:

$$
t_{1}^1 \land t_{2}^1 \lor \cdots \lor (t_{1}^1 \land t_{2}^1 \land \cdots \land t_{k_i}^1)
$$

And example of such expression could be:

$$
(x \land \neg y) \lor (\neg x \land y)
$$

*Conjunctive Normal Form* can be written as this:

![](/assets/images/2022-03-06-13-41-36.png)

![](/assets/images/2022-03-06-13-42-22.png)

>**Note:** CNF is [[lectures.lecture5.efficientInferenceAlgorithms.conjunctiveNormalForm]]

![](/assets/images/2022-03-06-13-43-11.png)

# If-then-else Normal Form (INF)
![](/assets/images/2022-03-06-13-59-22.png)
By using the *Shannon Expression*

$$
t = x \to t[1/x], t[0/x]
$$

Then we can see that the boolean expression is an equivalence relation.

![](/assets/images/2022-03-06-14-05-03.png)
