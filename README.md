# powerline-web-fonts

[Powerline Web Fonts](https://github.com/powerline/fonts) working in [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo)
working also on Chromebook (or pretty much anything running Chrome).

There are other fonts as well for you to choose from:
  * `Anonymous Pro` - [Anonymice
    Powerline](https://github.com/powerline/fonts/tree/master/AnonymousPro)
  * `DejaVu Sans Mono` -
    [DejaVu Sans Mono for Powerline](https://github.com/powerline/fonts/tree/master/DejaVuSansMono)
  * `Inconsolata` - [Inconsolata for
    Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata)
  * `Inconsolata-g` - [Inconsolata-g for
    Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata-g)
  * `Liberation Mono` - [Literation Mono
    Powerline](https://github.com/powerline/fonts/tree/master/LiberationMono)
  * `PT Mono` - PT Mono for Powerline
  * `Source Code Pro` or `Source Code Pro for Powerline` - [Source Code for Powerline](https://github.com/powerline/fonts/tree/master/SourceCodePro)
  * `Ubuntu Mono` - [Ubuntu Mono derivative
    Powerline](https://github.com/powerline/fonts/tree/master/UbuntuMono)

See [preview in test/index.html](https://rawgit.com/wernight/powerline-web-fonts/master/test/index.html)
and [Slant](http://www.slant.co/topics/67/~programming-fonts) if you don't know which to choose.

## Usage example for [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo)

  - Options:
      - font-family: `"Source Code Pro for Powerline", monospace`
      - user-css: `http://rawgit.com/wernight/powerline-web-fonts/master/PowerlineFonts.css`

## Usage example for [Crosh Window](https://chrome.google.com/webstore/detail/crosh-window/nhbmpbdladcchdhkemlojfjdknjadhmh)

  - Start crosh window then press `Ctrl+Shift+J` and paste in the following:

```js
term_.prefs_.set('font-family', '"Source Code Pro for Powerline", monospace');
term_.prefs_.set('user-css', 'https://rawgit.com/wernight/powerline-web-fonts/master/PowerlineFonts.css');
```

If you have [Crouton](https://github.com/dnschneid/crouton) installed on a developer mode Chromebook,
or if you're pretty much on any other OS, you can install those fonts locally or copy them locally
and it'll work with little to not effort.

## Suggesting a new font

To add a new font, you can submit a GitHub pull request. Your PR should:

  - Include a new font file in [WOFF2
    format](https://gist.github.com/sergejmueller/cf6b4f2133bcb3e2f64a).
  - Add your font to `PowerlineFonts.css`, `test/test.html` and `README.md` (might use [Transfonter](http://transfonter.org/) to help with the CSS).

### Converting to WOFF2

There are various methods, including:

  * [otf to woff2 | Everything Fonts](https://everythingfonts.com/otf-to-woff2)
  * [ttf to woff2 | Everything Fonts](https://everythingfonts.com/ttf-to-woff2)
  * [Webfont Generator | Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator)
  * Using [FontForge](https://fontforge.github.io/en-US/):

        #!/usr/bin/env fontforge
        Open($1)
        Generate($1:r + ".woff2")`
