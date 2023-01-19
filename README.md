# Minecraft

Simple Minecraft-inspired demo written in Python and Pyglet.

<http://www.youtube.com/watch?v=kC3lwK631X8>

**Like this project?**

You might also like my other Minecraft clone written in C using modern OpenGL (GL shader language). It performs better, has better terrain generation and saves state to a sqlite database. See here:

<https://github.com/fogleman/Craft>

## Goals and Vision

The code should become well commented and more easily configurable. It should be easy to make some simple changes
and see the results quickly.

I think it would be great to turn the project into more of a library / API... a Python package that you import and then
use / configure to setup a world and run it. Something along these lines...

```python
import mc

world = mc.World(...)
world.set_block(x, y, z, mc.DIRT)
mc.run(world)
```

The API could contain functionality for the following:

- Easily configurable parameters like gravity, jump velocity, walking speed, etc.
- Hooks for terrain generation.

## How to Run

```shell
pip install pyglet
git clone https://github.com/fogleman/Minecraft.git
cd Minecraft
pip install -r requirments.txt
python main.py
```

### If you don't have pip or git

For pip:

- Mac or Linux: install with `sudo easy_install pip` (Mac or Linux) - or (Linux) find a package called something like 'python3-pip' in your package manager.
- Windows: [install Distribute then Pip](http://stackoverflow.com/a/12476379/992887) using the linked .MSI or .EXE installers.

For git:

- Mac: install [Homebrew](http://mxcl.github.com/homebrew/) first, then `brew install git`.
- Windows or Linux: see [Installing Git](http://git-scm.com/book/en/Getting-Started-Installing-Git) from the _Pro Git_ book.

See the [wiki](https://github.com/fogleman/Minecraft/wiki) for this project to install Python, and other tips.

## How to Play

### Moving

- W: forward
- S: back
- A: strafe left
- D: strafe right
- Mouse: look around
- Space: jump
- Tab: toggle flying mode

### Building

- Selecting type of block to create:
  - 1: brick
  - 2: grass
  - 3: sand
- Mouse left-click: remove block
- Mouse right-click: create block

### Quitting

- ESC: release mouse, then close window
