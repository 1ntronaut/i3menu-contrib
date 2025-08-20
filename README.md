# i3menu-contrib
i3menu-compatible wrapper scripts

Hosted mostly for example purposes.

- Download and install [i3menu](https://github.com/budlabs/i3menu)
- REQUIRES this [fork of dmenu](https://github.com/budRich/dmenu)


#### [`i3menu_run`](https://github.com/1ntronaut/i3menu-contrib/blob/main/i3menu_run)
dmenu_run drop-in replacement oneliner script

#### [`i3menufyra'](https://github.com/1ntronaut/i3menu-contrib/blob/main/i3menufyra)
apply and/or redo i3fyra layouts via menu.

requires:
- [i3wm](https://www.i3wm.org)
- [i3fyra](https://github.com/budlabs/i3ass/wiki/i3fyra)
- i3menu
  - dmenu-bud
optional:
- notify-send (or dunstify)

optional config:
> ~/.config/i3/config
```
## launch i3menufyra script
bindsym $mod+p       exec --no-startup-id i3menufyra
## restore/redo/switch between the previous and current i3fyra layout
bindsym $mod+Shift+p exec --no-startup-id i3fyra --layout redo ; exec --no-startup-id notify-send "i3fyra" "i3fyra --layout redo" 
```

#### [`i3menuunicode`](https://github.com/1ntronaut/i3menu-contrib/blob/main/i3menuunicode)
i3menu-compatible rewrite of [dmenuunicode](https://gitlab.com/LukeSmithxyz/voidrice/blob/master/.local/bin/dmenuunicode) (previously: dmenumoji), uses [this file](https://github.com/1ntronaut/i3menu-contrib/blob/main/.local/share/emoji) ( obtained via (https://gitlab.com/LukeSmithxyz/voidrice/-/raw/master/.local/share/larbs/chars/emoji) ) for it's content.

requires:
- i3menu
  - dmenu-bud
- font containing emoji glyphs Noto Color Emoji
- xdotool
- xclip
- notify-send (or dunstify)

- uses custom i3menu theme file '[emoji](https://github.com/1ntronaut/i3menu-contrib/blob/main/.config/i3menu/emoji)'

Make sure to use a font containing the necessary glyphs/unicode references for emoji support. I like using [Unifont](https://unifoundry.com/unifont/) for a monotone look, but (installed system-wide) Noto Color Emoji font is (automatically) used as fallback for any emoji glyphs that the Unifont font doesn't cover.

optional config:
> ~/.config/i3/config
```
bindsym $mod+shift+quotedbl      exec --no-startup-id i3menuunicode
```

#### [`i3menunf`](https://github.com/1ntronaut/i3menu-contrib/blob/main/i3menunf)

i3menu wrapper script showing all [Nerd Font](https://www.nerdfonts.com/) symbols, allowing for writing selected icon to clipboard. Uses [this file](https://raw.githubusercontent.com/1ntronaut/i3menu-contrib/refs/heads/main/nf-cheatsheet) for listing the Nerd Font icons. The nf-cheatsheet file was, in turn, generated using [this script](https://github.com/ryanoasis/nerd-fonts/blob/master/bin/scripts/lib/i_all.sh) from the [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) repo.

requires:
- i3menu
  - dmenu-bud
- any Nerd Font
- xdotool
- xclip
- notify-send (or dunstify)

- uses custom i3menu theme file [nf](https://github.com/1ntronaut/i3menu-contrib/blob/main/.config/i3menu/nf); edit that file to change the font to any Nerd Font of your liking.

optional config:
> ~/.config/i3/config
```
bindsym $mod+apostrophe          exec --no-startup-id i3menunf
```
