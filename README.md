
## cbpp-ui-theme-src

Honestly just a fork of greybird-gtk-theme, with a few runs of

```
## png desaturate
$ for I in $(find . -type f -iname '*.png' ); do convert $I -colorspace gray $I; done
```

```
## svg desaturate
$ for I in $(ls *.svg); do inkscape --batch-process --actions="org.inkscape.color.desaturate;export-overwrite;export-do;" $I; done
```

And since I can't be bothered to actually learn how to do proper debian
packaging like you see here, the files get copied into (cbpp/cbpp-ui-theme)[https://github.com/cbpp/cbpp-ui-theme]
as flat files c:
