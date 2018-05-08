# HoloLensCameraStream for Unity
This Unity plugin makes the HoloLens video camera frames available to a Unity app in real time. This enables Unity devs to easily use the HoloLens camera for computer vision (or anything they want).

Use this if you need access to the HoloLens camera's frame buffer in Unity, including the [locatable camera attributes](https://developer.microsoft.com/en-us/windows/mixed-reality/locatable_camera).

## With this plugin, you can
* Do computer vision and machine learning on the frames in real time. (algorithms not included)
* Show a preview of what the HoloLens camera sees.
* Obtain a 3D coordinate given an image pixel coordinate from the HoloLens video camera. For instance, you could identify a book using computer vision, then render something on top of that book.

## Getting Started
The tutorials below will show you how to run the **Unity sample app**.

### Things you need
* [The HoloLens development tools](https://developer.microsoft.com/en-us/windows/mixed-reality/install_the_tools), sans Vuforia and the Emulator.

### Running the example Unity project
The example Unity project can be found in the root `HoloLensVideoCaptureExample/` directory. This Unity project is a great way to learn how to use the CameraStream plugin in Unity, or to use as a template for your own Unity project. Read on to learn how to build and run the example project on your HoloLens. You should be familiar with creating and configuring a new Unity-HoloLens project [according to Microsoft's instructions](https://developer.microsoft.com/en-us/windows/mixed-reality/holograms_100). As Microsoft and Unity update their HoloLens documentation, I'm sure this tutorial will become out of date.
1. **Open the example project:** Navigate to and open the example project directory (`HoloLensVideoCaptureExample/`) in Unity.
2. **Configure build settings:** Once the project opens, select **File > Build Settings**. In the Platform list, select `Windows Store`. Set the SDK to `Universal 10`; set Target device to `HoloLens`; set UWP Build Type to `D3D`; check the Unity C# Projects checkbox; and finally, click **Switch Platform**.
3. **Build the project:** You can now build the Unity project, which generates a Visual Studio Solution (which you will then have to also build). With the Build Settings window still open, click **Build**. In the explorer window that appears, make a new folder called `App`, which should live as a sibling next to the `Assets` folder. Then click Select Folder to generate the VS solution in that folder. Then wait for Unity to build the solution.
4. **Open the VS Solution:** When the solution is built, a Windows explorer folder will open. Open the newly-built VS solution, which lives in `App/HoloLensVideoCaptureExample.sln`. This is the solution that ultimately gets deployed to your HoloLens.
5. **Configure the deploy settings:** In the Visual Studio toolbar, change the solution platform from `ARM` to `x86`; Change the deploy target (the green play button) to `Device` (if your HoloLens is plugged into your computer), or `Remote Machine` (if your HoloLens is connected via WiFi).
6. **Run the app:** Go to **Debug > Start Debugging**. Once the app is deployed to the HoloLens, you should see some confirmation output in the Output window.

If you have questions, [check out the FAQ](https://github.com/VulcanTechnologies/HoloLensCameraStream/wiki/FAQ).

## Contributing
We would love for you to contribute to this project. Take a look at the TODO list in the Plugin's solution, or look at the Issues tab on GitHub to see how you can contribute. Thanks, enjoy!
