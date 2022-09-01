---
layout: project
type: project
image: img/Queen-Of-Hearts.png
title: "Card Game"
date: 2022
published: true
labels:
  - Java
  - Programming
summary: "I developed a Java program to run the Game of War."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

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

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
