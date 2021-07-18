Sporak Keyboard Layout
======================

Synopsis
--------

A Dvorak-based layout with zero-indexed numbers and with punctuation grouped
more logically for programmers.

```
  `~ 0! 1@ 2# 3$ 4% 5^ 6& 7* 8| 9? _- =+
     .: (< )> pP yY fF gG cC rR lL [{ ]} /\
     aA oO eE uU iI dD hH tT nN sS '"
     ,; qQ jJ kK xX bB mM wW vV zZ
```

Why?
----

I've been using Dvorak for almost 20 years now. It's undoubtedly superior to
QWERTY in most ways, but there are a few things that have always bugged me:

- It's pretty weird that the digits are laid out sequentially with one exception.
- The brackets ([{<>}]) (which programmers may very well use more than any other
  punctuation) are in three different locations, two of which are in the top
  row, which is a difficult to reach accurately.
- Some keys require shift that shouldn't.
- Some similar keys are illogically separated, like plus/minus and slash/backslash.

Features
--------

- Numerals are sorted. Punctuations on these keys remain in place with the
  exception of parentheses.
- Minus and plus: together again, but now they both require shift instead of
  behaving inversely to each other.
- Underscore no longer requires shift key, so anyone trying to type out
  snake_case—­or UPPER_SNAKE_CASE with the CapsLock—can breath a sigh of relief.
- Brackets are in two locations, just above home row.
- Colons and semicolons are just the shifted versions of their undotted
  counterparts. Similarly, backslash is the shifted version of its reflection.
- Question Mark is now in the opposite pinky-position to its brother Exclamation
  Point.
- _- += [{ ]} \ '" have been returned to their original QWERTY positions.
  Perfect for those of us who sometimes resort to sight-typing for those
  peripheral, hard-to-reach punctuations. _Note that underscore, hyphen, and
  backslash have different shiftedness from their QWERTY counterparts_

Installation
------------

For the console:
```sh
sudo loadkeys sporak.map
```

For X11:
```sh
sudo cp sporak /usr/share/X11/xkb/symbols
setxkbmap -layout sporak
```
