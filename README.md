# Start-up crash fix for Far Cry 3.

This mod fixes a crash on startup on systems with a large number of cores.

During launch, the game calls a function which enumerates the processors (cores) in the system and sets the thread affinity. (Ie. Which cores the game will run on)

On systems with large numbers of cores (Probably more than 16 or 32) this function has a bug which causes the game to hang on the splash screen.

This mod patches out an infinite loop that causes the game to hang on the splash screen.

To install, overwrite FC3_d3d11.dll and systemdetection.dll in your Far Cry 3 folder with the files in the zip file.