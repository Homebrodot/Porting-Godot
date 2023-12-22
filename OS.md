# Overview

The OS singleton is essentially Godot's translator into your platform's low level features. It's used for everything from setting up a main loop, to getting the tick offset, to displaying errors, etc. 

# What MUST Be Implemented
* `print()`: Used by a lot of internal Engine things, including debug printing to terminal
* `initialize()`
* `finalize()`
* `finalize_core()`
* `get_ticks_usec()`
* `benchmark_begin_measure()`
* `set_use_benchmark(bool benchmark)`
* `set_benchmark_file(String file)`
* `get_cmdline_platform_args()`
* `set_cwd(String p)`
* `run()`: Starts your platform's main loop.
* `get_main_loop()`
* `add_frame_delay()`
* `set_exit_code()`
* `setup_remote_filesystem()
