# Every Steps For the Unity 2.0 Course learning on Udemy.

Launch Unity client on Windows.

Login into Unity using your Unity email and password. Choose Personal Edition. Fill Survey questions

Create new Github repository Unity2-Course that will contain all the courses projects

![Course2 Clone Visual Studio](Team-Explorer-Clone-Course2-Repository.png)

Go to the cloned directory in Posh-Git and create a directory for the first steps projects :
```
cd C:\Users\gamedev\Github\Unity2
mkdir 1_first_steps
```

Make a new Unity Project in Unity Client :

![New Unity Project](new-unity-project.png)

Point the new project directory to the created directory above (Unity2\1_first_steps) and name it My Block Model :

![My Block Model Project](my-block-model-new-project.png)

Once the project opened, go to Windows->Layout->Default to restore the Windows layout to the default view.

## Basic Geometry and transforms

Then Game Object->3D Object->Cube

Then File->Save Scene. Name it "car" it will be saved in the assets folder of the existing project directory (Unity2\1_first_steps\My Block Model\assets if you've followed all the steps above).

You should have an object car appear in the Assets panel at the bottom. You can click on the "car" name and use that to rename to "Street Scene" for example. Now if you save everything again (File->Save Project), the name of the file in the directory above will have changed automatically to "Street Scene.unity".

You can now play in the main 3d View, drag on the arrows to move the cube (after selecting it first). Use middle button to pan the camera, hold right button to change to regular First Person Shooter control (mouse look + WASD to strafe left right/forward/back).

You can invoke the Unity Manual from Help->Unity Manual then use the browser to navigate to the Keyboard shortcuts to find more keyboard shortcuts.

Most important keys are "Q/W/E/R/T" that control the top left most buttons (hand, cross, swap, blow up, square)

Hand moves the view, cross moves the selected object (using either the arrows to move along one axis or the colored "planes" to move along two dimensions).

E or "swap" will rotate (grab one of the circle that will rotate either in object space or camera space).

R or "blow up" will scale the object. Either along one axis or in all three dimensions.

Now delete your cube and make a very basic looking car using cubes/scale/move and cylinders.

![Crappy car](crappy-car.png)

You can name one wheel "wheel (0)". And then when you duplicate that object Unity will automatically name the copy "wheel (1)" and so on.

## Prefabs

Now create an empty GameObject (GameObject->Create Empty). Rename it Car. Select all geometry for the car we created above (using shift, or control or dragging rectangle selection). Then by holding the mouse button, drag the geometry from Hierarchy view onto the new "Car" empty object line.

Now you can just click on the "Car" line to select the whole car and move and transform the car as a whole.

Now grab the "Car" line and drag it into the Assets panel at the bottom. This will create a "prefab" called car. Now the car object in the hierarchy view has turned blue that means it's not a simple object anymore but it's a link to the prefab asset.

You can then again drag the Car icon in the asset panel into the Scene panel and that will create a car from your prefab in the scene.

Challenge : Create a street scene with at least two different types of prefabs that are duplicated.

![Cars and Hydrants](cars-and-hydrants.png)

## First CSharp script

Make sure our street scene is opened. Then in the Assets panel, right click and selecte "Create->C# Script" from the context menu. Call it "Introducer" immediately as you create it (because the client will fill the script with some default text that needs to match the name you've given it). Usually we want to name scripts with names that indicate somebody doing an action (a "doer"/"introducer"). Just as a meaningful convention.

Once it is created, drag and drop the script icon onto a car in the scene. If you've made an error and dragged it twice onto the same car, you can reselect the car, and then choose one of the Introducer script in the Inspector Panel on the right and choose the "remove component" (on the cog icon of the panel).

If you click once on the script icon in the asset panel it shows the preview of the script in the Inspector panel. If you want to open it to edit it, double click on the script icon so that it opens Visual Studio 2017 (or whatever editor is in the Preferences->External Tools selection). So go ahead and open it.

Once in Visual Studio, modify the Introducer::Start() function. By adding a line saying print Hello VR Jammer :
```
	// Use this for initialization
	void Start () {
        print("Hello VR Jammer");
	}
```

Then save the file (ctrl+s). Go back to the Unity Client Window. Check in the script preview that the line with print has been added. Then click on the Play button on top. This will launch the "game mode", as if we were playing the game.

While the game is playing, check the console panel on the bottom (there's a "console" tab next the project tab). It should display one time or more "Hello VR Jammer". 

If we see more than one "Hello VR Jammer" (and we can clear the console window before starting the game to make sure those are not old messages), that means we have multiple instances of the Introducer script. In order to find where those instances are, we right-click on the script, select "Find references in scene", this will put a filter on the Hierarchy panel that tells to list only the game objects that have a reference to the script. Select the game objects that shouldn't have the instance of the script (in case you misclicked earlier) and use the cog "remove component" to remove the unneeded component/script.

Go back to the console, clear it. Hit the play button again on top, and repeat the above operations until you only see one "Hello VR Jammer" line in your console panel.

