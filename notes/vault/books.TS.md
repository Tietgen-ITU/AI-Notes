---
id: 52vm7qktysp8hwavs50cj49
title: TS - Chapter 2 of Tabu Search
desc: ''
updated: 1651744199692
created: 1648614813112
---
This is a note about Chapter 2 in a PDF about *Tabu Search* which is somekind of a [[Local Search for optimization problems|books.RN.Chapter4]].

# What is Tabu search?
Tabu Search is [[books.RN.Chapter5.localSearch]] with heuristic(but Glover does not see this algorithm as a heuristic algorithm but more of a *metaheuristic algorithm*[^1]). This algorithm nearly optimal and is among one the most effective, if not the best, to handle difficult problems at hand. 

This has made the Tabu search(TS from now on) very popular for finding good solutions to the large combinatorial problems in many practical settings. 

## Tabus
*Tabus* are one the key elements in TS. Tabus are used to prevent cycling when moving away from local optima through non-improving moves. 

Basically, when this occurs it needs to prevent the search from tracking back its steps to where it came from. This is being done with *tabus*. 

## Aspiration Criteria
Tabus are essential for TS. But, in some situations it can be too powerful. For that reason, it is necessary to use algorithmic solutions in order to allow cancellation of tabus. These are called *aspiration criteria*. 

I am not completely sure, but in short the aspiration criteria is some sort of rules that says even though there's a tabu, then do it anyway. 

## Termination Criteria
In theory TS could go on forever. Of course we dont like that. So the PDF gives us some solutions on how to fix that:

![](/assets/images/2022-03-31-08-41-21.png)



# Conclusion
![](/assets/images/2022-03-31-06-59-51.png)

---
[^1] Metaheuristic algorithm is a general strategy for guiding and controlling inner heuristics which is created for the problem which is at hand. So it is some kind of balance between exploration and exploitation.