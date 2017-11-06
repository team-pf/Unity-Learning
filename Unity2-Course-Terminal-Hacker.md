
## Select words

* Easy difficulty
** Books, aisle, shelf, password, font, borrow

* Medium difficulty
** prisoner, handcuffs, holster, uniform, arrest

* Hard difficulty
** starfield, telescope, environment, exploration, astronauts

## Setup

Download package (WM2000 Package.unitypackage). Decompress it in a local folder.

Create new project in Unity2\2_Terminal_Hacker\ call the project "Terminal Hacker". Use "2d" project style.

Now you can import the unitypackage file above in two ways. First way is to go to assets->import package->custom package and then select the file using the file browser. Second is to have the file in a Windows Explorer Window, then drag and drop the icon of the unitypackage file onto the Project panel at the bottom of the Unity Editor.

Now in the project panel, select the WM2000 folder. There's a prefab called WM2000 that you can drag and drop in the Scene panel.

If you start the game using the play button on top, it will display the terminal on the main screen, with a background noise and a blinking cursor. If you type then the terminal will display green text that you just typed with a keyboard clicking sound.

## Using the terminal.writeln

In the Assets folder below create a script called "Hacker". Drag and drop it on the collapsed WM2000 Game object in the Hierarchy panel.
Do it only once (you can verify using the print method we used earlier in section 1).

Then use the Terminal.WriteLine() method (that method is specific to this project and is not a Unity method, it has been provided to us in the downloaded unity package). Use the method to write "Hello Terminal" on the terminal screen inside the game window.
The game will play exactly the same, except that now there is a "Hello Terminal" on top of the screen. You can still use the keyboard to write random text after that.

Now use the same Terminal.WriteLn() to write a blurb of text that looks like a game menu.

![War Game menu](joshua-game-menu.png)



