Sporak Keyboard Layout
======================

Synopsis
--------

A Dvorak-based layout with zero-indexed numbers and with punctuation grouped
more logically for programmers.

```
  `~ 0! 1@ 2# 3$ 4% 5^ 6& 7* 8/ 9? _- =+
     ,; (< )> pP yY fF gG cC rR lL [{ ]} \|
     aA oO eE uU iI dD hH tT nN sS .:
     '" qQ jJ kK xX bB mM wW vV zZ
```

Installation
------------

For the console run `sudo loadkeys spoak.map`

For X11:
```sh
sudo cp sporak /usr/share/X11/xkb/symbols
setxkbmap -layout sporak
```
