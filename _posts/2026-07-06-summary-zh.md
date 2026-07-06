---
layout: default
title: "Horizon Summary: 2026-07-06 (ZH)"
date: 2026-07-06
lang: zh
---

> 从 73 条内容中筛选出 19 条重要资讯。

---

1. [Cloudflare 推出 Workers Cache API](#item-1) ⭐️ 8.0/10
2. [sqlite-utils 4.0rc2：AI 编写了大部分代码，并发现关键漏洞](#item-2) ⭐️ 8.0/10
3. [新版 Claude 模型工具调用合规性反而更差](#item-3) ⭐️ 8.0/10
4. [解析七十年：理论与实践](#item-4) ⭐️ 8.0/10
5. [天问二号抵达小行星 Kamo'oalewa，首张图像公布](#item-5) ⭐️ 8.0/10
6. [波士顿动力将 Atlas 转向 AI 驱动控制](#item-6) ⭐️ 8.0/10
7. [机器人像婴儿一样学说话](#item-7) ⭐️ 8.0/10
8. [宝马部署 Figure 03 人形机器人用于制造](#item-8) ⭐️ 8.0/10
9. [任天堂将在欧洲销售可更换电池的 Switch](#item-9) ⭐️ 7.0/10
10. [仅用 500 字节通过 Deflate 和数据 URI 生成世界地图](#item-10) ⭐️ 7.0/10
11. [计算机的速度极限](#item-11) ⭐️ 7.0/10
12. [意外发现新型元胞自动机](#item-12) ⭐️ 7.0/10
13. [Rayfish：基于 Iroh 的 P2P VPN](#item-13) ⭐️ 7.0/10
14. [PREEMPT_NONE 移除：对 PostgreSQL 影响甚微](#item-14) ⭐️ 7.0/10
15. [Gradle 因琐碎工作流问题拒绝使用 jj](#item-15) ⭐️ 7.0/10
16. [Rust 中新颖的错误处理方法](#item-16) ⭐️ 7.0/10
17. [Fortran 现代化：挑战与策略](#item-17) ⭐️ 7.0/10
18. [Threecrate：基于 Rust 的 3D 库在关键任务上超越 Open3D](#item-18) ⭐️ 7.0/10
19. [Agility Robotics 上市并与 NVIDIA 合作安全平台](#item-19) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Cloudflare 推出 Workers Cache API](https://blog.cloudflare.com/workers-cache/) ⭐️ 8.0/10

Cloudflare 宣布推出 Workers Cache，这是一个遵循 HTTP Cache-Control 语义并支持缓存标签失效的 Workers 新缓存 API。 这填补了 Workers 开发者长期以来的空白，使得在 Workers 内部实现细粒度、符合规范的缓存成为可能，从而减轻源站负载并提升性能。 启用 Workers Cache 可能会增加成本，因为之前免费的请求（静态资源、Worker 间调用）现在按标准请求费率计费。该 API 支持缓存标签以实现精确失效和 stale-while-revalidate。

hackernews · ilreb · 7月6日 13:02 · [社区讨论](https://news.ycombinator.com/item?id=48804014)

**背景**: Cloudflare Workers 是一个在边缘运行 JavaScript 的无服务器计算平台。缓存是 CDN 的核心功能，但此前 Workers 缺乏完全遵循 HTTP 缓存标准的原生缓存 API。缓存标签允许开发者按标签失效一组缓存响应，而不是按 URL 清除。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.cloudflare.com/workers/runtime-apis/cache/">Cache · Cloudflare Workers docs</a></li>
<li><a href="https://developers.cloudflare.com/workers/examples/cache-api/">Using the Cache API · Cloudflare Workers docs</a></li>

</ul>
</details>

**社区讨论**: 社区总体上对该功能持积极态度，称赞其遵循 HTTP 规范和缓存标签。然而，多位评论者对计费变化表示担忧，指出启用缓存可能会增加之前免费请求的成本。还有一些人批评文章的写作风格类似 LLM 输出。

**标签**: `#Cloudflare Workers`, `#caching`, `#CDN`, `#serverless`, `#HTTP`

---

<a id="item-2"></a>
## [sqlite-utils 4.0rc2：AI 编写了大部分代码，并发现关键漏洞](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/#atom-everything) ⭐️ 8.0/10

Simon Willison 发布了 sqlite-utils 4.0rc2，其中大部分代码由 Anthropic 的 Claude Fable AI 助手编写，该助手还发现了一个可能导致数据丢失的 delete_where() 关键漏洞，若后续修复将构成破坏性变更。 这展示了 AI 在软件开发中的实用且经济高效的应用：AI 助手不仅编写了主要版本的大部分代码，还在稳定版发布前发现了一个严重漏洞，节省了时间并确保了语义化版本控制（SemVer）合规性。 AI 助手 Claude Fable 通过 iPhone 和笔记本电脑上的 Claude Code 使用，订阅费用约为 149.25 美元。它生成了 34 次提交、跨 30 个文件新增 1,321 行代码并删除 190 行代码，还发现了 5 个发布阻塞问题，其中包括 delete_where() 的事务漏洞。

rss · Simon Willison · 7月5日 01:00

**背景**: sqlite-utils 是一个用于操作 SQLite 数据库的 Python 库和命令行工具。语义化版本控制（SemVer）采用主版本号.次版本号.修订号的格式，破坏性变更需要提升主版本号。Claude Fable 是 Anthropic 推出的 AI 模型，专为复杂编程任务设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/simonw/sqlite-utils">GitHub - simonw/sqlite-utils: Python CLI utility and library for manipulating SQLite databases · GitHub</a></li>
<li><a href="https://www.anthropic.com/news/claude-fable-5-mythos-5">Claude Fable 5 and Claude Mythos 5 \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI-assisted development`, `#sqlite-utils`, `#Claude`, `#software engineering`, `#release management`

---

<a id="item-3"></a>
## [新版 Claude 模型工具调用合规性反而更差](https://simonwillison.net/2026/Jul/4/better-models-worse-tools/#atom-everything) ⭐️ 8.0/10

Armin Ronacher 报告称，包括 Opus 4.8 和 Sonnet 5 在内的新版 Anthropic 模型会生成带有额外虚构字段的畸形工具调用，而旧版模型则没有此问题。 这种退化损害了最先进 LLM 在工具使用方面的可靠性，影响依赖严格模式合规的第三方编码框架（如 Pi），并引发对专有工具过度优化的担忧。 畸形调用特别出现在嵌套的`edits[]`数组中，模型添加了模式中不存在的键。Armin 推测，针对 Claude Code 内置编辑工具的强化学习使新模型对其他工具模式产生偏差。

rss · Simon Willison · 7月4日 22:53

**背景**: 工具调用是 LLM 输出结构化数据以调用外部函数的机制，通常由 JSON 模式定义。模型常通过微调或强化学习来有效使用特定工具，但这可能无意中降低对类似但不同模式的性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lucumr.pocoo.org/2026/7/4/better-models-worse-tools/">About an aggravating tool - calling regression in newer Claude models .</a></li>
<li><a href="https://deepintellica.com/physics-science/better-models-worse-tools/">Better Models : Worse Tools - Deep Intellica</a></li>
<li><a href="https://www.anthropic.com/news/claude-opus-4-8">Introducing Claude Opus 4.8 \ Anthropic</a></li>

</ul>
</details>

**标签**: `#LLM`, `#tool calling`, `#regression`, `#Anthropic`, `#AI reliability`

---

<a id="item-4"></a>
## [解析七十年：理论与实践](https://langsec.org/spw26/papers/lucas-70-years-of-parsing.pdf) ⭐️ 8.0/10

一篇在 LangSec SPW26 上发表的论文回顾了七十年的解析研究，审视了其在语言设计和安全方面的理论基础和实际影响。 这篇回顾性文章强调了解析理论如何塑造了现代编程语言和安全实践，为未来的语言设计和安全解析提供了经验教训。 论文涵盖了从早期形式语言理论到现代解析器生成器的演变，并讨论了解析选择如何影响注入攻击等安全漏洞。

rss · Lobsters · 7月6日 15:46

**背景**: 解析是根据形式语法规则分析符号串的过程，对编译器和解释器至关重要。七十年来，解析理论从上下文无关文法发展到 LR 和 LL 解析等高效算法，影响了语言设计和安全。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Parsing">Parsing - Wikipedia</a></li>
<li><a href="https://link.springer.com/book/10.1007/978-3-642-61345-6">Parsing Theory : Volume I Languages and Parsing | Springer Nature...</a></li>
<li><a href="https://webscraping.ai/faq/lxml/what-are-the-security-implications-of-using-lxml-for-parsing-untrusted-xml">What are the security implications of using lxml for parsing untrusted...</a></li>

</ul>
</details>

**标签**: `#parsing`, `#formal languages`, `#programming languages`, `#language design`, `#security`

---

<a id="item-5"></a>
## [天问二号抵达小行星 Kamo'oalewa，首张图像公布](https://spacenews.com/tianwen-2-arrives-at-asteroid-kamooalewa-first-image-revealed/) ⭐️ 8.0/10

中国的天问二号探测器已抵达近地小行星 Kamo'oalewa，并拍摄了首张图像，显示其是一个细长的小型岩石天体。该任务于 2025 年 5 月 29 日发射，将采集样本并返回地球。 这是中国首次小行星采样返回任务的重要里程碑，推动了行星科学的发展，并展示了中国日益增强的深空探测能力。对 Kamo'oalewa（地球的准卫星）的研究可能为了解近地天体的起源和月球抛射物提供线索。 该小行星直径约 40-100 米，每 28 分钟自转一周。天问二号计划于 2027 年将样本送回地球。

rss · SpaceNews · 7月6日 09:14

**背景**: 天问二号是中国继火星轨道器与巡视器天问一号之后的第二次行星探测任务。Kamo'oalewa（2016 HO3）是地球的准卫星，很可能是来自月球（如乔尔达诺·布鲁诺陨石坑）的抛射物。该任务旨在采集表面样本，随后还将探测一颗主带彗星。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tianwen-2">Tianwen-2 - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kamo'oalewa_(asteroid)">Kamo'oalewa (asteroid)</a></li>
<li><a href="https://spacenews.com/china-launches-tianwen-2-mission-to-sample-near-earth-asteroid/">China launches Tianwen-2 mission to sample near Earth asteroid - SpaceNews</a></li>

</ul>
</details>

**标签**: `#space exploration`, `#asteroid mission`, `#Tianwen-2`, `#planetary science`

---

<a id="item-6"></a>
## [波士顿动力将 Atlas 转向 AI 驱动控制](https://www.reddit.com/r/robotics/comments/1uo4jgo/boston_dynamics_on_aidriven_approach_for_atlas/) ⭐️ 8.0/10

波士顿动力正在将其 Atlas 人形机器人从硬编码行为转向基于 AI 的系统，使其能够在现实环境中更灵活地运行。 这一转变标志着从脚本化演示到实用自适应机器人的重要一步，可能加速在工业和商业环境中的部署。 新的 AI 系统允许 Atlas 从数据中学习并优化行为，无需显式重新编程，与之前的固定程序形成对比。波士顿动力已宣布推出全电动版 Atlas，并计划实现集群学习。

reddit · r/robotics · /u/Responsible-Grass452 · 7月5日 15:08

**背景**: 传统工业机器人依赖硬编码指令执行重复任务，灵活性有限。基于 AI 的系统利用机器学习，使机器人能够适应变化和意外情况。波士顿动力的 Atlas 历来以令人印象深刻但高度脚本化的演示而闻名；这种 AI 驱动的方法旨在使其适用于现实应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/artificial-intelligence-in-robotics/">Artificial Intelligence in Robotics - GeeksforGeeks</a></li>
<li><a href="https://bostondynamics.com/products/atlas/">Atlas Humanoid Robot | Boston Dynamics</a></li>
<li><a href="https://bostondynamics.com/blog/boston-dynamics-unveils-new-atlas-robot-to-revolutionize-industry/">Boston Dynamics Unveils New Atlas Robot to Revolutionize Industry | Boston Dynamics</a></li>

</ul>
</details>

**标签**: `#robotics`, `#humanoid`, `#AI`, `#Boston Dynamics`, `#Atlas`

---

<a id="item-7"></a>
## [机器人像婴儿一样学说话](https://www.reddit.com/r/robotics/comments/1uokw4i/scientists_built_a_robot_that_learns_to_talk_like/) ⭐️ 8.0/10

科学家制造了一个拥有机械声带、人工声道和鼻腔的会说话的机器人，它通过试错反馈学习说话，模仿人类婴儿习得语言的方式。 这种受生物启发的语音合成方法可能彻底改变辅助技术，特别是对于听力受损者，他们可以将机器人作为发音训练的物理模型。 机器人持续监听自己的声音并调整发声器官，直到输出匹配自然发声，使用 10 个伺服电机控制机械部件。

reddit · r/robotics · /u/Similar_Suit_3709 · 7月6日 02:35

**背景**: 传统的语音合成依赖于数字信号处理或神经网络，但这个机器人物理上模仿了人体解剖结构。该研究建立在 Hideyuki Sawada 早期关于 KTR-2“马达嘴”机器人的工作之上，该机器人使用机械声带产生声音。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=qobhDJ_vEOc">Motormouth Robot KTR-2 - Full Original Video - YouTube</a></li>
<li><a href="https://www.researchgate.net/publication/228932982_A_mechanical_voice_system_construction_of_vocal_cords_and_its_pitch_control">(PDF) A mechanical voice system: construction of vocal cords and its...</a></li>

</ul>
</details>

**社区讨论**: Reddit 评论对这种受生物启发的方法及其在言语治疗中的潜力表示着迷，但一些人质疑其与数字方法相比的实际可扩展性和鲁棒性。

**标签**: `#robotics`, `#speech synthesis`, `#AI`, `#assistive technology`, `#bio-inspired`

---

<a id="item-8"></a>
## [宝马部署 Figure 03 人形机器人用于制造](https://www.reddit.com/r/robotics/comments/1unlu7k/bmw_group_deploys_figure_03_humanoid/) ⭐️ 8.0/10

宝马集团已将 Figure AI 的第三代 Figure 03 人形机器人部署到其制造流程中，这标志着先进人形机器人在汽车生产中的重大实际应用。 此次部署标志着人形机器人在工业环境中商业可行性迈出重要一步，可能改变制造效率和劳动力格局。同时，它也验证了 Figure AI 的技术，该公司估值已达 390 亿美元。 Figure 03 是一款通用人形机器人，能够执行多种任务；Figure AI 此前曾展示其机器人连续近一周处理包裹，性能达到人类的 98.5%。该机器人还曾在 2026 年白宫活动中亮相。

reddit · r/robotics · /u/HenryGCase · 7月4日 22:27

**背景**: 人形机器人旨在模仿人类形态和运动，适合在人类环境中执行任务。Figure AI 成立于 2022 年，已迅速开发出三代机器人（Figure 01-03）和两版 Helix AI 模型。宝马的部署代表了此类机器人在汽车制造中首批大规模集成之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Figure_01_Humanoid_Robot">Figure 01 Humanoid Robot</a></li>
<li><a href="https://en.wikipedia.org/wiki/Figure_AI">Figure AI - Wikipedia</a></li>
<li><a href="https://www.figure.ai/">Figure</a></li>

</ul>
</details>

**标签**: `#humanoid robotics`, `#industrial automation`, `#BMW`, `#Figure 03`, `#manufacturing`

---

<a id="item-9"></a>
## [任天堂将在欧洲销售可更换电池的 Switch](https://www.nintendo.com/en-gb/Support/Nintendo-Switch-2/Information-about-upcoming-battery-related-revisions-to-some-Nintendo-products-3132901.html) ⭐️ 7.0/10

任天堂宣布，受欧盟维修权法规推动，将在欧洲推出配备用户可更换电池的 Nintendo Switch、Switch Lite 和 Switch OLED Model 修订版。该公司还计划于 2027 年 2 月中旬停止在欧洲销售所有 Switch 硬件。 此举标志着一家主要游戏硬件制造商向可维修性迈出重要一步，可能通过“布鲁塞尔效应”影响全球产品设计。同时，这也标志着 Switch 在欧洲生命周期的终结，为下一代主机设定了时间表。 修订版产品将在包括欧盟成员国、英国和沙特阿拉伯在内的欧洲地区推出，功能上与现有型号无差异。任天堂将继续生产 Switch 硬件至 2026 年，但从 2027 年 2 月起停止向零售商销售。

hackernews · akyuu · 7月6日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=48804193)

**背景**: 欧盟的维修权法规要求制造商提供备件并设计更易维修的产品，包括用户可更换的电池。任天堂目前的 Switch 型号内置电池难以由消费者自行更换，通常需要专业服务或存在损坏风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.eversheds-sutherland.com/en/united-kingdom/insights/right-to-repair-rules-introduced-in-europe-and-uk">" Right to repair " rules introduced in Europe and UK</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞欧盟法规迫使任天堂提高可维修性，一些人指出“布鲁塞尔效应”可能使这些改变在全球推广。其他人则对任天堂未更早采用可更换电池表示惊讶，因为这似乎是一种产品改进。

**标签**: `#Nintendo`, `#right-to-repair`, `#EU regulation`, `#gaming hardware`, `#sustainability`

---

<a id="item-10"></a>
## [仅用 500 字节通过 Deflate 和数据 URI 生成世界地图](https://simonwillison.net/2026/Jul/4/building-a-world-map-with-only-500-bytes/#atom-everything) ⭐️ 7.0/10

Iwo Kadziela 在 Codex 的协助下，利用 deflate 压缩和 JavaScript 的 fetch 与数据 URI，仅用 445 字节数据生成了一个可信的 ASCII 世界地图。 这展示了一种在 Web 应用中进行极端数据压缩的巧妙技术，说明了如何结合现代浏览器 API 从极少量数据创建丰富内容。 该技术通过 DecompressionStream API 使用 deflate-raw 压缩，压缩数据以 base64 编码的数据 URI 嵌入，并使用 JavaScript 的 fetch()获取。

rss · Simon Willison · 7月4日 23:09

**背景**: Deflate 是一种结合 LZ77 和霍夫曼编码的无损压缩算法，广泛用于 PNG 和 ZIP 等格式。DecompressionStream API 允许在浏览器中解压缩流，而 fetch()可以处理数据 URI 以及 HTTP URL。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DEFLATE_compression_algorithm">DEFLATE compression algorithm</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/API/DecompressionStream">DecompressionStream - Web APIs | MDN</a></li>
<li><a href="https://stackoverflow.com/questions/66573468/why-can-i-fetch-data-uris">javascript - Why can I fetch data URIs ? - Stack Overflow</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者称赞了这种方法的巧妙和简洁，一些人讨论了替代压缩方法和数据 URI 的实际限制。少数人注意到使用 fetch 处理数据 URI 的新颖性。

**标签**: `#compression`, `#JavaScript`, `#ASCII art`, `#data URI`, `#creative coding`

---

<a id="item-11"></a>
## [计算机的速度极限](https://caolan.uk/notes/2026-07-02_a_speed_limit_for_computers.cm) ⭐️ 7.0/10

Lobste.rs 上的一篇文章讨论了计算中的基本速度极限，可能探讨了制约计算性能的物理或理论约束。 理解这些极限对于系统研究和未来硬件设计至关重要，因为它为性能提升设定了现实预期，并指导计算架构的创新。 该文章托管在 caolan.uk 上，在 Lobste.rs 上评分为 7.0/10，表明社区兴趣浓厚。内容本身很简短，但评论区可能包含更深入的讨论。

rss · Lobsters · 7月6日 03:25

**背景**: 计算机面临来自物理学的根本速度极限，例如光速、量子力学约束和能量耗散。这些极限影响处理器的运行速度和数据传输速率。该文章可能探讨了这些约束及其对未来计算的影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.researchgate.net/publication/282691497_Fundamental_Speed_Limits_to_the_Generation_of_Quantumness">(PDF) Fundamental Speed Limits to the Generation of Quantumness</a></li>
<li><a href="https://phys.org/news/2018-03-quantum-limits.html">Quantum speed limits are not actually quantum</a></li>
<li><a href="https://arxiv.org/pdf/1710.03498">Quantum Speed Limit is Not Quantum</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上有社区评论，但内容中未提供。根据评分，讨论可能很活跃，可能围绕这些极限的实际影响展开辩论。

**标签**: `#computing`, `#performance`, `#systems`

---

<a id="item-12"></a>
## [意外发现新型元胞自动机](https://tekstien-marginaalien-keskus.aalto.fi/residenssi/heikki/blog/004-december-2/) ⭐️ 7.0/10

一种名为“Mr. Baby Paint”的新型元胞自动机被意外发现，并在个人博客上分享，同时在 Lobste.rs 上引发讨论。 这一发现为元胞自动机研究增添了新规则，该领域在物理、生物学和计算等领域有应用，可能激发进一步研究。 该自动机是意外发现的，博客文章链接到 Lobste.rs 的讨论以获取社区见解。现有内容未提供具体规则细节。

rss · Lobsters · 7月6日 07:48

**背景**: 元胞自动机是由网格细胞组成的离散计算模型，根据局部规则演化。它们由 Stanislaw Ulam 和 John von Neumann 在 20 世纪 40 年代开创，并通过 Conway 的生命游戏普及。Stephen Wolfram 后来根据行为将其分为四类。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cellular_automaton">Cellular automaton - Wikipedia</a></li>
<li><a href="https://news.ycombinator.com/item?id=48770291">Mr . Baby Paint and accidentally discovering a new cellular automata</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论可能包括对新自动机的技术分析和反应，但输入中未提供具体评论。

**标签**: `#cellular automata`, `#computer science`, `#discovery`, `#mathematics`

---

<a id="item-13"></a>
## [Rayfish：基于 Iroh 的 P2P VPN](https://rayfish.xyz/blog/01-introducing-rayfish) ⭐️ 7.0/10

Rayfish 是一款新型点对点 VPN，利用 Iroh 网络库通过公钥而非 IP 地址在节点间建立直接连接。 这种方法可以简化 VPN 设置并提高隐私性，因为无需中央服务器，可能使去中心化网络更易用。 Iroh 是一个 Rust 库，通过公钥在端点间建立直接连接，Rayfish 在其上构建 VPN 层，形成安全、去中心化的网络。

rss · Lobsters · 7月5日 18:39

**背景**: 传统 VPN 依赖中央服务器路由流量，可能成为瓶颈和隐私风险。P2P VPN 直接连接设备，但通常配置复杂。Iroh 通过使用加密密钥进行寻址简化了这一过程，使直接连接更容易建立。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/n0-computer/iroh">n0-computer/ iroh : IP addresses break, dial keys instead. A library that...</a></li>
<li><a href="https://docs.rs/iroh/latest/iroh/">iroh - Rust</a></li>
<li><a href="https://lib.rs/crates/iroh">Iroh — Rust network library // Lib.rs</a></li>

</ul>
</details>

**标签**: `#P2P`, `#VPN`, `#Iroh`, `#networking`, `#decentralized`

---

<a id="item-14"></a>
## [PREEMPT_NONE 移除：对 PostgreSQL 影响甚微](https://thebuild.com/blog/preempt_none-is-dead-your-postgres-probably-doesnt-care/) ⭐️ 7.0/10

Linux 内核已移除 PREEMPT_NONE 抢占模型，但文章认为这一变化对 PostgreSQL 性能影响甚微，与一些令人担忧的报告相反。 这一澄清意义重大，因为它让 PostgreSQL 用户和管理员放心，内核更改不会降低大多数工作负载的性能，从而避免不必要的恐慌或迁移。 性能回退仅影响高自旋锁争用的工作负载，这在典型的 PostgreSQL 部署中很少见；大多数服务器不会受到影响。

rss · Lobsters · 7月6日 12:31

**背景**: PREEMPT_NONE 是一种 Linux 内核抢占模型，它禁用了大多数抢占，从而最大化服务器工作负载的吞吐量。其在较新内核中的移除引发了对 PostgreSQL 性能的担忧，但实际影响仅限于特定的高争用场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lwn.net/Articles/944686/">Revisiting the kernel 's preemption models (part 1) [LWN.net]</a></li>
<li><a href="https://mydbanotebook.org/posts/postgres-performance-regression-are-we-there-yet/">Postgres performance regression: are we there yet? | My DBA Notebook</a></li>
<li><a href="https://www.reddit.com/r/linux/comments/1sc8yx8/aws_engineer_reports_postgresql_performance/">r/linux on Reddit: AWS Engineer Reports PostgreSQL Performance Halved By Linux 7.0</a></li>

</ul>
</details>

**社区讨论**: Lobsters 和 Reddit 上的社区评论普遍认为，对大多数用户来说影响很小，有些人指出问题被夸大了。少数评论者强调，调整其他内核参数（如 OOM killer 和 swappiness）对 PostgreSQL 性能更为关键。

**标签**: `#PostgreSQL`, `#Linux Kernel`, `#Performance`, `#Preemption`

---

<a id="item-15"></a>
## [Gradle 因琐碎工作流问题拒绝使用 jj](https://blog.gradle.org/the-petty-reason-we-didnt-end-up-using-jj-at-gradle) ⭐️ 7.0/10

Gradle 团队发布博客，解释他们决定不采用 jj（Jujutsu）作为版本控制系统，原因是一个微小但关键的不兼容性：jj 不支持他们依赖的 'git push --force-with-lease' 工作流。 这凸显了即使是像 jj 这样设计良好的工具，也可能因缺少某个工作流特性而被团队拒绝，强调了版本控制采用中向后兼容性和工作流保真度的重要性。 缺失的特性是 jj 无法模拟 'git push --force-with-lease'，Gradle 使用该命令安全地强制推送而不覆盖他人的更改。Gradle 承认 jj 的优势，但认为这个工作流阻碍对他们的团队不可接受。

rss · Lobsters · 7月6日 13:44

**背景**: Jujutsu (jj) 是 Google 开发的与 Git 兼容的版本控制系统，旨在通过更简洁的心智模型简化版本控制。Gradle 是 Java、Android 和 Kotlin 项目流行的构建工具。这篇博客详细介绍了他们评估 jj 作为 Git 潜在替代品的过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://guneycansanli.github.io/my-blog/jj-future-of-git/">Jujutsu ( jj ) – a simple, intuitive version control ... | Guneycan Sanli</a></li>
<li><a href="https://zenn.dev/kosk_t/articles/jj-introduction-guide?locale=en">Benefits and Basic Usage of Jujutsu ( jj ), a Git-Compatible Version ...</a></li>
<li><a href="https://medium.com/the-software-journal/if-you-use-git-daily-googles-jujutsu-jj-might-change-everything-7810f5de0082">If You Use Git Daily, Google’s Jujutsu ( JJ ) Might Change... | Medium</a></li>

</ul>
</details>

**社区讨论**: 在 Lobsters 上，评论者争论缺失的特性是否真的微不足道还是合理的障碍。一些人认为 Gradle 可以调整他们的工作流，而另一些人同意 'force-with-lease' 对于协作安全至关重要。

**标签**: `#version control`, `#jj`, `#Gradle`, `#tooling`, `#engineering culture`

---

<a id="item-16"></a>
## [Rust 中新颖的错误处理方法](https://jtjlehi.github.io/2026/06/25/novel-rust-error-handling.html) ⭐️ 7.0/10

一篇博客文章提出了 Rust 中错误处理的新颖视角，并在 Lobsters 上引发了讨论。 错误处理是 Rust 安全保证的核心方面；一种新方法可能会影响开发者编写健壮系统代码的方式。 该文章托管在个人博客上，并在 Lobsters 上吸引了社区评论，表明有兴趣但尚未广泛采用。

rss · Lobsters · 7月6日 00:17

**背景**: Rust 使用 Result 类型进行错误处理，并通过 ? 操作符进行传播。新颖的方法通常探索替代模式以改进易用性或表现力。

**社区讨论**: Lobsters 上的讨论可能包括对该方法的实用性和新颖性的看法，一些人称赞这个想法，而另一些人则质疑其相对于现有模式的优势。

**标签**: `#Rust`, `#error handling`, `#systems programming`

---

<a id="item-17"></a>
## [Fortran 现代化：挑战与策略](https://amenzwa.github.io/stem/PL/FortranModernisation/) ⭐️ 7.0/10

一篇题为《Fortran 现代化的渺茫希望》的文章探讨了在科学计算中更新 Fortran 代码库的困难和方法，强调了提高可维护性和与现代工具兼容性的必要性。 Fortran 在高性能科学计算中仍然至关重要，现代化遗留代码可以提高性能、减少错误，并实现与 Python 和 C++等新语言的集成。这影响到依赖数十年历史的 Fortran 模拟的研究人员和工程师。 现代化策略包括将 Fortran 代码直接集成到 C/C++/Python 中，或者完全重写。像集成并行化环境（IPE）这样的工具可以自动将遗留的 CFD Fortran 映射到现代 HPC 架构。

rss · Lobsters · 7月6日 04:46

**背景**: Fortran 是最古老的编程语言之一，因其在数值计算中的效率而被广泛应用于科学计算。许多关键代码是用 Fortran 77 等旧标准编写的，缺乏现代特性且难以维护。现代化旨在采用较新的标准（如 Fortran 90/95），提高可移植性和工具支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/codee-com/fortran-modernization">GitHub - codee-com/fortran-modernization</a></li>
<li><a href="https://www.astradian.com/fortran-code-modernization">Fortran Code Modernization — Astradian Technologies</a></li>
<li><a href="https://ntrs.nasa.gov/citations/20020070374">Legacy Code Modernization - NASA Technical Reports Server (NTRS)</a></li>

</ul>
</details>

**标签**: `#Fortran`, `#scientific computing`, `#legacy code`, `#software modernization`

---

<a id="item-18"></a>
## [Threecrate：基于 Rust 的 3D 库在关键任务上超越 Open3D](https://www.reddit.com/r/robotics/comments/1up0ehq/threecrate_a_highperformance_3d_point_cloud_and/) ⭐️ 7.0/10

Threecrate 是一个新的基于 Rust 的 3D 点云和网格处理库，带有 Python 绑定，已在 TUM RGB-D、KITTI 和 nuScenes-mini 数据集上与 Open3D v0.19 进行基准测试。它在文件读取上快 1.8–2.2 倍，CPU 体素下采样快 1.6–1.8 倍，通过 wgpu 的 GPU 下采样最高快 2.9 倍。 该库为常见的 3D 处理任务提供了显著的性能提升，可能惠及依赖点云数据的机器人、自动驾驶和计算机视觉应用。其 Rust 基础保证了内存安全和并发性，而 Python 绑定使其易于被广泛用户使用。 Threecrate 使用 wgpu 进行 GPU 加速的体素下采样，但在大型点云上，其法线估计和单尺度 ICP 比 Open3D 慢（分别为 0.57–1.09 倍和 0.71–0.99 倍）。该项目是开源的，作者积极寻求社区反馈和贡献。

reddit · r/robotics · /u/Practical-Dig-4052 · 7月6日 15:21

**背景**: 点云处理在机器人、自动驾驶和 3D 重建中至关重要。体素下采样通过平均 3D 网格单元内的点来降低点密度，而 ICP（迭代最近点）通过最小化距离来对齐两个点云。Open3D 是一个流行的开源 3D 数据处理库，wgpu 是一个基于 Rust 的便携式 GPU 计算库，实现了 WebGPU 标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pointclouds.org/documentation/tutorials/voxel_grid.html">Downsampling a PointCloud using a VoxelGrid filter — Point Cloud Library 1.15.1-dev documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Iterative_closest_point">Iterative closest point - Wikipedia</a></li>
<li><a href="https://wgpu.rs/">wgpu: portable graphics library for Rust</a></li>

</ul>
</details>

**标签**: `#3D point cloud`, `#Rust`, `#Python bindings`, `#performance`, `#open source`

---

<a id="item-19"></a>
## [Agility Robotics 上市并与 NVIDIA 合作安全平台](https://www.reddit.com/r/robotics/comments/1uoxluu/agility_takes_on_ai_generalization_and_humanoid/) ⭐️ 7.0/10

Agility Robotics 宣布通过与 Churchill Capital Corp. XI 的 SPAC 合并上市，投前估值 25 亿美元，并透露与 NVIDIA 合作，成为其 Halos for Robots 安全平台的首个采用者，用于其人形机器人 Digit。 这标志着人形机器人在仓库中商业化迈出重要一步，重点关注安全性和 AI 泛化能力，可能加速人形机器人在物流和制造业中的采用。 Digit 早期的商业角色包括重复性任务，如搬运料箱、卸载自主移动机器人（AMR）以及将物品放到货架上。SPAC 交易预计将带来 6.2 亿美元的总收益。

reddit · r/robotics · /u/Responsible-Grass452 · 7月6日 13:37

**背景**: Agility Robotics 开发人形机器人 Digit，用于仓库和制造自动化。NVIDIA 的 Halos for Robots 是一个面向物理 AI 的全栈功能安全平台，将自动驾驶汽车的安全技术扩展到机器人领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/ai-trust-center/halos/robotics/">NVIDIA Halos: Functional Safety for Humanoids & Industrial Robots</a></li>
<li><a href="https://nvidianews.nvidia.com/news/nvidia-announces-halos-for-robotics-the-industrys-first-full-stack-safety-system-for-physical-ai">NVIDIA Announces Halos for Robotics, the Industry’s First Full-Stack Safety System for Physical AI | NVIDIA Newsroom</a></li>
<li><a href="https://developer.nvidia.com/blog/inside-nvidia-halos-for-robotics-a-full-stack-functional-safety-system-for-physical-ai/">Inside NVIDIA Halos for Robotics: A Full-Stack Functional Safety System for Physical AI | NVIDIA Technical Blog</a></li>

</ul>
</details>

**社区讨论**: Reddit 讨论中对 IPO 和安全合作表示兴奋，部分用户质疑估值和 Digit 的实际能力。其他人则强调人形机器人安全标准的重要性。

**标签**: `#robotics`, `#humanoid`, `#AI safety`, `#IPO`, `#warehouse automation`

---