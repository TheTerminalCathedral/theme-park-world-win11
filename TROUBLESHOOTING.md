# Troubleshooting

Seen on one PC. "Fixed" means fixed there. Change one thing at a time.

| Symptom | Look for | Known cause or status | Try |
|---|---|---|---|
| Nothing starts | No `dxwrapper-*.log` | Files in the wrong folder, or the game does not start without the mod | Check both. The mod needs a game that starts by itself |
| Tiny or misplaced picture, mouse off | Window size in the log | DPI scaling is a likely cause | The DPI step in INSTALL.md, through the Properties window |
| Blocky software look | `fallback.txt`: software renderer or "Out of VRAM" | The game fell back from Direct3D. Seen together with the byte at offset 4 of `save\Config.tcf` being 00 instead of 01 | Choose Direct3D in the game. Back up `Config.tcf` before any edit |
| Too fast | - | Speed appears to follow frame rate | `LimitPerFrameFPS = 30` |
| Picture freezes | `TPW watchdog: no frame for` | Open. Seen at 60 fps, and at the lowest game speed | Wait 30 s before closing. Keep 30 fps, avoid the lowest speed, report the lines |
| Closes at the screen edge | `empty rect copy skipped` | Failed zero-size cursor copy; worked around | Report if it still closes |
| Crash entering a park | Last log lines | Surface/texture links without multisampling; changed, limited retesting | Report |
| Square next to the cursor | - | `DdrawSkipRenderTargetReadback = 2` | Use `1` |
| Mouse stuck in the window | `mouse trapped` | Intended | Ctrl+Alt |
| Window lost off screen | `dxwrapper-window.txt` | Saved position | Close the game, delete that file |
| Want borderless | - | - | `DdrawPillarboxWindowed`: 0 = black surround, 1 = desktop visible, 2 = window |
| Game closes itself | `TPW: game called` | Shows which code asked to quit | Report the line |

RTX Remix is not part of this release. With it, the sky, rain and lightning needed extra handling, and the
sky is still wrong.
