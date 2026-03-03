# Creo

> *Creo* — Latin: "I create"

Multimodal aesthetic memory platform for AIGC creation.

多模态美学记忆平台，让 AI Agent 在创作中积累、共享和复用审美经验。

---

## What is Creo? / Creo 是什么？

Every time you start a new AIGC session, your aesthetic context is lost. Creo solves this by persisting brand knowledge, visual DNA, and design patterns so future sessions can produce style-consistent output from the start.

每次开启新的 AIGC 对话，之前积累的审美认知就清零了。Creo 把品牌知识、视觉基因、设计规律结构化地存下来，让下一次创作从经验开始，而不是从零开始。

## How it works / 工作原理

```
Reflect → Record → Reuse
反思    →  记录  →  复用
   ↑                  |
   └──────────────────┘
```

1. **Reflect / 反思** — 每次设计任务后，提炼有效的审美经验：配色、排版、调性、摄影风格
2. **Record / 记录** — 以结构化的品牌档案 + 多模态素材存储
3. **Reuse / 复用** — 未来的创作会话读取档案和素材，确保 AIGC 输出的风格一致性

## Architecture / 架构

### Three-Level Degradation / 三层降级

Agent 获取美学经验时，按可用性自动降级：

```
Level 3 ★★★  原始素材        creo://seek-within/photo/001
  ↓ 无权限时降级
Level 2 ★★☆  社区风格样本    creo://styles/minimal-warm/ref-03
  ↓ 无匹配时降级
Level 1 ★☆☆  文字档案        brand-seek-within.md → Visual DNA
```

每一层都能独立工作，有上层效果更好。

### Asset ID System / 资产 ID 系统

所有素材通过 `creo://` 统一寻址，平台负责存储和访问控制：

```
creo://seek-within/photo/001      → 白T平铺正面
creo://seek-within/photo/002      → 包装盒开箱
creo://seek-within/catalog/26ss   → 26SS产品手册
creo://1747/store/banner-01       → 店铺Banner
creo://styles/denim-raw/ref-01    → 社区公共风格样本
```

Agent 不需要知道图片存在哪，只需要 `creo://` ID，平台处理剩下的。

### Platform Responsibilities / 平台职责

```
Upload   用户/Agent 上传素材 → 平台生成 creo:// ID → 存入后端
Access   Agent 请求 creo:// ID → 平台校验权限 → 返回素材或降级
Share    品牌方开放 ID 访问权 → 其他社区成员的 Agent 可拉取
Degrade  无权限？→ 返回 Level 2 风格样本；无样本？→ 返回 Level 1 文字描述
```

## Brand Profile Structure / 品牌档案结构

```
creo.md                  ← 系统框架与规则
brand-<name>.md          ← 品牌美学档案（每品牌一份）
  ├── Identity           ← 品牌哲学、定位、差异化
  ├── Visual DNA         ← 色板、字体、摄影风格、排版规律
  ├── Tone of Voice      ← 文案风格、关键词、写作规律
  ├── Product Catalog    ← 产品数据
  └── Asset Inventory    ← creo:// ID 索引（替代文件路径）
```

## Community Vision / 社区愿景

Creo 不只是一个本地工具，而是一个**美学经验的共享社区**：

- Agent 在创作中总结经验教训，上传素材，分享到社区
- 其他 Agent 利用社区经验和素材，提升创作质量
- 贡献是分层的 — 你可以贡献文字经验、风格样本、或开放原始素材授权
- **GPL-3.0 协议保证互助**：使用了社区资源，你的经验也必须回馈社区，没人能只取不予

## Usage / 使用方式

将 `creo.md` 和 `brand-*.md` 放在你的 AI Agent 能读取的位置。

Agent 开始设计任务时：
1. 读取品牌档案，建立基本认知 (Level 1)
2. 通过 `creo://` ID 拉取风格样本 (Level 2)
3. 如有授权，拉取原始素材做精准还原 (Level 3)

## Brands / 已收录品牌

- **Seek Within** — 克制美学女装，"你或许不需要那么多衣服"
- **1747** — 淘宝原创国潮女装

## License / 协议

GPL-3.0 — 用了就要回馈，共建美的社区。
