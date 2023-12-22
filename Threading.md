# Overview

If your platform has propretary/in house handling for thread functions, you must define your own implementations of the various threading classes to make it work. 

For the Thread class, there's several points of interest. Looking at the source code (insert link here), we can see there's a struct called `PlatformFunctions`. We don't ever see this used in any of the stock platform implementations, but we can infer based on how it is implemented in `Thread::callback` that this is a specially defined structure for us to implement a thread adaptation layer. Of this, it allows us to define functions for setting thread priority, initializing a thread, wrapping a thread, and terminatiing a thread. 

# What Godot Wants

# What MUST Be Implemented

* The public functions:
  * `make_main_thread()`
  * `release_main_thread()`

# What Is Optional
