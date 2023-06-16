# Emily's Modifier Dictionary 

## Design

This dictionary was created with the following goals in mind:

- Have a consistent method to type (pretty much) every shortcut 
- Do it all in only one stroke
- Hackable and understandable to anyone who finds it useful :)

## Section

To achieve this, for each stroke there are 4 main sections:
1. Character (Purple)
2. Switcher (Orange)
3. Modifiers (Green)
4. Unique ending (Red)

![Coloured Layout Diagram](img/layout.png)

### Unique Ending

Due to fingerspelling existing on the left hand, a unique chord with the right hand must be stroked.
This stroke is used to uniquely identify a dictionary entry chord from any other chord.
By default this is `-LTZ`, this should be stroked with pinky on the `-Z` and ring finger for `-LT`.
Due to physical and practical limitations, this key combination is both difficult to press, and also will generate clashes. 
Please check with your dictionary to see what clashes may occur, and potentially change what this stroke is.
With Magnum as I currently use it, the `-LTZ` stroke clashes with only 71 entries, most of which are misstroke entries, so I don't have to worry about it too much. 

![Ender Keys Layout Diagram](img/ender.png)

### Modifiers 

`FRPB` are used to specify the modifier keys to be used against the selected character. 
These can all be used in any variation to produced the desired shortcut.  

| modifier pattern                            | modifier  |
|---------------------------------------------|-----------|
| ![Control Pattern Diagram](img/control.png) | `control` |
| ![Shift Pattern Diagram](img/shift.png)     | `shift`   |
| ![super Pattern Diagram](img/super.png)     | `super`   |
| ![Alt Pattern Diagram](img/alt.png)         | `alt`     |


### Character

Character input is based on fingerspelling and takes up the whole left hand and vowels.
Valid fingerspelling entries contain methods from multiple steno theories, hence why there are duplicate entries for some.

| fingerspelling pattern                | letter  |
|---------------------------------------|---------|
| ![Letter A Diagram](img/a.png)        | `A`     |
| ![Letter B Diagram](img/b.png)        | `B`     |
| ![Letter C Diagram](img/c.png)        | `C`     |
| ![Letter D Diagram](img/d.png)        | `D`     |
| ![Letter E Diagram](img/e.png)        | `E`     |
| ![Letter F Diagram](img/f.png)        | `F`     |
| ![Letter G Diagram](img/g.png)        | `G`     |
| ![Letter H Diagram](img/h.png)        | `H`     |
| ![Letter I Diagram](img/i.png)        | `I`     |
| ![Letter I Diagram](img/i-p.png)      | `I`     |
| ![Letter J Diagram](img/j.png)        | `J`     |
| ![Letter J Diagram](img/j-p.png)      | `J`     |
| ![Letter K Diagram](img/k.png)        | `K`     |
| ![Letter L Diagram](img/l.png)        | `L`     |
| ![Letter M Diagram](img/m.png)        | `M`     |
| ![Letter N Diagram](img/n.png)        | `N`     |
| ![Letter O Diagram](img/o.png)        | `O`     |
| ![Letter P Diagram](img/p.png)        | `P`     |
| ![Letter Q Diagram](img/q.png)        | `Q`     |
| ![Letter R Diagram](img/r.png)        | `R`     |
| ![Letter S Diagram](img/s.png)        | `S`     |
| ![Letter T Diagram](img/t.png)        | `T`     |
| ![Letter U Diagram](img/u.png)        | `U`     |
| ![Letter V Diagram](img/v.png)        | `V`     |
| ![Letter W Diagram](img/w.png)        | `W`     |
| ![Letter X Diagram](img/x.png)        | `X`     |
| ![Letter Y Diagram](img/y.png)        | `Y`     |
| ![Letter Z Diagram](img/z.png)        | `Z`     |
| ![Letter Z Diagram](img/z-p.png)      | `Z`     |

When `AO` is held, as that's not valid fingerspelling, the bottom row of the left hand (`SKWR`) will turn into binary number input from 0 to 9.

| binary number pattern                 | number  |
|---------------------------------------|---------|
| ![Number 0 Diagram](img/0.png)        | `0`     |
| ![Number 1 Diagram](img/1.png)        | `1`     |
| ![Number 2 Diagram](img/2.png)        | `2`     |
| ![Number 3 Diagram](img/3.png)        | `3`     |
| ![Number 4 Diagram](img/4.png)        | `4`     |
| ![Number 5 Diagram](img/5.png)        | `5`     |
| ![Number 6 Diagram](img/6.png)        | `6`     |
| ![Number 7 Diagram](img/7.png)        | `7`     |
| ![Number 8 Diagram](img/8.png)        | `8`     |
| ![Number 9 Diagram](img/9.png)        | `9`     |

If `TP` (`F`) is also held, the number input will specify function number keys.

| binary function number pattern | function |
|--------------------------------|----------|
| ![F1 Diagram](img/F1.png)      | `F1`     |
| ![F2 Diagram](img/F2.png)      | `F2`     |
| ![F3 Diagram](img/F3.png)      | `F3`     |
| ![F4 Diagram](img/F4.png)      | `F4`     |
| ![F5 Diagram](img/F5.png)      | `F5`     |
| ![F6 Diagram](img/F6.png)      | `F6`     |
| ![F7 Diagram](img/F7.png)      | `F7`     |
| ![F8 Diagram](img/F8.png)      | `F8`     |
| ![F9 Diagram](img/F9.png)      | `F9`     |
| ![F10 Diagram](img/F10.png)    | `F10`    |
| ![F11 Diagram](img/F11.png)    | `F11`    |
| ![F12 Diagram](img/F12.png)    | `F12`    |

### Switcher

When `*` is used, the left bank will switch from fingerspelling letters, to a reflected and modified symbol dictionary. 
This will allow you to apply modifiers to symbols.
However, please note:
> Due to the way plover can operate and the way computers receive shortcut keys, when specifying a symbol, you only specify the key it is mapped to in the current keymap. This means that if the symbol is under shift, then you still need to use the shift modifier. For example, `control+shift+1` is not the same as `control+!`, you still need to add in the `shift` modifier.

Additionally, while using the switcher for symbol specification, the `A` and `O` keys are used to specify variants of a particular symbol, similar to the emily-symbols dictionary.`A` represents adding 1, while `O` represents adding 2 to the entries below.

 | symbol pattern                                 | output | name |
 |------------------------------------------------|--------|------|
 | ![tab Pattern Diagram](img/s-tab.png)          | `tab`, `backspace`, `delete`, `escape` | `tab`, `backspace`, `delete`, `escape` |
 | ![arrow Pattern Diagram](img/s-arrow.png) | `up`, `left`, `right`, `down` | `up`, `left`, `right`, `down` |
 | ![page Pattern Diagram](img/s-page.png) | `pageup`, `home`, `end`, `pagedown` | `pageup`, `home`, `end`, `pagedown` |
 | ![blank Pattern Diagram](img/s-blank.png) | `escape`, `tab`, `return`, ` ` | `escape`, `tab`, `return`, `space` |
 | ![exclam Pattern Diagram](img/s-exclam.png) | `!`, , `¬`, `¡` | `exclam`, , `notsign`, `exclamdown` |
 | ![quotedbl Pattern Diagram](img/s-quotedbl.png) | `"`, , ,  | `quotedbl`, , ,  |
 | ![numbersign Pattern Diagram](img/s-numbersign.png) | `#`, `®`, `©`,  | `numbersign`, `registered`, `copyright`,  |
 | ![dollar Pattern Diagram](img/s-dollar.png) | `$`, `€`, `¥`, `£` | `dollar`, `euro`, `yen`, `sterling` |
 | ![percent Pattern Diagram](img/s-percent.png) | `%`, , ,  | `percent`, , ,  |
 | ![apostrophe Pattern Diagram](img/s-apostrophe.png) | `'`, , , | `apostrophe`, , , |
 | ![ampersand Pattern Diagram](img/s-ampersand.png) | `&`, , ,  | `ampersand`, , ,  |
 | ![parenleft Pattern Diagram](img/s-parenleft.png) | `(`, `<`, `[`, `{` | `parenleft`, `less`, `bracketleft`, `braceleft` |
 | ![parenright Pattern Diagram](img/s-parenright.png) | `)`, `>`, `]`, `}` | `parenright`, `greater`, `bracketright`, `braceright` |
 | ![asterisk Pattern Diagram](img/s-asterisk.png) | `*`, `§`, , `×` | `asterisk`, `section`, , `multiply` |
 | ![plus Pattern Diagram](img/s-plus.png) | `+`, `¶`, , `±` | `plus`, `paragraph`, , `plusminus` |
 | ![comma Pattern Diagram](img/s-comma.png) | `,`, , ,  | `comma`, , ,  |
 | ![minus Pattern Diagram](img/s-minus.png) | `-`, , ,  | `minus`, , ,  |
 | ![period Pattern Diagram](img/s-period.png) | `.`, `·`, ,  | `period`, `periodcentered`, ,  |
 | ![slash Pattern Diagram](img/s-slash.png) | `/`, , , `÷` | `slash`, , , `division` |
 | ![colon Pattern Diagram](img/s-colon.png) | `:`, , ,  | `colon`, , ,  |
 | ![semicolon Pattern Diagram](img/s-semicolon.png) | `;`, , ,  | `semicolon`, , ,  |
 | ![equal Pattern Diagram](img/s-equal.png) | `=`, , ,  | `equal`, , ,  |
 | ![question Pattern Diagram](img/s-question.png) | `?`, , `¿`,  | `question`, , `questiondown`,  |
 | ![at Pattern Diagram](img/s-at.png) | `@`, , ,  | `at`, , ,  |
 | ![backslash Pattern Diagram](img/s-backslash.png) | `\`, , ,  | `backslash`, , ,  |
 | ![asciicircum Pattern Diagram](img/s-asciicircum.png) | `^`, `«`, `»`, `°` | `asciicircum`, `guillemotleft`, `guillemotright`, `degree` |
 | ![grave Pattern Diagram](img/s-grave.png) |  `` ` ``, , ,  | `grave`, , ,  |
 | ![bar Pattern Diagram](img/s-bar.png) | `|`, , , `¦` | `bar`, , , `brokenbar` |
 | ![asciitilde Pattern Diagram](img/s-asciitilde.png) | `~`, , ,  | `asciitilde`, , ,  |

## A few favourites

This is a list of a few shortcuts I use often so you can see how it all comes together. :)
| Chord | Use |
|-------|-----|
| ![spotlight Pattern Diagram](img/spotlight.png) | press `cmd+space` to activate spotlight search on my mac |
| ![workspace Pattern Diagram](img/workspace-right.png) | press `control+right` to move over a desktop on my mac |
| ![sigint Pattern Diagram](img/sigint.png) | press `control+c` to interrupt a running program when programming |
| ![sigquit Pattern Diagram](img/sigquit.png) | press `control+\` to stop a running program when programming |

## Poster

Check out the summary poster made by @sammdot for a nice one-page overview of how the whole dictionary works!
[emily-modifiers-poster](emily-modifiers-poster.pdf)
