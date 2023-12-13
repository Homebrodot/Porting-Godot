# Overview

Porting Godot to a platform is both very simple and very not. Assuming you want the full 9 yards implemented for your game, you need the following implemented:
* "Core processor things" (Semaphores, mutexes, threads, etc.)
* Audio
* Input (Possibly from multiple controllers)
* Graphics:
  * Shaders
* Networking (things such as HTTPClient)
* OS integration (Unless you happen to be running on a more or less bare-metal platform)

Now, *your* list on what needs to be implemented may not need all of that. For example, if you were to hypothetically port Godot 4 to a 6th generation game console (I'd consider this the ***very*** edge of what Godot 4 could be ported to comfortably, if at all. The docs weren't kidding: Use Godot 3 or lower for that instead), you wouldn't need to implement much for the OS, and arguably the networking. However, you would have to implement input for several controllers, up to 4. On the flipside, if you were to port Godot 4 to something like a handheld device, you would usually only have to implement input for one controller. 
