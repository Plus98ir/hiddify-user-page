<h1 align="center">Hiddify user page</h1>

<p align="center"><a href="https://hits.sh/github.com/Plus98ir/hiddify-user-page/"><img src="https://hits.sh/github.com/Plus98ir/hiddify-user-page.svg?style=for-the-badge&label=views&color=2563eb" alt="Views"></a> <a href="https://corenetbase.com/#support"><img src="https://img.shields.io/badge/support-buy%20me%20a%20coffee-e11d2a?style=for-the-badge&logo=buymeacoffee&logoColor=white" alt="Support"></a></p>

<details>
<summary><b>☕ Support · حمایت</b> — USDT (TRC20) / TRX</summary>
<br>
<p align="center"><img src="https://raw.githubusercontent.com/Plus98ir/.github/main/tron-qr.png" width="200" alt="TRON address QR"></p>

```
TA53aFyGNfSAcrCaJi9QmA9x5W47nPJcf7
```

> [!WARNING]
> **TRON network only.** Sending from ERC20 / BEP20 will lose the funds.<br>
> **فقط شبکه‌ی TRON.** ارسال از ERC20 یا BEP20 پول را از بین می‌برد.

</details>

<div align="center">

[<img src="https://flagcdn.com/w40/us.png" width="20" alt=""> &nbsp;**English**](README.md) &nbsp;&nbsp;|&nbsp;&nbsp; [<img src="https://flagcdn.com/w40/ir.png" width="20" alt=""> &nbsp;**فارسی**](README.fa.md)

</div>

A one-file user page for [Hiddify Manager](https://github.com/hiddify/hiddify-manager) panels: the subscription at a
glance, the link and QR code, apps per platform, and the configs grouped by kind (direct, CDN, REALITY, QUIC/UDP,
other) and by server, in English and Persian, light and dark.

No build step: `index.html`, three font files and a QR library.

| Desktop (Persian, light) | Phone (Persian, dark) |
| --- | --- |
| ![desktop](screenshots/userpage_desk_light_fa.png) | ![phone](screenshots/userpage_phone_dark_fa.png) |

English, dark: [screenshot](screenshots/userpage_desk_dark_en.png)

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
