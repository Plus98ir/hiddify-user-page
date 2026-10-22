# Hiddify user page

A one-file user page for [Hiddify Manager](https://github.com/hiddify/hiddify-manager) panels: the subscription at a
glance, the link and QR code, apps per platform, and the configs grouped by kind (direct, CDN, REALITY, QUIC/UDP,
other) and by server, in English and Persian, light and dark.

No build step: `index.html`, two fonts and a QR library.

## Use it

In the panel: **Settings › Customizing User Page › User page URL**:

    https://github.com/Plus98ir/hiddify-user-page/tree/main

The panel downloads the files itself and serves them on each user's own link, so users never connect to GitHub.
Needs a panel with the custom user page setting (hiddify/HiddifyPanel#79).

To change it, fork this repository, edit `index.html` and put your fork's link in the setting.

## How it works

The panel puts `window.__HIDDIFY__` first in `<head>` (see "Custom user page" in
[hiddify-user-front](https://github.com/hiddify/hiddify-user-front)). The page uses:

- `api_base`: the user API (`me/`, `all-configs/`, `apps/`, `mtproxies/`, `short/`);
- `profile_url` and `deep_link`: the subscription link, its QR code and the Hiddify app button;
- `lang`, `brand_title`, `version`, `page_base`, `proxy_path`, `static_base`.

Opened anywhere else, it only says that it is meant to be shown by a panel.

## Licenses

- Vazir font: SIL Open Font License 1.1, by Saber Rastikerdar.
- `js/qrcode.js`: MIT, by davidshimjs (QRCode.js).
