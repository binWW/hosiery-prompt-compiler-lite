# Hosiery Visual Language

## 01_Basic.md

Version: 1.0

---

# Purpose

The Basic Layer defines what type of hosiery is being described.

It is the foundation of every prompt.

Before describing:

* opacity
* material
* finish
* lighting

you must first define the **garment type**.

AI models respond best when garment identity is explicit and unambiguous.

---

# AI Interpretation Priority

When interpreting hosiery-related prompts, AI models prioritize:

1. Garment Type (Basic Layer)
2. Opacity (Visibility)
3. Material (Fabric Structure)
4. Finish (Surface Reflection)
5. Lighting (Photography)

If Basic Layer is unclear, all downstream layers become unstable.

---

# Hosiery Type Categories

## 1. Pantyhose System

Full-leg coverage from waist to toes.

### Types

```id="p1b9kq"
pantyhose
tights
sheer pantyhose
opaque pantyhose
control-top pantyhose
high-waist tights
seamless pantyhose
```

### Description Rules

* Covers entire leg and waist
* Unified fabric appearance
* Most common commercial category

---

## 2. Stockings System

Upper leg coverage only, usually thigh-high.

### Types

```id="x7v2qp"
stockings
thigh-high stockings
hold-up stockings
lace-top stockings
silicone band stockings
```

### Description Rules

* Ends mid-thigh
* Often paired with garter or silicone grip
* Creates visible skin transition at upper thigh

---

## 3. Socks-Based Hosiery

Lower-leg focused hosiery variants.

### Types

```id="k9d2lm"
knee-high socks
over-the-knee socks
ankle socks (fashion hosiery context)
```

### Description Rules

* Does not fully cover thigh
* Focus on lower leg silhouette
* Often fashion-oriented rather than formal wear

---

## 4. Sheer Stockings System

Lightweight transparent legwear.

### Types

```id="q3n8xv"
sheer stockings
ultra sheer stockings
transparent pantyhose
invisible tights
barely-there tights
```

### Description Rules

* High skin visibility
* Designed to enhance natural leg appearance
* Used in fashion/editorial photography

---

## 5. Opaque Tights System

Heavy coverage hosiery.

### Types

```id="z8t4ld"
opaque tights
black tights
winter tights
thermal tights
microfiber tights
```

### Description Rules

* Low or no skin visibility
* Strong fabric dominance
* Seasonal fashion usage (autumn/winter)

---

## 6. Patterned / Decorative Hosiery

Hosiery with visual design elements.

### Types

```id="f2m7rk"
fishnet tights
patterned tights
lace tights
striped tights
polka-dot tights
embroidered tights
```

### Description Rules

* Texture is part of visual identity
* Pattern overrides material subtlety
* Often fashion/editorial focused

---

## 7. Seamless / Invisible System

Minimal visual structure hosiery.

### Types

```id="v6c9st"
seamless pantyhose
invisible tights
second-skin tights
ultra-thin tights
```

### Description Rules

* No visible seams
* Designed to simulate bare skin
* Often used in beauty advertising

---

# Combination Rule with Opacity Layer

Basic Layer MUST always be combined with Opacity Layer.

Example:

Good

```id="b2k8mn"
sheer pantyhose
ultra sheer
natural skin visible underneath
```

Good

```id="l9x4pq"
opaque tights
deep black
fully covered legs
dense knit texture
```

Bad

```id="c7v1sd"
tights
```

(too vague, unstable output)

---

# Prompt Construction Order

When building prompts:

### Step 1 — Basic Layer (REQUIRED)

Define garment type

### Step 2 — Opacity Layer (REQUIRED)

Define transparency

### Step 3 — Material Layer

Define fabric

### Step 4 — Finish Layer

Define surface reflection

### Step 5 — Photography Layer

Define lighting and composition

---

# Recommended Core Structure

```id="m4t8lp"
[Basic Type]
+
[Opacity Level]
+
[Material]
+
[Finish]
+
[Lighting]
+
[Realism Details]
```

---

# Best Practices

✔ Always explicitly state hosiery type first
✔ Prefer “pantyhose / tights / stockings” over generic “leggings”
✔ Match Basic type with correct opacity expectations
✔ Use “stockings” only when thigh is visible
✔ Use “tights” when full leg coverage is intended

---

# Common Mistakes

❌ Using “tights” for thigh-high visuals
❌ Mixing stockings and pantyhose in same prompt
❌ Omitting garment type entirely
❌ Using fashion terms like “leggings” for hosiery (creates wrong structure)
❌ Combining incompatible systems:

```id="x3k9vp"
pantyhose
thigh-high stockings
```

---

# System Dependency Map

Basic Layer connects to:

* 02_Opacity.md → transparency behavior
* 03_Material.md → fabric realism
* 04_Finish.md → surface reflection
* 05_Color.md → visual tone
* 06_Lighting.md → photographic realism

---

# Version History

v1.0

Initial release of Hosiery Basic Layer taxonomy.
