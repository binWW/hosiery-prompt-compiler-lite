# Hosiery Visual Language

## 03_Material.md

Version: 1.1

---

# Purpose

The Material Layer defines the physical fabric composition of hosiery.

It determines:

* visual texture realism
* fabric density perception
* surface behavior under light
* skin interaction quality
* seasonal textile identity

Material does NOT define garment structure (handled in Basic Layer).

---

# AI Interpretation Priority

When interpreting hosiery materials, AI models prioritize:

1. Fabric Type (primary visual identity)
2. Fabric Weight (thickness perception)
3. Surface Texture (smooth / knit / mesh)
4. Elastic Behavior (fit and deformation)
5. Skin Interaction (how fabric overlays skin)

If Material is missing or unclear, AI may:

* render bare skin instead of hosiery
* generate plastic/latex-like surfaces
* produce sweater-like or non-leg structures
* break fabric realism consistency

---

# Fabric Type System

---

## 1. Nylon-Based Hosiery (Core System)

```text id="nyl01"
nylon
fine nylon
ultra-fine nylon
polyamide fiber
stretch nylon
```

Visual Characteristics:

* smooth surface
* lightweight appearance
* natural elastic fit
* subtle sheen (low to medium)
* classic hosiery behavior

Use Case:

Default system for pantyhose and tights.

---

## 2. Microfiber Hosiery

```text id="mfc01"
microfiber
soft microfiber
dense microfiber blend
brushed microfiber
```

Visual Characteristics:

* matte finish
* soft diffused surface
* reduced transparency perception
* thicker visual density
* smooth skin blending

Use Case:

Opaque tights, autumn/winter hosiery.

---

## 3. Silk-Effect Synthetic Fiber

```text id="sil01"
silk-blend nylon
silky polyamide
luxury sheen fiber
smooth silk-effect textile
```

Visual Characteristics:

* soft elegant reflection
* refined surface highlights
* premium fashion appearance
* smooth light distribution

Use Case:

Editorial fashion / luxury advertising visuals.

---

## 4. Cotton-Based Hosiery (NEW)

```text id="cot01"
cotton blend
soft cotton fiber
cotton knit fabric
breathable cotton yarn
natural cotton textile
```

Visual Characteristics:

* matte, non-gloss surface
* visible textile grain
* soft natural appearance
* thicker than nylon visually
* casual everyday aesthetic

Skin Interaction Behavior:

* reduces glossy skin effect
* creates diffused leg tone
* natural soft coverage
* less “silky” leg appearance

Use Case:

* casual fashion hosiery
* autumn daily wear tights
* comfort-oriented legwear

Anti-Misinterpretation Rules:

Must NOT generate:

❌ glossy nylon skin look
❌ latex / plastic surface
❌ sheer silk-like transparency

Must generate:

✔ soft matte textile surface
✔ visible fabric grain
✔ natural casual leg coverage

---

## 5. Wool Knit Hosiery (NEW)

```text id="wol01"
wool knit
wool blend fiber
thermal wool yarn
soft knitted wool fabric
dense wool textile
```

Visual Characteristics:

* strong knit visibility
* warm textile appearance
* thick seasonal fabric feel
* low surface gloss
* structured leg coverage

Skin Interaction Behavior:

* skin mostly hidden
* leg shape defined by fabric tension
* strong winter fashion identity

Use Case:

* winter tights
* thermal hosiery
* cold-weather fashion visuals

Anti-Misinterpretation Rules:

Must NOT generate:

❌ fuzzy blanket texture
❌ sweater wrapped around legs
❌ carpet-like material

Must generate:

✔ fitted knit-on-leg garment
✔ structured thermal hosiery
✔ body-following wool textile

---

## 6. Stretch / Elastic Fiber System

```text id="str01"
high-stretch nylon
elastic polyamide blend
4-way stretch fabric
compression hosiery fabric
```

Visual Characteristics:

* tight skin adhesion
* smooth contour adaptation
* no sagging behavior
* natural tension at joints (knees/ankles)

Use Case:

All fitted hosiery types.

---

## 7. Sheer Mesh Structure

```text id="mes01"
sheer mesh nylon
ultra-fine mesh weave
transparent knit structure
delicate net fiber
```

Visual Characteristics:

* micro-grid visibility
* high transparency
* extremely light fabric presence
* visible skin-through structure

Use Case:

Ultra-sheer hosiery (VOL-1 ~ VOL-3).

---

## 8. Fishnet / Open Structure (Reference System)

```text id="fis01"
fishnet mesh
open weave structure
large grid nylon
netted fabric system
```

Note:

Fishnet belongs to Basic Layer (structure classification), but material behavior is defined here for consistency.

---

# Fabric Weight System

Used to stabilize cotton and wool rendering behavior.

---

## Light Weight

```text id="wgt01"
ultra-light cotton blend
fine wool yarn
thin nylon fiber
```

---

## Medium Weight

```text id="wgt02"
standard cotton knit
balanced wool blend
medium density nylon
```

---

## Heavy Weight

```text id="wgt03"
dense wool knit
thick cotton fabric
thermal knit blend
```

---

# Material Behavior Rules

---

## Rule 1 — Material must define visible texture

Good:

```text id="ok01"
opaque tights
dense microfiber fabric
matte surface texture
```

Bad:

```text id="bad01"
tights
```

---

## Rule 2 — Material must align with opacity system

Ultra sheer example:

```text id="op01"
ultra-fine nylon
sheer mesh structure
```

Opaque example:

```text id="op02"
dense microfiber
thick knit fabric
```

---

## Rule 3 — Cotton & Wool must include textile qualifiers

Always include:

* knit / fiber / yarn / textile

Correct:

```text id="ok02"
cotton knit fabric
wool knit textile
```

Incorrect:

❌ cotton tights
❌ wool tights

---

## Rule 4 — Elastic behavior is mandatory

Always include at least one:

```text id="el01"
stretch fabric
elastic blend
compression fit
```

---

# Material → Opacity Mapping Reference

| Material Type | Compatible Opacity Range |
| ------------- | ------------------------ |
| Nylon         | VOL-1 → VOL-4            |
| Microfiber    | VOL-4 → VOL-8            |
| Silk-effect   | VOL-2 → VOL-5            |
| Cotton blend  | VOL-4 → VOL-6            |
| Wool knit     | VOL-6 → VOL-8            |
| Sheer mesh    | VOL-1 → VOL-3            |

---

# System Integration

Material Layer connects with:

* 01_Basic.md → garment structure definition
* 02_Opacity.md → transparency control system
* 04_Finish.md → surface reflection behavior
* 06_Lighting.md → photographic realism enhancement

---

# Version History

v1.0 — Initial material system
v1.1 — Added cotton + wool knit systems, improved fabric weight system, strengthened anti-misinterpretation rules
