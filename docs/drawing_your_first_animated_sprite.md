# Drawing animated sprites on your window

This is a new example without the shapes from last example, but  still usues the original as a base.

```C#
using AsteriskEngine;
using Raylib_cs;

int WindowWidth = 600;
int WindowHeight = 600;

string cowsprite = "cow.png";
int cowX = 100;
int cowY = 100;

int frameWidth = 32;
int frameHeight = 32;

Game.Window("Test Game", WindowWidth, WindowHeight, () =>
{
    Game.ClearBackground("Black");
    Game.DrawFPS(WindowWidth - 100, 10, "White");
    Game.DrawAnimatedSprite(cowsprite, cowX, cowY, "White", frameWidth, frameHeight, 5, scale: 10f, framesPerCycle: 60);
});
```

The new bits of code are explained below as before.

```C#
string cowsprite = "cow.png";
int cowX = 100;
int cowY = 100;

int frameWidth = 32;
int frameHeight = 32;
```
The cowsprites file path and x/y positions are specified to be used later on.
In Asterisk Engine you have specify the frame width and height to allow the frame to render properly, when specifying frame width and height this goes of the size of each frame in your spritesheet which is what Asterisk Engine uses to make the animation.

```C#
Game.DrawAnimatedSprite(cowsprite, cowX, cowY, "White", frameWidth, frameHeight, 5, scale: 10f, framesPerCycle: 60);
```
This line draws an animated sprite on the window. Here’s what each parameter means:

- `cowsprite`: The file path to your sprite sheet image.
- `cowX`, `cowY`: The position on the window where the sprite will be drawn.
- `"White"`: The color tint to apply to the sprite (use `"White"` for no tint).
- `frameWidth`, `frameHeight`: The width and height of each animation frame in the sprite sheet.
- `5`: The number of frames in the animation cycle.
- `scale: 10f`: The scale factor to resize the sprite (10 times larger in this case).
- `framesPerCycle: 60`: The number of game frames it takes to complete one animation cycle.

This function will automatically cycle through the frames in your sprite sheet, creating a smooth animation at the specified position and scale.
