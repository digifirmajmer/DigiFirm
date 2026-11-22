# DigiFirm QA report

Date: 2026-11-21

## Automated package and source checks — PASS

- Final ZIP archive integrity checked (`testzip`: no corrupt entries); 25 archive entries.
- All local `src` and local `href` references in `index.html` resolve to files in the project.
- All in-page anchor targets resolve.
- No duplicate HTML IDs detected.
- All embedded CSS parsed with no stylesheet syntax errors.
- All inline JavaScript blocks pass `node --check`.
- All 16 packaged raster image assets decode successfully (8 WebP and 8 PNG).
- Both MP4 assets pass `ffprobe` container inspection (10.04s and 7.37s).
- Four Creative Playbook PNGs match the supplied original ZIP byte-for-byte (SHA-256 comparison).
- The full project folder, HTML, assets, README, credits, upgrade notes and this report are included.

## Browser/device testing — NOT COMPLETED

An attempted headless Chromium run at desktop (1440px), tablet (768px), mobile (390px) and small mobile (320px) viewports was blocked by the execution environment (`ERR_BLOCKED_BY_ADMINISTRATOR`) before the page could load. Therefore visual layout, horizontal overflow, menu interaction, modal interaction and runtime console behaviour are **not certified** by this report. Physical Android/iPhone/tablet/laptop devices have not been tested.

## External integrations — NOT VERIFIED

- The contact form posts to the existing Google Apps Script endpoint. A real submission was not made, so delivery is unverified.
- The newsletter form has no configured submission endpoint in the supplied source.
- Remote Google Fonts, GSAP, ScrollTrigger, Lenis and third-party network behaviour were not verified because browser/network access was unavailable.

## Run locally

Extract the ZIP and open `DigiFirm-Portfolio-Full/index.html` in a modern browser, or serve the `DigiFirm-Portfolio-Full` folder with a static web server. Deploy the complete folder, not only `index.html`.
