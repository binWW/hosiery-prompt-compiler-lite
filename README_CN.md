# Hosiery Prompt Compiler Lite

> 一套确定性的丝袜图像生成提示词编译器 —— 仅输出丝袜片段。

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![WorkBuddy Skill](https://img.shields.io/badge/WorkBuddy-Skill-blue)](https://www.codebuddy.cn)

[English](README.md) | **中文**

---

## 概述

**Hosiery Prompt Compiler Lite** 是一个 WorkBuddy 技能，能将简单的丝袜描述转化为物理一致的、开箱即用的丝袜提示词片段，用于 AI 图像生成。

它的定位是**确定性编译器**，而非创意写作工具。每个输出都基于 [Hosiery Visual Language 知识库](references/) 组装 —— 这是一个涵盖丝袜类型、透明度等级、面料、表面光泽、颜色、灯光和物理真实感的精细分类体系。编译器绝不凭空编造或猜测，每个输出都可追溯到知识库。

### Lite 版与完整版的区别

| 特性 | Lite 版 | 完整版 ([hosiery-prompt-compiler](https://github.com)) |
|------|---------|------|
| 丝袜片段 | ✅ | ✅ |
| 模特 / 主体 | ❌ | ✅ |
| 姿势 | ❌ | ✅ |
| 场景 / 背景 | ❌ | ✅ |
| 相机参数 | ❌ | ✅ |
| 质量标签 | ❌ | ✅ |
| 推理说明 | ❌ | ✅ |
| 纯文本复制块 | ✅ | ✅ |

**Lite 版只输出丝袜提示词片段** —— 作为可直接嵌入更大 prompt 的积木块。

---

## 快速示例

**输入：**
```
80D 白色 哑光 过膝袜
```

**输出（知识映射）：**

```
Basic: over-the-knee socks
Opacity: VOL-7 (Opaque)
Material: dense knit microfiber
Color: soft white
Finish: soft matte finish (User Override)
Lighting: soft studio lighting
Realism: natural fabric tension, knit structure
```

**输出（复制块）：**

```
over-the-knee socks, opaque, dense knit microfiber, soft white, soft matte finish, soft studio lighting, natural fabric tension, visible knit structure
```

---

## 核心特性

- **确定性编译** —— 相同输入永远产生相同输出
- **知识库驱动** —— 8 个参考模块覆盖丝袜外观的每个维度
- **物理一致性校验** —— 自动检测并阻止不可能的面料/透明度/光泽组合
- **智能补全** —— 未指定属性自动从知识库默认值填充（不问多余问题）
- **用户覆盖优先** —— 用户明确指定的属性始终具有最高优先级
- **纯净输出** —— 仅丝袜片段，不含模特/姿势/场景/相机/质量等干扰信息
- **一键复制** —— 最终 prompt 置于独立纯文本块中

---

## 安装

### 前置条件

- 已安装 [WorkBuddy](https://www.codebuddy.cn)

### 手动安装

1. 从 [Releases](https://github.com) 下载最新的 `hosiery-prompt-compiler-lite.zip`
2. 解压到 `~/.workbuddy/skills/hosiery-prompt-compiler-lite/`（用户级）或 `.workbuddy/skills/hosiery-prompt-compiler-lite/`（项目级）

### 验证安装

重启 WorkBuddy，然后输入测试 prompt：
```
80D 黑色 连裤袜
```

---

## 使用方法

用自然语言描述你想要的丝袜效果即可。当输入中包含丝袜相关关键词时，技能会自动触发。

### 触发关键词

D/Denier、pantyhose、tights、stockings、hosiery、sheer、opaque、matte、satin、nylon、fishnet、丝袜、连裤袜、袜子、过膝袜、中筒袜

### 使用示例

```
20D 黑色 连裤袜
```
```
15D 肤色 连裤袜 缎面光泽
```
```
80D 不透肉 打底袜 冬季 哑光
```
```
超薄 自然肤色 长筒袜
```
```
厚棉 过膝袜 奶白色
```

> **注意：** 如果输入中包含模特描述、姿势、场景或相机设置，编译器会静默忽略这些信息，仅输出丝袜片段。

---

## 工作原理

编译器遵循**5 步确定性流水线**：

```
第 1 步：提取     → 解析用户输入，提取丝袜相关属性
第 2 步：映射     → 与 8 模块知识库交叉匹配
第 3 步：补全     → 从知识库默认值填充缺失属性
第 4 步：覆盖     → 应用用户明确指定的覆盖值
第 5 步：编译     → 组装最终 prompt 片段
```

### 知识库模块

| # | 模块 | 内容 |
|---|------|------|
| 01 | **基础层 (Basic)** | 袜型分类（连裤袜、长筒袜、打底袜等） |
| 02 | **透明度 (Opacity)** | 视觉透明度等级（VOL 1-7），从隐现到完全不透 |
| 03 | **面料 (Material)** | 面料定义（尼龙、超细纤维、棉、羊毛等） |
| 04 | **光泽 (Finish)** | 表面反光（哑光、缎面、亮光、丝光等） |
| 05 | **灯光 (Lighting)** | 摄影布光配置 |
| 06 | **真实感 (Realism)** | 物理面料行为（张力、褶皱、织纹细节） |
| 07 | **颜色 (Color)** | 色彩分类（含精细的商业摄影命名） |
| 08 | **模板 (Template)** | 标准 prompt 构造顺序与范例 |

### 优先级体系

```
1. 用户明确需求     ← 最高
2. 知识库规则
3. 视觉推理
4. 通用 AI 知识     ← 最低
```

---

## 输出格式

每次编译输出分为**两部分**：

### 第一部分 —— 知识映射

展示每个模块所选值的结构化列表：

```
Basic: [值]
Opacity: [VOL 等级] ([标签])
Material: [值]
Color: [值]
Finish: [值] [(User Override) 标记用户覆盖项]
Lighting: [值]
Realism: [值]
```

### 第二部分 —— 复制块

最终丝袜 prompt，置于纯文本块中。无格式、无解释 —— 直接复制粘贴到你的图像生成工作流中。

---

## 冲突处理

当用户请求物理上不可能的组合时，编译器不会静默修改。处理流程：

1. 输出 `⚠️ Conflict Detected`
2. 解释为何该组合相互矛盾
3. 推荐有效的替代方案
4. 等待用户选择后继续编译

**冲突示例：** `80D 超薄` —— 80 丹尼属于不透肉等级，无法同时为超薄。

---

## 目录结构

```
hosiery-prompt-compiler-lite/
├── SKILL.md                         # 编译器指令（WorkBuddy 读取此文件）
├── README.md                        # 英文说明文档
├── README_CN.md                     # 中文说明文档（本文件）
└── references/                      # Hosiery Visual Language 知识库
    ├── 01_Basic.md                  # 袜型分类
    ├── 02_Opacity.md                # 视觉透明度等级
    ├── 03_Material.md               # 面料定义
    ├── 04_Finish.md                 # 表面反光
    ├── 05_Lighting.md               # 摄影灯光
    ├── 06_Realism.md                # 物理面料行为
    ├── 07_Color.md                  # 颜色分类
    └── 08_PromptTemplate.md         # prompt 结构与范例
```

---

## 支持的模型

编译生成的 prompt 兼容所有主流图像生成模型：

- GPT Image
- Flux
- SDXL / Stable Diffusion
- Midjourney
- Imagen
- DALL-E

---

## 参与贡献

欢迎贡献。如需改进知识库：

1. Fork 本仓库
2. 编辑对应的 `references/` 文件
3. 确保物理一致性规则不被破坏
4. 提交 Pull Request

### 修改编译器逻辑

编辑 `SKILL.md` 来调整编译逻辑。该文件遵循 [WorkBuddy Skill 规范](https://www.codebuddy.cn/docs/workbuddy)。

---

## 许可证

MIT © 2026

---

*为 [WorkBuddy](https://www.codebuddy.cn) 构建 —— 让 AI 助手真正能干活。*
