# Drawing your first shape

After making a window you probably want to start making basic shapes on screen. In this part of the documentation, you'll learn how to make rectangles, squares, and circles on your game window.

This is the working example so far:

```C#
using AsteriskEngine;
using Raylib_cs;

int WindowWidth = 600;
int WindowHeight = 600;

int x = 300;
int y = 300;

Game.Window("Test Game", WindowWidth, WindowHeight, () =>
{
    Game.ClearBackground("Black");
    Game.DrawFPS(WindowWidth - 100, 10, "White");
    Game.DrawText("Hello, Asterisk Engine!", x, y, "White");

    // Mouse input
    Game.OnMouseDown(mouseButton =>
    {
        if (mouseButton == MouseButton.Left)
        {
            // Move the text to the current mouse position
            x = Game.MouseX();
            y = Game.MouseY();
        }
    });
});
```

The new bits of code are explained below:

```C#
Game.OnMouseDown(mouseButton =>
{
    if (mouseButton == MouseButton.Left)
    {
        // Move the text to the current mouse position
        x = Game.MouseX();
        y = Game.MouseY();
    }
});
```
This listens for mouse input and updates the position of the text when the left mouse button is pressed. The `x` and `y` variables are set to the current mouse coordinates, so the text will jump to wherever you click in the window.

- `MouseButton.Left` corresponds to the left mouse button.
- The `Game.OnMouseDown` method registers a callback that runs every time a mouse button is pressed.
- `Game.MouseX()` and `Game.MouseY()` return the current mouse position.

This approach allows you to handle mouse input and interactively move objects in your game window.

In the next part of the manual you will be shown how to draw static and animated sprites in your window.