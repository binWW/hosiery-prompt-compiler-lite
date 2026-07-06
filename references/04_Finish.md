# Hosiery Visual Language

## 04_Finish.md

Version: 1.0

---

# Purpose

The Finish Layer defines the surface optical behavior of hosiery.

It controls how light interacts with the fabric.

It determines:

* gloss level
* reflection behavior
* surface softness perception
* luxury vs casual visual tone
* photographic realism

If Material defines “what it is made of”,
Finish defines “how it looks under light”.

---

# AI Interpretation Priority

When rendering hosiery finish, AI models prioritize:

1. Surface reflection (specular behavior)
2. Light diffusion
3. Micro texture visibility
4. Fabric smoothness perception
5. Contrast between highlights and shadows

If Finish is missing:

* hosiery may look plastic
* skin may look waxy
* fabric may look flat or CGI-like
* lighting may lose realism

---

# Finish Classification System

---

## 1. Matte Finish (Core Standard)

```text id="mt01"
matte finish
soft matte
natural matte surface
powder matte texture
```

Visual Characteristics:

* no strong reflection
* soft diffused surface
* natural fabric appearance
* high realism in studio lighting
* most common in opaque hosiery

Use Case:

* VOL-5 to VOL-8 hosiery
* cotton / wool materials
* commercial catalog photography

---

## 2. Satin Finish (Balanced Elegance)

```text id="sa01"
satin finish
soft satin sheen
low gloss satin surface
silky satin reflection
```

Visual Characteristics:

* controlled soft highlights
* elegant light reflection
* smooth surface transition
* slightly luxurious appearance

Use Case:

* fashion hosiery
* semi-sheer tights
* editorial commercial style

---

## 3. Silk-Like Sheen (Premium Visual Layer)

```text id="sl01"
silky sheen
elegant gloss
smooth reflective surface
luxury soft shine
```

Visual Characteristics:

* refined highlight streaks
* soft directional reflections
* premium fashion aesthetic
* controlled specular response

Use Case:

* VOL-2 to VOL-4 hosiery
* luxury advertising
* high-end brand visuals

---

## 4. Gloss Finish (High Shine System)

```text id="gl01"
high gloss
strong sheen
reflective surface
polished fabric finish
```

Visual Characteristics:

* strong visible highlights
* reflective leg surface
* artificial polished look if overused
* fashion editorial drama

Use Case:

* fashion editorials
* stylized commercial shoots
* stage or performance aesthetics

---

## 5. Wet Look Finish (Special Effect)

```text id="wt01"
wet look finish
oily sheen
wet surface reflection
liquid-like gloss
```

Visual Characteristics:

* strong specular highlights
* liquid-like reflection behavior
* dramatic lighting response
* highly stylized appearance

Use Case:

* high fashion editorial
* conceptual photography
* artistic campaigns

---

## 6. Velvet Soft Finish (Soft Diffusion System)

```text id="vl01"
velvet soft finish
soft diffused surface
cushioned light absorption
smooth fabric blur
```

Visual Characteristics:

* soft light absorption
* reduced highlight intensity
* smooth visual softness
* “expensive fabric” feel

Use Case:

* cotton / wool hosiery
* winter fashion
* lifestyle commercial images

---

# Finish Intensity Control System

Each finish type can be adjusted by intensity level:

## Low Intensity

```text id="fi01"
subtle
light
minimal
```

## Medium Intensity

```text id="fi02"
balanced
controlled
moderate
```

## High Intensity

```text id="fi03"
strong
pronounced
high impact
```

---

# Finish → Material Compatibility Rules

---

## Nylon Materials

Best Finishes:

```text id="ny01"
satin finish
silky sheen
soft matte (low gloss nylon)
```

Avoid:

❌ heavy velvet finish
❌ wool-like diffusion

---

## Microfiber Materials

Best Finishes:

```text id="mf01"
matte finish
velvet soft finish
natural diffusion
```

Avoid:

❌ high gloss
❌ wet look

---

## Cotton Materials

Best Finishes:

```text id="ct01"
matte finish
velvet soft finish
powder matte texture
```

Avoid:

❌ satin shine
❌ reflective gloss

---

## Wool Knit Materials

Best Finishes:

```text id="wl01"
velvet soft finish
matte finish
soft diffusion
```

Avoid:

❌ glossy finish
❌ wet look

---

## Sheer Mesh Materials

Best Finishes:

```text id="sm01"
satin finish
silky sheen
controlled gloss
```

Avoid:

❌ heavy matte (kills transparency perception)

---

# Finish → Opacity Interaction Rules

---

## Ultra Sheer Hosiery (VOL-1 ~ VOL-2)

Recommended:

```text id="opf01"
silky sheen
soft satin finish
light reflection
```

Reason:

Too matte destroys “sheer illusion”

---

## Semi Sheer (VOL-3 ~ VOL-4)

Recommended:

```text id="opf02"
balanced satin finish
soft sheen
controlled reflection
```

---

## Opaque Hosiery (VOL-5 ~ VOL-8)

Recommended:

```text id="opf03"
matte finish
velvet soft finish
diffused surface
```

---

# Lighting Interaction Rules

Finish must respond to lighting:

---

## Matte Finish

* absorbs light
* reduces highlight intensity
* enhances realism in studio lighting

---

## Satin Finish

* creates soft gradient highlights
* best for fashion photography

---

## Gloss Finish

* produces strong specular highlights
* increases visual drama

---

## Velvet Finish

* diffuses light heavily
* creates premium softness perception

---

# Common Mistakes

❌ Using gloss on wool or cotton

→ produces plastic-looking fabric

---

❌ Using full matte on ultra-sheer hosiery

→ destroys transparency illusion

---

❌ Mixing wet look with microfiber or cotton

→ creates unnatural material conflict

---

❌ Overusing satin finish

→ makes legs look artificially coated

---

# Best Practice Prompt Pattern

Recommended structure:

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
[Realism]
```

Example:

```text id="bp02"
semi sheer tights
fine nylon
satin finish
soft studio lighting
natural leg stretch
```

---

# System Role

Finish Layer connects:

* 01_Basic.md → garment identity
* 02_Opacity.md → transparency behavior
* 03_Material.md → fabric composition
* 05_Lighting.md → visual rendering control
* 06_CommercialStyle.md → branding tone

---

# Version History

v1.0 — Initial finish system with gloss classification, satin/matte/wet look framework
