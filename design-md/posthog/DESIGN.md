# 设计系统：PostHog

## 1. 视觉主题与氛围

PostHog 的网站就像一个初创公司内部维基逃逸到了野外——温暖、不屑一顾，且刻意反企业化。背景不是开发者工具中常见的 crisp 白色或黑暗虚空，而是一种温暖的鼠尾草色调奶油色（`#fdfdf8`），让每个表面都呈现出手工纸般的质感。色彩倾向于朴实的橄榄绿和柔和的鼠尾草色，而非 SaaS 世界传统的蓝色和紫色。就像有人在舒适的花园小屋里设计了一个开发者分析平台。

个性是亮点：手绘刺猬插图、古怪的手办和俏皮的 imagery 取代了 B2B SaaS 常见的库存照片和抽象渐变。IBM Plex Sans Variable 作为字体基础——这款字体具有真正的技术可信度（由 IBM 创建，广泛用于开发者场景），在这里以粗体字重（700、800）用于标题，正文则采用 generous 的行高。字体在说"我们是认真的工程师"，而周围的一切则在说"但我们不过分严肃"。

交互设计秉承同样的精神：hover 状态会闪现 PostHog 橙色（`#F54E00`）文本——这是一种隐藏的品牌色，在静止时不出现，但在交互时带来惊喜。接近黑色的深色按钮（`#1e1f23`）在 hover 时使用透明度降低而非颜色变化，激活状态则轻微缩放。边框系统使用鼠尾草色调的灰色（`#bfc1b7`），与橄榄色文本调色板和谐统一。基于 Tailwind CSS 与 Radix UI 和 shadcn/ui 原语构建，技术基础是现代且组件驱动的，但视觉输出却固执地独特。

**关键特征：**
- 温暖的鼠尾草/橄榄色调色板，而非传统的蓝色——朴实且亲和
- IBM Plex Sans Variable 字体以粗体字重（700/800）用于标题，行高 generous 达 1.50+
- 隐藏的品牌橙色（`#F54E00`）仅在 hover 交互时出现——一个令人愉悦的惊喜
- 手绘刺猬插图和俏皮 imagery——刻意反企业化
- 鼠尾草色调的边框（`#bfc1b7`）和背景（`#eeefe9`）营造统一的暖绿色系统
- 深色近黑色 CTA（`#1e1f23`）采用基于透明度的 hover 状态
- 内容密集的报道式布局——网站读起来像杂志，而非典型的落地页
- Tailwind CSS + Radix UI + shadcn/ui 组件架构

## 2. 色彩调色板与角色

### 主色
- **Olive Ink**（`#4d4f46`）：主要文本颜色——独特的橄榄灰色，赋予所有文本温暖的朴实质感
- **Deep Olive**（`#23251d`）：链接文本和高强调标题——带绿色底调的近黑色
- **PostHog Orange**（`#F54E00`）：隐藏的品牌强调色——仅在 hover 状态出现，令人惊喜的鲜艳橙色

### 次要色与强调色
- **Amber Gold**（`#F7A501`）：深色按钮上的次要 hover 强调色——与橙色配对的温暖金色
- **Gold Border**（`#b17816`）：特殊按钮边框——用于特色 CTA 的琥珀金色
- **Focus Blue**（`#3b82f6`）：焦点环颜色（Tailwind 默认）——系统中唯一的蓝色，专为可访问性保留

### 表面与背景
- **Warm Parchment**（`#fdfdf8`）：主要页面背景——带黄绿色底调的温暖近白色
- **Sage Cream**（`#eeefe9`）：输入框背景、次要表面——浅鼠尾草色调
- **Light Sage**（`#e5e7e0`）：按钮背景、三级表面——柔和的鼠尾草绿
- **Warm Tan**（`#d4c9b8`）：特色按钮背景——用于强调的暖褐色/卡其色
- **Hover White**（`#f4f4f4`）：通用 hover 背景状态

### 中性色与文本
- **Olive Ink**（`#4d4f46`）：主要正文和 UI 文本
- **Muted Olive**（`#65675e`）：次要文本、浅色背景上的按钮标签
- **Sage Placeholder**（`#9ea096`）：占位符文本、禁用状态——暖鼠尾草绿
- **Sage Border**（`#bfc1b7`）：主要边框颜色——所有边框的橄榄色调灰色
- **Light Border**（`#b6b7af`）：次要边框、工具栏边框——稍深的鼠尾草色

### 语义与强调色
- **PostHog Orange**（`#F54E00`）：hover 文本强调—— signaled 交互性和品牌个性
- **Amber Gold**（`#F7A501`）：深色按钮 hover 强调——温暖 signal
- **Focus Blue**（`#3b82f6`，50% 透明度）：键盘焦点环——仅用于可访问性的颜色
- **Dark Text**（`#111827`）：高对比度链接文本——近黑色用于重要链接

### 渐变系统
- 营销网站上无渐变——PostHog 的视觉语言刻意扁平且温暖
- 深度通过分层表面和边框容器实现，而非颜色过渡

## 3. 字体排印规则

### 字体系列
- **Display 与正文**：`IBM Plex Sans Variable`——可变字体（100–700+ 字重范围）。后备：`IBM Plex Sans, -apple-system, system-ui, Avenir Next, Avenir, Segoe UI, Helvetica Neue, Helvetica, Ubuntu, Roboto, Noto, Arial`
- **等宽字体**：`ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, Liberation Mono, Courier New`——系统等宽字体系列
- **代码 Display**：`Source Code Pro`——后备：`Menlo, Consolas, Monaco`

### 层级

| 角色 | 字体 | 字号 | 字重 | 行高 | 字间距 | 备注 |
|------|------|------|--------|-------------|----------------|-------|
| Display Hero | IBM Plex Sans Variable | 30px | 800 | 1.20 | -0.75px | 超粗体、紧凑、最大冲击力 |
| Section Heading | IBM Plex Sans Variable | 36px | 700 | 1.50 | 0px | 大但 generous 的行高 |
| Feature Heading | IBM Plex Sans Variable | 24px | 700 | 1.33 | 0px | 功能区块标题 |
| Card Heading | IBM Plex Sans Variable | 21.4px | 700 | 1.40 | -0.54px | 略显不寻常的字号（缩放） |
| Sub-heading | IBM Plex Sans Variable | 20px | 700 | 1.40 | -0.5px | 内容子区块 |
| Sub-heading Uppercase | IBM Plex Sans Variable | 20px | 700 | 1.40 | 0px | 标签使用大写转换 |
| Body Emphasis | IBM Plex Sans Variable | 19.3px | 600 | 1.56 | -0.48px | 半粗体强调文本 |
| Label Uppercase | IBM Plex Sans Variable | 18px | 700 | 1.50 | 0px | 大写分类标签 |
| Body Semi | IBM Plex Sans Variable | 18px | 600 | 1.56 | 0px | 半粗体正文 |
| Body | IBM Plex Sans Variable | 16px | 400 | 1.50 | 0px | 标准阅读文本 |
| Body Medium | IBM Plex Sans Variable | 16px | 500 | 1.50 | 0px | 中等字重正文 |
| Body Relaxed | IBM Plex Sans Variable | 15px | 400 | 1.71 | 0px | 长阅读的 relaxed 行高 |
| Nav / UI | IBM Plex Sans Variable | 15px | 600 | 1.50 | 0px | 导航和 UI 标签 |
| Caption | IBM Plex Sans Variable | 14px | 400–700 | 1.43 | 0px | 小文本，多种字重 |
| Small Label | IBM Plex Sans Variable | 13px | 500–700 | 1.00–1.50 | 0px | 标签、徽章、微标签 |
| Micro | IBM Plex Sans Variable | 12px | 400–700 | 1.33 | 0px | 最小文本，部分大写 |
| Code | Source Code Pro | 14px | 500 | 1.43 | 0px | 代码片段和终端 |

### 原则
- **粗体标题主导**：标题使用 700–800 字重——PostHog 的字体排印自信且坚定，不轻柔
- **Generous 正文行高**：正文行高 1.50–1.71 创造极其舒适的阅读体验——网站内容密集，针对长时间会话优化
- **小数点字号**：多个字号（21.4px、19.3px、13.7px）表明使用流体/缩放字体系统而非固定节点——可能从 Tailwind 的非标准基准 rem 比例计算而来
- **大写作为分类 signal**：粗体大写标签（18px–20px 字重 700）用于产品类别标题——一种杂志编辑惯例
- **选择性负字间距**：Display 文本字间距收紧（30px 时为 -0.75px），但正文放松至 0px——标题压缩，正文呼吸

## 4. 组件样式

### 按钮
- **深色主按钮**：`#1e1f23` 背景，白色文本，6px 圆角，`10px 12px` 内边距。Hover：透明度 0.7 配 Amber Gold 文本。Active：透明度 0.8 带轻微缩放变换。主要的 CTA——深色且自信
- **Sage Light**：`#e5e7e0` 背景，Olive Ink（`#4d4f46`）文本，4px 圆角，`4px` 内边距。Hover：`#f4f4f4` 背景配 PostHog Orange 文本。紧凑型实用按钮
- **Warm Tan Featured**：`#d4c9b8` 背景，黑色文本，无可见圆角。Hover：同样的橙色文本闪现。特色/高级操作
- **输入框样式**：`#eeefe9` 背景，Sage Placeholder（`#9ea096`）文本，4px 圆角，1px `#b6b7af` 边框。看起来像搜索/筛选控件
- **近白色 Ghost**：`#fdfdf8` 背景，Olive Ink 文本，4px 圆角，透明 1px 边框。最小存在感
- **Hover 模式**：所有按钮在 hover 时闪现 PostHog Orange（`#F54E00`）或 Amber Gold（`#F7A501`）文本——品牌的标志性交互惊喜

### 卡片与容器
- **边框卡片**：Warm Parchment（`#fdfdf8`）或白色背景，1px `#bfc1b7` 边框，4px–6px 圆角——简洁 minimal
- **Sage Surface 卡片**：`#eeefe9` 背景用于次要内容容器
- **阴影卡片**：`0px 25px 50px -12px rgba(0, 0, 0, 0.25)`——单个深阴影用于提升的内容（模态框、下拉菜单）
- **Hover**：交互卡片上的橙色文本闪现——与按钮行为一致

### 输入框与表单
- **默认**：`#eeefe9` 背景，`#9ea096` 占位符文本，1px `#b6b7af` 边框，4px 圆角，`2px 0px 2px 8px` 内边距
- **焦点**：50% 透明度的 `#3b82f6` 环（Tailwind 蓝色焦点环）
- **文本颜色**：`#374151` 用于输入值——比主要文本更深以提高可读性
- **边框变体**：多种边框模式——一些输入框使用复合边框（顶部、左侧、仅底部）

### 导航
- **顶部导航**：温暖背景，IBM Plex Sans 15px 字重 600
- **下拉菜单**：丰富的 mega-menu 结构包含产品类别
- **链接颜色**：Deep Olive（`#23251d`）用于导航链接，hover 时带下划线
- **CTA**：导航中的深色主按钮（#1e1f23）——"Get started - free"
- **移动端**：折叠为汉堡菜单配简化菜单

### 图片处理
- **手绘插图**：刺猬吉祥物和古怪插图——标志性视觉元素
- **产品截图**：UI 截图嵌入设备框架或简洁容器中
- **手办**：刺猬小玩偶的俏皮产品摄影——反企业化
- **信任标志**：企业标志（Airbus、GOV.UK）显示在柔和的信任条中
- **宽高比**：混合——插图不规则，截图为 16:9 或宽屏

### AI 聊天组件
- 浮动 PostHog AI 助手配对话气泡——嵌入营销网站的交互式产品演示

## 5. 布局原则

### 间距系统
- **基准单位**：8px
- **比例**：2px、4px、6px、8px、10px、12px、16px、18px、24px、32px、34px
- **区块内边距**：区块间垂直间距 32px–48px（对于内容密集的网站来说紧凑）
- **卡片内边距**：4px–12px 内部（显著紧凑）
- **组件间距**：相关元素间 4px–8px

### 网格与容器
- **最大宽度**：1536px（最大断点），内容容器可能为 1200px–1280px
- **列模式**：变化——文本内容单列，功能卡片 2-3 列网格，产品演示非对称布局
- **断点**：13 个定义——1px、425px、482px、640px、768px、767px、800px、900px、1024px、1076px、1160px、1280px、1536px

### 留白哲学
- **刻意内容密集**：PostHog 的网站信息丰富——留白是经过丈量的，而非奢侈
- **编辑节奏**：内容区块像杂志一样流畅，变化的布局让视线保持移动
- **插图作为呼吸空间**：手绘刺猬艺术自然地打破密集内容区块

### 圆角比例尺
- **2px**：小型内联元素、标签（`span`）
- **4px**：主要 UI 组件——按钮、输入框、下拉菜单、菜单项（`button`、`div`、`combobox`）
- **6px**：次要容器——较大按钮、列表项、卡片变体（`button`、`div`、`li`）
- **9999px**：药丸形状——徽章、状态指示器、圆角标签（`span`、`div`）

## 6. 深度与提升

| 级别 | 处理 | 用途 |
|-------|-----------|-----|
| Level 0（扁平）| 无阴影，Warm Parchment 背景 | 页面画布、大多数表面 |
| Level 1（边框）| `1px solid #bfc1b7`（Sage Border） | 卡片容器、输入框边框、区块分隔线 |
| Level 2（复合边框）| 不同侧的多个 1px 边框 | 输入框组合、工具栏元素 |
| Level 3（深阴影）| `0px 25px 50px -12px rgba(0, 0, 0, 0.25)` | 模态框、浮动元素、mega-menu 下拉菜单 |

### 阴影哲学
PostHog 的提升系统异常 minimal——整个系统中只有一个阴影定义。深度通过以下方式传达：
- **边框容器**：1px 的鼠尾草色调边框（`#bfc1b7`）创造柔和的温暖分离
- **表面颜色变化**：从 `#fdfdf8` 到 `#eeefe9` 再到 `#e5e7e0` 创造分层深度而无需阴影
- **单一阴影**：唯一定义的阴影（`0 25px 50px -12px`）保留给浮动元素——模态框、下拉菜单、popovers。这是一个深邃、戏剧性的阴影，在需要时创造清晰分离

### 装饰深度
- **插图分层**：手绘刺猬艺术自然创造视觉深度
- **无渐变或发光**：扁平温暖表面系统完全依赖边框和表面颜色区分
- **无玻璃拟态**：全部使用不透明表面

## 7. 宜与忌

### 宜
- 使用橄榄/鼠尾草色系（#4d4f46、#23251d、#bfc1b7）用于文本和边框——暖绿色底调对品牌至关重要
- 在 hover 状态闪现 PostHog Orange（#F54E00）——这是隐藏的品牌 signature
- 使用 IBM Plex Sans 粗体字重（700/800）用于标题——字体承载技术可信度
- 保持正文文本 generous 的行高（1.50–1.71）——内容密集的网站需要可读性
- 保持温暖的 parchment 背景（#fdfdf8）——非纯白，永不冷
- 对大多数 UI 元素使用 4px 圆角——保持角落微妙且功能化
- 包含俏皮的手绘插图元素——个性是差异化因素
- 在深色按钮上使用基于透明度的 hover 状态（0.7 透明度）而非颜色变化

### 忌
- 使用蓝色、紫色或典型科技 SaaS 颜色——PostHog 的调色板刻意是橄榄/鼠尾草色
- 添加厚重阴影——系统仅对一个阴影用于浮动元素；其他一切使用边框
- 让设计看起来"精致"或"高级"（传统意义上）——PostHog 的魅力在于其不屑一顾、拼搏的活力
- 对正文文本使用紧缩行高——generous 的 1.50+ 间距对内容密集布局至关重要
- 对卡片应用大圆角（12px+）——PostHog 使用 4px–6px，保持紧凑功能化
- 移除橙色 hover 闪现——这是核心交互模式，而非装饰
- 用库存照片替换插图——手绘刺猬艺术就是品牌
- 使用纯白色（#ffffff）作为页面背景——温暖的鼠尾草奶油色（#fdfdf8）底调是基础

## 8. 响应式行为

### 断点
| 名称 | 宽度 | 关键变化 |
|------|-------|-------------|
| Mobile Small | <425px | 单列、紧凑内边距、堆叠卡片 |
| Mobile | 425px–640px | 轻微布局调整、更大触摸目标 |
| Tablet | 640px–768px | 2 列网格开始、导航部分可见 |
| Tablet Large | 768px–1024px | 多列布局、扩展导航 |
| Desktop | 1024px–1280px | 完整布局、3 列功能网格、扩展 mega-menu |
| Large Desktop | 1280px–1536px | 最大宽度容器、generous 边距 |
| Extra Large | >1536px | 居中容器于最大宽度 |

### 触摸目标
- 按钮：4px–6px 圆角配 `4px–12px` 内边距——紧凑但可用
- 导航链接：15px 文本字重 600 配充足内边距
- 移动端：汉堡菜单配简化导航
- 输入框：generous 垂直内边距用于拇指友好的表单

### 折叠策略
- **导航**：带下拉菜单的完整 mega-menu → 移动端汉堡菜单
- **功能网格**：3 列 → 2 列 → 单列堆叠
- **字体排印**：Display 字号跨断点减小（30px → 更小）
- **插图**：在容器内缩放，部分可能在移动端为节省空间而隐藏
- **区块间距**：成比例减小同时保持可读性

### 图片行为
- 插图在容器内响应式缩放
- 产品截图保持宽高比
- 信任标志在移动端重流为多行网格
- AI 聊天组件在小屏幕上可能重新定位或简化

## 9. Agent 提示词指南

### 快速颜色参考
- 主要文本：Olive Ink（`#4d4f46`）
- 深色文本：Deep Olive（`#23251d`）
- Hover 强调：PostHog Orange（`#F54E00`）
- 深色 CTA：Near-Black（`#1e1f23`）
- 按钮表面：Light Sage（`#e5e7e0`）
- 页面背景：Warm Parchment（`#fdfdf8`）
- 边框：Sage Border（`#bfc1b7`）
- 占位符：Sage Placeholder（`#9ea096`）

### 示例组件提示词
- "在温暖 parchment 背景（#fdfdf8）上创建 hero 区块，30px IBM Plex Sans 标题字重 800，行高 1.20，字间距 -0.75px，olive ink 文本（#4d4f46），以及深色 CTA 按钮（#1e1f23，6px 圆角，白色文本，hover 时透明度 0.7）"
- "设计功能卡片，#fdfdf8 背景，1px #bfc1b7 边框，4px 圆角，IBM Plex Sans 标题 20px 字重 700，以及 16px 正文文本字重 400 行高 1.50 olive ink 文本（#4d4f46）"
- "构建导航栏，温暖背景，IBM Plex Sans 链接 15px 字重 600 deep olive 文本（#23251d），hover 时带下划线，右侧深色 CTA 按钮（#1e1f23）"
- "创建按钮组：主深色（#1e1f23，白色文本，6px 圆角）、次要鼠尾草色（#e5e7e0，#4d4f46 文本，4px 圆角）和 ghost/文本按钮——全部在 hover 时闪现 #F54E00 橙色文本"
- "设计输入框，#eeefe9 背景，1px #b6b7af 边框，4px 圆角，#9ea096 占位符文本，焦点环 #3b82f6 50% 透明度"

### 迭代指南
使用此设计系统优化现有屏幕时：
1. 验证背景是温暖 parchment（#fdfdf8）而非纯白色——鼠尾草奶油温暖感至关重要
2. 检查所有文本使用橄榄色系（#4d4f46、#23251d）而非纯黑或中性灰
3. 确保 hover 状态闪现 PostHog Orange（#F54E00）——如果 hover 感觉平淡，你可能遗漏了这个
4. 确认边框使用鼠尾草色调灰色（#bfc1b7）而非中性灰——温暖贯穿于每个元素
5. 整体基调应感觉像一个有趣、拼搏的初创公司维基——永不企业化精致或无菌
