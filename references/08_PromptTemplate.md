# Hosiery Visual Language

## 08_PromptTemplate.md

Version: 1.0

---

# Purpose

This document defines the standard prompt construction workflow for the Hosiery Visual Language system.

Instead of writing prompts from scratch, every prompt should be assembled from reusable semantic blocks.

This modular approach improves:

* consistency
* controllability
* maintainability
* cross-model compatibility

Supported models include (but are not limited to):

* GPT Image
* Flux
* SDXL
* Imagen
* Midjourney

---

# Prompt Construction Pipeline

Every hosiery prompt should be built in the following order:

```text
Subject
↓

Basic

↓

Opacity

↓

Material

↓

Color

↓

Finish

↓

Lighting

↓

Physical Realism

↓

Pose

↓

Scene

↓

Camera

↓

Quality
```

This order reflects how modern image models typically interpret prompts—from subject identity to fine visual characteristics and finally photographic context.

---

# Core Semantic Blocks

---

## Block 1 — Subject

Defines the wearer.

Examples:

```text
young Asian woman
fashion model
commercial female model
editorial fashion model
```

---

## Block 2 — Basic Layer

Defines garment type.

Source:

01_Basic.md

Example:

```text
pantyhose
opaque tights
thigh-high stockings
fishnet tights
```

---

## Block 3 — Opacity Layer

Defines transparency.

Source:

02_Opacity.md

Example:

```text
ultra sheer
semi sheer
opaque
```

---

## Block 4 — Material Layer

Defines fabric.

Source:

03_Material.md

Example:

```text
fine nylon
microfiber
cotton knit
wool knit
```

---

## Block 5 — Color Layer

Defines perceived color.

Source:

07_Color.md

Example:

```text
soft charcoal black
natural nude
espresso brown
mist grey
```

---

## Block 6 — Finish Layer

Defines surface reflection.

Source:

04_Finish.md

Example:

```text
soft matte finish
satin finish
silky sheen
```

---

## Block 7 — Lighting Layer

Defines fabric illumination.

Source:

05_Lighting.md

Example:

```text
soft studio lighting
soft side lighting
gradient lighting
```

---

## Block 8 — Physical Realism Layer

Defines fabric behavior.

Source:

06_Realism.md

Example:

```text
body-conforming fit
natural fabric tension
micro weave detail
fine ankle wrinkles
```

---

## Block 9 — Pose

Defines body posture.

Examples:

```text
standing naturally
walking gracefully
crossed legs
weight shifted onto one hip
sitting elegantly
```

---

## Block 10 — Scene

Defines environment.

Examples:

```text
studio
luxury boutique
minimal interior
street fashion
office environment
hotel lobby
```

---

## Block 11 — Camera

Defines photographic style.

Examples:

```text
85mm lens
fashion photography
editorial composition
eye-level shot
full body portrait
```

---

## Block 12 — Quality

Defines rendering quality.

Examples:

```text
commercial advertising photography
photorealistic
high-end fashion campaign
realistic fabric texture
natural skin texture
```

---

# Standard Prompt Structure

Recommended universal template:

```text
[Subject],
[Basic],
[Opacity],
[Material],
[Color],
[Finish],
[Lighting],
[Physical Realism],
[Pose],
[Scene],
[Camera],
[Quality]
```

---

# Example A — Luxury Semi-Sheer Pantyhose

```text
young Asian fashion model,
pantyhose,
semi sheer,
fine nylon,
soft charcoal black,
soft satin finish,
soft side studio lighting,
body-conforming fit,
natural fabric tension,
smooth knee transition,
standing gracefully,
luxury boutique entrance,
85mm fashion photography,
commercial advertising photography,
photorealistic,
realistic fabric texture
```

---

# Example B — Opaque Winter Tights

```text
commercial female model,
opaque tights,
dense microfiber,
deep black,
soft matte finish,
soft studio lighting,
structured knit behavior,
subtle compression,
minimal ankle wrinkles,
standing naturally,
minimal studio background,
editorial fashion photography,
high-end commercial catalog
```

---

# Example C — Ultra Sheer Nude Pantyhose

```text
editorial fashion model,
pantyhose,
ultra sheer,
ultra-fine nylon,
natural nude,
soft silky sheen,
soft backlight,
body-conforming fit,
micro weave detail,
natural leg tension,
walking naturally,
luxury hotel interior,
85mm portrait lens,
premium commercial photography
```

---

# Prompt Assembly Rules

## Rule 1 — One selection per core block

Choose a single primary option from:

* Basic
* Opacity
* Material
* Color
* Finish

Avoid mixing multiple competing concepts.

---

## Rule 2 — Build from general to specific

Correct order:

```text
Garment

↓

Transparency

↓

Fabric

↓

Color

↓

Surface Finish

↓

Lighting

↓

Realism
```

---

## Rule 3 — Maintain physical consistency

Examples:

✔ Ultra sheer → fine nylon → silky sheen

✔ Opaque → microfiber → matte finish

Avoid:

❌ Ultra sheer → wool knit

❌ Cotton knit → wet look

❌ Opaque → transparent veil

---

## Rule 4 — Let the camera enhance, not replace

Lighting and camera should reinforce the material rather than compensate for missing fabric descriptions.

---

# Model Adaptation Notes

## GPT Image

* Responds well to natural language.
* Benefits from descriptive phrases instead of keyword repetition.
* Use complete visual descriptions.

---

## Flux

* Prefers concise semantic blocks.
* Avoid excessive repetition.
* Keep each block focused.

---

## SDXL

* Sensitive to prompt order.
* Keep the pipeline consistent.
* Add quality descriptors near the end.

---

# Checklist

Before finalizing a prompt, verify:

✔ Garment type defined

✔ Opacity defined

✔ Material defined

✔ Color defined

✔ Finish defined

✔ Lighting defined

✔ Physical realism included

✔ Pose included

✔ Scene included

✔ Camera included

✔ Quality descriptors included

---

# Version History

v1.0 — Initial modular prompt assembly framework for the Hosiery Visual Language system.
