# Wolf as Genichiro - Genichiro's Arsenal — review package

This repository hosts the exact file published on Nexus
(https://www.nexusmods.com/sekiro/mods/2606) for independent review by the
Nexus Mods team, in response to the file-submission review.

## What this mod is
A single-player gameplay mod for Sekiro: Shadows Die Twice. It adds 7 hotkey
combat-art-style skills (Genichiro's moveset) to the player. It works by
in-process hooking of the game — the standard Souls/Sekiro modding approach —
and is loaded by Sekiro Mod Engine.

## On the antivirus flag ("external connections")
The external connections the scanner observed came from **ModEngine**
(katalash's `dinput8.dll` loader), which we had previously bundled. ModEngine's
crash handler uses Windows' DbgHelp, which downloads debug symbols from
Microsoft's public symbol server (`msdl.microsoft.com`) when it writes a crash
log. ModEngine is open-source (https://github.com/katalash/ModEngine) and is
itself hosted on Nexus (sekiro/mods/6).

We have **removed ModEngine from the package entirely.** Users now install it
separately from katalash's page, as with most Sekiro mods. The file in this
repo contains only our own mod DLL plus Sekiro game-data and a text config —
none of which open any external connections.

## Our own DLL has no networking
`sekiro_boss_control.dll` imports **no** Winsock / WinINet / WinHTTP or any
networking library at all, so it physically cannot open a network connection.
The full PE import table is in `NEXUS_dll_import_table.txt`.

## Package contents (`sekiro_boss_control_release_en.zip`)
- `sekiro_boss_control.dll` — our mod DLL (the only executable binary)
- `modengine.ini` — plain-text config (tells the user-installed ModEngine to load the DLL)
- `keybinds.ini`, `README.txt` — text
- `mods/` — Sekiro game-data resources (`.dcx` / `.hks` / `.txt`)

## How it's built (toolchain)
The DLL is written in Rust and built with
`cargo build --release --target x86_64-pc-windows-msvc` (diagnostics disabled
for the release build). In-process hooking uses the public Rust crates `ilhook`
and `iced-x86`. Hotkey input uses `user32` (`GetAsyncKeyState` / `SendInput`).
The source itself is closed, but we're glad to answer any specific questions to
help your review.

## SHA-256
- `sekiro_boss_control_release_en.zip`: `685edb7beff05cacc8774469b544c97251e1b7c03d87e2e43bc1927721405fcb`
- `sekiro_boss_control.dll` (inside): `0ffa116f2387db66205232d3884616d91cc20d6592d7a3df19dc8bf700938276`
