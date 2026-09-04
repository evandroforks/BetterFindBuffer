# BetterFindBuffer for SublimeText 3
Adds a couple of missing features to SublimeText Find Results buffer.

**Note**: You need to *restart* your SublimeText after installing this plugin.

## Features
- Open the the file and line under the cursor by pressing <kbd>Enter</kbd> or <kbd>o</kbd>
- <kbd>n</kbd> and <kbd>p</kbd> to jump to next/previous file
- <kbd>j</kbd> and <kbd>k</kbd> to jump to next/previous match
- Open multiple files with multiple cursor at the same time by selecting lines and pressing <kbd>Enter</kbd> or <kbd>o</kbd>
- Open all files in the result with <kbd>a</kbd>
- Fold a result with <kbd>f</kbd> and move to next file
- Show shortcuts with <kbd>?</kbd>
- Remove path prefix in filenames based on open sublime's project folders (can be disabled in settings)
- Set find results as readonly (can be disabled in settings)
- Adds search keyword and file names to the symbols list (use <kbd>Super</kbd>+<kbd>R</kbd>)
- Cleaner UI (hides line numbers, gutter, indent guides)
- Better Syntax highlighting for find results
- Custom color scheme

![BetterFindBuffer Screenshot1](https://cloud.githubusercontent.com/assets/3202/16536669/d9ed24c0-3ff4-11e6-9d4f-779049c063cd.png)

![BetterFindBuffer Screenshot2](https://cloud.githubusercontent.com/assets/3202/16536672/e07db07a-3ff4-11e6-865d-1f24cb2a8dad.png)


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
    wait few seconds until the installation finishes up
1. Now,
    Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    input the following address and press <kbd>Enter</kbd>
    ```
    https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
    ```
1. Go to the menu **`Tools -> Command Palette...
    (Ctrl+Shift+P)`**
1. Type **`Preferences:
    Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    find the following setting on your **`Package Control.sublime-settings`** file:
    ```js
    "channels":
    [
        "https://packagecontrol.io/channel_v3.json",
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
    ],
    ```
1. And,
    change it to the following, i.e.,
    put the **`https://raw.githubusercontent...`** line as first:
    ```js
    "channels":
    [
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
        "https://packagecontrol.io/channel_v3.json",
    ],
    ```
    * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
      you will not install this forked version of the package,
      but the original available on the Package Control default channel **`https://packagecontrol.io...`**
    > [!WARNING]
    > Placing this custom channel before the default channel changes Package Control's resolution globally.
    > Packages from this channel with the same name will override versions from the default channel.
    >
    > You can review the channel contents here:
    > https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
1. Now,
    go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    search for **`BetterFindBuffer`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


## Changing color scheme
If you don't like colors used in the find results buffer just copy [this file](https://github.com/aziz/BetterFindBuffer/blob/master/FindResults.hidden-tmTheme) to your User folder, change colors and save it and then create a file called `Find Results.sublime-settings` in your User folder and paste the code below:

``` json
{
  "color_scheme": "Path to your custom color scheme file. e.g. Packages/User/Custom_FindResults.hidden-tmTheme",
}
```

Alternatively, you can use [BetterFindBuffer-Designer](http://bobtherobot.github.io/BetterFindBuffer-Designer/) tool as GUI to easily customize the Find-Results color scheme.

### Credit
`FindInFilesOpenFileCommand` is inspired by [this answer on StackOverflow](http://stackoverflow.com/a/16779397/78254)

#### License
See the LICENSE file
