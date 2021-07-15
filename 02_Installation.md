## Introduction
To use Wase Engine you will first need to install it. You can choose to use a pre-compiled build or you can build Wase Engine yourself from the source code. On the [builds](https://wase-engine.com/builds.html) page you can see which builds are available.

If you choose to use a pre-compiled build you can just include the Wase Engine include and lib folder in your project. If you choose to build Wase Engine from the source code you can head over to [building wase engine](https://wase-engine.com/documentation/building-wase.html) for a more in depth explanation.

Wase Engine uses the following tools that you will have to install before you can use Wase Engine:

- C++17 or higher
- SDL2
- SDL2 Image
- SDL2 Mixer
- SDL2 TTF

## Include Wase Engine to your Visual Studio project
When you have the pre-compiled build or when you've build Wase Engine yourself you can start using it for your Visual Studio projects.

- In the *Solution Explorer* right click on your project, select *Properties*.
- In *Properties > C/C++ > General >> Additional Include Directories*, enter the path to the Wase Engine include directory, for example
	* C:\Program Files\wase-engine\include
- In *Properties > Linker > General > Additional Library Directories*, enter the path to the Wase Engine lib directory where the .lib file(s) are located, for example
	* C:\Program Files\wase-engine\lib\x86
- In *Properties > Linker > Input > Additional Dependencies*, enter the .lib file name with extension.

Go through the same steps for SDL2, SDL2 Image, SDL2 Mixer and SDL TTF. Make sure that you add the /include and /lib/x86 folder locations to your *system Path* or copy the .lib files to your project root.
