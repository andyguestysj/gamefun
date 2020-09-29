---
title: Pygame - Introduction
permalink: /docs/pyg-intro/
---

This module is focused on the game development process and its useful to illustrate this by, well, going through the process, and that means making a game or two along the way. So we're going to have a look at using Pygame to make games. Pygame is a games library for the Python programming language.  

This module isn't a **programming** module as such. You won't be assessed on your coding or even your code dessign. I'm not expecting you to learn a whole new language (Python) when you are still being taught the first one (Java). I'll provide you with games as a starting point, provide you with code to work from and to use. You might need to extend it a little but I'm happy to explain how to do that.   

I want to show you how things work in games and Python with Pygame gives me a way to do this. Ideally I'd like to use a Game Engine but getting that installed, setup and supported on computers you can use is very difficult under the current situation. So we'll use Pygame and see what we can do!  

## Pygame On repl.it

Repl.it, the browser based code compiler, supports Pygame. If you haven't already [signed up for a repl.it account](repl.it) please do so now.  

Once you've registered you can log in. Then go to [https://repl.it/@andyguest/pygHelloWorld](https://repl.it/@andyguest/pygHelloWorld) and click on the `Fork` button at the top of the screen. Then click on the three lines icon at the top left of the screen and select `My repls` from the pop out menu. From their click on `pygHelloWorld` to open your copy of my Pygame HelloWorld programme. Run it by clicking on the green triangle button at the top of the screen. (I recommend going in to the settings by using the cog icon on the left of the screen and change the Layout to Stacked).  

Impressive huh? Okay, it's kinda pathetic, it opens up a window. It sets the title to "Hello World!". That's about it. Click the stop button at the top of the screen (with the square on it) to end the 'game'.    Or you can click on the X at the top right of the game window.  

Lets have a look at the code.

## Hello World Code

As basic as this code is, it uses many of the core concepts needed by all Pygames. Lets work our way through the code and see what's there.

### Library Importing

If we want to use a games library the first thing we need to do is import it.  

```python
import pygame, sys
from pygame.locals import *
```
The first line `import pygame` imports the core of the Pygame library. Don't worry about `sys` for now, that is a library that provided system specific information. The `import pygame` line doesn't import all of Pygame, it would be unusual to use all of Pygame so we will only import what we need. The second line `from pygame.locals import *` imports a specific part of the Pygame library. `pygame.locals` gives us easy access to constants we'll be using.  

### Initialise Pygame
```python
pygame.init()
```
The first thing we need to do is to initialise Pygame. `pygame.init()` does an the standard initialisation required for all Pygame games. It should basically be the first line of code after the imports of every Pygame.  

### Window Setup

```python
DISPLAYSURF = pygame.display.set_mode((400, 300))
pygame.display.set_caption('Hello World!')
```
These two lines set up the game window.  
`DISPLAYSURF = pygame.display.set_mode((400, 300))` creates a game window of 400x300 pixels.  
`pygame.display.set_caption('Hello World!')` sets the caption in the window title bar to "Hello World!".  

### The Game Loop
```python
while True: # main game loop
```
This single line encapsulates one of the biggest concepts in games programming, the game loop.  
<div class="row">
    <div class="col-md-6">        
        <img src="{{ "/assets/img/pyg2/gameloop.png" | relative_url }}" alt="Game loop cycle - input, update, render" class="img-responsive">
    </div>
</div>




