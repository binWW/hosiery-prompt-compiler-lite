# Hosiery Visual Language

## 05_Lighting.md

Version: 1.0

---

# Purpose

The Lighting Layer defines how hosiery is perceived under light.

It controls:

* realism level
* fabric visibility enhancement
* leg shape definition
* texture readability
* commercial photography authenticity

Lighting does NOT describe the environment.

It describes how light interacts with subject and fabric.

---

# AI Interpretation Priority

When generating hosiery imagery, AI models prioritize lighting in this order:

1. Light direction
2. Light softness
3. Shadow behavior
4. Specular highlight placement
5. Contrast distribution

If Lighting is missing:

* hosiery loses texture detail
* legs appear flat or plastic
* fabric loses realism
* commercial quality drops significantly

---

# Lighting Classification System

---

## 1. Soft Studio Lighting (Core Standard)

```text id="lt01"
soft studio lighting
diffused studio light
large softbox lighting
even lighting setup
```

Visual Characteristics:

* smooth shadow transitions
* balanced exposure
* minimal harsh contrast
* ideal for commercial product shots
* safest default lighting

Use Case:

* all hosiery categories
* e-commerce catalog images
* clean advertising visuals

---

## 2. Side Lighting (Shape Definition System)

```text id="lt02"
soft side lighting
angled studio lighting
directional soft light
45-degree lighting setup
```

Visual Characteristics:

* enhances leg contours
* improves fabric texture visibility
* creates depth and volume
* natural shadow shaping

Use Case:

* fashion photography
* leggings / tights emphasis
* slimming visual effect

---

## 3. Top Lighting (Clean Commercial Look)

```text id="lt03"
top-down soft lighting
overhead studio lighting
even top illumination
```

Visual Characteristics:

* clean and neutral presentation
* reduces dramatic shadows
* emphasizes uniform fabric tone
* slightly flattening effect

Use Case:

* product catalog
* minimalist advertising
* neutral presentation shots

---

## 4. Backlight / Rim Light (Edge Definition System)

```text id="lt04"
soft backlight
rim lighting
edge lighting
backlit studio setup
```

Visual Characteristics:

* creates glowing leg edges
* enhances silhouette separation
* improves transparency perception (important for sheer hosiery)
* adds premium fashion feel

Use Case:

* sheer stockings (VOL-1 ~ VOL-3)
* luxury fashion campaigns
* editorial photography

---

## 5. Natural Window Light (Lifestyle System)

```text id="lt05"
natural window light
soft daylight
indirect natural lighting
ambient daylight
```

Visual Characteristics:

* soft realistic tone
* lifestyle aesthetic
* less controlled shadows
* natural skin rendering

Use Case:

* casual hosiery
* cotton / wool materials
* lifestyle advertising

---

## 6. High-Key Lighting (E-commerce Clean System)

```text id="lt06"
high key lighting
bright even lighting
shadowless studio lighting
clean white lighting
```

Visual Characteristics:

* near-zero shadows
* very clean product visibility
* flat but clear presentation
* strong commercial clarity

Use Case:

* e-commerce product listings
* marketplace images
* catalog consistency

---

## 7. Low-Key Lighting (Fashion Dramatic System)

```text id="lt07"
low key lighting
dark studio lighting
high contrast lighting
dramatic shadow lighting
```

Visual Characteristics:

* strong contrast
* deep shadows
* dramatic mood
* premium editorial aesthetic

Use Case:

* fashion editorials
* luxury brand campaigns
* artistic photography

---

## 8. Soft Gradient Lighting (Premium Commercial System)

```text id="lt08"
soft gradient lighting
cinematic studio lighting
smooth light falloff
professional fashion lighting
```

Visual Characteristics:

* smooth light transitions
* cinematic depth
* premium advertising feel
* balanced highlight control

Use Case:

* high-end e-commerce ads
* brand campaigns
* magazine-style visuals

---

# Lighting Intensity Control

Each lighting type can be adjusted:

## Soft

```text id="li01"
soft
diffused
gentle
```

## Medium

```text id="li02"
balanced
controlled
moderate
```

## Strong

```text id="li03"
strong
defined
high contrast
```

---

# Lighting → Hosiery Interaction Rules

---

## Ultra Sheer Hosiery (VOL-1 ~ VOL-2)

Best Lighting:

```text id="li04"
soft backlight
rim lighting
soft studio lighting
```

Reason:

Sheer fabrics require edge light to reveal structure.

---

## Semi Sheer Hosiery (VOL-3 ~ VOL-4)

Best Lighting:

```text id="li05"
soft studio lighting
soft side lighting
balanced gradient lighting
```

---

## Opaque Hosiery (VOL-5 ~ VOL-8)

Best Lighting:

```text id="li06"
soft studio lighting
high key lighting
soft side lighting
```

---

## Cotton / Wool Hosiery

Best Lighting:

```text id="li07"
natural window light
soft studio lighting
high key lighting
```

Reason:

Enhances textile realism and avoids artificial gloss.

---

# Lighting → Finish Interaction Rules

---

## Matte Finish

Best Lighting:

* soft studio lighting
* high key lighting

Avoid:

❌ harsh backlight (kills texture visibility)

---

## Satin Finish

Best Lighting:

* soft side lighting
* gradient studio lighting

---

## Gloss Finish

Best Lighting:

* directional lighting
* rim lighting
* controlled highlights

---

## Velvet Finish

Best Lighting:

* diffused studio lighting
* soft box lighting

---

# Common Mistakes

❌ Using high contrast lighting for cotton hosiery
→ makes fabric look plastic

---

❌ Using flat high-key lighting for sheer hosiery
→ removes transparency effect

---

❌ Overusing rim light
→ creates unrealistic glowing legs

---

❌ Mixing multiple lighting systems
→ breaks realism consistency

---

# Best Practice Prompt Pattern

Recommended full structure:

```text id="bp01"
[Basic]
+
[Opacity]
+
[Material]
+
[Finish]
+
[Lighting]
+
[Realism Detail]
```

Example:

```text id="bp02"
semi sheer tights
fine nylon
satin finish
soft side lighting
natural leg stretch
```

---

# System Role

Lighting Layer connects:

* 01_Basic.md → garment structure
* 02_Opacity.md → transparency behavior
* 03_Material.md → fabric realism
* 04_Finish.md → surface reflection
* 06_Realism.md → micro detail amplification

---

# Version History

v1.0 — Full lighting system: studio, fashion, commercial, lifestyle, and cinematic lighting framework
