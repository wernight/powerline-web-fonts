# powerline-web-fonts

[**Powerline** Web Fonts](https://github.com/powerline/fonts) working in [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo) and working also on **Chromebook** (or pretty much anything running Chrome).

There are several `font-family` you can choose from (all Powerline-enabled):

  * `Anonymous Pro` - [Anonymice
    Powerline](https://github.com/powerline/fonts/tree/master/AnonymousPro)
  * `DejaVu Sans Mono` -
    [DejaVu Sans Mono for Powerline](https://github.com/powerline/fonts/tree/master/DejaVuSansMono)
  * `Hack` - [Hack Webfont](https://github.com/chrissimpkins/Hack)
  * `Inconsolata` - [Inconsolata for
    Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata)
  * `Inconsolata-g` - [Inconsolata-g for
    Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata-g)
  * `Iosevka` - [Iosevka Webfont](https://github.com/be5invis/Iosevka)
  * `Liberation Mono` - [Literation Mono
    Powerline](https://github.com/powerline/fonts/tree/master/LiberationMono)
  * `Monofur` - [monofur for
    Powerline](https://github.com/powerline/fonts/tree/master/Monofur)
  * `PT Mono` - PT Mono for Powerline
  * `Source Code Pro` - [Source Code for Powerline](https://github.com/powerline/fonts/tree/master/SourceCodePro)
  * `Ubuntu Mono` - [Ubuntu Mono derivative
    Powerline](https://github.com/powerline/fonts/tree/master/UbuntuMono)
  * `Monofur` - [Monofur for Powerline](https://github.com/powerline/fonts/tree/master/Monofur)
    

See [preview.html](https://rawgit.com/wernight/powerline-web-fonts/master/preview.html) and [Slant](http://www.slant.co/topics/67/~programming-fonts) if you don't know which to choose.

## Usage example

### Usage example for [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo)

  - Launch *Secure Shell* and click on **Options**
    (or go to `chrome-extension://pnhechapfaindjhompbnflcldabbghjo/html/nassh_preferences_editor.html`):
      - Set **font-family**: `"Source Code Pro", monospace`
      - Set **user-css**: `https://cdn.rawgit.com/wernight/powerline-web-fonts/e4d967ca4f95d9fa0cf1d51afed2e5a5927d759e/PowerlineFonts.css`

### Usage example for [Crosh Window](https://chrome.google.com/webstore/detail/crosh-window/nhbmpbdladcchdhkemlojfjdknjadhmh)

  - Start crosh window then press `Ctrl+Shift+J` and paste in the following:

```js
term_.prefs_.set('font-family', '"Source Code Pro", monospace');
term_.prefs_.set('user-css', 'https://cdn.rawgit.com/wernight/powerline-web-fonts/e4d967ca4f95d9fa0cf1d51afed2e5a5927d759e/PowerlineFonts.css');
```

If you have [Crouton](https://github.com/dnschneid/crouton) installed on a developer mode Chromebook,
or if you're on pretty much any other OS, you can install those fonts locally or copy them locally
and it'll work with little to no effort.

Note that the RawGit links require a specific commit SHA-1 because files are cached permanently. Please update your projects to use the `CDN` links, as [overusage of the development URLs (those without `cdn.`), could result in this repo being blacklisted from RawGit](https://github.com/rgrove/rawgit/wiki/Frequently-Asked-Questions).

## Suggesting a new font

To add a new font, you can submit a GitHub pull request through a forked repository. Your pull request should:

  - Include a new font file in [WOFF2 format](https://gist.github.com/sergejmueller/cf6b4f2133bcb3e2f64a).
  - Add your font to `PowerlineFonts.css`, `preview.html` and `README.md` (might use [Transfonter](http://transfonter.org/) to help with the CSS).
  - Once merged, send another pull request, I might forget, that updates all `https://cdn.rawgit.com/` in this README to the [latest commit SHA-1](https://github.com/wernight/powerline-web-fonts/commits/master). You can do that in the original Pull Request if it gets rebased (merge and sqashes would not work in that case).

### Converting to WOFF2

There are various methods, including:

  * [otf to woff2 | Everything Fonts](https://everythingfonts.com/otf-to-woff2)
  * [ttf to woff2 | Everything Fonts](https://everythingfonts.com/ttf-to-woff2)
  * [Webfont Generator | Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator)
  * Using [FontForge](https://fontforge.github.io/en-US/):
        
    ```bash
    #!/usr/bin/env fontforge
    Open($1)
    Generate($1:r + ".woff2")`
    ```
