# Blender Animation Tests

Test repository for blender animations.

[blender-wow-studio fork](https://gitlab.com/ihm-tswow/blender-wow-studio)

[pywowlib fork](https://github.com/ihm-tswow/pywowlib)

## Installation
I don't publish binaries while this is in develoment, so you need to build it from source. This is how I do it on windows.

### Requirements
- Visual Studio 2019 (probably need basic C++ development kit and maybe some windows kit)
- blender 3.0
- python 3.9.7 (must be your default system version, `python --version` should give output `Python 3.9.7`)
- Cython and wheel packages (`pip install Cython wheel`)

## Install
In a terminal, run the following commands:
- `git clone --recurse-submodules https://gitlab.com/ihm-tswow/blender-wow-studio`
- `cd blender-wow-studio/io_scene_wmo`
- `python build.py`
- Download [this file](https://github.com/wowdev/pyCASCLib/raw/5afc012e41415af805d1fea71319e66c58061fe7/CASC.cp39-win_amd64.pyd) and save it as `blender-wow-studio/io_scene_wmo/pywowlib/archives/casc/CASC.cp39-win_amd64.pyd`

In an admin terminal, run the following command (replacing `<path-to-your-installation>` with the directory path containing your cloned `blender-wow-studio` folder:
- `mklink /J "C:\Program Files\Blender Foundation\Blender 3.0\3.0\scripts\addons\io_scene_wmo" "<path-to-your-installation>\blender-wow-studio\io_scene_wmo"`
- Open blender and enable the `WoW Blender Studio` addon.

_(Idk if there's a better way to do the last part, that's just what I do lol)_
