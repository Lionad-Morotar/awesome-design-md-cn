<a href="https://github.com/VoltAgent/voltagent">
     <img width="1500" height="801" alt="claude-skills" src="https://github.com/user-attachments/assets/d012a0d2-cec3-4630-ba5e-acc339dbe6cf" />
</a>


<br/>
<br/>

<div align="center">
    <strong>受开发者导向网站启发，精心策划的 DESIGN.md 文件合集。</strong>
    <br />
    <br />

</div>

<div align="center">

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
![DESIGN.md Count](https://img.shields.io/badge/DESIGN.md%20count-55-10b981?style=classic)
[![Last Update](https://img.shields.io/github/last-commit/VoltAgent/awesome-design-md?label=Last%20update&style=classic)](https://github.com/VoltAgent/awesome-design-md)
[![Discord](https://img.shields.io/discord/1361559153780195478.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://s.voltagent.dev/discord)

</div>
</div>




# Awesome Design MD

将一份 DESIGN.md 复制到你的项目中，告诉你的 AI 智能体"按照这个样子帮我构建页面"，就能获得真正匹配的像素级精准 UI。


## 什么是 DESIGN.md？

[DESIGN.md](https://stitch.withgoogle.com/docs/design-md/overview/) 是 Google Stitch 引入的一个新概念。它是一份纯文本设计系统文档，AI 智能体可以读取它来生成一致的 UI。

它就是一个 Markdown 文件。不需要 Figma 导出，不需要 JSON Schema，不需要专用工具。把它放到你的项目根目录，任何 AI 编码智能体或 Google Stitch 都能立刻理解你的 UI 应该长什么样。Markdown 是大语言模型最擅长阅读的格式，所以无需额外解析或配置。

| 文件 | 谁来读取 | 定义了什么 |
|------|-------------|-----------------|
| `AGENTS.md` | 编码智能体 | 如何构建项目 |
| `DESIGN.md` | 设计智能体 | 项目的外观与体验 |

**本仓库提供了从真实网站提取的、可直接使用的 DESIGN.md 文件。**



## 每份 DESIGN.md 包含什么

每个文件都遵循 [Stitch DESIGN.md 格式](https://stitch.withgoogle.com/docs/design-md/format/)，并包含扩展章节：

| # | 章节 | 捕获内容 |
|---|---------|-----------------|
| 1 | 视觉主题与氛围 | 情绪、密度、设计哲学 |
| 2 | 调色板与角色 | 语义名称 + 十六进制值 + 功能角色 |
| 3 | 排版规则 | 字体族、完整的层级表 |
| 4 | 组件样式 | 按钮、卡片、输入框、导航及其各状态 |
| 5 | 布局原则 | 间距梯度、网格、留白哲学 |
| 6 | 深度与层级 | 阴影系统、表面层级 |
| 7 | 宜与忌 | 设计护栏与反模式 |
| 8 | 响应式行为 | 断点、触摸目标、折叠策略 |
| 9 | 智能体提示词指南 | 快速颜色参考、可直接使用的提示词 |

每个站点包含：

| 文件 | 用途 |
|------|---------|
| `DESIGN.md` | 设计系统（智能体读取的内容） |
| `preview.html` | 可视化目录，展示色板、字号梯度、按钮、卡片 |
| `preview-dark.html` | 相同目录的深色表面版本 |

### 如何使用


1. 将某个站点的 `DESIGN.md` 复制到你的项目根目录
2. 告诉你的 AI 智能体使用它。

## 合集

### AI 与机器学习

- [**Claude**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/claude/) - Anthropic 的 AI 助手。温暖的陶土色调，干净的编辑式布局
- [**Cohere**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/cohere/) - 企业级 AI 平台。活力渐变，数据密集的仪表盘美学
- [**ElevenLabs**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/elevenlabs/) - AI 语音平台。深色电影感 UI，音频波形美学
- [**Minimax**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/minimax/) - AI 模型提供商。大胆的深色界面，霓虹点缀
- [**Mistral AI**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/mistral.ai/) - 开源权重大语言模型提供商。法式极简主义，紫色调
- [**Ollama**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/ollama/) - 本地运行大语言模型。终端优先，单色极简
- [**OpenCode AI**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/opencode.ai/) - AI 编码平台。面向开发者的深色主题
- [**Replicate**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/replicate/) - 通过 API 运行 ML 模型。干净的白色画布，代码优先
- [**RunwayML**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/runwayml/) - AI 视频生成。电影感深色 UI，富媒体布局
- [**Together AI**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/together.ai/) - 开源 AI 基础设施。技术感，蓝图式设计
- [**VoltAgent**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/voltagent/) - AI 智能体框架。纯黑画布，翡翠绿点缀，终端原生
- [**xAI**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/x.ai/) - Elon Musk 的 AI 实验室。朴素单色，未来主义极简

### 开发者工具与平台

- [**Cursor**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/cursor/) - AI 优先的代码编辑器。流畅的深色界面，渐变点缀
- [**Expo**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/expo/) - React Native 平台。深色主题，紧凑字距，代码导向
- [**Linear**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/linear.app/) - 面向工程师的项目管理。极致极简，精准，紫色点缀
- [**Lovable**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/lovable/) - AI 全栈构建器。活泼的渐变，友好的开发者美学
- [**Mintlify**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/mintlify/) - 文档平台。干净，绿色点缀，阅读优化
- [**PostHog**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/posthog/) - 产品分析。可爱的刺猬品牌，开发者友好的深色 UI
- [**Raycast**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/raycast/) - 效率启动器。流畅的深色外壳，活力渐变点缀
- [**Resend**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/resend/) - 面向开发者的邮件 API。极简深色主题，等宽字体点缀
- [**Sentry**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/sentry/) - 错误监控。深色仪表盘，数据密集，粉紫点缀
- [**Supabase**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/supabase/) - 开源 Firebase 替代方案。深色翡翠主题，代码优先
- [**Superhuman**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/superhuman/) - 高速邮件客户端。高端深色 UI，键盘优先，紫色光晕
- [**Vercel**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/vercel/) - 前端部署平台。黑白精准，Geist 字体
- [**Warp**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/warp/) - 现代终端。深色 IDE 风格界面，块状命令 UI
- [**Zapier**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/zapier/) - 自动化平台。温暖的橙色，友好的插画驱动

### 基础设施与云服务

- [**ClickHouse**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/clickhouse/) - 高速分析数据库。黄色点缀，技术文档风格
- [**Composio**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/composio/) - 工具集成平台。现代深色，多彩集成图标
- [**HashiCorp**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/hashicorp/) - 基础设施自动化。企业级整洁，黑白配色
- [**MongoDB**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/mongodb/) - 文档数据库。绿叶品牌，开发者文档导向
- [**Sanity**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/sanity/) - 无头 CMS。红色点缀，内容优先的编辑式布局
- [**Stripe**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/stripe/) - 支付基础设施。标志性的紫色渐变，weight-300 优雅感

### 设计与效率

- [**Airtable**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/airtable/) - 电子表格-数据库混合体。色彩丰富，友好，结构化数据美学
- [**Cal.com**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/cal/) - 开源日程安排。干净的中性 UI，面向开发者的简约设计
- [**Clay**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/clay/) - 创意机构。有机形状，柔和渐变，艺术指导布局
- [**Figma**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/figma/) - 协作设计工具。多彩活力，活泼又不失专业
- [**Framer**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/framer/) - 网站构建器。大胆的黑蓝配色，动效优先，设计导向
- [**Intercom**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/intercom/) - 客户消息。友好的蓝色调，对话式 UI 模式
- [**Miro**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/miro/) - 可视化协作。亮黄色点缀，无限画布美学
- [**Notion**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/notion/) - 一站式工作空间。温暖的极简主义，衬线标题，柔和表面
- [**Pinterest**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/pinterest/) - 视觉发现平台。红色点缀，瀑布流网格，图片优先
- [**Webflow**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/webflow/) - 可视化网页构建器。蓝色点缀，精致的营销站点美学

### 金融科技与加密货币

- [**Coinbase**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/coinbase/) - 加密货币交易所。干净的蓝色身份，注重信任，机构感
- [**Kraken**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/kraken/) - 加密货币交易平台。紫色点缀的深色 UI，数据密集的仪表盘
- [**Revolut**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/revolut/) - 数字银行。流畅的深色界面，渐变卡片，金融科技精准感
- [**Wise**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/wise/) - 国际汇款。亮绿色点缀，友好且清晰

### 企业与消费

- [**Airbnb**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/airbnb/) - 旅行市场。温暖的珊瑚色点缀，摄影驱动，圆角 UI
- [**Apple**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/apple/) - 消费电子产品。高端留白，SF Pro 字体，电影感图片
- [**BMW**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/bmw/) - 豪华汽车。深色高端表面，精准的德式工程美学
- [**IBM**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/ibm/) - 企业技术。Carbon 设计系统，结构化蓝色调
- [**NVIDIA**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/nvidia/) - GPU 计算。绿黑能量感，技术力量美学
- [**SpaceX**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/spacex/) - 航天技术。朴素黑白，全出血图片，未来感
- [**Spotify**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/spotify/) - 音乐流媒体。深色上的活力绿，大胆字体，专辑封面驱动
- [**Uber**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/uber/) - 出行平台。大胆的黑白配色，紧凑字体，都市能量



## 贡献

欢迎贡献！请参阅 [CONTRIBUTING.md](CONTRIBUTING.md) 了解指南。

- [**请求添加站点**](https://github.com/VoltAgent/awesome-design-md/issues)：提交一个包含 URL 的 Issue
- **改进现有文件**：修正错误的颜色、缺失的 Token、薄弱的描述
- **报告问题**：如果某些内容看起来不对，请告知我们


## 许可证

MIT 许可证 - 详见 [LICENSE](LICENSE)

本仓库是一个从公开网站提取的设计系统文档的精选合集。所有 DESIGN.md 文件按"原样"提供，不作任何担保。提取的设计 Token 代表公开可见的 CSS 值。我们不对任何站点的视觉标识主张所有权。这些文档的存在是为了帮助 AI 智能体生成一致的 UI。
