# Hadi Rasouli — Personal Website

Personal portfolio of **Hadi Rasouli**, an industrial electrical (BMS) graduate turned mobile, web and server developer (Java, Kotlin, PHP, Python).

**Live:** https://therasuoli.github.io/

> فارسی: وب‌سایت شخصی هادی رسولی؛ تک‌فایل، بدون وابستگی و بدون نیاز به build. توضیحات فارسی در انتهای همین فایل است.

---

## Features

- **Single file, zero dependencies:** everything lives in `index.html` (HTML + CSS + vanilla JS). No framework, no build step.
- **Three languages:** Persian (default), English and Arabic, with automatic RTL/LTR switching. The choice is remembered in `localStorage`.
- **Responsive:** desktop, tablet, phone and small-phone layouts. On phones the navigation becomes a bottom bar and respects safe areas (notches).
- **Motion:** staggered scroll-reveal, animated hero, count-up number, floating chips, card spotlight following the pointer, 3D photo tilt, particle background and a scroll progress bar.
- **Accessible:** respects `prefers-reduced-motion`, visible focus styles, ARIA labels, and the content stays visible if JavaScript is disabled.
- **SEO ready:** meta description, Open Graph / Twitter tags, canonical URL and JSON-LD (`Person`).
- **Resilient loading:** Google Fonts load without blocking the first paint, so the page still shows when Google is slow or blocked.

## Project structure

```
.
├── index.html   # the whole site
├── photo.jpg    # hero portrait (square, 1536×1536)
└── README.md
```

## Run locally

No install needed. Open `index.html` in a browser, or serve the folder:

```bash
# Python
python3 -m http.server 8000

# or Node
npx serve .
```

Then visit http://localhost:8000.

## Deploy to GitHub Pages

1. Put `index.html` and `photo.jpg` in the repository root (repo name `<username>.github.io`).
2. Go to **Settings → Pages**, choose the main branch and the `/ (root)` folder.
3. Wait a minute and open `https://<username>.github.io/`.

If you update the site and still see the old version, hard-refresh or clear the browser cache.

## Customize it for yourself

| What | Where |
| --- | --- |
| Colors | CSS variables in `:root` (`--bg`, `--a`, `--b`, `--c`, …) |
| Texts in all languages | the `T` object in the `<script>` (keys `fa`, `en`, `ar`); elements are linked with `data-t="key"` |
| Photo | replace `photo.jpg` (square works best) |
| Skills | `.skills` chips in the About section and the marquee strip |
| Timeline | `<ol class="tl">` items and keys `t1y…t4y` / `t1…t4` in `T` |
| Contact links | the `.soc` list in the footer (`#bridge`) |
| SEO / social preview | `<head>` meta tags and the JSON-LD block |

The e-mail address is assembled in JavaScript (`mailto:` is built at runtime) so it is not exposed as a plain `mailto:` link to simple scrapers. It is displayed as `name[at]domain.com`.

## Browser support

Modern evergreen browsers (Chrome, Edge, Firefox, Safari) and in-app browsers such as Instagram's. The site uses CSS variables, `IntersectionObserver`, `backdrop-filter` and `background-clip: text`.

## Note about the source code

A website's HTML, CSS and JavaScript are always downloadable by visitors, so the source cannot be fully hidden. If you want to reuse parts of this design, please contact me first.

## Contact

- Instagram: [@the.rasuoli](https://instagram.com/the.rasuoli)
- LinkedIn: [@the.rasuoli](https://www.linkedin.com/in/the.rasuoli)
- GitHub: [Therasuoli](https://github.com/therasuoli)
- E-mail: info.hadirasuoli[at]gmail.com

Designed & Developed by Hadi Rasouli — © 2026

---

## توضیحات فارسی

این مخزن شامل وب‌سایت شخصی هادی رسولی است.

- کل سایت در یک فایل `index.html` است؛ بدون فریم‌ورک و بدون نیاز به build.
- سه زبان فارسی، انگلیسی و عربی با تغییر خودکار جهت راست‌به‌چپ / چپ‌به‌راست.
- کاملاً ریسپانسیو و دارای انیمیشن‌های اسکرول، ذرات پس‌زمینه و افکت‌های تعاملی.
- برای انتشار کافی است `index.html` و `photo.jpg` را در ریشه‌ی مخزن GitHub Pages قرار دهید.
- برای تغییر متن‌ها، شیء `T` در بخش اسکریپت را ویرایش کنید؛ برای رنگ‌ها، متغیرهای CSS در `:root`.
- اگر قصد استفاده از بخشی از طراحی را دارید، لطفاً ابتدا هماهنگ کنید.
