# custom-keyboard-layout

## Tables of Contents
    - [Introduction](#introduction)
    - [Mappings](#mappings)
    - [Installation](#installation)
        -[Windows](#windows)
            -[Notes](#notes)
    -[Credits](#credits)
    -[TODO](#todo)


## Introduction
I was trying to create a custom keyboard layout for both Linux and Windows based on the USA international layout. However, I encountered a particular challenge with this layout some time ago—it didn't offer a straightforward method for typing vowels with accents. Fortunately, I discovered a useful layout on Linux known as "USA international with dead keys," which was able to address this issue.

In that layout, certain keys are designated as "dead keys," such as the apostrophe (') and double quotes ("). When a key is marked as a dead key, typing it alone didn't produce a character immediately. Instead, it is waiting for a subsequent keypress to combine with and generate a specific character. For instance, to input a single ', you need to press ' followed by a space. The same applies to other dead keys like ``` and ".

This setup became quite inconvenient when I needed to input multiple instances of these characters, as each one then required two key presses—first for the dead key, and then for the spacebar to output the desired character.

So, I decided to customize the entire layout. And due to that, I decided to make this layout for Windows and Linux.

## Mappings

Here is the list of the principal mappings, which are the solutions to my main problem:

- **grave accent**: `ALTGR + VOWEL` | `ALTGR + BACKTICK + VOWEL`
- **acute accent**: `ALTGR + ' + VOWEL`

## Installation

### Windows
You can download the installer [from the releases tab of this repo](https://github.com/DanielePeruzzi97/windows-keyboard-layout/releases) or build it from file.

If you prefer to build from source, you can open the .KLC source file in [Microsoft Keyboard Layout Creator](https://download.microsoft.com/download/6/f/5/6f5ce43a-e892-4fd1-b9a6-1a0cbb64e6e2/MSKLC.exe).

Open the source file.
![Image 1](/images/loadSource.png)

Then build DLL.
![Image 2](/images/buildDll.png)

### Notes
To delete the custom keyboard layout you need to delete the folder **us-altgr.dll** from the windows file systems.
Then, you need to remove the registry entry:
```
WIN + r

regedit (as administrator)

HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\Keyboard Layouts

delete the values of the custom keyboard (usually at the end of the list)
```

## Credits
Thanks to:
- [barkloaf](https://github.com/barkloaf/US-Reformed-International)
- [thomasfaingnaert](https://github.com/thomasfaingnaert/win-us-intl-altgr)

## TODO
- Linux conversion
- Use [`klfc`](https://github.com/39aldo39/klfc) to simplify the process and to automatically generate keyboard layouts.