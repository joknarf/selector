[![Joknarf Tools](https://img.shields.io/badge/Joknarf%20Tools-Visit-darkgreen?logo=github)](https://joknarf.github.io/joknarf-tools)
[![Build and Release Packages](https://github.com/joknarf/selector/actions/workflows/release.yml/badge.svg)](https://github.com/joknarf/selector/actions/workflows/release.yml)
[![Packages](https://img.shields.io/badge/Packages-%20rpm%20|%20deb%20|%20pkg%20|%20apk%20|%20brew%20-darkgreen.svg)](https://github.com/joknarf/selector/releases/latest)
[![bash](https://img.shields.io/badge/shell-bash%20|%20zsh%20|%20ksh%20-blue.svg)]()
[![Licence](https://img.shields.io/badge/licence-MIT-blue.svg)](https://shields.io/)

# selector

Shell interactive menu (bash/zsh/ksh compatible)

![image](https://github.com/joknarf/selector/assets/10117818/c3c782eb-ad34-4c31-b806-fbd30270f03a)

## features

* dynamic interactive menu with items filtering / selection
* customizable key interaction
* possible display file/folder icons 
* customizable colors

## demo

![selector](https://github.com/user-attachments/assets/d3be018d-1a6e-4101-b292-8f1fd6744d67)

## install

Use a shell plugin manager like the famous [thefly](https://github.com/joknarf/thefly) or use your favorite OS package manager with [release](https://github.com/joknarf/selector/releases/latest) packages
```
fly add joknarf/selector
or
brew install joknarf/tools/selector
dnf install https://github.com/joknarf/selector/releases/latest/download/selector.rpm
...
```
see [joknarf tools](https://joknarf.github.io/joknarf-tools) for package repositories

## usage

```
usage: selector [-p <prompt>] -i <items>|-f <itemfile> [-P <y|n>]
args :
  -p, --prompt          menu prompt
  -i, --items           menu items \n separated
  -f, --file            file with items
  -F, --filter          regexp pattern filter items
  -P, --powerline       y or n, powerline symbol usage
  -a, --autofilter      y or n, filter at keystrokes
  -k, --keyfunc         Custom additional key function
```

selector can be used as command line or sourced to be used as function (bash/zsh/ksh compatible)  
When sourced, the selected item is available as `$selected`.

## keys

|key                             | action                                                |
|--------------------------------|-------------------------------------------------------|
|<kbd>▼</kbd>                    | select next item                                      | 
|<kbd>▲</kbd>                    | select prev item                                      |
|<kbd>End</kbd>/<kbd>▶</kbd>     | select last item                                      |
|<kbd>Home</kbd>/<kbd>◀</kbd>    | select first item                                     | 
|<kbd>Shift</kbd><kbd>▼</kbd>/<kbd>PgUp</kbd>/<kbd>Ctl</kbd><kbd>F</kbd>| next page    |
|<kbd>Shift</kbd><kbd>▲</kbd>/<kbd>PgDn</kbd>/<kbd>Ctl</kbd><kbd>B</kbd>| previous page|
|<kbd>Del</kbd>/<kbd>F8</kbd>    | delete item in menu                                   |
|<kbd>Esc</kbd>                  | exit                                                  |
|<kbd>Ctrl</kbd><kbd>A</kbd>    | use all screen to display menu                        |
|<kbd>Tab</kbd>                  | apply/new filter                                      |
|<kbd>Enter</kbd>                | validate item selected                                |

* filter pattern can be applied entering text
* selection can be done entering item number

# customize

selector menu can be customized setting following variables:
```
SELECTOR_FOLDER_ICON=🖿            # folder icon
SELECTOR_FILE_ICON=📄             # file icon
SELECTOR_CASEI=false               # case sensitivity filter
SELECTOR_POWERLINE=y               # avoid using glyphs with 'n'
SELECTOR_COL_PROMPT="30;90;180"    # blue
SELECTOR_COL_TEXT="255;255;255"    # white
SELECTOR_COL_TOTAL="32;64;64"      # darkggrey
SELECTOR_COL_NUM="36;114;67"       # green
SELECTOR_COL_ARROW="41;98;114"     # cyan
SELECTOR_COL_ITEM="118;141;255"    # light blue
SELECTOR_COL_SELECTED="42;221;244" # light cyan
```

demo usage at:

* [seedee](https://github.com/joknarf/seedee) : navigate in directories from command line with arrow keys with dir history (bash/zsh/ksh)
* [redo](https://github.com/joknarf/redo) : replacement for <kbd>Ctrl</kbd><kbd>R</kbd> and <kbd>Esc</kbd><kbd>/</kbd> to search in command history (bash/zsh)
* [complete-ng](https://github.com/joknarf/complete-ng) : bash/zsh command line completion replacement for multiple choices output with interactive menu
