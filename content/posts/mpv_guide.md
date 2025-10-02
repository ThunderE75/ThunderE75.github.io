+++
title = 'MPV Media Player Guide'
date = '2025-10-02T19:43:38+05:30'
tags = ['windows', 'FOSS', 'guide']
+++
 This guide demonstrates how i setup my MPV will all the Configs, Scripts & Keybindings. 
 > This was setup on Windows 11, so some changes might be necessary (Like File paths & CLI commands) to make it work on Linux/MacOS. 

## Script Breakdown

- {{< linkicon "https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/autoload.lua" "fa-brands fa-github" "autoload" >}} - This script automatically loads playlist entries before and after the currently played file. 
- {{< linkicon "https://github.com/davidde/mpv-autosub" "fa-brands fa-github" "autosub" >}} - This script uses Subliminal to download subtitles.
- {{< linkicon "https://github.com/sibwaf/mpv-scripts/blob/master/blackout.lua" "fa-brands fa-github" "blackout" >}} - Turns the screen completely black and pauses on a button press.
- {{< linkicon "https://github.com/zenyd/mpv-scripts/blob/master/delete_file.lua" "fa-brands fa-github" "delete_file" >}} - This script is used to delete files.
- {{< linkicon "https://github.com/tsl0922/mpv-menu-plugin" "fa-brands fa-github" "mpv-menu-plugin" >}} - Configurable context menu for mpv on Windows, with additional support for native file dialog and clipboard.
- {{< linkicon "https://github.com/Samillion/ModernZ/" "fa-brands fa-github" "ModernZ" >}} - A fork of ModernX, with built-in support for interactive menus & better UI customization. 
- {{< linkicon "https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/pause-when-minimize.lua" "fa-brands fa-github" "pause-when-minimize" >}} - This script pauses playback when minimizing the window, and resumes playback.
- {{< linkicon "https://github.com/jonniek/mpv-playlistmanager" "fa-brands fa-github" "playlistmanager" >}} - This script allows you to see and interact with your playlist in an intuitive way.
- {{< linkicon "https://github.com/po5/thumbfast" "fa-brands fa-github" "thumbfast" >}} - High-performance on-the-fly thumbnailer script for mpv.
- {{< linkicon "https://github.com/christoph-heinrich/mpv-pointer-event" "fa-brands fa-github" "mpv-pointer-event" >}} - Mouse/Touch input event detection for mpv.
- {{< linkicon "https://github.com/christoph-heinrich/mpv-touch-gestures" "fa-brands fa-github" "touch-gestures" >}} - Touch gestures for mpv.
- {{< linkicon "https://github.com/occivink/mpv-gallery-view" "fa-brands fa-github" "mpv-gallery-view (Playlist View)" >}} - Playlist grid view.
- {{< linkicon "https://github.com/occivink/mpv-gallery-view" "fa-brands fa-github" "mpv-gallery-view (Contact Sheet)" >}} - Contact sheet view.

## Fonts

### Preferred font for subtitles
- {{< linkicon "https://fonts.google.com/specimen/Space+Grotesk" "fa-brands fa-google" "Google Fonts - Space Grotesk" >}} 
- {{< linkicon "https://fonts.google.com/specimen/Atkinson+Hyperlegible" "fa-brands fa-google" "Google Fonts - Atkinson Hyperlegible" >}}

### OSC Fonts
- {{< linkicon "https://github.com/Samillion/ModernZ/blob/main/material-design-icons.ttf" "fa-brands fa-github" "ModernZ/Material Design Iconic">}} - Material Design Icons used for ModernZ OSC
- {{< linkicon "https://github.com/microsoft/fluentui-system-icons" "fa-brands fa-github" "microsoft/fluentui-system-icons">}} - A modified version by {{< linkicon "https://github.com/Xurdejl" "fa-solid fa-user" "Github/Xurdejl" >}}

## Installing (Windows)

> Prerequisites {{<linkicon "https://mpv.io/installation/" "fa-solid fa-play" "mpv">}}, {{<linkicon "https://git-scm.com/" "fa-brands fa-git-alt" "git">}} & {{<linkicon "https://www.python.org/downloads/" "fa-brands fa-python" "python3 (pip)">}}

1. Clone the repository into `%APPDATA%` folder
    ```sh 
    git clone https://github.com/ThunderE75/mpv-scripts %APPDATA%\mpv
    ```
1. Download {{<linkicon "https://pypi.org/project/subliminal/" "fa-brands fa-python" "pip/Subliminal">}} for {{< linkicon "https://github.com/davidde/mpv-autosub" "fa-brands fa-github" "autosub" >}}
   ```sh
   pip install subliminal
   ```
## Key Bindings

### Miscellaneous Script Keybindings

| Keybinds                                             | Description                            |
| ---------------------------------------------------- | -------------------------------------- |
| {{< kbd "b" >}}                                      | blackout (black screen)                |
| {{< kbd "0" >}} ↔ {{< kbd "9" >}} (on Keypad)        | Seek to `num*10%` (YouTube-esque seek) |

### Playlist Management

| Keybinds                                                      | Description                   |
| ------------------------------------------------------------- | ----------------------------- |
| {{< kbd "p" >}}                                               | Peek current playlist         |
| {{< kbd "Ctrl ⌃" >}} + {{< kbd "→" >}}                        | Next File                     |
| {{< kbd "Ctrl ⌃" >}} + {{< kbd "←" >}}                        | Previous File                 |
| {{< kbd "Shift ⇧" >}} + {{< kbd "Enter ⏎" >}}                 | Show playlist manager console |
| {{< kbd "Shift ⇧" >}} + {{< kbd "Alt ⎇" >}} + {{< kbd "s" >}} | Cycle Playlist Sort           |
| {{< kbd "Shift ⇧" >}} + {{< kbd "Alt ⎇" >}} + {{< kbd "h" >}} | Shuffle current playlist      |
| {{< kbd "c" >}}                                               | Open contact sheet            |
| {{< kbd "g" >}}                                               | Open grid playlist view       |

### Subtitle Keybinds

| Keybinds                                                      | Description                 |
| ------------------------------------------------------------- | --------------------------- |
| {{< kbd "v" >}}                                               | Toggle Subtitle             |
| {{< kbd "Ctrl ⌃" >}} + {{< kbd "Alt ⎇" >}} + {{< kbd "s" >}} | Download Subtitles          |
| {{< kbd "j" >}}                                               | Cycle Subtitle              |
| {{< kbd "z" >}}                                               | Reduce subtitle delay (1ms) |
| {{< kbd "Shift ⇧" >}} + {{< kbd "z" >}}                       | Add subtitle delay (1ms)    |

### Bulk Delete Files

> Files will be deleted only upon exit [more info](https://github.com/zenyd/mpv-scripts/tree/master?tab=readme-ov-file#delete-file).

| Keybinds                                                                 | Description                                                |
| ------------------------------------------------------------------------ | ---------------------------------------------------------- |
| {{< kbd "Shift ⇧" >}} + {{< kbd "Del ⌦" >}}                              | Mark/Unmark file to be deleted                             |
| {{< kbd "Alt ⎇" >}} + {{< kbd "Del ⌦" >}}                                | Show the list of files marked for deletion                 |
| {{< kbd "Ctrl ⌃" >}} + {{< kbd "Shift ⇧" >}} + {{< kbd "Del ⌦" >}}       | Clear the list of marked files (files will not be deleted) |

### Common Default Keybinds

| Keybinds                                    | Description                           |
| ------------------------------------------- | ------------------------------------- |
| {{< kbd "PgUp ⇞" >}} or {{< kbd "@" >}}     | Next Chapter                          |
| {{< kbd "PgDn ⇟" >}} or {{< kbd "!" >}}     | Previous Chapter                      |
| {{< kbd "a" >}}                             | Cycle Aspect Ratio                    |
| {{< kbd "s" >}}                             | Screenshot View                       |
| {{< kbd "Shift ⇧" >}} + {{< kbd "s" >}}     | Screenshot Video (without Subtitle)   |

> Reference: {{<linkicon "https://github.com/ThunderE75/mpv-scripts" "fa-brands fa-github" "ThunderE75/mpv">}}