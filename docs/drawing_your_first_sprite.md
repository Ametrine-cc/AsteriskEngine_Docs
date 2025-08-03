# Drawing static sprites on your window

This is a new example without the shapes from last example, but  still usues the original as a base.

```C#
using AsteriskEngine;
using Raylib_cs;

int WindowWidth = 600;
int WindowHeight = 600;

string cowsprite = "cow.png";
int cowX = 100;
int cowY = 100;

Game.Window("Test Game", WindowWidth, WindowHeight, () =>
{
    Game.ClearBackground("Black");
    Game.DrawFPS(WindowWidth - 100, 10, "White");
    Game.DrawSprite(cowsprite, cowX, cowY, "White");
});
```

The new bits of code are explained below as before.

```C#
Game.DrawSprite(cowsprite, cowX, cowY, "White");
```
This line draws a static sprite (not animated) on the window. Here’s what each parameter means:

- `cowsprite`: The file path to your sprite image.
- `cowX`, `cowY`: The position on the window where the sprite will be drawn.
- `"White"`: The color tint to apply to the sprite (use `"White"` for no tint).

This function simply draws the image at the specified position with the given color tint, without any animation or scaling.