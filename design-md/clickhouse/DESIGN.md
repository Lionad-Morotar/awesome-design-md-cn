# Design System: ClickHouse

## 1. Visual Theme & Atmosphere

ClickHouse 的界面是一个高性能控制台，以黑曜石黑为底色渲染出酸黄绿色的视觉效果——这是一种在你阅读任何文字之前就高喊着"速度"的设计。整个体验都沉浸在黑暗中：纯黑背景 (`#000000`) 搭配深木炭色卡片 (`#414141` 边框)，营造出终端级别的美学风格，其中唯一的色彩打断是标志性的霓虹黄绿色 (`#faff69`)，它像深色控制台上的荧光笔一样划过 CTA、边框和高亮时刻。

排版设计极具攻击性——Inter 字体使用 900 粗细 (Black) 用于 96px 的主标题，创造出具有物理质量感的文本块。这个"为 AI 打造的数据库"网站通过视觉重量传达原始力量：粗体字、高对比度的霓虹点缀，以及作为超大号数字展示的性能数据。ClickHouse 的设计没有任何微妙之处，而这正是其要点所在——它反映了产品对极致速度和性能的承诺。

ClickHouse 最独特之处在于近乎黑色的画布与霓虹黄绿色点缀之间令人 electrifying 的张力。这种色彩组合 (`#faff69` 配 `#000000`) 创造了科技品牌中对比度最高的配对之一，使每个 CTA 按钮、每张高亮卡片和每条装饰边框都无法被忽视。支撑这一点的是森林绿 (`#166534`) 用于次要 CTA，为操作层级增添深度而不与霓虹竞争。

**关键特征：**
- 纯黑画布 (#000000) 配霓虹黄绿色 (#faff69) 点缀——最大对比度
- 超重型展示排版：Inter 字体 900 粗细 (Black)，最大 96px
- 深木炭色卡片系统，#414141 边框 80% 不透明度
- 森林绿 (#166534) 次要 CTA 按钮
- 性能数据以超大号展示数字呈现
- 大写字母标签配宽字母间距 (1.4px) 用于导航结构
- 激活/按下状态将文本切换为淡黄色 (#f4f692)
- 所有链接悬停时变为霓虹黄绿色——统一的交互信号
- 部分元素使用内阴影创造"压入表面"的深度感

## 2. Color Palette & Roles

### Primary
- **Neon Volt** (`#faff69`): 标志性品牌色——一种生动的酸黄绿色，是黑色画布上唯一的色彩点缀。用于主 CTA、装饰边框、链接悬停和高亮时刻。
- **Forest Green** (`#166534`): 次要 CTA 颜色——一种深邃饱和的绿色，用于"Get Started"和需要从霓虹中区分的主操作按钮。
- **Dark Forest** (`#14572f`): 更深的绿色变体，用于边框和次要装饰。

### Secondary & Accent
- **Pale Yellow** (`#f4f692`): 激活/按下状态文本颜色——Neon Volt 的柔和、更 muted 版本，用于状态反馈。
- **Border Olive** (`#4f5100`): 深橄榄黄色用于 ghost 按钮边框——霓虹的 muted 兄弟。
- **Olive Dark** (`#161600`): 最深的霓虹色调颜色，用于微妙的品牌文本。

### Surface & Background
- **Pure Black** (`#000000`): 主页面背景——绝对黑色，实现最大对比度。
- **Near Black** (`#141414`): 按钮背景和略微elevated的深色表面。
- **Charcoal** (`#414141`): 主边框颜色，80% 不透明度——卡片和容器enclosure的主力。
- **Deep Charcoal** (`#343434`): 更深的边框变体，用于微妙的分隔线。
- **Hover Gray** (`#3a3a3a`): 按钮悬停状态背景——比 Near Black 稍亮。

### Neutrals & Text
- **Pure White** (`#ffffff`): 深色表面上的主文本。
- **Silver** (`#a0a0a0`): 次要正文文本和 muted 内容。
- **Mid Gray** (`#585858` at 28%): 用于深度效果的微妙灰色叠加。
- **Border Gray** (`#e5e7eb`): 浅边框变体 (用于罕见的浅色上下文)。

### Gradient System
- **传统意义上无渐变。** ClickHouse 使用纯色色块和高对比度边框。"渐变"就是对比度本身——霓虹黄绿色对纯黑创造出一种渐变会稀释的视觉强度。

## 3. Typography Rules

### Font Family
- **Primary**: `Inter` (Next.js 优化变体 `__Inter_d1b8ee`)
- **Secondary Display**: `Basier` (`__basier_a58b65`)，回退字体：`Arial, Helvetica`
- **Code**: `Inconsolata` (`__Inconsolata_a25f62`)

### Hierarchy

| 角色 | 字体 | 字号 | 粗细 | 行高 | 字母间距 | 说明 |
|------|------|------|------|------|------|------|
| Display Mega | Inter | 96px (6rem) | 900 | 1.00 (tight) | normal | 最大影响力，超重型 |
| Display / Hero | Inter | 72px (4.5rem) | 700 | 1.00 (tight) | normal | 章节英雄标题 |
| Feature Heading | Basier | 36px (2.25rem) | 600 | 1.30 (tight) | normal | 功能章节锚点 |
| Sub-heading | Inter / Basier | 24px (1.5rem) | 600–700 | 1.17–1.38 | normal | 卡片标题 |
| Feature Title | Inter / Basier | 20px (1.25rem) | 600–700 | 1.40 | normal | 小型功能标题 |
| Body Large | Inter | 18px (1.13rem) | 400–700 | 1.56 | normal | 介绍段落、按钮文本 |
| Body / Button | Inter | 16px (1rem) | 400–700 | 1.50 | normal | 标准正文、导航、按钮 |
| Caption | Inter | 14px (0.88rem) | 400–700 | 1.43 | normal | 元数据、描述、链接 |
| Uppercase Label | Inter | 14px (0.88rem) | 600 | 1.43 | 1.4px | 章节上标线，宽间距 |
| Code | Inconsolata | 16px (1rem) | 600 | 1.50 | normal | 代码块、命令 |
| Small | Inter | 12px (0.75rem) | 500 | 1.33 | normal | 最小文本 |
| Micro | Inter | 11.2px (0.7rem) | 500 | 1.79 (relaxed) | normal | 标签、微小标签 |

### Principles
- **Weight 900 是武器**: 展示标题使用 Inter Black (900)——这是大多数网站从未触及的粗细。结合 96px 字号，创造出具有物理感、近乎建筑感的文本。
- **完整粗细谱系**: 系统使用 400、500、600、700 和 900——覆盖全范围。粗细即是层级。
- **大写配最大字间距**: 章节上标线使用 1.4px 字母间距——比大多数系统更宽——创造出在密集深色背景下脱颖而出的醒目结构标签。
- **双无衬线字体**: Inter 处理展示和正文；Basier 以 600 粗细处理功能章节标题。这在"数据/性能"(Inter) 和"产品/功能"(Basier) 上下文之间创造了微妙的个性转变。

## 4. Component Stylings

### Buttons

**Neon Primary**
- 背景：Neon Volt (`#faff69`)
- 文本：Near Black (`#151515`)
- 内边距：0px 16px
- 圆角：锐利 (4px)
- 边框：`1px solid #faff69`
- 悬停：背景切换为深色 (`rgb(29, 29, 29)`)，文本保持
- 激活：文本切换为 Pale Yellow (`#f4f692`)
- 引人注目的 CTA——黑底上的霓虹

**Dark Solid**
- 背景：Near Black (`#141414`)
- 文本：Pure White (`#ffffff`)
- 内边距：12px 16px
- 圆角：4px 或 8px
- 边框：`1px solid #141414`
- 悬停：背景切换为 Hover Gray (`#3a3a3a`)，文本切换为 80% 不透明度
- 激活：文本切换为 Pale Yellow
- 标准操作按钮

**Forest Green**
- 背景：Forest Green (`#166534`)
- 文本：Pure White (`#ffffff`)
- 内边距：12px 16px
- 边框：`1px solid #141414`
- 悬停：同样的深色切换
- 激活：Pale Yellow 文本
- "Get Started" / 主转化按钮

**Ghost / Outlined**
- 背景：透明
- 文本：Pure White (`#ffffff`)
- 内边距：0px 32px
- 圆角：4px
- 边框：`1px solid #4f5100` (橄榄色调)
- 悬停：深色背景切换
- 激活：Pale Yellow 文本
- 带霓虹色调边框的次要操作

**Pill Toggle**
- 背景：透明
- 圆角：药丸形 (9999px)
- 用于切换/开关元素

### Cards & Containers
- 背景：透明或 Near Black
- 边框：`1px solid rgba(65, 65, 65, 0.8)`——标志性木炭色enclosure
- 圆角：4px (小型元素) 或 8px (卡片、容器)
- 阴影 Level 1: 微妙 (`rgba(0,0,0,0.1) 0px 1px 3px, rgba(0,0,0,0.1) 0px 1px 2px -1px`)
- 阴影 Level 2: 中等 (`rgba(0,0,0,0.1) 0px 10px 15px -3px, rgba(0,0,0,0.1) 0px 4px 6px -4px`)
- 阴影 Level 3: 内嵌 (`rgba(0,0,0,0.06) 0px 4px 4px, rgba(0,0,0,0.14) 0px 4px 25px inset`)——"按下"效果
- 霓虹高亮卡片：选中/激活的卡片获得霓虹黄绿色边框或点缀

### Navigation
- 黑色背景上的深色导航
- Logo: ClickHouse 字标 + 黄/霓虹图标
- 链接：白色文本，悬停时变为 Neon Volt (#faff69)
- CTA: Neon Volt 按钮或 Forest Green 按钮
- 大写字母标签用于分类

### Distinctive Components

**Performance Stats**
- 超大号数字 (72px+, 粗细 700–900)
- 下方简短描述
- 关键指标上的高对比度霓虹点缀
- 性能声明的主要视觉证明

**Neon-Highlighted Card**
- 带霓虹黄绿色边框高亮的标准深色卡片
- 创造"选中"或"精选"效果
- 点缀边框使卡片在深色画布上脱颖而出

**Code Blocks**
- 深色表面，Inconsolata 字体 600 粗细
- 霓虹和白色语法高亮
- 终端般的美学风格

**Trust Bar**
- 深色背景上的公司 logo
- 单色/白色 logo 处理
- 水平布局

## 5. Layout Principles

### Spacing System
- 基础单位：8px
- 缩放：2px, 6px, 7px, 8px, 10px, 12px, 16px, 20px, 24px, 25px, 32px, 40px, 44px, 48px, 64px
- 按钮内边距：12px 16px (标准), 0px 16px (紧凑), 0px 32px (宽 ghost)
- 章节垂直间距：充裕 (48–64px)

### Grid & Container
- 最大容器宽度：高达 2200px (超宽)，带响应式缩放
- Hero: 全宽深色，巨型排版
- 功能章节：带深色边框的多列卡片网格
- 数据：水平指标条
- 全深色页面——无浅色章节

### Whitespace Philosophy
- **深色虚空作为画布**: 纯黑背景提供无限深度——元素漂浮在黑暗中。
- **密集信息**: 功能卡片和数据 packed 有数据，反映数据库产品的性能焦点。
- **霓虹高亮作为导引**: 黄绿色点缀像跑道灯一样引导视线穿过深色界面。

### Border Radius Scale
- 锐利 (4px): 按钮、徽章、小型元素、代码块
- 舒适 (8px): 卡片、容器、分隔线
- 药丸形 (9999px): 切换按钮、状态指示器

## 6. Depth & Elevation

| 级别 | 处理 | 用途 |
|------|------|------|
| 平面 (Level 0) | 无阴影 | 黑色背景、文本块 |
| 边框 (Level 1) | `1px solid rgba(65,65,65,0.8)` | 标准卡片、容器 |
| 微妙 (Level 2) | `0px 1px 3px rgba(0,0,0,0.1)` | 微妙卡片提升 |
| Elevated (Level 3) | `0px 10px 15px -3px rgba(0,0,0,0.1)` | 功能卡片、悬停状态 |
| 按下/内嵌 (Level 4) | `0px 4px 25px rgba(0,0,0,0.14) inset` | 激活/按下元素——"沉入表面" |
| 霓虹高亮 (Level 5) | Neon Volt 边框 (`#faff69`) | 精选/选中卡片，最大强调 |

**阴影理念**: ClickHouse 在黑色画布上使用阴影，几乎不可见——它们更多是为了微妙的维度感而非明显的elevated。最独特的深度机制是**内嵌阴影**(Level 4)，它创造出"压入表面"的效果，这是 ClickHouse 独有的。霓虹边框高亮 (Level 5) 是主要的吸引注意力的深度机制。

## 7. Do's and Don'ts

### Do
- 使用 Neon Volt (#faff69) 作为唯一的色彩点缀——它必须在纯黑背景下脱颖而出
- 对英雄展示文本使用 Inter 900 粗细——极端粗细即是个性
- 将所有内容保持在纯黑 (#000000) 上——切勿使用深灰色作为页面背景
- 对所有卡片enclosure使用木炭色边框 (rgba(65,65,65,0.8))
- 对主 CTA 按钮使用森林绿 (#166534)——与霓虹区分以建立操作层级
- 将性能数据展示为超大号展示数字——这是核心视觉论据
- 对章节标签使用大写字母配宽字母间距 (1.4px)
- 对激活/按下文本状态使用 Pale Yellow (#f4f692)
- 链接悬停时应始终切换为 Neon Volt——统一的交互反馈

### Don't
- 不要引入额外颜色——调色板严格限定为黑、霓虹、绿和灰
- 不要将霓虹用作背景填充——它仅作为点缀和边框颜色 (CTA 按钮除外)
- 不要将展示粗细降至 700 以下——粗粗是核心个性
- 不要在任何地方使用浅色/白色背景——整个体验都是深色的
- 不要将圆角超过 8px——锐利几何形状反映数据库精度
- 不要在黑色上使用柔和/扩散阴影——它们不可见。改用基于边框的深度
- 不要在激活状态跳过内嵌阴影——"按下"效果是独特的
- 不要使用暖色调中性色——所有灰色都是完全中性的

## 8. Responsive Behavior

### Breakpoints
| 名称 | 宽度 | 关键变化 |
|------|------|------|
| Mobile | <640px | 单列，堆叠卡片 |
| Small Tablet | 640–768px | 微调 |
| Tablet | 768–1024px | 2 列网格 |
| Desktop | 1024–1280px | 标准布局 |
| Large Desktop | 1280–1536px | 扩展内容 |
| Ultra-wide | 1536–2200px | 最大容器宽度 |

### Touch Targets
- 按钮最小内边距 12px 16px
- 卡片表面作为触摸目标
- 充足的导航链接间距

### Collapsing Strategy
- **Hero 文本**: 96px → 72px → 48px → 36px
- **功能网格**: 多列 → 2 列 → 1 列
- **数据**: 水平 → 堆叠
- **导航**: 完整 → 汉堡菜单

### Image Behavior
- 产品截图保持宽高比
- 窄屏上代码块使用水平滚动
- 所有图像在深色背景上

## 9. Agent Prompt Guide

### Quick Color Reference
- 品牌点缀："Neon Volt (#faff69)"
- 页面背景："Pure Black (#000000)"
- CTA Green: "Forest Green (#166534)"
- 卡片边框："Charcoal (rgba(65,65,65,0.8))"
- 主文本："Pure White (#ffffff)"
- 次级文本："Silver (#a0a0a0)"
- 激活状态："Pale Yellow (#f4f692)"
- 按钮表面："Near Black (#141414)"

### Example Component Prompts
- "在纯黑 (#000000) 上创建一个英雄章节，标题使用 96px Inter 900 粗细，行高 1.0。纯白文本。添加 Neon Volt (#faff69) CTA 按钮 (深色文本、4px 圆角、0px 16px 内边距) 和一个 ghost 按钮 (透明、1px solid #4f5100 边框)。"
- "设计一个黑色背景的功能卡片，1px solid rgba(65,65,65,0.8) 边框和 8px 圆角。标题 24px Inter 700 粗细，正文 16px Silver (#a0a0a0)。添加带 1px solid #faff69 边框的霓虹高亮变体。"
- "构建一个性能数据条：大数字 72px Inter 700 粗细，纯白文本。简短描述 14px Silver 文本。黑色背景。"
- "创建一个 Forest Green (#166534) CTA 按钮：白色文本、12px 16px 内边距、4px 圆角、1px solid #141414 边框。悬停：背景切换为 #3a3a3a，文本切换为 80% 不透明度。"
- "设计一个大写章节标签：14px Inter 600 粗细，字母间距 1.4px，大写。黑色背景上的 Silver (#a0a0a0) 文本。"

### Iteration Guide
1. 将所有内容保持在纯黑上——不使用深灰色替代方案
2. Neon Volt (#faff69) 仅用于点缀和 CTA——不要用于大背景
3. 英雄标题用 900 粗细，标题用 700，标签用 600，正文用 400-500
4. 激活状态使用 Pale Yellow (#f4f692)——不只是不透明度变化
5. 所有链接悬停时变为 Neon Volt——一致的交互反馈
6. 木炭色边框 (rgba(65,65,65,0.8)) 是主要的深度机制
