# Creo — Multimodal Aesthetic Memory Platform

> *Creo* — Latin: "I create"

## Purpose
Reflect on, record, and reuse aesthetic experience across AIGC creation sessions.
Every asset is stored in three levels: **text profiles** (Level 1) + **style samples** (Level 2) + **original assets** (Level 3).

---

## 0. Preflight Check / 初始化自检

**When**: Agent 开始任何设计/创作任务前，必须先执行自检。
**Why**: 确认品牌资源的完备性，提前发现缺失，避免创作到一半才发现素材不够。

### Check Procedure

```
[Creo Preflight] 品牌: <brand-name>
──────────────────────────────────────

Level 1 — 品牌档案
  [ ] brand-<slug>.md 存在
  [ ] Identity 完整（slogan / philosophy / audience / positioning）
  [ ] Visual DNA 完整（color palette / typography / photography / layout）
  [ ] Tone of Voice 完整（writing style / key phrases / patterns）
  [ ] Product Catalog 有数据
  [ ] Asset Inventory 有条目

Level 2 — 风格样本
  [ ] 至少 3 张可用的风格参考图（社区样本或脱敏参考）
  [ ] 配色板截图 / 色值表存在

Level 3 — 原始素材
  [ ] photos/ 目录有文件，数量: ___
  [ ] catalogs/ 目录有文件，数量: ___
  [ ] creo:// ID 可解析，抽查 1 个确认可访问

Summary
  可用层级: Level ___ (最高)
  缺失项: ___
  建议: ___
```

### Check Rules

1. **全部通过** → 正常开始创作
2. **Level 3 缺失** → 警告用户："原始素材不可用，将使用风格样本和文字档案，精准度会下降"
3. **Level 2 也缺失** → 警告用户："仅有文字档案可用，建议先补充素材再开始创作"
4. **Level 1 缺失** → **阻断**，不允许开始。要求先完成品牌档案录入
5. **Level 1 部分缺失** → 列出缺失字段，询问用户是否继续（带风险提示）

### Auto-fix Actions

自检发现问题时，Agent 应主动修复：

| 问题 | 自动修复 |
|------|----------|
| brand profile 不存在 | 引导用户提供资料，按 Intake Protocol 创建 |
| Visual DNA 为空 | 如果有 Level 3 素材，自动从图片提取色板/风格 |
| Asset Inventory 过期 | 扫描素材目录，补全缺失条目 |
| creo:// ID 无法解析 | 标记为 broken，降级到下一层 |
| 素材目录为空 | 提示用户上传，给出上传指引 |

---

## 1. Asset Intake Protocol

When user provides new design materials:

### Step 1: Stabilize Files
- Copy from temp paths (WeChat, /tmp, Downloads) → `design-assets/<brand-slug>/`
- Directory structure per brand:
  ```
  design-assets/<brand-slug>/
  ├── photos/        # Product photography, lookbook shots
  ├── catalogs/      # PDF line sheets, product manuals
  ├── brand-vi/      # Logo, brand guidelines, VI files
  ├── store-assets/  # Store screenshots, banners, homepage captures
  └── references/    # Competitor refs, mood boards, inspiration
  ```
- Upload to platform storage, generate `creo://` IDs

### Step 2: Visual DNA Extraction
For each batch of assets, extract and document:

**Color Palette** — identify dominant colors with descriptive names + approximate hex
**Typography** — font families, weights, sizes, hierarchy patterns
**Photography Style** — lighting, composition, model styling, background treatment
**Layout Patterns** — grid systems, whitespace usage, information hierarchy
**Texture & Materials** — recurring material/texture themes in imagery

### Step 3: Write Brand Profile
Create/update `brand-<slug>.md` with the template below.

### Step 4: Update Index & Run Preflight
Add/update entry in index. Run Preflight Check to verify completeness.

---

## 2. Brand Profile Template

```markdown
# Brand: <Name>

## Identity
- Slogan:
- Philosophy:
- Target audience:
- Price positioning:
- Key differentiator:

## Visual DNA

### Color Palette
| Name | Hex (approx) | Usage |
|------|-------------|-------|
| ... | ... | ... |

### Typography & Layout
- Heading style:
- Body style:
- Layout pattern:
- Whitespace philosophy:

### Photography Style
- Lighting:
- Backgrounds:
- Model styling:
- Composition:
- Post-processing:

### Tone of Voice
- Writing style:
- Key phrases:
- Copywriting patterns:

## Product Lines
(Series name, positioning, price range, key materials)

## Product Catalog
(Full SKU list with: code, name, colors, price, key fabric, design concept)

## Asset Inventory
(creo:// IDs with descriptions for each asset)
```

---

## 3. Querying Rules for Future Sessions

When a task involves design work for an existing brand:

1. **Run Preflight Check** — verify resource completeness before starting
2. **Read the brand profile** — `brand-<slug>.md`
3. **Pull visual references** — via `creo://` IDs, auto-degrade if unavailable
4. **Follow Visual DNA** — colors, typography, tone as constraints
5. **Cross-reference Product Catalog** — for product accuracy

### Three-Level Degradation

```
Agent requests creo://seek-within/photo/001
  → Level 3 available? Return original asset
  → Level 3 denied?   Return Level 2 style sample + warning
  → Level 2 empty?    Return Level 1 text description + strong warning
```

### Cross-brand reference
When designing for Brand A but referencing Brand B's style:
- Read both brand profiles
- Document which elements are borrowed vs. original
- Never mix brand identities without explicit user instruction

---

## 4. Asset Update Protocol

When user provides additional materials for an existing brand:
1. Copy files to existing `design-assets/<brand>/` subdirectory
2. Generate `creo://` IDs for new assets
3. Update the Asset Inventory section in the brand profile
4. If new visual patterns emerge, update Visual DNA
5. If new products, append to Product Catalog
6. Re-run Preflight Check to verify completeness

---

## 5. Multimodal Reference Patterns

### For AI image generation prompts
Use Visual DNA to construct style-consistent prompts:
- "Photography in the style of [brand]: [lighting], [background], [composition], [mood]"
- Reference `creo://` IDs for visual grounding

### For layout design (Pencil/.pen files)
Use Layout Patterns + Color Palette + Typography to ensure brand consistency.

### For copywriting
Use Tone of Voice section — key phrases, writing patterns, philosophy keywords.
