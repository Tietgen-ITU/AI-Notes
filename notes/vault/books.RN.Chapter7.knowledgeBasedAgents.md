---
id: 1pe0gju4ulqee08yphsso5i
title: knowledgeBasedAgents
desc: ''
updated: 1645980834704
created: 1645979175196
---
The central thing of a knowledge based agent is it knowledge base or KB. 

**Knowledge base** is a set og sentences. Sentences here is a technical term not a sentence as we know it from english.

Each sentence is expressed in a language called knowledge representation language. It represents some assertions of about the world.

There are two standard operations:
- **ASK** - Query sentences
- **TELL** - Add sentences

Some of these operations may involve **inference**. Inference is when it derives new sentences from old onew. 

Each time the program is being called it first **TELLS** the knowledge base what is percieves. Secondly is **ASKS** the knowledge base what action it should perform. In the process of answering this query, extensive reasoning may be done about the current state of the world, about the outcomes of possible action sequences and so on.

The function **Make-Perfect-Sentenc** constructs a sentence asserting that the agent perceived the given percept at the given time. 

The function **Make-Action-Query** constructs a sentence that asks what action should be done at the current time. 

The function **Make-ActionSentence** constructs a sentence asserting that the chosen action was executed. 

![](/assets/images/2022-02-27-17-53-53.png)


