# Overview

The OS singleton is essentially Godot's translator into your platform's low level features. It's used for everything from setting up a main loop, to getting the tick offset, to displaying errors, etc. Compared to some other features to implement, implementing an OS singleton class is very rigid, with a lot of specific functions expected by the engine.

# What MUST Be Implemented
Public functions: 
* `print()`: Used by Godot to print information to terminal
* `printerr()`: Used by Godot to print errors to terminal
* `alert()`: An OS/system native way to create a warning popup
* `add_logger()`
* `set_cmdline()`
* `ensure_user_data_dir()`
* `initialize()`
* `finalize()`
* `finalize_core()`
* `get_ticks_usec()`
* `benchmark_begin_measure()`
* `set_use_benchmark(bool benchmark)`
* `set_benchmark_file(String file)`
* `set_current_rendering_driver_name(String name)`
* `set_current_rendering_method(String method)`
* `get_cmdline_platform_args()`
* `set_cwd(String p)`
* `set_environment()`
* `unset_environment()`
* `run()`: Starts your platform's main loop.
* `get_main_loop()`
* `add_frame_delay()`
* `set_exit_code()`
* `setup_remote_filesystem()`
* `set_display_driver_id()`
* `set_low_processor_usage_mode()`
* `set_low_processor_usage_mode_sleep_usec()`

Public variables
* `OS::RenderThreadMode _render_thread_mode`
* `bool _verbose_stdout`
* 
