# Changelog

## 1.1.0 — 2026-11-20

- 30-day free trial with every feature, counted by the days the app is actually opened.
- Trial state is server-authoritative and machine-bound; reinstalling, clearing local data or changing the clock does not reset it.
- Remaining trial days are shown in the launcher, the top bar and the License panel.
- Offline trial support: days opened offline are queued and reported when the store is reachable again.
- Optional uninstall feedback on Windows (browser page, skippable, never blocks the uninstall).
- Self-service license recovery with checkout email + machine code, without needing the order number.
- Trial-first storefront and documentation; price now appears only on the purchase/checkout pages.
- New English and Chinese screenshots.

## 1.0.0 — 2026-11-10

First paid release.

- Offline machine-bound `HAC-` activation codes with ECDSA P-256.
- Activation screen in the launcher and dashboard, with machine code copy and purchase link.
- License panel in Settings, including edition, expiry, serial and local deactivation.
- All real-device write APIs return HTTP 402 until a valid license is activated.
- Demo mode remains available without a license.
- Store: Creem checkout, webhook, offline code claim, 2-device limit, reissue, revoke and audit.
- Store: English/Chinese sales site, guide, compatibility page, legal pages.
- SEO: sitemap, robots, llms.txt, structured data, canonical, hreflang, OG image.
- Windows and macOS packaging; macOS distribution requires developer signing.

## 0.2.0 — 2026-11-02

- Unified entity and integration APIs.
- SunLogin account cloud plugs and Bemfa voice bridge.
- Low-interference automatic reads and multi-client center improvements.

## 0.1.1 — 2026-11-01

- Mobile layout improvements and SunLogin account mirroring in Settings.

## 0.1.0 — 2026-10-31

- First installable release: Mijia import, LAN control, SunLogin local plugs, scenes and activity.
