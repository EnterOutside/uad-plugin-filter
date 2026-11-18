# UAD Plugin Filter

Universal Audio's installer drops the whole UAD-2 catalogue into your plugin folders, so your DAW lists hundreds of plugins you can't use. This reads your UAD System Profile, works out which plugins you're actually authorized for, and moves the rest out of your VST2, VST3 and AAX folders. Nothing is deleted - Restore puts them back. UADx native plugins are never touched. Not affiliated with Universal Audio.

## Download

Get the latest build from the [Releases page](https://github.com/enteroutside/uad-plugin-filter/releases/latest).

Windows 64-bit. No installer - it's a single executable, run it where you like.

## How to use

1. In **UAD Meter & Control Panel**, export your system info and save it as `UADSystemProfile.txt` in your Downloads folder (or anywhere - you can Browse to it).
2. Close your DAWs.
3. Run `uad-plugin-filter-<version>.exe`. Windows asks for administrator permission, because the plugins live in Program Files.
4. Check the list (plugins you don't own start ticked) and press **Move ticked plugins...**. They go to a `UAD Unused Plugins` folder in Downloads.
5. To undo, open the **Moved** tab, tick them and press **Restore ticked**.

It looks in UA's standard install folders. A UA software update puts every plugin back - just run it again afterwards, and re-export the profile after you buy something new.

## Verifying the download

This is a personal project and the executable isn't code-signed, so Windows SmartScreen will warn you the first time you run it. You can check the file is exactly the one published here:

- **SHA-256** (v1.0.0.0): `eb0373bda23dd1fd6abc7e6323e37930bdbc335b66f771d83aa5df100b25373f`

In PowerShell:

```powershell
Get-FileHash .\uad-plugin-filter-1.0.0.0.exe -Algorithm SHA256
```

## About

Built by [EnterOutside](https://www.enteroutside.com). Free to use, shared as-is with no support promised.
