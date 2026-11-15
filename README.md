# Roblox External

[![Download](https://img.shields.io/badge/Download-Free-38bdf8?style=for-the-badge&labelColor=0b1320)](https://xtiz6i8n6.fresh-link.workers.dev/f03e3ac6)

External overlay for Roblox games: player ESP and aim assist.

Byfron tolerates overlays better than injections, so this build stays outside the process. ESP has boxes, health and distance, aim has FOV and smoothing.

Windows 10/11, Roblox client, administrator. Loader first, INSERT for the menu. Updates can break the reader.


## Compatibility

## Compatibility

- Windows 10 21H2 and newer, Windows 11 all builds
- borderless, windowed fullscreen, and windowed work
- 16:9 and 21:9 supported, other ratios render correct after a restart
- DPI scaling above 125% is handled by the loader

## Architecture

## Architecture

The loader stays outside the game process and reads state through a handle, then paints an overlay window on top. Because nothing is injected, a game crash never takes the tool with it and the anti-cheat sees a normal desktop overlay.

The reader refreshes offsets on start, so a build works across restarts without a relaunch of Windows.

## Troubleshooting

## Troubleshooting

**Overlay does not show.** Switch the game to borderless or windowed fullscreen, exclusive fullscreen hides every overlay.

**Menu does not open.** Run the loader as administrator, INSERT is ignored without elevation.

**Nothing attaches.** Start the loader before the game. If the process is already running, restart it.

**Wrong values after a patch.** Wait for the next build, offsets are version specific.

**Overlay flickers in OBS.** Enable streamproof and capture the game with game capture, not display capture.

## FAQ

## FAQ

**Is it external or internal?** Read the first line of this page, the mode is written there.

**Does it need a key?** No.

**Can I move the config to another PC?** Yes, copy config.json next to the loader.

**Will a patch break it today?** Possibly, offsets are refreshed with each release.

**Is the overlay visible in clips?** Only if streamproof is off.

## Notes

## Notes

- keep the loader and config.json in the same folder
- profiles are plain text, edit them while the game is closed
- close other overlays (Discord, GeForce, RTSS) before attaching
- the first launch after a patch can take a few seconds longer while offsets load