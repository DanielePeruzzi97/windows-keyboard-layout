# windows-keyboard-layout

## Introduction
Windows includes a keyboard layout called "United States (International)", which allows typing many special characters easily.
The layout defines several keys as "dead keys", such as the apostrophe (`'`) and double quotes (`"`).
This means that to enter a single `'`, you have to press `'` followed by a space.
This can be annoying when you need to enter a lot of these characters, since each now requires two keys to be pressed.

This repo is a modified version of the default Windows "United States (International)" keyboard layout where
(`'` and `"`) are not dead keys and were accents for *vocals* are made by a composition of keys or dead keys:

- **grave** = ALTGR + vocal key
- **acute** = RIGHT SHIFT + vocal key

## How to Build or Install
You can download the installer from the releases tab of this repo (https://github.com/DanielePeruzzi97/windows-keyboard-layout/releases) or using the setup.exe in us-intl folder.

If you prefer to build from source, you can open the .KLC source file in Microsoft Keyboard Layout Creator (https://download.microsoft.com/download/6/f/5/6f5ce43a-e892-4fd1-b9a6-1a0cbb64e6e2/MSKLC.exe).

Open the source file.
![Image 1](/images/loadSource.png)

Then build DLL.
![Image 2](/images/buildDll.png)

## Notes
To delete the custom keyboard layout you need to delete the folder **US-intl.dll** from windows file systems.
Then we need to remove the registry:
- WIN + r
- regedit (as administrator)
- HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\Keyboard Layouts
- delete the values of the custom keyboard (usually at the end of the list)
