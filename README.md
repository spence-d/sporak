Sporak Keyboard Layout
======================

Synopsis
--------

A Dvorak-based layout with zero-indexed numbers and with punctuation grouped
more logically for programmers.


Why?
----

I've been using Dvorak for almost 20 years now. It's undoubtedly superior to
QWERTY in most ways, but there are a few things that have always bugged me about
these and most other layouts:

- It's pretty weird that the digits are laid out sequentially with one exception.
- The brackets ([{<>}]) (which programmers may very well use more than any other
  punctuation) are in odd locations which are often difficult to reach accurately.
  Since these are hit in pairs, inaccuracies are twice as frustrating.
- Many common programming operands require awkward finger travel and mismatched
  shifting.
- Some similar keys are illogically separated, like plus/minus and slash/backslash.
- Vim keybindings are all over the place.

It's pretty striking how well a layout designed in the 1930s holds up in the age
of computers, and I think that can be attributed to the following features:

- Decent placement of the most common letters in English usage.
- Great hand alternation and minimal same-finger bigrams.
- Fairly balanced workload between left and right hands, with a slight advantage
  to right-handers.

Let's see if we can tweak it a little to where we have great letter placement
without compromising the second point too much. If we can bridge the hand gap
a little along the way, all the better.

Features
--------

- Less cramped. The home keys have an extra column of keys between them, making
  good typing posture a bit easier to maintain. It is also designed for the
  right hand to angle outward so you can keep your hands centered in front of
  you.
- Non-character keys are in a single contiguous region, with the Backspace no
  longer taking your hand off of the home keys.
- The home row isn't everything. Following the Workman philosophy, the keys
  below the index fingers and the the keys above the ring and middle fingers are
  given preference over lateral movements.
- Easier on those poor pinkies:
  - Shift and the other mode keys latch on the first press and lock on the
    second press. No need to hold them down.
  - Left Ctrl is on the home row. No more pinky gymnastics.
  - Fewer responsibilities for the right pinky now that it's closer to the edge.
- Numerals are sorted and mostly relegated to a single hand, with general
  programming symbols on the other hand.
- Logical, symmetrical punctuation groupings. I find that being able to mentally
  reason about where things are helps with speed. There is also a good
  compromise between punctuation for human and computer languages, as no
  programmers use their keyboards exclusively for programming.
  - Colons and semicolons are just the shifted versions of their undotted
    counterparts. Similarly, backslash is the shifted version of its reflection,
    plus is a shifted minus, and exclamation point is a shifted question mark.
  - Underscore no longer requires shift key, so anyone trying to type out
    snake_case—­or UPPER_SNAKE_CASE with the CapsLock—can breath a sigh of relief.
  - Oft-shifted symbol pairs are grouped together. Comparators are in a handy
    triangle for easy <= >= <=> =>. Other nearby bigraphs are += != |= &= *=. ->
    -= ?= are also close, but require alternating shifts. ~:./ are kept close as
    well for filepaths and URLs.
- Some Ctrl shortcuts are meant to be kept to the left corners, so QWXZ are
  (essentially) back to their original slots. And with Left Ctrl moved to Caps
  Lock, these are even easier. Copy and paste can be accomplished easily with
  Sys-Ctrl-0 and Sys-Shift-0 respectively (Win-Caps-~ and Win-Shift-~ on QWERTY
  or Dvorak).
- For Vim users:
  - Z, Q and Shift are near each other for easy exiting with ZZ and ZQ
  - HJKL are on one hand, with K above J
  - Word navigation keys WEB are on one hand
  - Common ex commands :q :w :e :x are on one hand
  - ^ and $ are now easy-to-find neighbors, and the former shares a key with the
    similar movement 0
  - C-U and C-D are on the same hand and U is above D
  - Delete and yank are neighbors

The Layout
----------

### Base Layer

Sporak has four layers (eight, counting the shift layer for each of these),
which are accessed with the mode keys: Shift, System, Symbol, and Reverse in one
of three ways.
- Holding the mode key(s) while hitting the desired key(s)
- Hitting the mode key(s) and then one key from the desired layer. (Latching)
- Hitting the mode key(s) twice, then hitting the desired keys followed by the
  mode key(s) a third time to return to the base layer. (Locking)

Caps Lock, which has been moved to the Num Lock key, works similarly to pressing
Shift twice, but only shifts the numpad keys and alphabetic keys on the base layer.
Escape will automatically drop back to the base layer and cancel any locks
(Vim-users needn't fear being in normal mode with Caps Lock on anymore). Caps
and Shift lock also get canceled when Space or Enter are pressed.

```
┌───┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬───┐ ┌──┬──┬──┬──┐
│0^ │1$│2#│3@│4`│5~│6%│7*│8&│9|│?!│-+│[<│]> │ │ │/\│*x│-~│
├───┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬──┤ ├──┼──┼──┼──┤
│   │qQ│wW│uU│pP│.:│/\│,;│gG│cC│rR│kK│_=│⌫ │ │7^│8|│9&│  │
├────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴──┤ ├──┼──┼──┤+:│
│Ctrl │aA│oO│eE│iI│bB│'"│mM│hH│tT│nN│sS│   │ │4D│5E│6F│  │
├─────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴────┤ ├──┼──┼──┼──┤
│  ⇪   │zZ│xX│dD│yY│({│)}│fF│lL│jJ│vV│   ⇪  │ │1A│2B│3C│  │
├───┬──┴─┬┴──┴┬─┴──┴──┴──┴─┬┴──┴┬─┴─┬┴──┬───┤ ├──┴──┼──┤=│
│Rev│Sys │Alt │   Space    │Sym │Sys│Ctr│Rev│ │   0 │.,│  │
└───┴────┴────┴────────────┴────┴───┴───┴───┘ └─────┴──┴──┘
```

### System Layer
This layer lets you access the other parts of 100% keyboard without moving your
hands. Insert and Delete are in the top left corner; the F keys along the number
row; the arrow keys are in the traditional WASD location with Home, End, Page
Up, and Page Down adjacent; the numpad is replicated on the right hand;
Backspace changes keyboard layouts; and the rest are the punctuations from the
Base Layer (possibly in more convenient locations).

Shift-NumLock will also get you here.

```
┌───┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬───┐ ┌──┬──┬──┬──┐
│Ins│F1│F2│F3│F4│F5│F6│F7│F8│F9│F0│F1│F2│⎘ ⎗│ │ │/\│*x│-~│
├───┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬──┤ ├──┼──┼──┼──┤
│⌦   │↤ │↑ │↦ │↥ │;_│{}│/\│7^│8|│9&│-~│<>│⌫ │ │↤ │↑ │↦ │  │
├────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴──┤ ├──┼──┼──┤+:│
│Ctrl │← │↓ │→ │↧ │"'│()│*x│4D│5E│6F│+:│ = │ │← │↓ │→ │  │
├─────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴────┤ ├──┼──┼──┼──┤
│  ⇪   │$^│@#│~`│*%│!?│[]│.,│1A│2B│3C│   ⇪  │ │⌦⌫│ │↥ │  │
├───┬──┴─┬┴──┴┬─┴──┴──┴──┴─┬┴──┴┬─┴─┬┴──┬───┤ ├──┴──┼──┤=│
│Rev│Sys │Alt │          0 │Sym │Sys│Ctr│Rev│ │Space│↧ │  │
└───┴────┴────┴────────────┴────┴───┴───┴───┘ └─────┴──┴──┘
```

### Symbol Layer
This layer follows patterns from other two layers to add international
characters, mathematical, and formatting characters.
The numbers become their superscripts and subscripts (with the exception of
zero, which provides the degree symbol instead of superscript zero). The arrow
keys become real arrows and bullet points. The numpad becomes table borders and
math symbols. There are also variants on punctuations from other layers. The
rest are dead keys for combining with characters from the base layer.

To make fractions, make a superscript, then a solidus (the key under 7, shifted),
then the subscript. To make Greek letters, type the Greek dead key (the key
under 6, shifted) followed by the analogous Roman letter. Pretty much anything
that can't be produced here, can be made by hitting the compose key (the key
under 6, unshifted) followed by two other characters.

```
┌───┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬───┐ ┌──┬──┬──┬──┐
│°₀ │¹₁│²₂│³₃│⁴₄│⁵₅│⁶₆│⁷₇│⁸₈│⁹₉│¿¡│–—│≤«│≥» │ │ │÷⁄│× ││ │
├───┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬──┤ ├──┼──┼──┼──┤
│   │☜ │↑ │☞ │▪▫│àȁ│µ│÷⁄│┌ │┬ │┐ ││ │≠≈│⌫ │ │┌ │┬ │┐ │  │
├────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴──┤ ├──┼──┼──┤─±│
│Ctrl │← │↓ │→ │•◦│úű│“”│×·│├ │┼ │┤ │─±│   │ │├ │┼ │┤ │  │
├─────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴────┤ ├──┼──┼──┼──┤
│  ⇪   │äă│âǎ│ȧå│āã│çą│ạș│…✓│└ │┴ │┘ │   ⇪  │ │└ │┴ │┘ │  │
├───┬──┴─┬┴──┴┬─┴──┴──┴──┴─┬┴──┴┬─┴─┬┴──┬───┤ ├──┴──┼──┤≠≈│
│Rev│Sys │Alt │     ∅ nbsp │Sym │Sys│Ctr│Rev│ │   ∅ │  │  │
└───┴────┴────┴────────────┴────┴───┴───┴───┘ └─────┴──┴──┘
```

### Reverse Layer
This makes one-handed typing easier. You can access it with a combination of Sys
and Sym, but the former location of the Ctrl keys is very easy to hit with the
side of the palm, so those were added as shortcuts.

Note that the top row can't be mirrored symmetrically, so Escape is added after
Tab, and the _= key is spread between Backspace and Enter.

```
┌───┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬───┐
│[< │]>│-+│?!│9|│8&│7*│6%│5~│4`│3@│2#│1$│0^ │
├───┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬──┤
│ ⌫= │kK│rR│cC│gG│,;│/\│.:│pP│uU│wW│qQ│ │Es│
├────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴──┤
│  _ │sS│nN│tT│hH│mM│'"│bB│iI│eE│oO│aA│Ctrl│
├─────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴────┤
│  ⇪   │vV│jJ│lL│fF│({│)}│yY│dD│zZ│xX│   ⇪  │
├───┬──┴─┬┴──┴┬─┴──┴──┴──┴─┬┴──┴┬─┴─┬┴──┬───┤
│Rev│Sys │Alt │   Space    │Sym │Sys│Ctr│Rev│
└───┴────┴────┴────────────┴────┴───┴───┴───┘
```

### The Great Letter Migration

For the curious, here's a breakdown of the alphabetic changes and the rationale
for moving them.

The following are the letters that changed from Dvorak. Note that few changes
were made to the home keys and top row, so current Dvorak typists won't be
slowed down too much initially.

```
┌───┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬───┐
│   │  │  │  │  │  │  │  │  │  │  │  │  │   │
├───┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬──┤
│    │qQ│wW│uU│  │  │  │  │  │  │  │kK│  │  │
├────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴──┤
│     │  │  │  │iI│bB│  │mM│  │  │  │  │    │
├─────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴────┤
│      │xX│zZ│dD│yY│  │  │fF│lL│jJ│  │      │
├───┬──┴─┬┴──┴┬─┴──┴──┴──┴─┬┴──┴┬─┴─┬┴──┬───┤
│   │    │    │            │    │   │   │   │
└───┴────┴────┴────────────┴────┴───┴───┴───┘
```

Since one of our objectives is to move the punctuation out of the alphabetic
areas, let's start by replacing the period with U. U needs to stay with the other vowels,
but it comes somewhere in the middle of all the letter rankings, so we can't
justify having it on the home keys.

Replacing U is a no-brainer. I is the fourth most common vowel and it gets to stay
on the same finger. With this change, the eight most frequent letters are on the
eight home keys. This also breaks up the UP same-finger bigram (SFB).

B, being fairly low frequency, comes in to take a spot which is central and
accessible, but put the hands in an odd position due to lateral stretching.
Note that this does create some new SFBs with I.

Replacing B on the other side is F, which was previously in a harder to reach
location.

F's former spot is perfect for a common punctuation. Sounds like the comma to
me.

The comma was in a pretty nice spot on Dvorak. The ring finger isn't the
strongest finger, but it's pretty good at stretching to this spot. Let's put W,
which is a medium frequency letter, here. This has the benefit of adding
what I call a mirror bigram with R. These being in the same spot on opposite
hands make it mentally easy to type them in quick succession.  This also evens
out the workload of the hands and fingers somewhat, and takes it out of an
unsuitable spot, but at the same time, it adds an SFB with O.

This spot is pretty undesirable, so in goes the 3rd least common letter: J

J used to have a really nice spot. The index finger curls there pretty
naturally. We'll put D here, which is pretty common but has a relatively
infrequent SFBs with I. This is a common problem with moving frequent consonants
to the vowel side, which I suspect is why Dvorak avoided it. Now words like
"did" and "bidding" are slower, but I believe these compromises are justifiable.

M gets demoted to D's former lateral position. This has the benefit of adding
what a mirror bigram with B, but it's mostly to make room for a more common letter.

That letter is the former destroyer of pinkies: L. Way too common for its former
position and long bemoaned for making `ls -l` too unweildy. This adds a mirror
bigram with D.

We need an uncommon letter for the pinky stretch, and K does quite nicely. This
forms a nice roll for the CK and RK bigrams.

In comes Y, which is more common than K. This move is basically identical to the
one F made, so that this character needs slightly less stretching than before,
and the mirror bigram between the two letters is retained. Plus, we get a near
mirror with LY.

We'll put the period there and the journey is complete. But we still need to
fill out the left corners.

Q was in an okay spot, but now that the U is on the same finger on the opposite
row, we have a problem. We'll put it back to it's original QWERTY position for a
nice QU finger roll.

Z and X, being uncommon, fit great in their original QWERTY positions, but
swapped to avoid the more common EX bigram.

This leaves us two symmetrical alphabetic typing areas with the following
rankings (1 being the most common and 26 being the rarest letters in English
usage):

```
┌───┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬──┬───┐
│   │  │  │  │  │  │  │  │  │  │  │  │  │   │
├───┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬──┤
│    │25│14│12│19│  │  │  │18│13│ 9│22│  │  │
├────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴──┤
│     │ 3│ 4│ 1│ 5│20│  │15│ 8│ 2│ 6│ 7│    │
├─────┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴┬─┴────┤
│      │23│26│10│17│  │  │16│11│24│21│      │
├───┬──┴─┬┴──┴┬─┴──┴──┴──┴─┬┴──┴┬─┴─┬┴──┬───┤
│   │    │    │            │    │   │   │   │
└───┴────┴────┴────────────┴────┴───┴───┴───┘
```

Installation
------------

For the console (not as full-featured):
```sh
sudo loadkeys sporak.map
```

For X11:
```sh
sudo cp sporak /usr/share/X11/xkb/symbols
setxkbmap sporak
```

I also recommend the following xcape bindings, if you have it:
```sh
xcape -t 200 -e Control_L=Escape
xcape -t 200 -e Control_R=Caps_Lock
xcape -t 200 -e Alt_L=BackSpace
```
