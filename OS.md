# Overview

The OS singleton is essentially Godot's translator into your platform's low level features. It's used for everything from setting up a main loop, to getting the tick offset, to displaying errors, etc. Compared to some other features to implement, implementing an OS singleton class is very rigid, with a lot of specific functions expected by the engine. Luckily, a decent chunk of those functions are only relevant within the engine's code, as in they do not need to be redefined in an OS derived class for a platform. 

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
* `delay_usec()`
* `get_ticks_usec()`
* `benchmark_begin_measure()`
* `benchmark_end_measure()`
* `benchmark_dump()`
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
* `set_main_loop()`
* `delete_main_loop()`
* `add_frame_delay()`
* `set_exit_code()`
* `setup_remote_filesystem()`
* `set_display_driver_id()`
* `set_low_processor_usage_mode()`
* `set_low_processor_usage_mode_sleep_usec()`
* `set_delta_smoothing()`
* `get_executable_path()`
* `set_exit_code()`
* `get_render_thread_mode()`
* `initialize_joypads()`
* `get_bundle_icon_path()`
* `is_in_low_processor_mode()`
* `is_start_on_exit_set()`
* `get_restart_on_exit_arguments()`
* `create_instance(List<String> args)`
* `set_restart_on_exit()`

Public variables
* `OS::RenderThreadMode _render_thread_mode`
* `bool _verbose_stdout`
* `List<String> _cmdline`
* `List <String> _user_args`
* `String _execpath`
* `String _local_clipboard`
