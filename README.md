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
```

selector can be used as command line or sourced to be used as function (bash/zsh/ksh compatible)
When sourced, the selected item is available as `$selected`.

## demo

![selector](https://github.com/joknarf/selector/assets/10117818/586afdf3-fe0e-4801-b39e-db8efce6918c)

## keys

|key       | action                          |
|----------|---------------------------------|
|Down      | select nex item                 | 
|Up        | select prev item                |
|Right/End | select last item                |
|Left/Home | select first item               | 
|PgUp/Ctl-F| next page                       |
|PgDn/Ctl-B| previous page                   |
|Ctl-X     | Exit                            |
|Ctl-A     | Use all screen to display menu  |
|Enter     | select item/exit or apply filter|

* filter pattern can be applied entering text (ext regexp)
* selection can be done entering item number