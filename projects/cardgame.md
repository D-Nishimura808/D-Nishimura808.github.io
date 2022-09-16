---
layout: project
type: project
image: img/Queen-Of-Hearts.jpg
title: "Card Game Project"
date: 2022
published: true
labels:
  - Java
  - Programming
summary: "During the course of my ICS 211 class, we were tasked with implementing a version of the card game War using Java."
---


For my ICS 211 class, one of the homework assignments to write the code for a card game. The card game being made was for the card game "War" with the main purpose of the assignment being to test out knowledge of stacks.

Below is a function used in the project.

```java
public Stack<Card> combineStacks(Stack<Card> top, Stack<Card> bottom) {

    Stack<Card> finalstack = new Stack<Card>();
    Stack<Card> midstack = new Stack<Card>();

    finalstack = bottom;
    while(top.empty() == false) {
        Card midcard = top.pop();
        midstack.push(midcard);
    }
    while(midstack.empty() == false) {
        Card topcard = midstack.pop();
        finalstack.push(topcard);
    }

return finalstack;
}
```

The above code is a method used within the program to combine the two stacks of cards in our game. The bottom of the stack stays the same but when combining the top of the stack with the bottom, we have to take into account the nature of stacks to get the right output. Since stack is a FILO datastructure, this means when returning all items from the stack, they will be returned from the most recent element added to the oldest element added. Thus if we only ran the first while loop, all the items would be returned in the opposite order that we need. To prevent this, we use another stack to act as an intermediary stack to flip the elements. The first while loop, passes all the items into another stack however, these items are passed in backwards. Then we empty this new stack, into our final stack so our values will be passed in the correct order. We then return the final stack.

The code above and the project at large goes to show that being able to use a dataype isn't enough. To be an effective programmer, you need to understand why a datatype works the way it does so it can be implemented in the correct way. While this is a small part of a bigger project, these sorts of assignments made me realize the importance of knowing why things works as opposed to how they are used. Knowing the correct syntax isn't enough, understanding how any computer science concept works is a vital component of being an effective programmer.


