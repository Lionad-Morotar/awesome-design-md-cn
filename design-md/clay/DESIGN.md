# Design System: Clay

## 1. Visual Theme & Atmosphere

Clay 的网站是一场温暖而俏皮的色彩庆典，它将 B2B 数据丰富视为一种工艺，而非企业的繁琐任务。设计语言建立在温暖的奶油色背景（`#faf9f7`）和燕麦色调的边框（`#dad4c8`、`#eee9df`）之上，赋予每个表面如手工纸般的触感质地。在这幅工艺画布上，一组生动的色板调色板迸发出个性——Matcha 绿、Slushie 青、Lemon 金、Ube 紫、Pomegranate 粉、Blueberry 藏青和 Dragonfruit 玫红——每种颜色的命名都像是果汁吧的风味，而非企业 UI 套件中的色值。

字体排印以 Roobert 为核心，这是一款富有特色的几何无衬线字体，加载了广泛的 OpenType 风格集（`"ss01"`、`"ss03"`、`"ss10"`、`"ss11"`、`"ss12"`），赋予文本独特而略带俏皮的个性。在展示尺度（80px，字重 600）下，Roobert 使用激进的负字母间距（-3.2px），将标题压缩成如广告牌般有力的陈述。Space Mono 作为等宽字体的伴侣，用于代码和技术标签，完成了工艺与科技的双重性。

Clay 真正独特之处在于其悬停微动画：按钮在悬停时轻微旋转（`rotateZ(-8deg)`）、向上平移（`translateY(-80%)`）、背景变为对比鲜明的色板颜色，并投射出硬朗的偏移阴影（`rgb(0,0,0) -7px 7px`）。这种俏皮的悬停行为——按钮在交互时 literally 倾斜并跳跃——营造出一种在 B2B 软件中罕见的物理愉悦感。结合 generously 圆角容器（24px–40px 半径）、虚线边框与实线边框并存，以及包含内嵌高光的多层阴影系统，Clay 感觉像是一个由真正享受创造事物的人所打造的设计系统。

**Key Characteristics:**
- 温暖奶油画布（`#faf9f7`）配燕麦色调边框（`#dad4c8`）——工艺感，非临床感
- 命名色板调色板：Matcha、Slushie、Lemon、Ube、Pomegranate、Blueberry、Dragonfruit
- Roobert 字体配 5 组 OpenType 风格集——俏皮的几何个性
- 俏皮悬停动画：rotateZ(-8deg) + translateY(-80%) + 硬朗偏移阴影
- Space Mono 用于代码和技术标签
- generous 边框半径：12px 卡片、40px 区块、1584px 药丸
- 混合边框样式：同一界面中实线与虚线并存
- 多层阴影带内嵌高光：`0px 1px 1px` + `-1px inset` + `-0.5px`

## 2. Color Palette & Roles

### Primary
- **Clay Black** (`#000000`): 文本、标题、定价卡片文本、`--_theme--pricing-cards---text`
- **Pure White** (`#ffffff`): 卡片背景、按钮背景、反色文本
- **Warm Cream** (`#faf9f7`): 页面背景——温暖、如纸张般的画布

### Swatch Palette — Named Colors

**Matcha (Green)**
- **Matcha 300** (`#84e7a5`): `--_swatches---color--matcha-300`，浅绿强调色
- **Matcha 600** (`#078a52`): `--_swatches---color--matcha-600`，中绿
- **Matcha 800** (`#02492a`): `--_swatches---color--matcha-800`，深绿用于深色区块

**Slushie (Cyan)**
- **Slushie 500** (`#3bd3fd`): `--_swatches---color--slushie-500`，亮青强调色
- **Slushie 800** (`#0089ad`): `--_swatches---color--slushie-800`，深青绿

**Lemon (Gold)**
- **Lemon 400** (`#f8cc65`): `--_swatches---color--lemon-400`，暖淡金
- **Lemon 500** (`#fbbd41`): `--_swatches---color--lemon-500`，主金
- **Lemon 700** (`#d08a11`): `--_swatches---color--lemon-700`，深琥珀
- **Lemon 800** (`#9d6a09`): `--_swatches---color--lemon-800`，暗琥珀

**Ube (Purple)**
- **Ube 300** (`#c1b0ff`): `--_swatches---color--ube-300`，柔和薰衣草
- **Ube 800** (`#43089f`): `--_swatches---color--ube-800`，深紫
- **Ube 900** (`#32037d`): `--_swatches---color--ube-900`，最深紫

**Pomegranate (Pink/Red)**
- **Pomegranate 400** (`#fc7981`): `--_swatches---color--pomegranate-400`，暖珊瑚粉

**Blueberry (Navy Blue)**
- **Blueberry 800** (`#01418d`): `--_swatches---color--blueberry-800`，深藏青

### Neutral Scale (Warm)
- **Warm Silver** (`#9f9b93`): 次要/淡化文本、页脚链接
- **Warm Charcoal** (`#55534e`): 三级文本、深色淡化链接
- **Dark Charcoal** (`#333333`): 浅色背景上的链接文本

### Surface & Border
- **Oat Border** (`#dad4c8`): 主边框——温暖、奶油色调的结构线
- **Oat Light** (`#eee9df`): 次要浅色边框
- **Cool Border** (`#e6e8ec`): 对比区块的冷色调边框
- **Dark Border** (`#525a69`): 深色区块的边框
- **Light Frost** (`#eff1f3`): 微妙按钮背景（悬停时 0% 透明度）

### Badges
- **Badge Blue Bg** (`#f0f8ff`): 蓝色调徽章表面
- **Badge Blue Text** (`#3859f9`): 鲜艳蓝色徽章文本
- **Focus Ring** (`rgb(20, 110, 245) solid 2px`): 无障碍焦点指示器

### Shadows
- **Clay Shadow** (`rgba(0,0,0,0.1) 0px 1px 1px, rgba(0,0,0,0.04) 0px -1px 1px inset, rgba(0,0,0,0.05) 0px -0.5px 1px`): 多层带内嵌高光——标志性特征
- **Hard Offset** (`rgb(0,0,0) -7px 7px`): 悬停状态——俏皮的硬阴影

## 3. Typography Rules

### Font Families
- **Primary**: `Roobert`, fallback: `Arial`
- **Monospace**: `Space Mono`
- **OpenType Features**: `"ss01"`, `"ss03"`, `"ss10"`, `"ss11"`, `"ss12"` 应用于所有 Roobert 文本（display 使用全部 5 组；body/UI 使用 `"ss03"`, `"ss10"`, `"ss11"`, `"ss12"`）

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display Hero | Roobert | 80px (5.00rem) | 600 | 1.00 (tight) | -3.2px | 全部 5 组风格集 |
| Display Secondary | Roobert | 60px (3.75rem) | 600 | 1.00 (tight) | -2.4px | 全部 5 组风格集 |
| Section Heading | Roobert | 44px (2.75rem) | 600 | 1.10 (tight) | -0.88px to -1.32px | 全部 5 组风格集 |
| Card Heading | Roobert | 32px (2.00rem) | 600 | 1.10 (tight) | -0.64px | 全部 5 组风格集 |
| Feature Title | Roobert | 20px (1.25rem) | 600 | 1.40 | -0.4px | 全部 5 组风格集 |
| Sub-heading | Roobert | 20px (1.25rem) | 500 | 1.50 | -0.16px | 4 组风格集（无 ss01） |
| Body Large | Roobert | 20px (1.25rem) | 400 | 1.40 | normal | 4 组风格集 |
| Body | Roobert | 18px (1.13rem) | 400 | 1.60 (relaxed) | -0.36px | 4 组风格集 |
| Body Standard | Roobert | 16px (1.00rem) | 400 | 1.50 | normal | 4 组风格集 |
| Body Medium | Roobert | 16px (1.00rem) | 500 | 1.20–1.40 | -0.16px to -0.32px | 4–5 组风格集 |
| Button | Roobert | 16px (1.00rem) | 500 | 1.50 | -0.16px | 4 组风格集 |
| Button Large | Roobert | 24px (1.50rem) | 400 | 1.50 | normal | 4 组风格集 |
| Button Small | Roobert | 12.8px (0.80rem) | 500 | 1.50 | -0.128px | 4 组风格集 |
| Nav Link | Roobert | 15px (0.94rem) | 500 | 1.60 (relaxed) | normal | 4 组风格集 |
| Caption | Roobert | 14px (0.88rem) | 400 | 1.50–1.60 | -0.14px | 4 组风格集 |
| Small | Roobert | 12px (0.75rem) | 400 | 1.50 | normal | 4 组风格集 |
| Uppercase Label | Roobert | 12px (0.75rem) | 600 | 1.20 (tight) | 1.08px | `text-transform: uppercase`, 4 组风格集 |
| Badge | Roobert | 9.6px | 600 | — | — | 药丸徽章 |

### Principles
- **五组风格集作为身份标识**：Roobert 上 `"ss01"`, `"ss03"`, `"ss10"`, `"ss11"`, `"ss12"` 的组合创造出独特的排版个性。`ss01` 保留用于标题和强调——正文省略它，通过字形变化 creating 微妙的层次。
- **激进的展示压缩**：80px 时 -3.2px，60px 时 -2.4px——最压缩的展示字距 alongside 最宽松的正文间距（1.60 行高），创造出 dramatic 对比。
- **字重 600 用于标题，500 用于 UI，400 用于正文**：清晰的三层系统，每个字重有严格的角色。
- **大写标签配正字距**：12px 大写配 1.08px 字距 creates 系统的导航模式。

## 4. Component Stylings

### Buttons

**Primary (Transparent with Hover Animation)**
- Background: transparent (`rgba(239, 241, 243, 0)`)
- Text: `#000000`
- Padding: 6.4px 12.8px
- Border: none (或 `1px solid #717989` 用于 outlined 变体)
- Hover: background 变为色板颜色（如 `#434346`），text 变为 white，`rotateZ(-8deg)`, `translateY(-80%)`, hard shadow `rgb(0,0,0) -7px 7px`
- Focus: `rgb(20, 110, 245) solid 2px` outline

**White Solid**
- Background: `#ffffff`
- Text: `#000000`
- Padding: 6.4px
- Hover: oat-200 色板颜色，animated rotation + shadow
- Use: 彩色区块上的 Primary CTA

**Ghost Outlined**
- Background: transparent
- Text: `#000000`
- Padding: 8px
- Border: `1px solid #717989`
- Radius: 4px
- Hover: dragonfruit 色板颜色，white text, animated rotation

### Cards & Containers
- Background: `#ffffff` on cream canvas
- Border: `1px solid #dad4c8` (warm oat) or `1px dashed #dad4c8`
- Radius: 12px (standard cards), 24px (feature cards/images), 40px (section containers/footer)
- Shadow: `rgba(0,0,0,0.1) 0px 1px 1px, rgba(0,0,0,0.04) 0px -1px 1px inset, rgba(0,0,0,0.05) 0px -0.5px 1px`
- Colorful section backgrounds using swatch palette (matcha, slushie, ube, lemon)

### Inputs & Forms
- Text: `#000000`
- Border: `1px solid #717989`
- Radius: 4px
- Focus: `rgb(20, 110, 245) solid 2px` outline

### Navigation
- Sticky top nav on cream background
- Roobert 15px weight 500 for nav links
- Clay logo left-aligned
- CTA buttons right-aligned with pill radius
- Border bottom: `1px solid #dad4c8`
- Mobile: hamburger collapse at 767px

### Image Treatment
- Product screenshots in white cards with oat borders
- Colorful illustrated sections with swatch background colors
- 8px–24px radius on images
- Full-width colorful section backgrounds

### Distinctive Components

**Swatch Color Sections**
- Full-width sections with swatch-colored backgrounds (matcha green, slushie cyan, ube purple, lemon gold)
- White text on dark swatches, black text on light swatches
- Each section tells a distinct product story through its color

**Playful Hover Buttons**
- Rotate -8deg + translate upward on hover
- Hard offset shadow (`-7px 7px`) instead of soft blur
- Background transitions to contrasting swatch color
- Creates a physical, toy-like interaction quality

**Dashed Border Elements**
- Dashed borders (`1px dashed #dad4c8`) alongside solid borders
- Used for secondary containers and decorative elements
- Adds a hand-drawn, craft-like quality

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 1px, 2px, 4px, 6.4px, 8px, 12px, 12.8px, 16px, 18px, 20px, 24px

### Grid & Container
- Max content width centered
- Feature sections alternate between white cards and colorful swatch backgrounds
- Card grids: 2–3 columns on desktop
- Full-width colorful sections break the grid
- Footer with generous 40px radius container

### Whitespace Philosophy
- **Warm, generous breathing**: The cream background provides a warm rest between content blocks. Spacing is generous but not austere — it feels inviting, like a well-set table.
- **Color as spatial rhythm**: The alternating swatch-colored sections create visual rhythm through hue rather than just whitespace. Each color section is its own "room."
- **Craft-like density inside cards**: Within cards, content is compact and well-organized, contrasting with the generous outer spacing.

### Border Radius Scale
- Sharp (4px): Ghost buttons, inputs
- Standard (8px): Small cards, images, links
- Badge (11px): Tag badges
- Card (12px): Standard cards, buttons
- Feature (24px): Feature cards, images, panels
- Section (40px): Large sections, footer, containers
- Pill (1584px): CTAs, pill-shaped buttons

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat (Level 0) | No shadow, cream canvas | Page background |
| Clay Shadow (Level 1) | `rgba(0,0,0,0.1) 0px 1px 1px, rgba(0,0,0,0.04) 0px -1px inset, rgba(0,0,0,0.05) 0px -0.5px` | Cards, buttons — multi-layer with inset highlight |
| Hover Hard (Level 2) | `rgb(0,0,0) -7px 7px` | Hover state — playful hard offset shadow |
| Focus (Level 3) | `rgb(20, 110, 245) solid 2px` | Keyboard focus ring |

**Shadow Philosophy**: Clay's shadow system is uniquely three-layered: a downward cast (`0px 1px 1px`), an upward inset highlight (`0px -1px 1px inset`), and a subtle edge (`0px -0.5px 1px`). This creates a "pressed into clay" quality where elements feel both raised AND embedded — like a clay tablet where content is stamped into the surface. The hover hard shadow (`-7px 7px`) is deliberately retro-graphic, referencing print-era drop shadows and adding physical playfulness.

### Decorative Depth
- Full-width swatch-colored sections create dramatic depth through color contrast
- Dashed borders add visual texture alongside solid borders
- Product illustrations with warm, organic art style

## 7. Do's and Don'ts

### Do
- Use warm cream (`#faf9f7`) as the page background — the warmth is the identity
- Apply all 5 OpenType stylistic sets on Roobert headings: `"ss01", "ss03", "ss10", "ss11", "ss12"`
- Use the named swatch palette (Matcha, Slushie, Lemon, Ube, Pomegranate, Blueberry) for section backgrounds
- Apply the playful hover animation: `rotateZ(-8deg)`, `translateY(-80%)`, hard shadow `-7px 7px`
- Use warm oat borders (`#dad4c8`) — not neutral gray
- Mix solid and dashed borders for visual variety
- Use generous radius: 24px for cards, 40px for sections
- Use weight 600 exclusively for headings, 500 for UI, 400 for body

### Don't
- Don't use cool gray backgrounds — the warm cream (`#faf9f7`) is non-negotiable
- Don't use neutral gray borders (`#ccc`, `#ddd`) — always use the warm oat tones
- Don't mix more than 2 swatch colors in the same section
- Don't skip the OpenType stylistic sets — they define Roobert's character
- Don't use subtle hover effects — the rotation + hard shadow is the signature interaction
- Don't use small border radius (<12px) on feature cards — the generous rounding is structural
- Don't use standard shadows (blur-based) — Clay uses hard offset and multi-layer inset
- Don't forget the uppercase labels with 1.08px tracking — they're the wayfinding system

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile Small | <479px | Single column, tight padding |
| Mobile | 479–767px | Standard mobile, stacked layout |
| Tablet | 768–991px | 2-column grids, condensed nav |
| Desktop | 992px+ | Full layout, 3-column grids, expanded sections |

### Touch Targets
- Buttons: minimum 6.4px + 12.8px padding for adequate touch area
- Nav links: 15px font with generous spacing
- Mobile: full-width buttons for easy tapping

### Collapsing Strategy
- Hero: 80px → 60px → smaller display text
- Navigation: horizontal → hamburger at 767px
- Feature sections: multi-column → stacked
- Colorful sections: maintain full-width but compress padding
- Card grids: 3-column → 2-column → single column

### Image Behavior
- Product screenshots scale proportionally
- Colorful section illustrations adapt to viewport width
- Rounded corners maintained across breakpoints

## 9. Agent Prompt Guide

### Quick Color Reference
- Background: Warm Cream (`#faf9f7`)
- Text: Clay Black (`#000000`)
- Secondary text: Warm Silver (`#9f9b93`)
- Border: Oat Border (`#dad4c8`)
- Green accent: Matcha 600 (`#078a52`)
- Cyan accent: Slushie 500 (`#3bd3fd`)
- Gold accent: Lemon 500 (`#fbbd41`)
- Purple accent: Ube 800 (`#43089f`)
- Pink accent: Pomegranate 400 (`#fc7981`)

### Example Component Prompts
- "Create a hero on warm cream (#faf9f7) background. Headline at 80px Roobert weight 600, line-height 1.00, letter-spacing -3.2px, OpenType 'ss01 ss03 ss10 ss11 ss12', black text. Subtitle at 20px weight 400, line-height 1.40, #9f9b93 text. Two buttons: white solid pill (12px radius) and ghost outlined (4px radius, 1px solid #717989)."
- "Design a colorful section with Matcha 800 (#02492a) background. Heading at 44px Roobert weight 600, letter-spacing -1.32px, white text. Body at 18px weight 400, line-height 1.60, #84e7a5 text. White card inset with oat border (#dad4c8), 24px radius."
- "Build a button with playful hover: default transparent background, black text, 16px Roobert weight 500. On hover: background #434346, text white, transform rotateZ(-8deg) translateY(-80%), hard shadow rgb(0,0,0) -7px 7px."
- "Create a card: white background, 1px solid #dad4c8 border, 24px radius. Shadow: rgba(0,0,0,0.1) 0px 1px 1px, rgba(0,0,0,0.04) 0px -1px 1px inset. Title at 32px Roobert weight 600, letter-spacing -0.64px."
- "Design an uppercase label: 12px Roobert weight 600, text-transform uppercase, letter-spacing 1.08px, OpenType 'ss03 ss10 ss11 ss12'."

### Iteration Guide
1. Start with warm cream (#faf9f7) — never cool white
2. Swatch colors are for full sections, not small accents — go bold with matcha, slushie, ube
3. Oat borders (#dad4c8) everywhere — dashed variants for decoration
4. OpenType stylistic sets are mandatory — they make Roobert look like Roobert
5. Hover animations are the signature — rotation + hard shadow, not subtle fades
6. Generous radius: 24px cards, 40px sections — nothing looks sharp or corporate
7. Three weights: 600 (headings), 500 (UI), 400 (body) — strict roles
