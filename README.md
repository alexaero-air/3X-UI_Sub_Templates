# 3X-UI Sub Templates

**English** | [Русский](README.ru.md)

A collection of custom subscription page templates for the [3X-UI](https://github.com/MHSanaei/3x-ui) VPN panel.
Each template is a modern, fully self-contained page that replaces the default subscription page and gives your users a clean dashboard with everything they need in one place.

![HTML](https://img.shields.io/badge/HTML-single%20file-e34c26) ![CSS](https://img.shields.io/badge/CSS-no%20frameworks-264de4) ![JS](https://img.shields.io/badge/JS-vanilla-f7df1e) ![3X-UI](https://img.shields.io/badge/3X--UI-compatible-2aabee)

## Templates

| Template | Name | Description |
| --- | --- | --- |
| [`Template 1`](<Template 1/>) | **Dark Red Template** | Dark theme with red accents: glassy cards, simple background, rounded features, gradient traffic bar, smooth animations. |
| [`Template 2`](<Template 2/>) | **Dark Teal Template** | Dark theme with teal accents: Sci-fi style, thin elegant lines, config strings with stilyzed protocol tags, gradient traffic bar, quick but smooth animations. |

More templates in different styles are on the way.

## Common features

Every template in this collection is built on the same principles:

- **Single self-contained file** — all styles, scripts and icons are inline. No external images or CDNs, so it works out of the box with the Go server that renders 3X-UI subscription pages.
- **Subscription copy buttons** — one-click copy for Xray / Sing-box and Clash / Mihomo subscription links, with visual "Copied!" feedback.
- **Configuration cards** — every config link is parsed on the client and displayed with colored protocol / transport / security tags (VLESS, VMESS, Trojan, Shadowsocks, Hysteria2, TUIC, Reality, WS, gRPC and more).
- **Smart traffic bar** — the color smoothly shifts from green to red as the user runs out of traffic; unlimited plans show a full green bar.
- **Animated FAQ** — expandable question rows with smooth open/close animation and auto-scroll to the opened answer.
- **Support contacts block** — support link plus Telegram / WhatsApp / GitHub buttons that glow in their brand colors on hover.
- **Responsive** — adapts to mobile, tablet and desktop.
- **Easy to customize** — a customization map at the top of each file lists the exact line ranges for the logo, colors, FAQ, contacts and more.

## Quick start

1. Pick a template from the table above and take its `sub.html`.
2. Replace the subscription page template of your 3X-UI panel with it.
3. Open the file and follow the **customization map** in the comment at the very top:
   - replace the `Your Logo` placeholder with your logo,
   - set your Telegram / WhatsApp / GitHub links (they are `#` by default),
   - edit the FAQ answers and colors if you like.
4. Done — the page is rendered by the panel with your subscription data.

## Template variables

The pages use the standard Go template variables provided by 3X-UI:

`.subTitle`, `.enabled`, `.emails`, `.sId`, `.expire`, `.lastOnline`, `.used`, `.remained`, `.total`, `.download`, `.upload`, `.links`, `.subUrl`, `.subClashUrl`, `.subSupportUrl`

## Customization

Everything you are likely to change is listed in the comment block at the top of each template with exact line ranges:

- browser tab title and color theme (`:root` CSS variables),
- header logo and page heading,
- Xray / Clash subscription buttons (names, captions, SVG icons),
- support contacts and social buttons,
- FAQ section — add new questions by copying the `<details class="faq-item">` block,
- FAQ animation duration (`FAQ_ANIM_MS`).

## License

Free to use and modify for your own panel.
