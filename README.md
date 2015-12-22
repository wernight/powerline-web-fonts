# powerline-web-fonts

[Powerline Web Fonts](https://github.com/powerline/fonts) working in [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo)
working also on Chromebook (or pretty much anything running Chrome).
   
There are other fonts as well for you to choose from:

  * Anonymice Powerline
  * Inconsolata for Powerline
  * Literation Mono Powerline
  * PT Mono for Powerline
  * Sauce Code Powerline Regular
  * Sauce Code Powerline Regular
  * Ubuntu Mono derivative Powerline
  
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
