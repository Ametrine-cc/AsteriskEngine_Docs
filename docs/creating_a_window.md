# Creating a window

Making a window in Asterisk Engine is a little different from making one in other game frameworks
such as Pygame or Raylib.

To make a window follow this written example:

``` C#
using AsteriskEngine;
using Raylib_cs;

int WindowWidth = 600;
int WindowHeight = 600;

Game.Window("Test Game", WindowWidth, WindowHeight, () =>
{
    Game.ClearBackground("Black");
    Game.DrawFPS(WindowWidth - 100, 10, "White");
});
```

The following script shows you how to make a window in Asterisk Engine. Lets go through it line by line.

```C#
using AsteriskEngine;
using Raylib_cs;
```

These are importing Asterisk Engine and Raylib, Raylib is imported for any other things you want to use the original engine for if not incorperated into Asterisk Engine or your prefer the native method.


``` C#
int WindowWidth = 600;
int WindowHeight = 600;
```

These are global values declaring the width and height the window should be set at.

``` C#
Game.Window("Test Game", WindowWidth, WindowHeight, () => {
  // More in the next bit
});
```

This tells the engine the window should be made.

1. Fist declaring the title. "Test Game".
2. Then declaring the width and height of the window. "WindowWidth, WindowHeight".
3. Finally () which replaces "Action Draw" which allows you to define things to be drawn to the screen as soon as the window is created.

``` C#
  Game.ClearBackground("Black");
  Game.DrawFPS(WindowWidth - 100, 10, "White");
});
```

Next this part of the script does the following.

1. "ClearBackground" - Sets the background to whatever color specified (e.g: "Black" in this context).
2. "DrawFPS" - Draws the FPS that your window is running at to the window. In this context it draws it to the top right corner of the window this is done like this "WindowWidth - 100". Finally DrawFPS "10", relates to the font color and "White" is the color of the text.

In the next part of the manual you will be shown how to draw shapes to your window.