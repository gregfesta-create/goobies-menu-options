# Goobies Menu Options

Optional main-menu presentation settings for **Goobies**: button text color, opacity, grow on hover, and a hover highlight. Requires **Goobies Mod Menu**.

**Version:** 1.0.1 (see `Mods/MenuOptions/CHANGELOG.md`).

## Install
1. Install [Goobies Mod Menu](https://github.com/gregfesta-create/goobies-mod-menu) first.
2. Copy everything in this repository into the game's `Shooter/Binaries/Win64` folder, keeping the folder structure.
3. Start the game, open **Mods**, and adjust Menu Options there.

Details: `Mods/MenuOptions/INSTALL.txt`.

## Reporting a crash

1. Download [`CollectCrashReport.ps1`](https://raw.githubusercontent.com/gregfesta-create/goobies-mod-menu/main/Tools/CollectCrashReport.ps1) (right-click the link > **Save link as**; source: [Tools/CollectCrashReport.ps1](https://github.com/gregfesta-create/goobies-mod-menu/blob/main/Tools/CollectCrashReport.ps1)).
2. Right-click the saved file > **Run with PowerShell**. It finds the game through Steam, picking the DX11 or Vulkan copy you played last, and puts `Goobies_crash_report_<date>.zip` on your Desktop. If Windows blocks it: right-click > Properties > **Unblock** (or run `Unblock-File` on it).
3. Open a [Crash report issue](https://github.com/gregfesta-create/goobies-menu-options/issues/new?template=crash_report.yml), fill in the form and drag the zip into it.

From a console (in the download folder): `powershell -NoProfile -ExecutionPolicy Bypass -File .\CollectCrashReport.ps1 -GameDir "<Goobies folder>" [-NoDump]`. If it fails, it leaves `Goobies_crash_report_FAILED.txt` on the Desktop with the reason and the retry steps.

Included: UE4SS logs, `UE4SS-settings.ini`, `Configs/ModList.ini`, `Mods/mods.txt`, each mod's `mod_menu.ini`, the list of mod folders, the newest crash's `CrashContext.runtime-xml` and `CrashReportClient.ini`, a `summary.txt`, and the newest crash dump (`.dmp`) if it is 20 MB or less.

Removed from text files: your user name and profile folder, computer name, Steam and lobby IDs, IP and e-mail addresses, network host names, and the account/machine fields in the crash context. `summary.txt` warns if the newest crash looks older or newer than your last session, or came from a different Goobies copy; mention that in the issue.

**The `.dmp` file cannot be cleaned:** it is a snapshot of the game's memory and may contain personal information. To leave it out, run the script with `-NoDump`.

If the script cannot run, zip these by hand (open them first and remove anything personal): `Shooter/Binaries/Win64/UE4SS.log`, `Shooter/Binaries/Win64/Mods/mods.txt`, `Shooter/Binaries/Win64/Configs/ModList.ini`, and the newest folder in `%LOCALAPPDATA%\Shooter\Saved\Crashes\`.
