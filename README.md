# powerline-web-fonts

[**Powerline** Web Fonts](https://github.com/powerline/fonts) working in [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo) and working also on **Chromebook** (or pretty much anything running Chrome).

There are multiple `font-family` to choose from (all Powerline-enabled):

  * `Anonymous Pro` - [Anonymice
    Powerline](https://github.com/powerline/fonts/tree/master/AnonymousPro)
  * `DejaVu Sans Mono` -
    [DejaVu Sans Mono for Powerline](https://github.com/powerline/fonts/tree/master/DejaVuSansMono)
  * `Hack` - [Hack Webfont](https://github.com/chrissimpkins/Hack)
  * `Inconsolata` - [Inconsolata for
    Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata)
  * `Inconsolata-g` - [Inconsolata-g for
    Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata-g)
  * `Liberation Mono` - [Literation Mono
    Powerline](https://github.com/powerline/fonts/tree/master/LiberationMono)
  * `PT Mono` - PT Mono for Powerline
  * `Source Code Pro` - [Source Code for Powerline](https://github.com/powerline/fonts/tree/master/SourceCodePro)
  * `Ubuntu Mono` - [Ubuntu Mono derivative
    Powerline](https://github.com/powerline/fonts/tree/master/UbuntuMono)

See [preview.html](https://rawgit.com/wernight/powerline-web-fonts/master/preview.html) and [Slant](http://www.slant.co/topics/67/~programming-fonts) if you don't know which to choose.

## Usage example

### Usage example for [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo)

  - Options:
      - font-family: `"Source Code Pro", monospace`
      - user-css: `https://cdn.rawgit.com/wernight/powerline-web-fonts/8040cf32c146c7cd4f776c1484d23dc40685c1bc/PowerlineFonts.css`

### Usage example for [Crosh Window](https://chrome.google.com/webstore/detail/crosh-window/nhbmpbdladcchdhkemlojfjdknjadhmh)

  - Start crosh window then press `Ctrl+Shift+J` and paste in the following:

```js
term_.prefs_.set('font-family', '"Source Code Pro", monospace');
term_.prefs_.set('user-css', 'https://cdn.rawgit.com/wernight/powerline-web-fonts/8040cf32c146c7cd4f776c1484d23dc40685c1bc/PowerlineFonts.css');
```

If you have [Crouton](https://github.com/dnschneid/crouton) installed on a developer mode Chromebook,
or if you're on pretty much any other OS, you can install those fonts locally or copy them locally
and it'll work with little to no effort.

Note that the RawGit links require a specific commit SHA-1 because files are cached permanently. Please update your projects to use the `CDN` links, as [overusage of the development URLs (those without `cdn.`), could result in this repo being blacklisted from RawGit](https://github.com/rgrove/rawgit/wiki/Frequently-Asked-Questions).

## Suggesting a new font

To add a new font, you can submit a GitHub pull request. Your PR should:

  - Include a new font file in [WOFF2
    format](https://gist.github.com/sergejmueller/cf6b4f2133bcb3e2f64a).
  - Add your font to `PowerlineFonts.css`, `preview.html` and `README.md` (might use [Transfonter](http://transfonter.org/) to help with the CSS).

### Converting to WOFF2

There are various methods, including:

  * [otf to woff2 | Everything Fonts](https://everythingfonts.com/otf-to-woff2)
  * [ttf to woff2 | Everything Fonts](https://everythingfonts.com/ttf-to-woff2)
  * [Webfont Generator | Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator)
  * Using [FontForge](https://fontforge.github.io/en-US/):

        #!/usr/bin/env fontforge
        Open($1)
        Generate($1:r + ".woff2")`
