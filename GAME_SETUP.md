# Before the mod: install and patch the game

The mod needs a game that already starts. This page covers getting there.

## What is supplied, and what is not

| Item | Where it comes from |
|---|---|
| `dxwrapper.dll`, `ddraw.dll`, `dxwrapper.ini` | Supplied in this mod's release ZIP |
| Settings, instructions, source changes | Supplied here |
| Extra runtimes | None needed. The DLLs import only Windows' own libraries |
| The game | Your own copy. Not supplied |
| Official 2.0 patch | EA's work, so linked, not supplied |
| Game executables, no-CD or copy-protection changes | Not supplied, not linked |

## Steps

1. Install the game from your own disc. If Windows cannot run the old installer, report exactly what
   happened. Do not weaken Windows security to get past it.
2. Find out which version you have (`readme.txt`, or the version shown in the menu, for example `v 2.0`).
3. If it is the **English 1.0 or 1.1** version, apply the
   [official 2.0 patch (ModDB)](https://www.moddb.com/downloads/theme-park-world-20-patch) **before** any
   other change. ModDB says the Gold Edition does not need it. Other languages: look for the official
   patch for that language, and do not use the English one.
   - Reference: the Euro/American Patch 2 file we examined, `TPPatchTwoEUROAMER20000324a.exe`
     (5,947,043 bytes), has SHA-256
     `9ac5b8cf9138b973b58a72185e0cf4a3f027d5d6f6a982e0a2bb44be0ce6b0e1`. A different packaging has a
     different hash, so a mismatch alone does not mean the file is bad.
   - Scan downloads before running them.
4. Start the game once **without** the mod.
   - It starts: continue with [INSTALL.md](INSTALL.md).
   - It does not start: read "Copy protection" below.

## Copy protection

The original discs use SafeDisc, which Windows 10 and 11 do not support. An original copy may therefore
not start, however it is installed, and this mod does not change that.

**Getting your own copy to start on Windows 11 is up to you.** This project cannot tell you how, and does
not supply or link to anything for it. Continue with the mod when your copy starts without it.

## Optional, not tested with this release

- **Missing music in parks:** a separate community tool, TPW Patcher (MIT licence), listed on
  [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Theme_Park_World). It changes the game executable, so
  use it only on a backed-up copy, and only if the human chooses to.
