---
title: Game & Core Loops
permalink: /docs/loop-1/
---

There are two different "loops" that are critical in video games. The first is central to the code that runs the game, known as the game loop. The second is central to the game play experience, known as the core loop.  

### Game Loop

The game loop is the centre of the code in any video game. It can be expressed very simply in the pseudo-code below.  

```java
while (gameIsRunning)
{
  processInput();
  updateGame();
  renderGraphics();
}
```

This is a simple cycle that repeats, constantly checking for input (from mouse/keyboard/controller), then updating the game world based on that input, any game physics, AI or timed events. Finally once the game world has been updated the graphics are rendered to the screen. The game loop is so ubiquotous it is used in (almost) every game and is considered the most important games design pattern. You will learn more about design patterns in your second year.  

The most important role the game loop plays is in ensuring the game runs at a constant rate without stuttering or lagging. There are a number of approaches to this, depending on the target platform and style of game. (These will be covered in the Design Patterns module next year).  

### Core Loops

The `core loop` is the primary game system or mechanic which defines your game. This is the element of the game that players remember most frequently or engage with most often. You can think about this as the “engine” for your game and what empowers individual players to keep playing.  

The core loop comprises the most basic kinds of actions that players can take. Whether that is moving around the map in *League of Legends*; drafting cards in *Splendor*; or platforming across the screen in *Super Mario Bros*. The genre of your game doesn’t matter. What does matter is making sure that your players continue to engage over time through a well structured core loop.  

#### Videos on Core Loops

* [Extra Credits](https://www.youtube.com/watch?v=mGL5YGcAxEI&list=PLQM0OWYycizC0tX2iW7VL4dNLAEJjXi6T)
* [How Gameplay (Core) Loops Keep You Playing](https://www.youtube.com/watch?v=Sk-nbAtIUko)
* [Game Design With Michael](https://www.youtube.com/watch?v=PMj8Q4ViKzs)
* [Make School](https://www.youtube.com/watch?v=9SLxpCVnrFI)

#### Overview from Dave Eng on medium.com  

[https://medium.com/@davengdesign/core-loops-c98b1197e93d](https://medium.com/@davengdesign/core-loops-c98b1197e93d)  

