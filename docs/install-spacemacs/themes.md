# Themes

++spc++ ++t++ ++"s"++ opens a helm selection menu to select from all available themes

You can select a different theme or cycle through the currently added themes.

| Spacemacs                                       | Description                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------|
| ++spc++ ++t++ ++"n"++                           | Next theme in list                                                       |
| ++spc++ ++t++ ++"p"++                           | Previous theme in list                                                   |
| ++spc++ ++t++ ++"s"++                           | Select theme from list (all themes from gallery)                         |
| ++spc++ ++t++ ++"s"++ ++ctrl+"c"++ ++ctrl+"f"++ | Apply themes when scrolling through the list of names (helm-follow-mode) |

![Spacemacs Themes menu](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/spacemacs/screenshots/spacemacs-themes-menu.png)


## Adding Themes to Spacemacs

Themes are set by adding the theme name to the `dotspacemacs-themes` list.  The first theme in the list is loaded when Spacemacs starts.

```emacs
dotspacemacs-themes '(doom-gruvbox-light
                      doom-gruvbox
                      spacemacs-dark
                      spacemacs-light
                      cyberpunk)
```

The order of the themes in the list is the order Spacemacs will cycle through those themes, `SPC T n` for the next theme and `SPC T p` for the previous theme.

The first time you select a theme it will be automatically downloaded, installed and used.  This may take a few seconds to load.

!!! HINT "Doom Gruvbox Themes used for this guide"
    This guide uses the `doom-gruvbox-light` theme for screenshots and videos, some older screenshots are `doom-solarized-light` or `spacemacs-dark`.


## Example themes

There are many [themes available](http://themegallery.robdor.com/){target=_blank} for Spacemacs that will change the colours of text, background, etc.

??? HINT "Original Emacs theme"
    Add `(disable-theme)` to `dotspacemacs/user-config` section of `.spacemacs` to remove any custom theme and use the Emacs default colors.  Or set `(dotspacemacs-themes '(default))` in `.spacemacs` to use a theme similar to the Emacs colors.


This guide uses the minimal theme provided by doom modeline and doom-gruvbox-light theme.

![Spacemacs theme - doom solarized light](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/spacemacs/screenshots/spacemacs-doom-gruvbox-light-theme-example-clojure-spec.png)


Doom Solarized Light is also an excellent theme for working during the day, as well as presentations and videos due to a lighter color set having a better contrast.

![Spacemacs theme - doom solarized light](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/spacemacs/screenshots/spacemacs-themes-doom-solarized-light.png)

Doom Solarized Dark is a good theme for darker environments.

![Spacemacs theme - doom solarized dark](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/spacemacs/screenshots/spacemacs-themes-doom-solarized-dark.png)


Spacemacs has two default themes included, one light and one dark.  There are also many [themes available](http://themegallery.robdor.com/){target=_blank} that you can select and load on demand, ++spc++ ++t++ ++"s"++

![Spacemacs theme - spacemacs-dark](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/spacemacs/screenshots/spacemacs-theme-dark.png)

![Spacemacs theme - spacemacs-light](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/spacemacs/screenshots/spacemacs-theme-light.png)


The cyberpunk theme used a very striking color palette, familiar to those who use to use Emacs Live distribution (now deceased).

![Spacemacs theme - spacemacs-cyberpunk](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/spacemacs/screenshots/spacemacs-theme-cyberpunk.png)
