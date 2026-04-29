# BigText

**Live:** https://itsavibecode.github.io/bigtext/

Display anything, big. A single-file fullscreen large-text tool with a theme picker, screenshot export, copy-to-clipboard / share, line-break support, and an ALL CAPS toggle. Inspired by [bigtext.vercel.app](https://bigtext.vercel.app/).

## Features

- Auto-sizing fullscreen text — fills the viewport regardless of length, on desktop and mobile portrait
- Tap anywhere to edit; `Enter` for line breaks, `Ctrl/Cmd+Enter` to display
- ALL CAPS toggle in the editor (persists across opens)
- 8 background and 8 text colors with live theme switching
- Save button — downloads a clean 2x PNG of the current display
- Copy / Share button — copies the screenshot to clipboard on desktop, opens the native share sheet on iOS / Android
- Mobile screenshots render to an offscreen 4:3 canvas so the exported image is always landscape and shareable
- Auto-hiding toolbar (move the mouse / tap the screen to bring it back)
- Fullscreen toggle

## Stack

- Single static `index.html`, no build step
- [html2canvas 1.4.1](https://html2canvas.hertzen.com/) via cdnjs for screenshot capture
- DM Sans + Instrument Sans via Google Fonts
- Hosted on GitHub Pages

## Changelog

### v0.1.0 — 2026-04-29
- Bring repo into local workflow and tag the first versioned release
- Add Open Graph and Twitter Card meta tags so links render previews in Slack, iMessage, Discord, Twitter, etc.
- Add 1200×630 `og-image.png`, 180×180 `apple-touch-icon.png`, and SVG favicon
- Add canonical URL, theme-color, and meta description
- Add `APP_VERSION` constant in source for future bumps
- Add this README and changelog

### Pre-release — 2026-04-09
- Initial clone of bigtext.vercel.app with screenshot save and copy buttons
- Mobile fixes: 4:3 offscreen capture, Web Share API fallback for iOS, line-break support, offscreen-probe binary search for auto-sizing (fixes `width:100% + word-break` measurement bug)
- ALL CAPS toggle in editor
