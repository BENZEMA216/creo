# Creo

> *Creo* — Latin: "I create"

Multimodal aesthetic memory system for AIGC creation.

多模态美学记忆系统，让 AI Agent 在创作中积累、共享和复用审美经验。

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
2. **Record / 记录** — 以结构化的品牌档案 + 实体素材索引存储
3. **Reuse / 复用** — 未来的创作会话读取档案，确保 AIGC 输出的风格一致性

## Structure / 结构

```
creo.md                  ← 系统框架与规则
brand-<name>.md          ← 品牌美学档案（每品牌一份）
  ├── Identity           ← 品牌哲学、定位、差异化
  ├── Visual DNA         ← 色板、字体、摄影风格、排版规律
  ├── Tone of Voice      ← 文案风格、关键词、写作规律
  ├── Product Catalog    ← 产品数据
  └── Asset Inventory    ← 素材文件路径索引
```

## Community Vision / 社区愿景

Creo 不只是一个本地工具，而是一个 **美学经验的共享社区**：

- Agent 在创作中总结经验教训，分享到社区
- 其他 Agent 可以利用社区经验，提升自己的创作质量
- **GPL-3.0 协议保证互助**：使用了社区资源，你的经验也必须回馈社区，没人能只取不予

## Usage / 使用方式

将 `creo.md` 和 `brand-*.md` 放在你的 AI Agent 能读取的位置，素材路径指向你的图片/PDF 存储目录。

Agent 开始设计任务时，先读取品牌档案，然后以 Visual DNA 和 Tone of Voice 作为创作约束。

## Brands / 已收录品牌

- **Seek Within** — 克制美学女装，"你或许不需要那么多衣服"
- **1747** — 淘宝原创国潮女装

## License / 协议

GPL-3.0 — 用了就要回馈，共建美的社区。
