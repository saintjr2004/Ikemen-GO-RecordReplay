# Record/Replay Module for IKEMEN GO

This is a module for the IKEMEN GO engine that allows you to record a dummy and have
that sequence played back for you.

## Installation

Extract `jayrecordreplay.zss` directly into the folder you wish to store it in. It's recommended
you place it in the `data` folder or whatever folder you contain the `.zss` modules in.

You will need to make edits to your current IKEMEN config.ini file to "enable" the module.

Under `[Common]`, add `jayrecordreplay.zss` to your `States` files.

Example with the files stored in `data`:

```
[Common]
...
States  = data/functions.zss, data/action.zss, data/dizzy.zss, data/guardbreak.zss, data/score.zss, data/system.zss, data/tag.zss, data/training.zss, data/jayrecordreplay.zss
```

## Configuration

Within `jayrecordreplay.zss`, you have several configuration options to tweak the display and behavior of the recorder and text.
Because IKEMEN supports both 4:3 and 16:9 resolutions in the same build, there are visual config options for both resolutions, but if you
are intending to only use one resolution for, say, a fullgame, you can simply ignore the unused resolution options.

```
# ==================================
# CONFIG
# ==================================

map(jayrecordreplay_enable) := 1;			# Enable record/replay (0 = off, 1 = on)
map(jayrecordreplay_slotsMax) := 3;			# Amount of recording slots available (max: 100)
map(jayrecordreplay_absolute) := 0;			# Replayed left/right inputs won't flip based on facing if enabled

map(jayrecordreplay_textPosX) := 160;		# Pos X for the info text
map(jayrecordreplay_textPosY) := 50;		# Pos Y for the info text
map(jayrecordreplay_textOff169X) := 120;		# Pos X offset for widescreen
map(jayrecordreplay_textOff169Y) := 25;		# Pos Y offset for widescreen
map(jayrecordreplay_textFont) := -1;		# Font for the info text
map(jayrecordreplay_textBank) := -1;		# Bank for the info textt
map(jayrecordreplay_textScale) := 0.66;		# Scale for the info text
map(jayrecordreplay_textLayer) := 1;		# Layer for the info text
map(jayrecordreplay_textR) := 256;			# Red color for text
map(jayrecordreplay_textG) := 0;			# Blue color for text
map(jayrecordreplay_textB) := 0;			# Green color for text

# ==================================
```
You can of course edit the module directly with your own `fx.def` file to add visuals.