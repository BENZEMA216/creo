# Creo — Multimodal Aesthetic Memory System

> *Creo* — Latin: "I create"

## Purpose
Reflect on, record, and reuse aesthetic experience across AIGC creation sessions.
Every asset is stored in two layers: **physical files** (images/PDFs) + **structured knowledge** (brand profiles in memory).

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

### Step 2: Visual DNA Extraction
For each batch of assets, extract and document:

**Color Palette** — identify dominant colors with descriptive names + approximate hex
**Typography** — font families, weights, sizes, hierarchy patterns
**Photography Style** — lighting, composition, model styling, background treatment
**Layout Patterns** — grid systems, whitespace usage, information hierarchy
**Texture & Materials** — recurring material/texture themes in imagery

### Step 3: Write Brand Profile
Create/update `memory/brand-<slug>.md` with the template below.

### Step 4: Update Index
Add/update entry in `MEMORY.md` under Brand Profiles.

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
(File paths with descriptions for each asset category)
```

---

## 3. Querying Rules for Future Sessions

When a task involves design work for an existing brand:

1. **Always read the brand profile first** — `memory/brand-<slug>.md`
2. **For visual reference** — read actual image files listed in Asset Inventory
3. **For style consistency** — follow the Visual DNA section (colors, typography, tone)
4. **For product accuracy** — cross-reference the Product Catalog section
5. **For new designs** — use Photography Style + Layout Patterns as constraints

### Cross-brand reference
When designing for Brand A but referencing Brand B's style:
- Read both brand profiles
- Document which elements are borrowed vs. original
- Never mix brand identities without explicit user instruction

---

## 4. Asset Update Protocol

When user provides additional materials for an existing brand:
1. Copy files to existing `design-assets/<brand>/` subdirectory
2. Update the Asset Inventory section in the brand profile
3. If new visual patterns emerge, update Visual DNA
4. If new products, append to Product Catalog

---

## 5. Multimodal Reference Patterns

### For AI image generation prompts
Use Visual DNA to construct style-consistent prompts:
- "Photography in the style of [brand]: [lighting], [background], [composition], [mood]"
- Reference actual image paths for visual grounding

### For layout design (Pencil/.pen files)
Use Layout Patterns + Color Palette + Typography to ensure brand consistency.

### For copywriting
Use Tone of Voice section — key phrases, writing patterns, philosophy keywords.

