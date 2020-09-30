## A Game Template

If we wanted to keep things clean and tidy, we might modify the code a little.

```python
import pygame, sys
from pygame.locals import *

def init():
    pygame.init()
    DISPLAYSURF = pygame.display.set_mode((400, 300))
    pygame.display.set_caption('Hello World!')

def process_input():
  for event in pygame.event.get():  # process input
    if event.type == QUIT:
      pygame.quit()
      sys.exit()

def update_game_state():
    pass

def render_screen():
    pygame.display.update() # render - update the display

while True: # main game loop
    process_input()
    update_game_state()
    render_screen()
   
```