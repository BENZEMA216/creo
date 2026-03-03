# Brand: 1747 大话国潮

## Identity
- **Philosophy**: 国潮原创女装，融合东方文化元素与当代时尚
- **Target audience**: 追求个性国风的年轻女性
- **Price positioning**: 中端淘宝原创
- **Key differentiator**: 国潮文化 IP + 原创设计
- **Platform**: 淘宝店铺 (seller_id: 2207758505229)
- **Official site**: dbqy8.com（大话国潮域名，服务器 403 直连受限）

## Visual DNA

### Color Palette
(待补充 — 需要更多店铺首页/Banner素材分析)

### Photography Style
- 产品主图以白底/纯色底为主
- 国潮风格插画/图案元素
- (更多待从 alicdn 图片中提取)

### Tone of Voice
(待补充)

## Asset Inventory

### Store Images (15 files, via Google→alicdn pipeline)
**Location**: `design-assets/1747/images/`
| File | Source | Content |
|------|--------|---------|
| 1747_alicdn_01-10 | Google Images → alicdn CDN | 产品主图，包含 seller_id 2207758505229 的商品图 |
| 1747_brand_01-04 | Google Images | 品牌相关搜索结果图片 |
| banner_02.jpg | dbqy8.com (Google cache) | 品牌官网 banner |

### Technical Notes
- 淘宝店铺首页无法直接抓取（cloud_ip_bl 黑名单）
- maishou API 的 desc 字段始终为空
- Google Image Search → alicdn CDN 下载是目前唯一可行的采集路径
- alicdn CDN URL 不需要认证，可直接 HTTP 下载
- 采集脚本: `/root/.openclaw/skills/store-teardown/scripts/google_images.py`

## Product Catalog
(待补充 — 需要用户提供产品资料)
