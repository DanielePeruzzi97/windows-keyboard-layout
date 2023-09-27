# windows-keyboard-layout

## Introduction
Windows includes a keyboard layout called "United States (International)", which allows typing many special characters easily.
The layout defines several keys as "dead keys", such as the apostrophe (`'`) and double quotes (`"`).
This means that to enter a single `'`, you have to press `'` followed by a space.
This can be annoying when you need to enter a lot of these characters, since each now requires two keys to be pressed.

This repo is a modified version of the default Windows "United States (International)" keyboard layout where
(`'` and `"`) are now only dead when AltGr is pressed, otherwise they function as normal keys.
Plus to make accents:

- **grave** = ALTGR + vocal
- **acute** = CAPSLOCK(ALTGR + vocal)

## How to Build or Install
You can download the installer from the releases tab of this repo (https://github.com/DanielePeruzzi97/windows-keyboard-layout/releases) or unzipping *us-utils.zip*

If you prefer to build from source, you can open the .KLC source file in Microsoft Keyboard Layout Creator (https://download.microsoft.com/download/6/f/5/6f5ce43a-e892-4fd1-b9a6-1a0cbb64e6e2/MSKLC.exe).

Open the source file.
![Image 1](/images/loadSource.png)

Then build DLL.
![Image 2](/images/buildDll.png)

