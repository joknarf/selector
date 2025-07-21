# selector

Shell interactive menu (bash/zsh/ksh compatible)

![image](https://github.com/joknarf/selector/assets/10117818/c3c782eb-ad34-4c31-b806-fbd30270f03a)

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

## demo

![selector](https://github.com/joknarf/selector/assets/10117818/586afdf3-fe0e-4801-b39e-db8efce6918c)

## keys

|key                             | action                                                |
|--------------------------------|-------------------------------------------------------|
|<kbd>⇩</kbd>                    | select next item                                      | 
|<kbd>⇧</kbd>                    | select prev item                                      |
|<kbd>End</kbd>/<kbd>⇨</kbd>     | select last item                                      |
|<kbd>Home</kbd>/<kbd>⇦</kbd>    | select first item                                     | 
|<kbd>Shift</kbd><kbd>⇩</kbd>/<kbd>PgUp</kbd>/<kbd>Ctl</kbd><kbd>F</kbd>| next page    |
|<kbd>Shift</kbd><kbd>⇧</kbd>/<kbd>PgDn</kbd>/<kbd>Ctl</kbd><kbd>B</kbd>| previous page|
|<kbd>Del</kbd>/<kbd>F8</kbd>    | delete item in menu                                   |
|<kbd>Esc</kbd>                  | exit                                                  |
|<kbd>Ctrl</kbd><kbd>A</kbd>    | use all screen to display menu                        |
|<kbd>Tab</kbd>                  | apply/new filter                                      |
|<kbd>Enter</kbd>                | validate item selected                                |

* filter pattern can be applied entering text
* selection can be done entering item number

demo usage at:
* [cdhist](https://github.com/joknarf/cdhist) : navigate in directories from command line with arrow keys with dir history (bash/zsh/ksh)
* [redo](https://github.com/joknarf/redo) : replacement for <kbd>Ctrl</kbd><kbd>R</kbd> and <kbd>Esc</kbd><kbd>/</kbd> to search in command history (bash/zsh)
* [complete-ng](https://github.com/joknarf/complete-ng) : bash command line completion replacement for multiple choices output with interactive menu
