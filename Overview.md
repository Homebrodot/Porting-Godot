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

If your platform does not support the standard C library, or if the use of a platform's threading API is required to meet guidelines for the platform, you need to implement a custom thread class.

Godot allows for a platform specific `main` function to be defined in the code of the platform. This is where you will want to initialize any platform-specific libraries, set any special modes, and other "setup" things for your platform, as if you were making a standard native app for that platform (which, you kind of are).

# What Godot Wants

# What MUST Be Implemented
* [A `detect.py` file for properly compiling the platform](https://docs.godotengine.org/en/stable/contributing/development/core_and_modules/custom_platform_ports.html#required-features-of-a-platform-port)
* Platform guideline adherent thread handling. This is a must, because Godot runs its various servers on multiple threads.
* OS singleton, to some extent (See OS.md)

# What Is Optional

* Audio
* Graphics
* Input
* Networking

