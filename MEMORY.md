# Creative Cowork - Memory Index

## Creo — 美学经验系统
- Framework: [creo.md](creo.md)
- Asset root (local): `design-assets/` in project root
- Asset root (server): `/root/.openclaw/design-assets/`
- Rule: every brand gets a profile in `brand-<name>.md`

## Brand Profiles
- **Seek Within**: [brand-seek-within.md](brand-seek-within.md) — 克制美学女装，26SS 产品线完整录入
- **1747 大话国潮**: [brand-1747.md](brand-1747.md) — 淘宝原创国潮女装

## Infrastructure
- Remote server: 43.160.242.46 (root / Xz19990817.)
- OpenClaw skills: `/root/.openclaw/skills/`
- store-teardown skill: 含 google_images.py 备选采集路径
- Telegram bot: @openflycat_bot (needs Topics in DMs enabled for streaming)

## Key Patterns
- WeChat files arrive at `/Users/dongzhe/Library/Containers/com.tencent.xinWeChat/...` — always copy to `design-assets/` immediately
- PDF catalogs: read all pages, extract to brand profile's product-catalog section
- Product photos: copy to `design-assets/<brand>/photos/`, describe in asset-inventory
- alicdn images can be downloaded directly without auth (bypass cloud_ip_bl via CDN)
