# 设计系统：IBM

## 1. 视觉主题与氛围

IBM 网站是企业权威的数字化体现，构建于 Carbon 设计系统之上——这是一种经过严格规划的设计语言，其结构之严谨宛如一份以网页形式呈现的工程规范。页面运作于鲜明的二元性之上：亮白色 (`#ffffff`) 画布配以近黑色 (`#161616`) 文本，点缀以单一而坚定的强调色——IBM Blue 60 (`#0f62fe`)。这并非 playful 的科技初创极简主义，而是提炼为像素的企业级精准。每个元素都存在于 Carbon 严格的 2x 网格中，每种颜色都映射到语义 token，每个间距值都对齐到 8px 基础单位。

IBM Plex 字族是该系统的骨干。IBM Plex Sans 以浅字重 (300) 用于展示标题，在大字号下呈现出出人意料的通透感，甚至带有一丝精致——这是对 IBM 企业沉稳感的有意平衡。在正文字号下，常规字重 (400) 配合 14px 说明文字上的 0.16px 字母间距，引入了精密的微调追踪，让 Carbon 的文本感觉是经过工程化而非单纯设计的。IBM Plex Mono 服务于代码、数据和技术标签，与较少使用的 IBM Plex Serif 一起完成字族三要素。

超越单色加蓝色的 IBM 视觉识别特征，在于对 Carbon 组件 token 系统的依赖。每个交互状态都映射到以 `--cds-` 前缀（Carbon Design System）的 CSS 自定义属性。按钮没有硬编码的颜色；它们引用 `--cds-button-primary`、`--cds-button-primary-hover`、`--cds-button-primary-active`。这种 token 化的架构意味着整个视觉层是深层系统化基础之上的薄层皮肤——相当于设计领域的类型化 API。

**关键特征：**
- IBM Plex Sans 字重 300（Light）用于展示——通过排版克制体现企业沉稳
- IBM Plex Mono 用于代码和技术内容，在小字号下保持一致的 0.16px 字母间距
- 单一强调色：IBM Blue 60 (`#0f62fe`)——每个交互元素、每个 CTA、每个链接
- Carbon token 系统 (`--cds-*`) 驱动所有语义颜色，在变量级别实现主题切换
- 8px 间距网格严格遵守——无任意值，一切对齐
- `#f4f4f4` Gray 10 表面上的扁平无边界卡片——通过背景色分层而非阴影创造深度
- 底部边框输入框（非盒式）——Carbon 表单的标志性模式
- 主按钮上 0px 圆角半径——毫不妥协的矩形，无柔化处理

## 2. 色板与角色

### 主色
- **IBM Blue 60** (`#0f62fe`)：单一交互色。主按钮、链接、聚焦状态、激活指示器。这是核心 UI 色板中唯一的彩色色调。
- **White** (`#ffffff`)：页面背景、卡片表面、蓝色按钮上的文本、`--cds-background`。
- **Gray 100** (`#161616`)：主文本、标题、深色表面背景、导航栏、页脚。`--cds-text-primary`。

### 中性色阶（Gray 家族）
- **Gray 100** (`#161616`)：主文本、标题、深色 UI 框架、页脚背景。
- **Gray 90** (`#262626`)：次要深色表面、深色背景上的悬停状态。
- **Gray 80** (`#393939`)：三级深色、激活状态。
- **Gray 70** (`#525252`)：次要文本、辅助文本、描述。`--cds-text-secondary`。
- **Gray 60** (`#6f6f6f`)：占位符文本、禁用文本。
- **Gray 50** (`#8d8d8d`)：禁用图标、淡化标签。
- **Gray 30** (`#c6c6c6`)：边框、分割线、输入框底部边框。`--cds-border-subtle`。
- **Gray 20** (`#e0e0e0`)：微妙边框、卡片轮廓。
- **Gray 10** (`#f4f4f4`)：次要表面背景、卡片填充、交替行。`--cds-layer-01`。
- **Gray 10 Hover** (`#e8e8e8`)：Gray 10 表面的悬停状态。

### 交互色
- **Blue 60** (`#0f62fe`)：主交互——按钮、链接、聚焦。`--cds-link-primary`、`--cds-button-primary`。
- **Blue 70** (`#0043ce`)：链接悬停状态。`--cds-link-primary-hover`。
- **Blue 80** (`#002d9c`)：蓝色元素的激活/按下状态。
- **Blue 10** (`#edf5ff`)：蓝色色调表面、选中行背景。
- **Focus Blue** (`#0f62fe`)：`--cds-focus`——聚焦元素上的 2px 内嵌边框。
- **Focus Inset** (`#ffffff`)：`--cds-focus-inset`——深色背景上聚焦的白色内环。

### 支持与状态
- **Red 60** (`#da1e28`)：错误、危险。`--cds-support-error`。
- **Green 50** (`#24a148`)：成功。`--cds-support-success`。
- **Yellow 30** (`#f1c21b`)：警告。`--cds-support-warning`。
- **Blue 60** (`#0f62fe`)：信息。`--cds-support-info`。

### 暗色主题（Gray 100 主题）
- **Background**: Gray 100 (`#161616`)。`--cds-background`。
- **Layer 01**: Gray 90 (`#262626`)。卡片和容器表面。
- **Layer 02**: Gray 80 (`#393939`)。提升的表面。
- **Text Primary**: Gray 10 (`#f4f4f4`)。`--cds-text-primary`。
- **Text Secondary**: Gray 30 (`#c6c6c6`)。`--cds-text-secondary`。
- **Border Subtle**: Gray 80 (`#393939`)。`--cds-border-subtle`。
- **Interactive**: Blue 40 (`#78a9ff`)。链接和交互元素变浅以增强对比度。

## 3. 排版规则

### 字族
- **Primary**: `IBM Plex Sans`，后备字体：`Helvetica Neue, Arial, sans-serif`
- **Monospace**: `IBM Plex Mono`，后备字体：`Menlo, Courier, monospace`
- **Serif**（有限使用）: `IBM Plex Serif`，用于编辑/表达性场景
- **Icon Font**: `ibm_icons`——专有的图标字形，20px

### 层级

| 角色 | 字体 | 字号 | 字重 | 行高 | 字母间距 | 说明 |
|------|------|------|--------|-------------|----------------|-------|
| Display 01 | IBM Plex Sans | 60px (3.75rem) | 300 (Light) | 1.17 (70px) | 0 | 最大影响力，浅字重体现优雅 |
| Display 02 | IBM Plex Sans | 48px (3.00rem) | 300 (Light) | 1.17 (56px) | 0 | 次要主视觉，响应式回退 |
| Heading 01 | IBM Plex Sans | 42px (2.63rem) | 300 (Light) | 1.19 (50px) | 0 | 表达性标题 |
| Heading 02 | IBM Plex Sans | 32px (2.00rem) | 400 (Regular) | 1.25 (40px) | 0 | 章节标题 |
| Heading 03 | IBM Plex Sans | 24px (1.50rem) | 400 (Regular) | 1.33 (32px) | 0 | 子章节标题 |
| Heading 04 | IBM Plex Sans | 20px (1.25rem) | 600 (Semibold) | 1.40 (28px) | 0 | 卡片标题、功能标题 |
| Heading 05 | IBM Plex Sans | 20px (1.25rem) | 400 (Regular) | 1.40 (28px) | 0 | 较轻的卡片标题 |
| Body Long 01 | IBM Plex Sans | 16px (1.00rem) | 400 (Regular) | 1.50 (24px) | 0 | 标准阅读文本 |
| Body Long 02 | IBM Plex Sans | 16px (1.00rem) | 600 (Semibold) | 1.50 (24px) | 0 | 强调正文、标签 |
| Body Short 01 | IBM Plex Sans | 14px (0.88rem) | 400 (Regular) | 1.29 (18px) | 0.16px | 紧凑正文、说明文字 |
| Body Short 02 | IBM Plex Sans | 14px (0.88rem) | 600 (Semibold) | 1.29 (18px) | 0.16px | 粗体说明文字、导航项 |
| Caption 01 | IBM Plex Sans | 12px (0.75rem) | 400 (Regular) | 1.33 (16px) | 0.32px | 元数据、时间戳 |
| Code 01 | IBM Plex Mono | 14px (0.88rem) | 400 (Regular) | 1.43 (20px) | 0.16px | 行内代码、终端 |
| Code 02 | IBM Plex Mono | 16px (1.00rem) | 400 (Regular) | 1.50 (24px) | 0 | 代码块 |
| Mono Display | IBM Plex Mono | 42px (2.63rem) | 400 (Regular) | 1.19 (50px) | 0 | 主视觉 mono 装饰 |

### 原则
- **展示尺寸的浅字重**：Carbon 的表达性排版在 42px 以上使用字重 300（Light）。这创造出独特的张力——内容以企业权威发声，而字母形态以排版轻盈低语。
- **小字号的微调追踪**：14px 时为 0.16px 字母间距，12px 时为 0.32px。这些看似微不足道的值是 Carbon 在紧凑字号下可读性的秘密武器——它们将 tight 的 IBM Plex 字母形态撑开恰到好处。
- **三种功能性字重**：300（展示/表达）、400（正文/阅读）、600（强调/UI 标签）。字重 700 在生产排版比例中刻意缺席。
- **生产性与表达性**：生产性组合使用更紧密的行高 (1.29) 用于密集 UI。表达性组合呼吸更多 (1.40-1.50) 用于营销和编辑内容。

## 4. 组件样式

### 按钮

**主按钮（蓝色）**
- 背景：`#0f62fe` (Blue 60) → `--cds-button-primary`
- 文本：`#ffffff` (White)
- 内边距：14px 63px 14px 15px（不对称——为 trailing 图标留出空间）
- 边框：1px solid transparent
- 圆角半径：0px（锋利的矩形——Carbon 的签名）
- 高度：48px（默认）、40px（紧凑）、64px（表达性）
- 悬停：`#0353e9` (Blue 60 Hover) → `--cds-button-primary-hover`
- 激活：`#002d9c` (Blue 80) → `--cds-button-primary-active`
- 聚焦：`2px solid #0f62fe` 内嵌 + `1px solid #ffffff` 内环

**次要按钮（灰色）**
- 背景：`#393939` (Gray 80)
- 文本：`#ffffff`
- 悬停：`#4c4c4c` (Gray 70)
- 激活：`#6f6f6f` (Gray 60)
- 与主按钮相同的内边距/圆角

**第三级按钮（幽灵蓝）**
- 背景：transparent
- 文本：`#0f62fe` (Blue 60)
- 边框：1px solid `#0f62fe`
- 悬停：`#0353e9` 文本 + Blue 10 背景色调
- 圆角半径：0px

**幽灵按钮**
- 背景：transparent
- 文本：`#0f62fe` (Blue 60)
- 内边距：14px 16px
- 边框：none
- 悬停：`#e8e8e8` 背景色调

**危险按钮**
- 背景：`#da1e28` (Red 60)
- 文本：`#ffffff`
- 悬停：`#b81921` (Red 70)

### 卡片与容器
- 背景：白色主题上为 `#ffffff`，`#f4f4f4` (Gray 10) 用于提升的卡片
- 边框：none（扁平设计——大多数卡片无边框或阴影）
- 圆角半径：0px（匹配矩形的按钮美学）
- 悬停：可点击卡片背景切换为 `#e8e8e8` (Gray 10 Hover)
- 内容内边距：16px
- 分隔：背景色分层（white → gray 10 → white）而非阴影

### 输入框与表单
- 背景：`#f4f4f4` (Gray 10) — `--cds-field`
- 文本：`#161616` (Gray 100)
- 内边距：0px 16px（仅水平）
- 高度：40px（默认）、48px（大）
- 边框：侧面/顶部无 — 底部 `2px solid transparent`
- 底部边框激活：`2px solid #161616` (Gray 100)
- 聚焦：`2px solid #0f62fe` (Blue 60) 底部边框 — `--cds-focus`
- 错误：`2px solid #da1e28` (Red 60) 底部边框
- 标签：12px IBM Plex Sans，0.32px 字母间距，Gray 70
- 辅助文本：12px，Gray 60
- 占位符：Gray 60 (`#6f6f6f`)
- 圆角半径：0px（顶部）— 输入框为尖角

### 导航
- 背景：`#161616` (Gray 100) — 全宽深色 masthead
- 高度：48px
- Logo：IBM 8-bar 徽标，白底深色，左对齐
- 链接：14px IBM Plex Sans，字重 400，默认 `#c6c6c6` (Gray 30)
- 链接悬停：`#ffffff` 文本
- 激活链接：`#ffffff` 带底部边框指示器
- 平台切换器：左对齐水平标签页
- 搜索：图标触发的滑出式搜索框
- 移动端：汉堡菜单带左滑面板

### 链接
- 默认：`#0f62fe` (Blue 60) 无下划线
- 悬停：`#0043ce` (Blue 70) 带下划线
- 已访问：保持 Blue 60（无已访问状态变化）
- 内联链接：正文复制中默认带下划线

### 特色组件

**内容块（主视觉/功能）**
- 全宽交替白色/gray-10 背景带
- 标题左对齐，60px 或 48px 展示字体
- CTA 为带箭头图标的蓝色主按钮
- 图片/插图右对齐或在移动端置于下方

**Tile（可点击卡片）**
- 背景：`#f4f4f4` 或 `#ffffff`
- 全宽底部边框或背景切换悬停
- 悬停时箭头图标位于右下角
- 无阴影——扁平性是身份标识

**Tag / Label**
- 背景：上下文颜色的 10% 不透明度（例如 Blue 10、Red 10）
- 文本：对应的 60 级颜色
- 内边距：4px 8px
- 圆角半径：24px（药丸形——0px 规则的例外）
- 字体：12px 字重 400

**通知横幅**
- 全宽条，通常为 Blue 60 或 Gray 100 背景
- 白色文本，14px
- 关闭/解散图标右对齐

## 5. 布局原则

### 间距系统
- 基础单位：8px (Carbon 2x 网格)
- 组件间距比例：2px, 4px, 8px, 12px, 16px, 24px, 32px, 40px, 48px
- 布局间距比例：16px, 24px, 32px, 48px, 64px, 80px, 96px, 160px
- 最小单位：8px（最小可用间距）
- 组件内内边距：通常 16px
- 卡片/tiles 间间隙：1px（发丝）或 16px（标准）

### 网格与容器
- 16 列网格（Carbon 的 2x 网格系统）
- 最大内容宽度：1584px（最大断点）
- 列槽：32px（移动端 16px）
- 边距：16px（移动端）、32px（平板+）
- 内容通常跨越 8-12 列以获得可读的行长度
- 全出血区域与包含内容交替

### 留白哲学
- **功能密度**：Carbon 偏好生产性密度而非广阔留白。与消费者设计系统相比，区域包装更紧密——这反映了 IBM 的企业 DNA。
- **背景色分区**：Carbon 不使用区域间大量内边距，而是使用交替背景色（white → gray 10 → white）以最小垂直空间创造视觉分隔。
- **一致的 48px 节奏**：主要区域过渡使用 48px 垂直间距。主视觉区域可能使用 80px–96px。

### 圆角半径比例
- **0px**：主按钮、输入框、tiles、卡片——主导处理。Carbon 本质上是矩形的。
- **2px**：偶尔用于小型交互元素（tags）
- **24px**：Tags/labels（药丸形——唯一的圆角例外）
- **50%**：头像圆形、图标容器

## 6. 深度与高程

| 级别 | 处理 | 用途 |
|-------|-----------|-----|
| 扁平 (Level 0) | 无阴影，`#ffffff` 背景 | 默认页面表面 |
| Layer 01 | 无阴影，`#f4f4f4` 背景 | 卡片、tiles、交替区域 |
| Layer 02 | 无阴影，`#e0e0e0` 背景 | Layer 01 内的提升面板 |
| Raised | `0 2px 6px rgba(0,0,0,0.3)` | 下拉菜单、工具提示、溢出菜单 |
| Overlay | `0 2px 6px rgba(0,0,0,0.3)` + 深色蒙版 | 模态对话框、侧面板 |
| Focus | `2px solid #0f62fe` 内嵌 + `1px solid #ffffff` | 键盘聚焦环 |
| Bottom-border | 底部边缘 `2px solid #161616` | 激活输入框、激活标签页指示器 |

**阴影哲学**：Carbon 刻意回避阴影。IBM 主要通过背景色分层实现深度——堆叠 progressively 更深的灰色表面，而非添加 box-shadows。这创造出扁平的印刷灵感美学，层级通过色值传达，而非模拟光照。阴影仅保留给真正的悬浮元素（下拉菜单、工具提示、模态框），其中元素确实重叠内容。这种克制赋予罕见阴影有意义的影响力——当某物在 Carbon 中悬浮时，它很重要。

## 7. 宜与忌

### 宜
- 在展示尺寸 (42px+) 使用 IBM Plex Sans 字重 300——浅字重是有意的
- 在 14px 正文文本应用 0.16px 字母间距，在 12px 说明文字应用 0.32px
- 在按钮、输入框、卡片和 tiles 上使用 0px 圆角半径——矩形是系统
- 实现时引用 `--cds-*` token 名称（例如 `--cds-button-primary`、`--cds-text-primary`）
- 使用背景色分层（white → gray 10 → gray 20）创造深度而非阴影
- 使用底部边框（非盒式）作为输入框指示器
- 保持 48px 默认按钮高度和为图标适配的不对称内边距
- 应用 Blue 60 (`#0f62fe`) 作为唯一强调色——一蓝统天下

### 忌
- 不要圆角按钮边缘——0px 半径是 Carbon 身份
- 不要在卡片或 tiles 上使用阴影——扁平是要点
- 不要引入额外的强调色——IBM 的系统是单色 + 蓝色
- 不要使用字重 700（Bold）——比例停在 600（Semibold）
- 不要在展示尺寸文本上添加字母间距——追踪仅用于 14px 及以下
- 不要用全边框框定输入框——Carbon 输入框仅使用底部边框
- 不要使用渐变背景——IBM 的表面是扁平纯色
- 不要偏离 8px 间距网格——每个值都应被 8 整除（2px 和 4px 用于微调）

## 8. 响应式行为

### 断点
| 名称 | 宽度 | 关键变化 |
|------|-------|-------------|
| Small (sm) | 320px | 单列、汉堡导航、16px 边距 |
| Medium (md) | 672px | 2 列网格开始、扩展内容 |
| Large (lg) | 1056px | 完整导航可见、3-4 列网格 |
| X-Large (xlg) | 1312px | 最大内容密度、宽布局 |
| Max | 1584px | 最大内容宽度、居中带边距 |

### 触摸目标
- 按钮高度：默认 48px，最小 40px（紧凑）
- 导航链接：48px 行高用于触摸
- 输入框高度：默认 40px，大尺寸 48px
- 图标按钮：48px 方形触摸目标
- 移动端菜单项：全宽 48px 行

### 折叠策略
- 主视觉：60px 展示 → 42px → 32px 标题随视口变窄
- 导航：完整水平 masthead → 带滑出面板的汉堡菜单
- 网格：4 列 → 2 列 → 单列
- Tiles/卡片：水平网格 → 垂直堆叠
- 图片：保持宽高比，最大宽度 100%
- 页脚：多列链接组 → 堆叠单列
- 区域内边距：48px → 32px → 16px

### 图片行为
- 响应式图片带 `max-width: 100%`
- 产品插图按比例缩放
- 主视觉图片可能从并排切换到下方堆叠
- 数据可视化在移动端保持宽高比并水平滚动

## 9. 智能体提示词指南

### 快速颜色参考
- 主 CTA：IBM Blue 60 (`#0f62fe`)
- 背景：White (`#ffffff`)
- 标题文本：Gray 100 (`#161616`)
- 正文文本：Gray 100 (`#161616`)
- 次要文本：Gray 70 (`#525252`)
- 表面/卡片：Gray 10 (`#f4f4f4`)
- 边框：Gray 30 (`#c6c6c6`)
- 链接：Blue 60 (`#0f62fe`)
- 链接悬停：Blue 70 (`#0043ce`)
- 聚焦环：Blue 60 (`#0f62fe`)
- 错误：Red 60 (`#da1e28`)
- 成功：Green 50 (`#24a148`)

### 示例组件提示词
- "在白色背景上创建主视觉区域。标题为 60px IBM Plex Sans 字重 300，行高 1.17，颜色 #161616。副标题为 16px 字重 400，行高 1.50，颜色 #525252，最大宽度 640px。蓝色 CTA 按钮（#0f62fe 背景、#ffffff 文本、0px 圆角、48px 高度、14px 63px 14px 15px 内边距）。"
- "设计卡片 tile：#f4f4f4 背景、0px 圆角、16px 内边距。标题为 20px IBM Plex Sans 字重 600，行高 1.40，颜色 #161616。正文为 14px 字重 400，字母间距 0.16px，行高 1.29，颜色 #525252。悬停：背景切换为 #e8e8e8。"
- "构建表单字段：#f4f4f4 背景、0px 圆角、40px 高度、16px 水平内边距。上方标签为 12px 字重 400，字母间距 0.32px，颜色 #525252。底部边框：默认 2px solid transparent，聚焦时 2px solid #0f62fe。占位符：#6f6f6f。"
- "创建深色导航栏：#161616 背景、48px 高度。IBM 徽标白色左对齐。链接为 14px IBM Plex Sans 字重 400，颜色 #c6c6c6。悬停：#ffffff 文本。激活：#ffffff 带 2px 底部边框。"
- "构建 tag 组件：Blue 10 (#edf5ff) 背景、Blue 60 (#0f62fe) 文本、4px 8px 内边距、24px 圆角、12px IBM Plex Sans 字重 400。"

### 迭代指南
1. 始终在按钮、输入框和卡片上使用 0px 圆角半径——这在 Carbon 中是不可协商的
2. 字母间距仅在小字号：14px 时 0.16px，12px 时 0.32px——绝不在展示文本上
3. 三种字重：300（展示）、400（正文）、600（强调）——无粗体
4. Blue 60 是唯一强调色——不要引入次要强调色
5. 深度来自背景色分层（white → #f4f4f4 → #e0e0e0），而非阴影
6. 输入框仅有底部边框，永不完整盒式
7. 使用 `--cds-` 前缀命名 token 以保持 Carbon 兼容
8. 48px 是通用交互元素高度
