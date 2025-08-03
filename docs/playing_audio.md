# Playing and Stopping audio

This will show you how you can load, start and stop audio in Asterisk Engine.

```C#
using System.Threading;
using AsteriskEngine;
using Raylib_cs;

int WindowWidth = 600;
int WindowHeight = 600;

string soundfile = "Double_Shuffle.mp3";

Game.Window("Test Game", WindowWidth, WindowHeight, () =>
{
    Game.ClearBackground("Black");
    Game.DrawFPS(WindowWidth - 100, 10, "White");

    Game.LoadAudio(soundfile);
    Game.PlayAudio();
    Thread.Sleep(10000); // Play for 10 seconds
    Game.StopAudio();
    Game.UnloadAudio();
    Game.Close();
});
```

This example demonstrates how to load, play, and stop audio using the Asterisk Engine in a simple C# application.
The code initializes a game window, loads an audio file ("Double_Shuffle.mp3"), and plays it for 10 seconds.
After playback, the audio is stopped and unloaded, and the game window is closed.
    Key steps include:
- Setting up the window dimensions and title.

- Loading the audio file with `Game.LoadAudio`.
    
- Playing the audio with `Game.PlayAudio`.
    
- Pausing the execution for 10 seconds to allow the audio to play.
    
- Stopping and unloading the audio with `Game.StopAudio` and `Game.UnloadAudio`.
    
- Closing the game window with `Game.Close`.

This example is useful for understanding basic audio management in the Asterisk Engine.