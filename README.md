# Porting-Godot
Documentation on how SPECIFICALLY to port Godot to a platform.

The Godot official docs are extremely vague on how to create a fully fleshed out port of Godot, so we have created this to aid devs looking to port Godot (4) to a given platform.

Currently this is only centered around Godot 4. Godot 3 and prior are going to be distinctly different in their porting insofar as graphics are concerned. 

Each readme in this repo will contain 4 sections: 
* "Overview", which is, as the title suggests, an overview of the feature's implementation in Godot. 
* "What MUST be implemented", detailing the bare bones functions and/or functionality (based on an already implemented class) Godot will need to use this feature.
* "What Is Optional", which is some features you *may* see in the stock implemented platforms, but are not actually absolute musts per say.

This guide will assume that the porter is not looking to heavily modify the core aspects of the game engine in order to port to their target platform. Technically speaking, if someone so chooses, they *could* modify any core aspect of the game engine to get Godot running pretty much anywhere, with enough effort. However, that would be an extremely large undertaking, and would heavily convolute this guide, so it will not be covered. So, assume a "vanilla" port is the goal.


