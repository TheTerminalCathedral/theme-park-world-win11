# Project facts

Roles, authority, evidence and work orders are governed by
[AI Madpakken](https://github.com/TheTerminalCathedral/AI-Madpakken), not by this file. This file
holds project facts and limits. It grants no authority; that comes from the human in the conversation.

## What this is

Theme Park World (Sim Theme Park in some countries) is a 1999 Bullfrog/EA game that uses DirectDraw and
Direct3D 6/7-era calls. This mod is a modified dxwrapper: the game loads `ddraw.dll`, which loads
`dxwrapper.dll`, which runs the game on Direct3D 9 using the settings in `dxwrapper.ini`. It changes no game
files, except the optional resolution setting.

## How the layers can help

The human may never have modified a game. Layer 1: use plain language, one step at a time, and say what
the human should see after each step.

| Step | Layer 2 can | The human does |
|---|---|---|
| Game ready (`GAME_SETUP.md`) | Find the install, version and patches needed | Installs, patches, starts the game |
| Install (`INSTALL.md`) | Copy the game, download, check hashes, place files | Sets the DPI option, approves |
| Set up | Read screen size, propose window mode and resolution | Chooses |
| Test | Read `dxwrapper-*.log`, `fallback.txt`, `enginedebug.txt` afterwards | Plays, describes, takes photos |
| Fix (`TROUBLESHOOTING.md`) | Match the log, propose one change | Approves, tests again |
| Adapt the code (`BUILD.md`) | Change, build, install in a new copy | Approves, tests |

The Human Sandwich needs all three: a chat AI as Layer 1, the human, and a local coding agent as Layer 2. If the
human has no Layer 2 yet, Layer 1 first helps them set one up. The manual route in `INSTALL.md` is separate.

## Adapting the patch is part of the project

The patch was made for one PC. When it fails on the human's PC, the layers may change settings and source code,
within what the human approves, to make the game run there. A problem missing from `TROUBLESHOOTING.md` is
a new problem to investigate, not a reason to give up.

## Goal

The human's own copy of the game runs playably on their PC. The human decides when it does.

## Facts to verify, not assume

- The game already starts without the mod.
- The install folder, the game version, any existing `ddraw.dll`/`d3d9.dll` and other wrappers.
- Windows version, screen resolution and scaling.
- Release files match `manifest.json`.

## Limits

- The original game folder stays untouched. Work in a copy, and back up saves.
- This project supplies no game files or game executables. Getting the game to start without the mod is
  outside this project; see "Copy protection" in `GAME_SETUP.md`.
- Security software and Windows security settings are not weakened.
- No registry edits. The DPI setting is made by the human in the Properties window.
- The human launches the game and judges what is on the screen.
- Nothing is uploaded or posted unless the human has read it and agreed.

## Suggested stages

Each is a separate human decision:

1. Inspect only.
2. Copy the game, install the release files, human test.
3. Change settings, one at a time, with an undo for each.
4. Change and rebuild the source (needs several GB of build tools).

A result counts when the human saw it and the log does not contradict it.
