# Hosiery Visual Language

## 02_Opacity.md

Version: 1.0

---

# Purpose

Opacity is the most important visual property of hosiery.

AI image models do not truly understand Denier (D). They understand visual appearance.

This document defines opacity by visual characteristics instead of manufacturing specifications.

Every prompt should describe:

* Skin Visibility
* Fabric Visibility
* Overall Coverage
* Transparency
* Light Transmission

instead of relying only on Denier values.

---

# AI Interpretation Priority

When describing opacity, AI models generally prioritize the following information:

1. Skin Visibility
2. Transparency
3. Fabric Visibility
4. Overall Coverage
5. Denier Value

Therefore:

❌ black 20D tights

is weaker than

✅ semi sheer black pantyhose with natural skin visible underneath

---

# Visual Opacity Levels (VOL)

---

# VOL-0

Bare Legs

Approximate Denier

None

Visual Description

No hosiery.

Natural skin texture remains fully visible.

No fabric layer.

Skin Visibility

★★★★★

Fabric Visibility

☆☆☆☆☆

Coverage

None

Core Keywords

```
bare legs
no hosiery
natural skin
natural skin tone
visible pores
```

Support Keywords

```
real skin texture
natural leg appearance
healthy skin
```

Optional Keywords

```
subtle skin imperfections
natural color variation
```

---

# VOL-1

Ultra Sheer

Approximate Denier

5D

Visual Description

Almost invisible.

The fabric should disappear visually.

Only a very slight enhancement of skin tone.

Skin Visibility

★★★★★

Fabric Visibility

★☆☆☆☆

Coverage

Minimal

Core Keywords

```
ultra sheer
barely-there
nearly invisible
almost transparent
second-skin appearance
```

Support Keywords

```
crystal clear
extremely lightweight
natural skin completely visible
barely noticeable fabric
```

Optional Keywords

```
air-light nylon
transparent veil
delicate appearance
```

---

# VOL-2

Very Sheer

Approximate Denier

8D–10D

Visual Description

Skin remains clearly visible.

Fabric becomes slightly noticeable.

Legs appear smoother.

Skin Visibility

★★★★★

Fabric Visibility

★★☆☆☆

Coverage

Very Light

Core Keywords

```
very sheer
light transparent veil
natural transparency
clear skin visibility
```

Support Keywords

```
subtle skin enhancement
slight tone correction
lightweight nylon
barely visible weave
```

Optional Keywords

```
soft silky appearance
smooth transparency
clean finish
```

---

# VOL-3

Sheer

Approximate Denier

12D–15D

Visual Description

Clearly recognizable as pantyhose.

Skin remains dominant.

Fabric begins defining the leg shape.

Skin Visibility

★★★★☆

Fabric Visibility

★★★☆☆

Coverage

Light

Core Keywords

```
sheer
light coverage
soft transparency
visible nylon texture
```

Support Keywords

```
natural leg enhancement
slightly softened skin
light fabric presence
```

Optional Keywords

```
delicate weave
refined appearance
balanced transparency
```

---

# VOL-4

Semi Sheer

Approximate Denier

18D–20D

Visual Description

Classic everyday pantyhose.

Transparency and coverage are balanced.

Skin remains visible while fabric becomes more obvious.

Skin Visibility

★★★★☆

Fabric Visibility

★★★★☆

Coverage

Balanced

Core Keywords

```
semi sheer
balanced transparency
light opacity
natural leg shaping
```

Support Keywords

```
soft smoothing
even skin tone
subtle fabric presence
```

Optional Keywords

```
delicate nylon weave
clean appearance
light diffusion
```

---

# VOL-5

Medium Opacity

Approximate Denier

30D–40D

Visual Description

Skin visibility is reduced.

Fabric becomes dominant.

Leg color becomes more uniform.

Skin Visibility

★★★☆☆

Fabric Visibility

★★★★☆

Coverage

Medium

Core Keywords

```
medium opacity
partially opaque
moderately dense
uniform appearance
```

Support Keywords

```
smooth finish
reduced transparency
soft coverage
```

Optional Keywords

```
microfiber appearance
fine knit texture
```

---

# VOL-6

Mostly Opaque

Approximate Denier

50D–60D

Visual Description

Skin is barely visible.

Fabric dominates the appearance.

Suitable for cooler seasons.

Skin Visibility

★★☆☆☆

Fabric Visibility

★★★★★

Coverage

High

Core Keywords

```
mostly opaque
minimal transparency
dense appearance
full leg coverage
```

Support Keywords

```
soft microfiber
smooth fabric surface
thicker material
```

Optional Keywords

```
winter fashion
comfortable texture
```

---

# VOL-7

Opaque

Approximate Denier

70D–80D

Visual Description

Classic opaque tights.

Skin is almost completely hidden.

Only body contour remains visible.

Skin Visibility

★☆☆☆☆

Fabric Visibility

★★★★★

Coverage

Very High

Core Keywords

```
opaque
deep black
solid coverage
fully covered legs
```

Support Keywords

```
minimal skin visibility
dense knit
soft matte appearance
```

Optional Keywords

```
clean silhouette
uniform black finish
```

---

# VOL-8

Fully Opaque

Approximate Denier

100D–120D+

Visual Description

Heavy winter tights.

No visible skin.

Dense fabric completely covers the legs.

Skin Visibility

☆☆☆☆☆

Fabric Visibility

★★★★★

Coverage

Maximum

Core Keywords

```
fully opaque
dense fabric
heavy knit
complete coverage
```

Support Keywords

```
winter tights
thick microfiber
zero transparency
```

Optional Keywords

```
thermal appearance
soft winter texture
```

---

# Skin Visibility Reference

| VOL   | Visible Skin |
| ----- | ------------ |
| VOL-0 | 100%         |
| VOL-1 | 98%          |
| VOL-2 | 92%          |
| VOL-3 | 82%          |
| VOL-4 | 70%          |
| VOL-5 | 50%          |
| VOL-6 | 20%          |
| VOL-7 | 5%           |
| VOL-8 | 0%           |

---

# Prompt Combination Rule

Opacity should always be combined with:

```
Basic
+
Material
+
Finish
+
Lighting
+
Realism
```

Never use opacity alone.

Example

```
semi sheer
fine nylon
soft satin sheen
controlled specular highlights
natural stretch around the knees
```

---

# Best Practices

Prefer describing visual appearance.

Good

```
semi sheer black pantyhose

natural skin visible underneath

balanced transparency

fine nylon weave

soft matte finish
```

Avoid

```
20D tights
```

Good

```
opaque black tights

dense knit texture

minimal transparency

fully covered legs
```

Avoid

```
80D tights
```

---

# Common Mistakes

❌ Only describing Denier.

❌ Using transparency without describing skin visibility.

❌ Combining "ultra sheer" with "fully opaque."

❌ Mixing incompatible descriptions such as:

```
almost transparent

heavy knit
```

❌ Forgetting that lighting strongly affects perceived opacity.

---

# Version History

v1.0

Initial release of the Visual Opacity Level (VOL) specification.
