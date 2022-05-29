---
id: zlha29ltplmzwwuxt6luf6r
title: Definite Clause
desc: ''
updated: 1653744188538
created: 1646303814929
---
![](./assets/images/2022-03-03-11-37-10.png)
Definit clauses is when there are no negative literals. 

In order to see if there is only one positive literal you need to apply the implication elimination like the following:

![](/Users/andreastietgen/Documents/Programmering/UNI/ArtificialIntelligence/AI-Notes/notes/vault/assets/images/2022-05-28-15-21-21.png)

So the head stays as is. And the implication and conjunctions is converted to disjunctions. Then every symbol in the body will be negated. Then you should see in the bottom if there is a positive literal(as seen in the picture the a is the only positive literal).