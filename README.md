# firefox
My personal firefox setup.

Drastic changes include forcing webpages and browser UI to use `Iosevka Nerd Font` as the primary font as well as forcing all CSS rounded corners to 0.

A coherent theme - based on dark-blue/purple - is used for both browser UI and homepage. 

## Installing

1. Homepage Setup
```console
git clone https://github.com/cococry/firefox
cd firefox
mkdir -p .config/firefox-custom
cp homepage/index.html ~/.config/firefox-custom
```

2. Go to `about:profile` in firefox, select your profile folder and paste the [`chrome`](https://github.com/cococry/firefox/blob/main/chrome) folder into your profile folder.

3. install [New Tab Override](https://addons.mozilla.org/en-US/firefox/addon/new-tab-override/) and use `http://localhost:4242/`
as the page to load on new-tab.

4. Open your Firefox settings and search for "Home and startup" and select "Custom URLs..." for your 
Home page, then paste `http://localhost:4242/` as the site to use as your Home page.

5. Add the following line to your startup script for your DE/WM:

```console
cd ~/.config/firefox-custom && python3 -m http.server 4242 >/dev/null 2>&1 &
```

6. Restart firefox
```console
pkill firefox
firefox
```

## Screenshots

<p align="left">
  <img src="https://github.com/cococry/firefox/blob/main/firefox.png"alt="firefox screenshot">
</p>
