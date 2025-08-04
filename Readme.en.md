# CoConsole Mod User Guide

Only compatible with game version 1.9.7.12. The mod will become invalid after any game update. There is no commitment to future updates.

This mod only works under the following conditions:

1. There are **more** than one player in the room.
2. All players in the room must type "cmd ok" to allow you use the mod.

If there is (rarely) a new version, it may include security updates. In this case, you should update (or stop use the old mod) to avoid being hacked. The mod will send its version number to everyone in the room chat when you first use it after you start the game. If you see someone with a newer version, you should update.

## Installation

Copy `userenv.dll` to your game directory (the directory where `isaac-ng.exe` is located). This will not overwrite any files. To remove the mod, just delete this DLL.

## "cmd ok"

Type "cmd ok" in the chat to agree use of the mod, and "cmd no" to disagree it. The mod will automatically record each player’s agreement status with their steam ID, so you don’t need to re-agree when switching rooms. Console commands can only be used if all players in the room (including yourself) have agreed to use the mod. If you join a game in middle progress, other players also need to send "cmd ok" to let your mod knows, then you can send commands.

## Compatibility

All players in the room **must** patch the mod. Otherwise, the game will freeze if you send debug console command. Normally you can't freeze the game before all players allows you with "cmd ok".

## Console Commands

Send "cmd <command>" in the chatbox to execute a command. For example, "cmd spawn 5.100". Some commands (such as `giveitem` that attached to a specific player) may cause the game to desync. Do not use commands in the room menu, only use them in-game.

**You should understand that any game consequences caused by console commands are not bugs. Do not report these issues to Nicalis unless you can prove they occur during normal gameplay, or their fix would benefit Nicalis.**

**Do not report any desync issues caused directly by console commands to Nicalis—they won’t handle them.** ~~Nor should you report them to me; I don’t want to work overtime.~~

## Known Design Limitations

Known means these issues will not be fixed.

- Only one command per frame; do not send multiple commands or have multiple player use commands at the same time, as this may cause desync or disconnects.
- The mod does not handle packet loss; any packet loss will inevitably cause desync or disconnects.
- Console output is not displayed.
- The mod does not affect command history; the `repeat` command will not work.

## Game Restrictions & Security

- Lua commands have been banned to avoid security issues.
- Daily run is banned. Moving the cursor to `Daily Run` will cause the game to exit immediately.
- The game’s error log upload feature is disabled (i don't know if the official version enables this).

## Technical Principle

This mod adds a custom console message type to the game’s network code and completes subsequent development, without introducing significant additional security risks. However, you should understand that any feature development in a co-op scenario will inevitably introduce security risks that may expose your computer to hacking. Any unknown security risks introduced by this mod are entirely unrelated to Nicalis.

For these reasons, the source code of this mod is not public. If needed, you may discuss it with the author.

