# Drawing text to your window

This part of the documentation shows you how to draw text to your window.

```C#
using AsteriskEngine;
using Raylib_cs;

int WindowWidth = 600;
int WindowHeight = 600;

Game.Window("Test Game", WindowWidth, WindowHeight, () =>
{
    Game.ClearBackground("Black");
    Game.DrawFPS(WindowWidth - 100, 10, "White");
    Game.DrawText("Hello, Asterisk Engine!", 10, 10, "White");
});
```

Let's break down the new code:

```C#
Game.DrawText("Hello, Asterisk Engine!", 10, 10, "White");
```
This line draws text on the window. Here’s what each parameter means:

- `"Hello, Asterisk Engine!"`: The string of text to display.
- `10`, `10`: The X and Y coordinates where the text will appear on the window.
- `"White"`: The color of the text.

This function renders the specified text at the given position with the chosen color.
