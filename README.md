# selector

Shell interactive menu (bash/zsh/ksh compatible)

## usage

```
usage: selector [-p <prompt>] -i <items>|-f <itemfile> [-P <y|n>]
args :
  -p, --prompt          menu prompt
  -i, --items           menu items \n separated
  -f, --file            file with items
  -P, --powerline       y or n, powerline symbol usage
```

## demo

![selector](https://github.com/joknarf/selector/assets/10117818/586afdf3-fe0e-4801-b39e-db8efce6918c)

## keys

|key       | action                          |
|----------|---------------------------------|
|down      | select nex item                 | 
|up        | select prev item                |
|right/End | select last item                |
|left/Home | select first item               | 
|pgup/Ctl-F| next page                       |
|pgdn/Ctl-B| previous page                   |
|ctl-X     | Exit                            |
|enter     | select item/exit or apply filter|

* filter pattern can be applied entering text (ext regexp)
* selection can be done entering item number