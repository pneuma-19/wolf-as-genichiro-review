============================================================
  Wolf as Genichiro - Genichiro's Arsenal  (v0.1)
============================================================

[ What this is ]
  A single-player Sekiro mod. Wolf gains 7 hotkey skills lifted straight from
  Genichiro - lightning slashes, combos, real damage. Press a key, Wolf performs
  the move. Instant, local, no launcher, no extra program.

  This is v0.1, an early release. It works but it's rough - known issues are
  listed below, and your feedback shapes what's next.

  Note on appearance: this mod ships only my own work, so Wolf keeps his own look.
  Want to look like Genichiro too? See "Optional: Genichiro appearance" below.


[ Requirements ]
  - Sekiro: Shadows Die Twice (Steam, v1.06 - the standard version).
  - Sekiro Mod Engine by katalash - download it first from:
        https://www.nexusmods.com/sekiro/mods/6
    It provides dinput8.dll, the loader this mod runs on. I don't bundle it -
    please grab it from katalash's page (always the latest version).
  - Turn off Steam Cloud for Sekiro before installing
    (Steam -> right-click Sekiro -> Properties -> General -> uncheck Steam Cloud).
    This avoids save conflicts.


[ Install  (manual - copy & paste) ]
  1. Install Sekiro Mod Engine first (see Requirements): copy its dinput8.dll into
     your Sekiro folder - the one with sekiro.exe.
     In Steam: right-click Sekiro -> Manage -> Browse local files.
     It looks like: ...\steamapps\common\Sekiro
  2. Unzip this download.
  3. Copy these into that same Sekiro folder (next to sekiro.exe):
       - sekiro_boss_control.dll
       - modengine.ini       (replace Mod Engine's default if asked - mine loads this mod)
       - keybinds.ini        (optional - only if you want to remap keys)
       - the whole "mods" folder
     If Windows asks to replace or merge, choose yes.
  4. Launch Sekiro normally from Steam.


[ Controls ]
  Default keys - each fires a Genichiro skill:
       1  - Seven-slash combo
       2  - Lightning slash 1
     3 4 5 - Slash 1 / 2 / 3
       6  - Lightning slash 2
       `  - Lightning slash 3   (backtick, the key under Esc)
  Press while playing; give it 1-2 seconds after a fight or area loads, then go.

  Rebinding keys: edit keybinds.ini (in your Sekiro folder, next to the .dll),
  then restart the game. The comments in that file explain the format and list
  every technique.


[ Optional: Genichiro appearance  (third-party mods - credit to their authors) ]
  This mod only ships my own content, so Wolf stays Wolf. For the full
  play-as-Genichiro experience - Genichiro's model AND his normal-attack style -
  also grab these from Nexus (download from the original authors; I don't bundle
  their files):
    - Genichiro Moveset  by Trollaxethrowerrr  - mod 1511 - Genichiro-style combos
    - Costume Pack       by ZullieTheWitch     - mod 93   - Genichiro model
    - Genichiro's Gear   by vhgggg             - mod 268  - katana + longbow
  Install those first, then copy my files over them.


[ Known issues  (v0.1 - being honest) ]
  - Audio can occasionally cut out mid-session. I'm tracking it down.
  - Keyboard only for now - no controller buttons yet.
  - Wolf keeps his appearance unless you add the optional mods above.
  It's v0.1 - drop a comment with anything that breaks.


[ Uninstall ]
  Delete from your Sekiro folder: modengine.ini, sekiro_boss_control.dll,
  keybinds.ini, and the "mods" folder. (dinput8.dll belongs to Mod Engine -
  leave it if you use other mods, or delete it to disable all mods.)


[ Troubleshooting ]
  - Skills don't fire? Make sure all the files AND the "mods" folder are in the
    same folder as sekiro.exe. Wait a couple seconds after loading in, then press.
  - Crash / black screen on launch? Antivirus sometimes blocks injection mods like
    this one - add an exception for the folder (or briefly disable real-time
    protection), and remove other injection mods that might conflict.
  - Character isn't Genichiro? That's expected - the look comes from the optional
    Nexus mods above; this mod doesn't include them.


[ Credits ]
  - Genichiro Moveset - Trollaxethrowerrr (mod 1511)
  - Costume Pack      - ZullieTheWitch (mod 93)
  - Genichiro's Gear  - vhgggg (mod 268)
  - Mod Engine        - Katalash
  Made by pneuma19.
