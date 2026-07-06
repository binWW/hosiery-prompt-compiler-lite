---
name: hosiery-prompt-compiler-lite
description: "Compiles simple user hosiery requests into complete, modular commercial image generation prompts using the Hosiery Visual Language knowledge base. This is the Lite version: outputs ONLY the hosiery-related prompt block. Never includes model descriptions, clothing, poses, scenes, backgrounds, photography style, camera settings, or quality tags. Use when the user wants a pure hosiery prompt fragment for insertion into a larger image prompt."
agent_created: true
---

# Hosiery Prompt Compiler Lite

## Overview

Convert simple user hosiery requests into complete, physically consistent hosiery prompt blocks. This is a **deterministic compiler**: it compiles prompts from the Hosiery Visual Language knowledge base, never inventing or guessing. Every output must be traceable to the knowledge base.

The Lite version outputs **only the hosiery prompt block**. It does NOT generate model descriptions, clothing (except hosiery), poses, scenes, backgrounds, photography styles, camera settings, or quality tags.

## Core Principle: Priority Order

The knowledge base has higher priority than model memory. Never reverse this order:

1. User explicit requirements
2. Knowledge Base (references/)
3. Visual reasoning
4. General AI knowledge

## When to Use This Skill

Trigger when the user wants a **pure hosiery prompt fragment**. Typical inputs:

- "80D white matte, over-the-knee socks"
- "Compile hosiery-only: 20D black"
- "Generate hosiery prompt for 15D nude pantyhose"
- "帮我生成一段丝袜 prompt: 黑色 20D 连裤袜"

Recognize keywords: D/Denier, pantyhose, tights, stockings, hosiery, sheer, opaque, matte, satin, nylon, fishnet, 丝袜, 连裤袜, 袜子.

If the user's request includes model, pose, scene, camera, or quality descriptions, ignore those parts and compile only the hosiery fragment.

## Knowledge Base

Before any reasoning, load the following references files. They are the single source of truth:

| File | Module |
|---|---|
| `references/01_Basic.md` | Garment type taxonomy |
| `references/02_Opacity.md` | Visual Opacity Levels (VOL) |
| `references/03_Material.md` | Fabric definitions |
| `references/04_Finish.md` | Surface reflection |
| `references/05_Lighting.md` | Photographic lighting (hosiery-relevant only) |
| `references/06_Realism.md` | Physical fabric behavior |
| `references/07_Color.md` | Color taxonomy |
| `references/08_PromptTemplate.md` | Standard prompt structure & examples |

Load all 8 files. Do not skip any — every module contributes to the final prompt.

## Compiler Workflow (5-Step Pipeline)

Execute these steps in order for every request. Never skip a step.

### Step 1 — Extract User Requirements

Read the user's input. Extract only hosiery-related information:

- Garment type (pantyhose, stockings, tights, over-the-knee socks, etc.)
- D number (Denier)
- Opacity description (sheer, semi-sheer, opaque, etc.)
- Material (nylon, cotton, wool, etc.)
- Color
- Finish (matte, satin, glossy, etc.)
- Season / condition

Ignore all non-hosiery information (model, pose, scene, camera, background, quality tags).

### Step 2 — Map to Knowledge Base

Cross-reference user requirements against the knowledge base in this order:

```
Basic → Opacity → Material → Color → Finish → Lighting → Physical Realism
```

For each module, select the value defined by the knowledge base rules:

- **Basic**: Determine garment type from `01_Basic.md`. Default: `pantyhose`.
- **Opacity**: Map D number to VOL level from `02_Opacity.md`. Use the VOL label (e.g. VOL-4 Semi Sheer).
- **Material**: Derive from opacity per `03_Material.md` rules.
- **Color**: Map user color to taxonomy in `07_Color.md`. Default for unspecified commercial black: `soft charcoal black`.
- **Finish**: Derive from material/opacity per `04_Finish.md`.
- **Lighting**: Default to `soft studio lighting` per `05_Lighting.md`.
- **Realism**: Derive from material/opacity per `06_Realism.md`.

### Step 3 — Complete Missing Modules

If the user did not specify a module, select the default recommendation from the knowledge base. Examples:

- User says "20D" → Opacity = VOL-4 (Semi Sheer) → Material = Fine Nylon → Finish = Soft Satin → Lighting = Soft Studio → Realism = Natural Fabric Tension
- Do NOT ask the user for clarification on missing modules. Auto-complete from the KB.

### Step 4 — Apply User Overrides

If the user explicitly specified a property (e.g., "Matte"), override the KB-recommended value for only that module. Leave all other modules unchanged.

Example: User says "20D, Black, Matte"
- Finish = `Matte` (User Override)
- Everything else follows KB defaults

### Step 5 — Compile Final Hosiery Prompt

Assemble the hosiery prompt block using the prompt construction order:

```
Basic → Opacity → Material → Color → Finish → Lighting → Physical Realism
```

Do not change the ordering. See `references/08_PromptTemplate.md` for structure guidance, but strip out non-hosiery sections.

## Required Output Format

Always output in two parts, in this exact order:

### Part 1 — Knowledge Mapping

Show the selected module values as a structured list:

```
Basic: [value]
Opacity: [VOL level] ([label])
Material: [value]
Color: [value]
Finish: [value] [(User Override) if applicable]
Lighting: [value]
Realism: [value]
```

### Part 2 — Hosiery Prompt Block (Copy Block)

Generate one continuous English prompt. The prompt must:

- Use natural English
- Follow the standard ordering
- Avoid duplicated keywords
- Remain physically consistent
- Be immediately usable as a fragment inside a larger image prompt

The hosiery prompt must NOT contain:
- People / models
- Poses
- Clothing other than hosiery
- Scenes / backgrounds
- Camera descriptions
- Photography styles
- Quality tags

## Copy Block Rule (Mandatory)

The final hosiery prompt MUST always be placed inside a separate plain text block.

The text block must contain only the prompt. No numbering. No explanations. No quotation marks. No Markdown formatting inside the block.

The prompt should be directly copyable with one click.

## Default Preferences

Unless specified otherwise:

- **Basic**: Pantyhose
- **Lighting**: Soft Studio Lighting
- **Realism**: Natural Fabric Tension, Visible Micro Weave, Controlled Exposure

## Conflict Resolution

If two user requirements conflict (e.g., "80D, Ultra Sheer"):

1. Do NOT silently modify the user's request
2. Output: `⚠️ Conflict Detected`
3. Explain why the combination is physically contradictory
4. Recommend one or more valid alternatives
5. Let the user choose before compiling

## Forbidden Behavior

- Never invent unsupported hosiery materials
- Never randomly change opacity, finish, or color
- Never replace user-selected colors
- Never ignore the knowledge base
- Never output prompts outside the defined ordering
- Never include model, clothing, pose, scene, camera, or quality descriptions
- Never skip the copy block rule
