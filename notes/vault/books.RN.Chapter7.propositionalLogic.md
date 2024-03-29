---
id: mwv2prq6rhmcu7rhs34fld8
title: Propositional Logic
desc: ''
updated: 1654005827914
created: 1646032953355
---
Here it will go through everything that we have talked about in the previous sections ([[books.RN.Chapter7.knowledgeBasedAgents]], [[books.RN.Chapter7.logic]])

# Syntax 
Here we have the syntax of the logic. 
When creating a bit more complex sentences then the

![](./assets/images/2022-02-28-08-24-41.png)
![](./assets/images/2022-03-03-10-34-03.png)
# Semantics
The semantics determines the rules for determining the truth of a sentence with the respect to a particular model. 

![](./assets/images/2022-02-28-18-22-30.png)
![](./assets/images/2022-03-03-10-36-32.png)
These rules can be expressed in a truth table:

![](./assets/images/2022-02-28-18-22-55.png)

![](./assets/images/2022-02-28-18-25-17.png)

# Validity
![](./assets/images/2022-03-03-10-37-59.png)

This also seems a bit like tautologies. So it is sentences that is always true. 

# Satisfiability
![](./assets/images/2022-03-03-10-39-38.png)

Having no models is equivalent to false.
The statement at the bottom is unsatisfiable because it is a contradiction. If $a$ entails $b$ then the sentence $a$ ^ $not(b)$ cannot happen.

# A simple inference procedure
Now our goal is to see if the KB(i.e. the knowledge base) can derive new sentences. Or in other words **entail** new sentences.

![](./assets/images/2022-02-28-18-32-06.png)

## Example
![](./assets/images/2022-03-03-10-48-31.png)

## Properties of the TT-Entails algorithm
![](./assets/images/2022-03-03-10-55-14.png)