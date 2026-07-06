# Hosiery Prompt Compiler Lite

> A deterministic prompt compiler for hosiery image generation — hosiery fragment only.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![WorkBuddy Skill](https://img.shields.io/badge/WorkBuddy-Skill-blue)](https://www.codebuddy.cn)

---

## Overview

**Hosiery Prompt Compiler Lite** is a WorkBuddy skill that converts simple hosiery descriptions into physically consistent, ready-to-use hosiery prompt blocks for AI image generation.

It acts as a **deterministic compiler**, not a creative writer. Every output is assembled from the [Hosiery Visual Language Knowledge Base](references/) — a curated taxonomy of hosiery types, opacity levels, materials, finishes, colors, lighting, and physical realism rules. The compiler never invents or guesses; every output is traceable to the knowledge base.

### Lite vs Full

| Feature | Lite | Full ([hosiery-prompt-compiler](https://github.com)) |
|---------|------|------|
| Hosiery fragment | ✅ | ✅ |
| Model / Subject | ❌ | ✅ |
| Pose | ❌ | ✅ |
| Scene / Background | ❌ | ✅ |
| Camera settings | ❌ | ✅ |
| Quality tags | ❌ | ✅ |
| Reasoning output | ❌ | ✅ |
| Clean copy block | ✅ | ✅ |

**Lite outputs only the hosiery prompt fragment** — perfect as a building block to drop into larger prompts.

---

## Quick Example

**Input:**
```
80D white matte, over-the-knee socks
```

**Output (Knowledge Mapping):**

```
Basic: over-the-knee socks
Opacity: VOL-7 (Opaque)
Material: dense knit microfiber
Color: soft white
Finish: soft matte finish (User Override)
Lighting: soft studio lighting
Realism: natural fabric tension, knit structure
```

**Output (Copy Block):**

```
over-the-knee socks, opaque, dense knit microfiber, soft white, soft matte finish, soft studio lighting, natural fabric tension, visible knit structure
```

---

## Features

- **Deterministic compilation** — same input always produces the same output
- **Knowledge-base driven** — 8 reference modules covering every aspect of hosiery appearance
- **Physical consistency** — detects and prevents impossible material/opacity/finish combinations
- **Auto-completion** — fills in missing attributes from KB defaults (no unnecessary questions)
- **User override support** — explicitly specified properties always take priority
- **Clean output** — hosiery fragment only, no model/pose/scene/camera/quality noise
- **One-click copy** — final prompt in a dedicated plain text block

---

## Installation

### Prerequisites

- [WorkBuddy](https://www.codebuddy.cn) installed

### Install from Marketplace

Open WorkBuddy and run:

```
/install hosiery-prompt-compiler-lite
```

### Manual Install

1. Download the latest `hosiery-prompt-compiler-lite.zip` from [Releases](https://github.com)
2. Extract to `~/.workbuddy/skills/hosiery-prompt-compiler-lite/` (user-level) or `.workbuddy/skills/hosiery-prompt-compiler-lite/` (project-level)

### Verify

Restart WorkBuddy, then type a test prompt:
```
80D black pantyhose
```

---

## Usage

Simply describe the hosiery you want in natural language. The skill triggers automatically when it detects hosiery-related keywords.

### Trigger Keywords

D/Denier, pantyhose, tights, stockings, hosiery, sheer, opaque, matte, satin, nylon, fishnet, 丝袜, 连裤袜, 袜子

### Examples

```
20D black pantyhose
```
```
15D nude pantyhose, satin finish
```
```
80D opaque tights, winter, matte
```
```
ultra sheer natural nude stockings
```
```
dense cotton over-the-knee socks, cream white
```

> **Note:** If your input includes model descriptions, poses, scenes, or camera settings, the compiler silently ignores them and outputs only the hosiery fragment.

---

## How It Works

The compiler follows a **5-step deterministic pipeline**:

```
Step 1: Extract     → Parse user input for hosiery-related attributes
Step 2: Map         → Cross-reference against the 8-module knowledge base
Step 3: Complete    → Fill missing attributes from KB defaults
Step 4: Override    → Apply any user-explicit overrides
Step 5: Compile     → Assemble into the final prompt block
```

### Knowledge Base Modules

| # | Module | Content |
|---|--------|---------|
| 01 | **Basic** | Garment type taxonomy (pantyhose, stockings, tights, etc.) |
| 02 | **Opacity** | Visual Opacity Levels (VOL 1-7), from invisible to solid |
| 03 | **Material** | Fabric definitions (nylon, microfiber, cotton, wool, etc.) |
| 04 | **Finish** | Surface reflection (matte, satin, glossy, silky, etc.) |
| 05 | **Lighting** | Photographic lighting configurations |
| 06 | **Realism** | Physical fabric behavior (tension, wrinkles, weave detail) |
| 07 | **Color** | Color taxonomy with nuanced commercial names |
| 08 | **Template** | Standard prompt construction order and examples |

### Priority System

```
1. User explicit requirements   ← Highest
2. Knowledge Base rules
3. Visual reasoning
4. General AI knowledge         ← Lowest
```

---

## Output Format

Every compilation produces **two sections**:

### Part 1 — Knowledge Mapping

A structured list showing which KB values were selected for each module:

```
Basic: [value]
Opacity: [VOL level] ([label])
Material: [value]
Color: [value]
Finish: [value] [(User Override) if applicable]
Lighting: [value]
Realism: [value]
```

### Part 2 — Copy Block

The final hosiery prompt in a plain text block. No formatting, no explanations — copy and paste directly into your image generation workflow.

---

## Conflict Resolution

If the user requests a physically impossible combination, the compiler does NOT silently modify it. Instead it:

1. Outputs `⚠️ Conflict Detected`
2. Explains why the combination is contradictory
3. Recommends valid alternatives
4. Waits for user choice before compiling

**Example conflict:** `80D, Ultra Sheer` — 80 Denier is opaque, cannot be ultra sheer simultaneously.

---

## Directory Structure

```
hosiery-prompt-compiler-lite/
├── SKILL.md                         # Compiler instructions (WorkBuddy reads this)
├── README.md                        # This file
├── README_CN.md                     # Chinese version
└── references/                      # Hosiery Visual Language Knowledge Base
    ├── 01_Basic.md                  # Garment type taxonomy
    ├── 02_Opacity.md                # Visual Opacity Levels
    ├── 03_Material.md               # Fabric definitions
    ├── 04_Finish.md                 # Surface reflection
    ├── 05_Lighting.md               # Photographic lighting
    ├── 06_Realism.md                # Physical fabric behavior
    ├── 07_Color.md                  # Color taxonomy
    └── 08_PromptTemplate.md         # Prompt structure & examples
```

---

## Supported Models

The compiled prompts work with all major image generation models:

- GPT Image
- Flux
- SDXL / Stable Diffusion
- Midjourney
- Imagen
- DALL-E

---

## Contributing

Contributions are welcome. To improve the knowledge base:

1. Fork the repository
2. Edit the relevant `references/` file
3. Ensure physical consistency rules are maintained
4. Submit a pull request

### Improving the Compiler

To modify the compilation logic, edit `SKILL.md`. The file follows the [WorkBuddy Skill specification](https://www.codebuddy.cn/docs/workbuddy).

---

## License

MIT © 2026

---

*Built for [WorkBuddy](https://www.codebuddy.cn) — the AI assistant that gets things done.*
