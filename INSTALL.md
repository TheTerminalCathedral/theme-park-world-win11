# Install

1. Copy the whole game folder and work in the copy.
2. Download the release ZIP and check its SHA-256 against `manifest.json`.
3. Put `dxwrapper.dll`, `ddraw.dll` and `dxwrapper.ini` beside `TP.EXE`. Keep a copy of any file they
   would replace.
4. In the same folder, copy `TP.EXE` to `TPWtest.exe` and use that to start the game. Windows applies an
   old compatibility rule to the original name.
5. Right-click `TPWtest.exe` > Properties > Compatibility > Change high DPI settings > tick
   "Override high DPI scaling behavior" > Application.
6. Optional, 1600x1200: set `Res.RESOLUTION` to `6` in `data\Resolution.sam`, after copying that file.
7. Start `TPWtest.exe`.

## Test

- Reaches the menu; sharp picture; `fallback.txt` says "Direct3D initialized succesfully" (the game's spelling)
- Normal speed, readable text, usable menus
- Move, resize, minimize, restore; Ctrl+Alt frees the mouse
- Cursor along all four window edges
- Enter each park; rain and thunder; a 30-minute session; quit from the menu

## Undo

Delete the copied folder. In an existing install, instead remove the three files,
`dxwrapper-window.txt` and `dxwrapper-*.log`, then restore what you backed up and untick the DPI setting.
