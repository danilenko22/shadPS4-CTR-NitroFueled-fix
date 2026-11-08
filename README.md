# Crash Team Racing Nitro-Fueled fur fix for shadPS4

Unofficial shader patch for **Crash Team Racing Nitro-Fueled (CUSA13795)** on [shadPS4](https://github.com/shadps4-emu/shadPS4). Works with regular shadPS4 builds (tested with v0.20.1 WIP); no custom emulator needed.

**Download:** [latest release](../../releases/latest)

## What it fixes
Grey speckles on the skin/fur of the characters (Coco, Crash, etc.).

The game draws fur as 6 layers. On layers 1-5 the skin shader takes a fur branch that outputs a wrong grey color on shadPS4. The patched skin shaders discard those layers, so only the base layer is drawn: smooth skin, no speckles. Hair shaders are not touched, so hair keeps its volume.

## Installation
1. Copy `shader_patch\*.spv` to `%APPDATA%\shadPS4\shader\patch\`.
2. Copy `custom_configs\CUSA13795.json` to `%APPDATA%\shadPS4\custom_configs\` (enables `patch_shaders`, disables FSR and RCAS).
3. Play.

If a character still shows speckles, patch its shader with `spv_furpatch.py`: see [README-INSTALL.txt](README-INSTALL.txt) (English) or [LEEME.txt](LEEME.txt) (Spanish).

## License
GPL-2.0, same as shadPS4 (see [LICENSE](LICENSE)). No game files are included.
