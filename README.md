# Porting-Godot
Documentation on how SPECIFICALLY to port Godot to a platform.

The Godot official docs are extremely vague on how to create a fully fleshed out port of Godot, so I have created this to aid a dev looking to port Godot (4) to a given platform.

Currently this is only centered around Godot 4. Godot 3 and prior are going to be distinctly different in their porting insofar as graphics are concerned, and I have not personally ported Godot 3 and prior to any platform, only Godot 4. 

Each readme in this repo will contain 3 sections: 
* "What Godot Wants", detailing what Godot expects, on a general level, from your platform
* "What MUST be implemented", detailing the bare bones functions (based on an already implemented class) Godot will need to use this feature.
* "What Is Optional", which is some features you may see in the stock implemented platforms, but are not actually absolute musts per say.


# Overview

Godot gives a lot of freedom about how to port a platform to it. Generally speaking though, there are some core things that are critical to Godot functioning on that platform:
* Threading: If your platform does not support the standard C library, or if some threading features in Godot (eg. priority) are not present without using a platform's API, you need to implement a custom thread class.
* A "main" function in a file of your choice: Basically what you'd expect a `main` function to do; set the bones up so the skeleton can dance. More on that later.
