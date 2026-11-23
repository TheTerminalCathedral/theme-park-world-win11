# Theme Park World / Sim Theme Park: Windows 11 fix (beta 1)

An unofficial wrapper mod, and a demonstration of the **Human Sandwich Model** from
[AI Madpakken](https://github.com/TheTerminalCathedral/AI-Madpakken): your AI layers install the mod,
and if it does not work on your PC, they help you adapt it.

Not affiliated with EA or Bullfrog. **Contains no game files.** You need your own copy of the game,
and it must already start on your PC. Original discs use SafeDisc copy protection, which Windows 11 does
not support. Getting your own copy to start is up to you: this project cannot tell you how, and the mod
does not remove or work around copy protection. See [GAME_SETUP.md](GAME_SETUP.md).

## Install with the Human Sandwich

The Human Sandwich Model **requires three layers**:

| Layer | Who | What it does |
|---|---|---|
| **Layer 1** (COULD) | A **chat AI** | Talks with you, explains, plans, writes the work orders and reviews the results |
| **The human layer** (SHOULD) | **You** | Decide and approve, start the game, and say what you see |
| **Layer 2** (DID) | A **local coding agent** on your PC, for example Claude Code or Codex | Reads and changes the files, checks the logs and reports back |

You carry the messages between the two AI layers: Layer 1's work order goes to Layer 2, and Layer 2's
report goes back to Layer 1. Set up both before you begin.
1. Open a new conversation with your chat AI (Layer 1).
2. Copy the **official kick-off message** from
   [AI Madpakken, "Start here"](https://github.com/TheTerminalCathedral/AI-Madpakken#start-here--copy-this-into-a-fresh-layer-1)
   and paste it. Use it from there, so you always get the current one.
3. Below it, in the same message, add this and fill in the last two lines:

   ```text
   I have a new project.
   Theme Park World (also sold as Sim Theme Park) is a Windows game from 1999. The Theme Park World
   Windows 11 mod is a wrapper that lets my own copy run on Windows 11, in a resizable window.
   Mod: https://github.com/TheTerminalCathedral/theme-park-world-win11, release beta1.
   Help me, step by step, to:
   1. check that the game is installed, patched to version 2.0 and starts (GAME_SETUP.md)
   2. install the mod in a copy of the game, and set it up for my PC (INSTALL.md)
   3. test it, and if something does not work, find the cause and adapt it (TROUBLESHOOTING.md)
   Read PROJECT.md in that repository first: it holds the facts and limits of this project.
   I launch the game myself, I tell you what I see, and I approve each stage.
   My game is installed in: <FOLDER, or "not installed yet">
   My Layer 2, the local coding agent on this PC, is: <for example Claude Code>
   ```

4. Layer 1 plans with you and writes the work order. Paste it into Layer 2, your local coding agent.
   You approve, Layer 2 does the work and reports, you paste the report into Layer 1, and you test the game.
5. If something fails, tell Layer 1 what you saw. Layer 2 reads the log, and you decide on the next change.

Without the Human Sandwich: follow [GAME_SETUP.md](GAME_SETUP.md), then [INSTALL.md](INSTALL.md), by hand.

## What it does

- Runs the game's Direct3D through Direct3D 9
- Real window: move, resize (fixed 4:3), minimize; the size is remembered
- Keeps the mouse in the window; Ctrl+Alt frees it, a click traps it again
- Limits the game to 30 fps, because it ran too fast at 60
- Avoids crashes at the screen edge and when entering a park

## Beta status

Tested on one Windows 11 PC, with the English 2.0 version. The release configuration was tested
for a short session only. The game can freeze, especially at the lowest game speed; the cause is
unknown. Back up your game and saves.

## Files

| File | Purpose |
|---|---|
| [PROJECT.md](PROJECT.md) | Project facts and boundaries for the layers |
| [GAME_SETUP.md](GAME_SETUP.md) | Installing and patching the game first |
| [INSTALL.md](INSTALL.md) | Install, test and undo |
| [TROUBLESHOOTING.md](TROUBLESHOOTING.md) | Known problems |
| [BUILD.md](BUILD.md) | Building from source |
| [REPORT_TEMPLATE.md](REPORT_TEMPLATE.md) | Reporting a result |
| [manifest.json](manifest.json) | Release files and hashes |
| [CREDITS.txt](CREDITS.txt), `licenses/` | Credits and licences |

`dxwrapper.dll` is a modified version of [dxwrapper](https://github.com/elishacloud/dxwrapper).

## Use it however you want

Everything we made here, the text and our code changes, is free for anyone to use, change, share or sell, for
any purpose, with no conditions and no credit required. It comes with no warranty.

This covers only our own work. The software it builds on belongs to others and keeps its own terms, in
`licenses/` and [CREDITS.txt](CREDITS.txt).
