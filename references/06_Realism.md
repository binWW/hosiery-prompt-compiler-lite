# Hosiery Visual Language

## 06_Realism.md

Version: 1.0

---

# Purpose

The Realism Layer defines the physical behavior of hosiery after it is worn on the human body.

Unlike Material or Finish, this layer does not describe the fabric itself.

Instead, it describes how the fabric behaves under tension, gravity, anatomy, movement, and photography.

This layer is responsible for transforming a synthetic-looking render into a believable commercial photograph.

---

# AI Interpretation Priority

When rendering physical realism, AI models generally prioritize:

1. Fabric tension
2. Body conformity
3. Compression behavior
4. Wrinkle formation
5. Highlight distribution
6. Edge transitions

---

# Physical Behavior System

---

## 1. Skin Conformity

The fabric should closely follow the natural anatomy of the leg.

Core Keywords

```text id="sk01"
second-skin fit
body-conforming fabric
close-fitting hosiery
natural body contour
anatomically fitted
```

Visual Characteristics

* follows leg shape naturally
* no floating fabric
* continuous surface
* realistic body contact

---

## 2. Fabric Tension

Hosiery is always under stretch.

Core Keywords

```text id="tn01"
natural fabric tension
elastic stretch
uniform tension
realistic stretch distribution
body tension
```

Visual Characteristics

* slight tension across thighs
* stretched over knees
* smooth calf transition
* gentle ankle compression

---

## 3. Compression Behavior

The fabric compresses soft tissue slightly.

Core Keywords

```text id="cp01"
subtle compression
gentle shaping effect
soft leg contour enhancement
light compression fit
```

Visual Characteristics

* slightly slimmer appearance
* natural contour definition
* realistic compression around calves
* no exaggerated shaping

---

## 4. Wrinkle Formation

Wrinkles only appear where fabric naturally relaxes.

Core Keywords

```text id="wr01"
fine ankle wrinkles
subtle fabric folds
natural compression folds
micro fabric creases
```

Visual Characteristics

* light wrinkles at ankles
* slight folds behind knees
* almost invisible elsewhere
* no random folding

---

## 5. Joint Transition

Fabric stretches differently across joints.

Core Keywords

```text id="jt01"
smooth knee transition
natural elbow-like curvature
fabric stretched across joints
continuous surface transition
```

Visual Characteristics

* tighter over knees
* softer behind knees
* natural bending response
* continuous stretch

---

## 6. Highlight Behavior

Highlights should follow anatomy.

Core Keywords

```text id="hl01"
anatomically correct highlights
natural specular flow
soft leg reflections
directional fabric highlights
```

Visual Characteristics

* highlight follows shin
* softer reflection on calves
* reduced highlight near ankles
* no random shine patches

---

## 7. Edge Transition

The transition between hosiery and exposed skin should be realistic.

Core Keywords

```text id="ed01"
clean edge transition
natural fabric boundary
smooth skin transition
realistic garment edge
```

Visual Characteristics

* seamless waist transition
* clean stocking top
* realistic sock edge
* no floating borders

---

## 8. Fabric Micro Detail

Tiny details improve realism dramatically.

Core Keywords

```text id="mc01"
micro weave detail
fine knit texture
visible fiber structure
subtle textile grain
```

Visual Characteristics

* visible only upon close inspection
* never exaggerated
* consistent across the leg

---

# Motion Behavior

When posing dynamically:

Include:

```text id="mv01"
fabric responds naturally to movement
stretch follows leg motion
wrinkles increase near bending joints
elastic tension remains consistent
```

---

# Footwear Interaction

If shoes are visible:

Include:

```text id="ft01"
natural compression around shoe opening
fabric smoothly enters footwear
no clipping
no floating fabric
```

---

# Garment Interaction

If wearing skirts or dresses:

Include:

```text id="gm01"
natural draping interaction
fabric remains smooth beneath clothing
no unrealistic intersections
```

---

# Realism Intensity

Low

```text id="ri01"
clean commercial appearance
minimal wrinkles
smooth surface
```

Medium

```text id="ri02"
subtle textile detail
visible fabric behavior
natural compression
```

High

```text id="ri03"
micro wrinkle detail
fine weave visibility
high physical realism
anatomically correct fabric response
```

---

# Common Mistakes

❌ Random wrinkles across the thigh

❌ Floating fabric separated from skin

❌ Perfectly smooth legs with no tension

❌ Overly strong compression causing unrealistic anatomy

❌ Identical highlights on every part of the leg

---

# Best Practice Prompt Pattern

Recommended final pipeline:

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
[Physical Realism]
```

Example:

```text id="bp02"
sheer pantyhose
fine nylon
soft satin finish
soft side studio lighting
natural fabric tension
fine ankle wrinkles
smooth knee transition
body-conforming fit
micro weave detail
```

---

# System Role

Physical Realism Layer completes the Hosiery Visual Language.

It transforms descriptive prompts into physically believable hosiery imagery suitable for commercial advertising, editorial photography, and high-end fashion visualization.

---

# Version History

v1.0 — Initial release of the Physical Realism specification.
