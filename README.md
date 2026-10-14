# Menu Options for Goobies

Optional styling for the game's menus: button text color, opacity, grow on hover and a hover highlight, on the main menu
and the Esc (pause) menu. **Version 1.1.0-test.1 is a test build.**

## Requirements

- Goobies on Steam (Windows).
- **Requires Mod Menu 1.1.0-test.2 or newer**: [download it here](https://github.com/gregfesta-create/goobies-mod-menu/releases/tag/v1.1.0-test.2); install both, in any order.
  Every Goobies mod needs Mod Menu; it also brings the UE4SS mod loader.

## Install

1. Find the game folder: in Steam, right-click Goobies, *Manage > Browse local files*. Open `Shooter\Binaries\Win64`
   (the folder with `Shooter-Win64-Shipping.exe`); below this is called `Win64`.
2. If Windows marks a downloaded zip as blocked: right-click it, *Properties*, tick **Unblock**.
3. Put `goobies_menu_options_1.1.0-test.1.zip` and the Mod Menu zip into `Win64` and extract each there (*right-click > Extract All*, target `Win64`
   itself). The zips share no files, so install both, in any order.
4. Start Goobies through Steam, open *Mods* and change Menu Options there (the gear next to it).

## Known limits

- The Esc (pause) menu styling is new in this test build. If a pause-menu button looks wrong, or text shows up that should not be there, please report it.

## Reporting a problem

`Report a problem.bat` ships inside the Mod Menu mod folder, `Win64\Mods\mod_menu`, because every Goobies mod needs
Mod Menu. From the Mod Menu README:

**Easiest way: double-click `Report a problem.bat` in your Mod Menu folder.**

Every Goobies mod needs Mod Menu, so the report tool comes with it. It is in your Goobies folder under `Shooter\Binaries\Win64\Mods\mod_menu\` (in Steam: right-click Goobies > **Manage** > **Browse local files**; if you see `Goobies_DX11` or `Goobies_Vulkan`, open the one you play).

1. Double-click `Report a problem.bat`. It works without a window, so give it a few seconds: it reports on the game copy it sits in, saves `Goobies_crash_report_<date>.zip` in your Downloads folder, opens the crash-report page in your browser and tells you in a small popup where the zip is. If Windows warns about the file, choose **More info > Run anyway**.
2. Fill in the form on that page and drag the zip into it.

## Uninstall

Delete `Win64\Mods\MenuOptions`. Mod Menu stays for your other mods. Your save is not changed.

## License

See `LICENSE`.
