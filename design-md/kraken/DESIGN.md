# 设计系统：Kraken

## 1. 视觉主题与氛围

Kraken 的网站是一个简洁、值得信赖的加密货币交易所，以紫色作为标志性的品牌色。设计以白色背景为基础，通过 Kraken Purple（`#7132f5`、`#5741d8`、`#5b1ecf`）打造出独特而专业的加密品牌形象。专有的 Kraken-Brand 字体用于展示性标题，采用粗体（700）和负字间距；Kraken-Product（回退字体为 IBM Plex Sans）则作为 UI 界面的主力字体。

**关键特征：**
- 以 Kraken Purple（`#7132f5`）作为主品牌色，搭配更深的变体（`#5741d8`、`#5b1ecf`）
- Kraken-Brand（展示用）+ Kraken-Product（UI 用）双字体系统
- 近黑色（`#101114`）文本，搭配冷调蓝灰色中性色阶
- 12px 圆角按钮（圆润但不呈胶囊形）
- 极淡阴影（`rgba(0,0,0,0.03) 0px 4px 24px`）——若有若无的层级
- 绿色强调色（`#149e61`）用于正面/成功状态

## 2. 色彩系统与角色

### 主色
- **Kraken Purple**（`#7132f5`）：主要 CTA、品牌强调、链接
- **Purple Dark**（`#5741d8`）：按钮边框、描边变体
- **Purple Deep**（`#5b1ecf`）：最深的紫色
- **Purple Subtle**（`rgba(133,91,251,0.16)`）：16% 透明度紫色——淡雅的按钮背景
- **Near Black**（`#101114`）：主要文本

### 中性色
- **Cool Gray**（`#686b82`）：主要中性色，24% 透明度用于边框
- **Silver Blue**（`#9497a9`）：次要文本、弱化元素
- **White**（`#ffffff`）：主表面
- **Border Gray**（`#dedee5`）：分隔线边框

### 语义色
- **Green**（`#149e61`）：成功/正面状态，16% 透明度用于徽章
- **Green Dark**（`#026b3f`）：徽章文本

## 3. 排版规则

### 字体族
- **展示字体**：`Kraken-Brand`，回退字体：`IBM Plex Sans, Helvetica, Arial`
- **UI / 正文**：`Kraken-Product`，回退字体：`Helvetica Neue, Helvetica, Arial`

### 层级

| 角色 | 字体 | 大小 | 字重 | 行高 | 字间距 |
|------|------|------|--------|-------------|----------------|
| 展示级英雄标题 | Kraken-Brand | 48px | 700 | 1.17 | -1px |
| 章节标题 | Kraken-Brand | 36px | 700 | 1.22 | -0.5px |
| 子标题 | Kraken-Brand | 28px | 700 | 1.29 | -0.5px |
| 功能标题 | Kraken-Product | 22px | 600 | 1.20 | normal |
| 正文 | Kraken-Product | 16px | 400 | 1.38 | normal |
| 正文（中等） | Kraken-Product | 16px | 500 | 1.38 | normal |
| 按钮 | Kraken-Product | 16px | 500–600 | 1.38 | normal |
| 说明文字 | Kraken-Product | 14px | 400–700 | 1.43–1.71 | normal |
| 小号文本 | Kraken-Product | 12px | 400–500 | 1.33 | normal |
| 微型文本 | Kraken-Product | 7px | 500 | 1.00 | uppercase |

## 4. 组件样式

### 按钮

**主要紫色按钮**
- 背景：`#7132f5`
- 文本：`#ffffff`
- 内边距：13px 16px
- 圆角：12px

**紫色描边按钮**
- 背景：`#ffffff`
- 文本：`#5741d8`
- 边框：`1px solid #5741d8`
- 圆角：12px

**紫色淡雅按钮**
- 背景：`rgba(133,91,251,0.16)`
- 文本：`#7132f5`
- 内边距：8px
- 圆角：12px

**白色按钮**
- 背景：`#ffffff`
- 文本：`#101114`
- 圆角：10px
- 阴影：`rgba(0,0,0,0.03) 0px 4px 24px`

**次要灰色按钮**
- 背景：`rgba(148,151,169,0.08)`
- 文本：`#101114`
- 圆角：12px

### 徽章
- 成功：`rgba(20,158,97,0.16)` 背景，`#026b3f` 文本，6px 圆角
- 中性：`rgba(104,107,130,0.12)` 背景，`#484b5e` 文本，8px 圆角

## 5. 布局原则

### 间距：1px, 2px, 3px, 4px, 5px, 6px, 8px, 10px, 12px, 13px, 15px, 16px, 20px, 24px, 25px
### 圆角：3px, 6px, 8px, 10px, 12px, 16px, 9999px, 50%

## 6. 深度与层级
- 淡雅：`rgba(0,0,0,0.03) 0px 4px 24px`
- 微型：`rgba(16,24,40,0.04) 0px 1px 4px`

## 7. 设计规范

### 推荐
- CTA 和链接使用 Kraken Purple（#7132f5）
- 所有按钮统一使用 12px 圆角
- 标题使用 Kraken-Brand，正文使用 Kraken-Product

### 禁止
- 不要使用胶囊形按钮——12px 是按钮的最大圆角
- 不要在定义色阶之外使用其他紫色

## 8. 响应式行为
断点：375px, 425px, 640px, 768px, 1024px, 1280px, 1536px

## 9. 智能体提示词指南

### 快速色彩参考
- 品牌：Kraken Purple（`#7132f5`）
- 深色变体：`#5741d8`
- 文本：Near Black（`#101114`）
- 次要文本：`#9497a9`
- 背景：White（`#ffffff`）

### 示例组件提示词
- "创建英雄区域：白色背景。Kraken-Brand 48px 字重 700，letter-spacing -1px。紫色 CTA（#7132f5, 12px 圆角, 13px 16px 内边距）。"
