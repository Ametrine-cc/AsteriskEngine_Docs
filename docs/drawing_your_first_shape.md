# Drawing your first shape

After making a window you probably want to start making basic shapes on screen. In this part of the documentation, you'll learn how to make rectangles, squares, and circles on your game window.

This is the working example so far:

```C#
using AsteriskEngine;
using Raylib_cs;

int WindowWidth = 600;
int WindowHeight = 600;

int Width = 20;
int Height = 40;

int rect_x = 500;
int rect_y = 400;

int sqr_x = 200;
int sqr_y = 300;
int sqr_size = 50;

int radius = 20;
int circle_x = 300;
int circle_y = 300;

Game.Window("Test Game", WindowWidth, WindowHeight, () =>
{
    Game.ClearBackground("Black");
    Game.DrawFPS(WindowWidth - 100, 10, "White");
    Game.DrawCircle(circle_x, circle_y, radius, "Yellow");
    Game.DrawRectangle(rect_x, rect_y, Width, Height, "Red");
    Game.DrawSquare(sqr_x, sqr_y, sqr_size, "Green");
});
```

The new bits of code are explained below:

```C#
int Width = 20;
int Height = 40;

int rect_x = 500;
int rect_y = 400;

int sqr_x = 200;
int sqr_y = 300;
int sqr_size = 50;

int radius = 20;
int circle_x = 300;
int circle_y = 300;
```

This is just initializing variables for the shapes to be drawn on screen.

```C#
    Game.DrawCircle(circle_x, circle_y, radius, "Yellow");
    Game.DrawRectangle(rect_x, rect_y, Width, Height, "Red");
    Game.DrawSquare(sqr_x, sqr_y, sqr_size, "Green");
});
```

- **`Game.DrawCircle(circle_x, circle_y, radius, "Yellow");`**  
  Draws a circle on the screen. The arguments required are:
    - The circle's X position
    - The circle's Y position
    - The circle's radius
    - The circle's color

- **`Game.DrawRectangle(rect_x, rect_y, Width, Height, "Red");`**  
  Draws a rectangle on the screen. The arguments required are:
    - The rectangle's X position
    - The rectangle's Y position
    - The rectangle's width
    - The rectangle's height
    - The rectangle's color

- **`Game.DrawSquare(sqr_x, sqr_y, sqr_size, "Green");`**  
  Draws a square on the screen. The arguments required are:
    - The square's X position
    - The square's Y position
    - The square's size
    - The square's color

In the next part of the manual you will be shown how to draw static and animated sprites in your window.