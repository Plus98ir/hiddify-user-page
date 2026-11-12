<h1 align="center">Hiddify user page</h1>

<p align="center"><a href="https://hits.sh/github.com/Plus98ir/hiddify-user-page/"><img src="https://hits.sh/github.com/Plus98ir/hiddify-user-page.svg?style=for-the-badge&label=views&color=2563eb" alt="Views"></a> <a href="https://corenetbase.com/#support"><img src="https://img.shields.io/badge/support-buy%20me%20a%20coffee-e11d2a?style=for-the-badge&logo=buymeacoffee&logoColor=white" alt="Support"></a></p>

<div align="center">

[<img src="https://flagcdn.com/w40/us.png" width="20" alt=""> &nbsp;**English**](README.md) &nbsp;&nbsp;|&nbsp;&nbsp; [<img src="https://flagcdn.com/w40/ir.png" width="20" alt=""> &nbsp;**فارسی**](README.fa.md)

</div>

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

<div dir="rtl">

یک صفحه‌ی کاربر تک‌فایلی برای پنل‌های [Hiddify Manager](https://github.com/hiddify/hiddify-manager): خلاصه‌ی اشتراک در یک نگاه، لینک و QR کد، برنامه‌ها برای هر سیستم‌عامل، و کانفیگ‌ها دسته‌بندی‌شده بر اساس نوع (مستقیم، CDN، REALITY، QUIC/UDP، بقیه) و بر اساس سرور؛ فارسی و انگلیسی، روشن و تیره.

بدون مرحله‌ی build: یک `index.html`، سه فایل فونت و یک کتابخانه‌ی QR.

| دسکتاپ (فارسی، روشن) | گوشی (فارسی، تیره) |
| --- | --- |
| ![desktop](screenshots/userpage_desk_light_fa.png) | ![phone](screenshots/userpage_phone_dark_fa.png) |

انگلیسی، تیره: [تصویر](screenshots/userpage_desk_dark_en.png)

## استفاده

در پنل: **Settings › Customizing User Page › User page URL**:

</div>

    https://github.com/Plus98ir/hiddify-user-page/tree/main

<div dir="rtl">

پنل خودش فایل‌ها را دانلود می‌کند و روی لینک اختصاصی هر کاربر نشان می‌دهد، پس کاربرها هیچ‌وقت به GitHub وصل نمی‌شوند.
پنلی لازم است که تنظیم صفحه‌ی کاربر سفارشی را داشته باشد (hiddify/HiddifyPanel#79).

برای تغییر دادن، این مخزن را fork کنید، `index.html` را ویرایش کنید و لینک fork خودتان را در همان تنظیم بگذارید.

## چطور کار می‌کند

پنل `window.__HIDDIFY__` را اول `<head>` می‌گذارد (بخش «Custom user page» در [hiddify-user-front](https://github.com/hiddify/hiddify-user-front) را ببینید). صفحه از این‌ها استفاده می‌کند:

- `api_base`: API کاربر (`me/`، `all-configs/`، `apps/`، `mtproxies/`، `short/`)؛
- `profile_url` و `deep_link`: لینک اشتراک، QR کد آن و دکمه‌ی برنامه‌ی Hiddify؛
- `lang`، `brand_title`، `version`، `page_base`، `proxy_path`، `static_base`.

اگر جای دیگری باز شود، فقط می‌گوید که باید از طریق پنل نمایش داده شود.

## مجوزها

- فونت وزیر: SIL Open Font License 1.1، اثر صابر راستی‌کردار.
- `js/qrcode.js`: MIT، اثر davidshimjs (QRCode.js).

</div>
