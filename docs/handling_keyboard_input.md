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

    Game.OnKeyDown(key =>
    {
        if (key == KeyboardKey.Escape) Game.Close();
        else if (key == KeyboardKey.F11) Game.ToggleFullscreen();
        else if (key == KeyboardKey.Up) y -= 25;
        else if (key == KeyboardKey.Down) y += 25;
        else if (key == KeyboardKey.Left) x -= 25;
        else if (key == KeyboardKey.Right) x += 25;
    });
});
```

The new bits of code are explained below:

```C#
Game.OnKeyDown(key =>
{
    if (key == KeyboardKey.Escape) Game.Close();
    else if (key == KeyboardKey.F11) Game.ToggleFullscreen();
    else if (key == KeyboardKey.Up) y -= 25;
    else if (key == KeyboardKey.Down) y += 25;
    else if (key == KeyboardKey.Left) x -= 25;
    else if (key == KeyboardKey.Right) x += 25;
});
```
This listens for keyboard input and updates the position of the text accordingly. When an arrow key is pressed, the `x` or `y` variable is incremented or decremented, moving the text in the corresponding direction. Pressing `Escape` will close the window, and pressing `F11` will toggle fullscreen mode.

- `KeyboardKey.Up`, `KeyboardKey.Down`, `KeyboardKey.Left`, and `KeyboardKey.Right` correspond to the arrow keys.
- The `Game.OnKeyDown` method registers a callback that runs every time a key is pressed.
- The `x` and `y` variables control the position of the text drawn by `Game.DrawText`.

This approach allows you to handle keyboard input and move objects or trigger actions in your game loop.

In the next part of the manual you will be shown how to draw static and animated sprites in your window.