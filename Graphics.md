# Overview

Godot 4 has two main ways of integrating graphics, with their pros and cons. There's either what I'll call the "RenderDevice" method, which is what is implemented in the Mobile and Forward+ graphics, and then there's what I'll call the "Direct" method, which is implemented for OpenGL3 in the Compatibility graphics.

[This graph](https://raw.githubusercontent.com/godotengine/godot-docs/4.0/contributing/development/core_and_modules/img/rendering_architecture_diagram.webp), courtesy of the Godot Docs, is a very good summary of how the overall graphics system works. In fact, if you want to deep dive into how graphics work in Godot 4, I would suggest looking at [the page it comes from](https://docs.godotengine.org/en/4.2/contributing/development/core_and_modules/internal_rendering_architecture.html#core-rendering-classes-architecture). But, the main point of interest for our purposes are the following classes: `RenderDevice`, `RendererStorage`, `RendererCanvasRender`, and `RendererSceneRender`. All of those except for `RenderDevice` are what the Direct method uses, and then the RenderDevice method uses, well, the `RenderDevice` class. 

# What MUST Be Implmented
Either:

A. A `RenderDevice` derived class

or 

B. `RendererStorage`, `RendererCanvasRender`, and `RendererSceneRender` derived classes. 

# What Is Optional
