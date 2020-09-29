---
title: Pygame - Basics
permalink: /docs/pyg-1-basics/
---

## Coordinates

Pygame uses a Cartesian coordinate system with the origin at the top left of the screen. Pygame coordinates are in the for x, y and always refer to an x offset from the left of the window and a y offset from the top of the window.

<centre>        
    <img src="{{ "/assets/img/pyg2/coords.png" | relative_url }}" alt="Cartesian coordinates system, origin top left" class="img-responsive">
</centre>

## Colours (or Colors) in Pygame

Colours in Pygame are defines in RGB format with a value of 0-255 representing the amount of red, green and blue in the colour. A fourth value in the same range can be used to change the transparency of the colour. This is known as the alpha value. The alpha value is a measure of opaqueness - a value of 0 is completely transparent, a value of 255 is completely opaque (solid).  

|Colour|RGB Values|
|---|---|
|Aqua|(  0, 255, 255)|
|Black|(  0,   0,   0)|
|Blue|(  0,  0, 255)|
|Fuchsia|(255,   0, 255)|
|Gray|(128, 128, 128)|
|Green|(  0, 128,   0)|
Lime|(  0, 255,   0)|
|Maroon|(128,  0,   0)|
|Navy Blue|(  0,  0, 128)|
|Olive|(128, 128,   0)|
|Purple|(128,  0, 128)|
|Red|(255,   0,   0)|
|Silver|(192, 192, 192)|
|Teal|(  0, 128, 128)|
|White|(255, 255, 255)|
|Yellow|(255, 255,   0)|

## Surface Objects

Surface objects are objects that represent a rectangular 2D image. The pixels of the Surface object can be changed by calling the Pygame drawing functions and then displayed on the screen. The window border, title bar, and buttons are not part of the display Surface object.

In particular, the Surface object returned by pygame.display.set_mode() is called the display Surface. Anything that is drawn on the display Surface object will be displayed on the window when the pygame.display.update() function is called. It is a lot faster to draw on a Surface object (which only exists in the computer’s memory) than it is to draw a Surface object to the computer screen. Computer memory is much faster to change than pixels on a monitor.

## Rect Objects

Pygame has two ways to represent rectangular areas (just like there are two ways to represent colors). The first is a tuple of four integers:  
1. The X coordinate of the top left corner.
2. The Y coordinate of the top left corner.
3. The width (in pixels) of the rectangle.
4. Then height (in pixels) of the rectangle.
The second way is as a pygame.Rect object, which we will call Rect objects for short. For example, the code below creates a Rect object with a top left corner at (10, 20) that is 200 pixels wide and 300 pixels tall:  
```python
import pygame
myRect = pygame.Rect(10, 20, 200, 300)
```
The handy thing about this is that the Rect object automatically calculates the coordinates for other features of the rectangle. For example, if you need to know the X coordinate of the right edge of the pygame.Rect object we stored in the myRect variable, you can just access the Rect object’s right attribute:  
```python
print(myRect.right)
```

|Attribute Name|Description|
|---|---|
|myRect.left|The int value of the X-coordinate of the left side of the rectangle.|
|myRect.right|The int value of the X-coordinate of the right side of the rectangle.|
|myRect.top|The int value of the Y-coordinate of the top side of the rectangle.|
|myRect.bottom|The int value of the Y-coordinate of the bottom side.|
|myRect.centerx|The int value of the X-coordinate of the center of the rectangle.|
|myRect.centery|The int value of the Y-coordinate of the center of the rectangle.|
|myRect.width|The int value of the width of the rectangle.|
|myRect.height|The int value of the height of the rectangle.|
|myRect.size|A tuple of two ints: (width, height)|
|myRect.topleft|A tuple of two ints: (left, top)|
|myRect.topright|A tuple of two ints: (right, top)|
|myRect.bottomleft|A tuple of two ints: (left, bottom)|
|myRect.bottomright|A tuple of two ints: (right, bottom)|
|myRect.midleft|A tuple of two ints: (left, centery)|
|myRect.midright|A tuple of two ints: (right, centery)|
|myRect.midtop|A tuple of two ints: (centerx, top)|
|myRect.midbottom|A tuple of two ints: (centerx, bottom)|
