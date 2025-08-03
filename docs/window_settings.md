
# Window Settings

This is showing the different window settings for your game when using Asterisk Engine.

```C#
using AsteriskEngine;
using Raylib_cs;

int WindowWidth = 600;
int WindowHeight = 600;

Game.Window("Test Game", WindowWidth, WindowHeight, () =>
{
    Game.ClearBackground("Black");
    Game.Set_FPS(60);
    
    Game.DrawFPS(WindowWidth - 100, 10, "White");

    Game.ToggleFullscreen();
    Game.Enable_ExitKey(false);

    Game.Close();
});
```

This example demonstrates how to configure window settings in a game using Asterisk Engine with Raylib_cs.

- Sets the window title to "Test Game" and dimensions to 600x600 pixels.

- Clears the background to black each frame.

- Sets the target frames per second (FPS) to 60.

- Draws the current FPS in white at the top-right corner of the window.

- Toggles fullscreen mode.

- Disables the default exit key to prevent accidental closure.

- Closes the game window when the main loop ends.