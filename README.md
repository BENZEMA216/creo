# Creo

> *Creo* — Latin: "I create"

Multimodal aesthetic memory system for AIGC creation.

## What is Creo?

Creo is a structured system for **reflecting on, recording, and reusing aesthetic experience** across AI-generated content creation sessions.

It solves a core problem: every time you start a new AIGC session, your aesthetic context is lost. Creo persists brand knowledge, visual DNA, and design patterns so future sessions can produce style-consistent output from the start.

## How it works

```
Reflect → Record → Reuse
   ↑                  |
   └──────────────────┘
```

1. **Reflect** — After each design task, extract what worked: colors, layouts, tone, photography style
2. **Record** — Store findings as structured brand profiles + physical asset references
3. **Reuse** — Future sessions read profiles to maintain style consistency across AIGC outputs

## Structure

```
creo.md                  ← System framework & rules
brand-<name>.md          ← Per-brand aesthetic profiles
  ├── Identity           ← Philosophy, positioning, differentiator
  ├── Visual DNA         ← Color palette, typography, photography style, layout
  ├── Tone of Voice      ← Writing style, key phrases, patterns
  ├── Product Catalog    ← SKU data for content creation
  └── Asset Inventory    ← File paths to images, PDFs, references
```

## Brands

- **Seek Within** — Minimalist women's fashion, "You might not need that many clothes"
- **1747** — Chinese contemporary streetwear

## Usage

Put `creo.md` and `brand-*.md` files where your AI agent can read them. Point asset paths to your image/PDF storage.

When starting a design task, the agent reads the brand profile first, then follows Visual DNA and Tone of Voice as constraints for all AIGC output.
