---
layout: default
title: "Horizon Summary: 2026-06-15 (ZH)"
date: 2026-06-15
lang: zh
---

> 从 69 条内容中筛选出 26 条重要资讯。

---

1. [Pyodide 314.0 允许将 WASM 轮子发布到 PyPI](#item-1) ⭐️ 9.0/10
2. [vLLM v0.23.0 发布，深度优化 DeepSeek-V4](#item-2) ⭐️ 8.0/10
3. [Iroh 1.0：基于 Rust 的 P2P 网络库，支持 QUIC 打洞](#item-3) ⭐️ 8.0/10
4. [Kobo 拒绝有效 EPUB 文件：Adobe RMSDK 被指为罪魁祸首](#item-4) ⭐️ 8.0/10
5. [Salesforce 以 36 亿美元收购 Fin（前身为 Intercom）](#item-5) ⭐️ 8.0/10
6. [Anthropic 的安全超能力受质疑](#item-6) ⭐️ 8.0/10
7. [为何 AI 不会取代软件工程师](#item-7) ⭐️ 8.0/10
8. [AGI 时代来临，治理体系尚未就绪](#item-8) ⭐️ 8.0/10
9. [Xavier Leroy 出版控制结构新书](#item-9) ⭐️ 8.0/10
10. [Diplomat：为 Rust 库生成多语言 FFI 绑定的工具](#item-10) ⭐️ 8.0/10
11. [DROP TABLE：Postgres 中唯一可扩展的删除操作](#item-11) ⭐️ 8.0/10
12. [利用 C++26 静态反射在编译时解析 JSON](#item-12) ⭐️ 8.0/10
13. [Typst 0.15 带来排版系统重大升级](#item-13) ⭐️ 8.0/10
14. [谷歌 2009 年研究：延迟损害搜索参与度](#item-14) ⭐️ 8.0/10
15. [福克斯以 220 亿美元收购 Roku](#item-15) ⭐️ 7.0/10
16. [苹果将 Claude 集成到 Foundation Models 框架](#item-16) ⭐️ 7.0/10
17. [OpenRouter Fusion API：多模型查询的权衡](#item-17) ⭐️ 7.0/10
18. [科技界书呆子身份的稀释](#item-18) ⭐️ 7.0/10
19. [Kage：将任意网站打包成单个二进制文件供离线浏览](#item-19) ⭐️ 7.0/10
20. [将 SQLite 结果列映射回源表](#item-20) ⭐️ 7.0/10
21. [OpenAI 推出合作伙伴网络，投资 1.5 亿美元](#item-21) ⭐️ 7.0/10
22. [pyinfra：用纯 Python 实现无代理基础设施自动化](#item-22) ⭐️ 7.0/10
23. [解构 Datalog：深入技术探讨](#item-23) ⭐️ 7.0/10
24. [Zinnia：用 Rust 编写的模块化 64 位类 Unix 内核](#item-24) ⭐️ 7.0/10
25. [Clojure 通过优化接近 C 语言性能](#item-25) ⭐️ 7.0/10
26. [MONOLITH：面向 x86 的实验性非 Unix 操作系统](#item-26) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Pyodide 314.0 允许将 WASM 轮子发布到 PyPI](https://simonwillison.net/2026/Jun/13/publishing-wasm-wheels/#atom-everything) ⭐️ 9.0/10

Pyodide 314.0 允许 Python 包维护者直接将 WebAssembly (WASM) 轮子发布到 PyPI，消除了之前 Pyodide 维护者需要手动构建和托管 300 多个包的需求。 这减轻了 Pyodide 维护者的负担，加速了基于浏览器的 Python 运行时的包可用性，使社区更容易通过 WebAssembly 在浏览器中贡献和使用 Python。 该功能由定义 PyEmscripten 平台的 PEP 783 支持，对应的 PyPI 仓库 PR 已于 4 月 21 日合并。首个示例包 luau-wasm 展示了一个 276KB 的轮子，可通过 Pyodide 中的 micropip 安装。

rss · Simon Willison · 6月13日 23:55

**背景**: Pyodide 是将 CPython 移植到 WebAssembly/Emscripten 的项目，允许 Python 在浏览器中运行。此前，带有 C 扩展的包必须由 Pyodide 团队手动移植和托管，形成了瓶颈。PEP 783 标准化了 Emscripten 轮子的平台标签，使得直接发布到 PyPI 成为可能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://peps.python.org/pep-0783/">PEP 783 – Emscripten Packaging | peps.python.org</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（条目 48462759）非常积极，许多用户对减少分发基于 WASM 的 Python 包的摩擦表示兴奋。一些评论者指出这有望提升性能并促进 Pyodide 在 Web 应用中的更广泛采用。

**标签**: `#Pyodide`, `#WebAssembly`, `#Python`, `#PyPI`, `#WASM`

---

<a id="item-2"></a>
## [vLLM v0.23.0 发布，深度优化 DeepSeek-V4](https://github.com/vllm-project/vllm/releases/tag/v0.23.0) ⭐️ 8.0/10

vLLM v0.23.0 正式发布，包含来自 200 位贡献者的 408 次提交，主要改进了 DeepSeek-V4 支持，包括新的注意力内核、Mega-MoE 的 EPLB 支持，并将 Model Runner V2 扩展到 Llama 和 Mistral 等更多稠密模型。 此版本显著提升了 DeepSeek-V4 等先进 MoE 模型的推理性能，并提高了稠密模型的效率，使所有在生产环境中使用 vLLM 的 AI/ML 社区受益。 关键技术细节包括：为 DeepSeek-V4 解耦稀疏 MLA 元数据、TRTLLM-gen 注意力内核、Mega-MoE 的 EPLB 负载均衡，以及 Model Runner V2 现在默认用于 Llama 和 Mistral 稠密模型，并支持 FlashInfer 采样器和可中断 CUDA 图等功能。

github · khluu · 6月15日 05:27

**背景**: vLLM 是一个高性能的大语言模型推理引擎，广泛用于服务 Llama、Mistral 和 DeepSeek 等模型。Model Runner V2 是对核心执行引擎的彻底重写，旨在提高模块化和性能。EPLB（专家并行负载均衡）通过动态平衡 GPU 上的专家副本，解决了 MoE 模型中的热点专家问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://effloow.com/articles/vllm-08-llama4-moe-routing-performance-2026">vLLM 0.8: Native Llama 4 MoE Routing Explained — Effloow</a></li>
<li><a href="https://www.tkj.ai/ai-news/deepseek-open-source-release-dualpipe-and-eplb-technology-innovation-in-large-model-training">DeepSeek open source release: DualPipe and EPLB ... | Tkj.ai</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#DeepSeek-V4`, `#open source`, `#AI infrastructure`

---

<a id="item-3"></a>
## [Iroh 1.0：基于 Rust 的 P2P 网络库，支持 QUIC 打洞](https://www.iroh.computer/blog/v1) ⭐️ 8.0/10

Iroh 1.0 正式发布，这是一个基于 Rust 的点对点网络库，采用 QUIC 打洞技术并支持自定义传输协议，使对等节点之间无需依赖传统 IP 地址即可建立直接连接。 该版本简化了文件共享和分布式系统等应用的点对点连接，减少了对中心化基础设施的依赖。其可扩展的传输设计使其能够适应多样化的网络环境，可能影响未来的网络协议栈。 Iroh 1.0 原生支持 IPv4、IPv6 和中继传输，并通过插件系统支持 WebRTC 或 BLE 等自定义传输。它使用 QUIC 实现加密的多路复用连接，并通过同时连接实现 NAT 打洞。

hackernews · Lobsters · 6月15日 15:13 · [社区讨论](https://news.ycombinator.com/item?id=48542480)

**背景**: 传统的点对点通信在 NAT 后常常失败，需要中继服务器。QUIC 打洞相比基于 TCP 的方法降低了延迟并提高了成功率。Iroh 基于这些技术，为构建 P2P 应用提供了一个开发者友好的库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.rs/iroh/latest/iroh/">iroh - Rust</a></li>
<li><a href="https://github.com/n0-computer/iroh">GitHub - n0-computer/ iroh : IP addresses break, dial keys instead.</a></li>
<li><a href="https://arxiv.org/abs/2408.01791">[2408.01791] Implementing NAT Hole Punching with QUIC Implementing NAT Hole Punching with QUIC - NASA/ADS NAT traversal: QUIC Hole Punching · Issue #1015 · libp2p/go ... Implementing NAT Hole Punching with QUIC - IEEE Xplore Implementing NAT Hole Punching with QUIC - Semantic Scholar NAT traversal and hole punching: from UDP to QUIC with iroh</a></li>

</ul>
</details>

**社区讨论**: 社区反响热烈，开发者称赞 Iroh 的务实方法和生产级应用。一些人质疑其相对于传统 IP/DNS 的价值，并对类似协议的库收费表示担忧。自定义传输功能被视为关键差异化优势。

**标签**: `#peer-to-peer`, `#networking`, `#rust`, `#QUIC`, `#hole-punching`

---

<a id="item-4"></a>
## [Kobo 拒绝有效 EPUB 文件：Adobe RMSDK 被指为罪魁祸首](https://andreklein.net/your-epub-is-fine-kobo-disagrees-blame-adobe/) ⭐️ 8.0/10

一篇技术深度分析文章揭示，Kobo 设备拒绝有效 EPUB 文件的原因是 Adobe RMSDK 中的错误，而非用户操作失误。该文揭露了 Adobe 的软件质量问题如何导致 EPUB 生态系统中广泛的兼容性问题。 这很重要，因为它揭示了 Adobe RMSDK 的系统性可靠性问题，影响了数百万电子书用户和开发者。这些发现强调了数字出版行业需要更好的标准合规性和测试。 作者证明，通过 EPUBCheck 验证的 EPUB 文件仍会被 Kobo 拒绝，原因是 RMSDK 的严格解析。问题源于 Adobe 的专有代码，该代码不透明且难以由第三方调试。

hackernews · Lobsters · 6月14日 22:54 · [社区讨论](https://news.ycombinator.com/item?id=48533848)

**背景**: EPUB 是一种标准电子书格式，除 Kindle 外大多数阅读器都使用。Adobe 的 RMSDK 是一个广泛使用的软件开发工具包，用于渲染带有 DRM 的 EPUB 文件，但它有 bug 多且维护性差的历史。Kobo 设备依赖 RMSDK 渲染 EPUB，因此容易受到其问题的影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.adobe.com/solutions/ebook/rmsdk/faq.html">Adobe Content Server and RMSDK / FAQ</a></li>
<li><a href="https://medium.com/@jiminypan/five-interesting-facts-about-adobe-legacy-ebook-rmsdk-b7be0123c874">Five interesting facts about Adobe legacy eBook RMSDK | by Jiminy Panoz | Medium</a></li>
<li><a href="https://kobowritinglife.zendesk.com/hc/en-us/articles/360058976112-Validating-and-Testing-Your-eBooks">Validating and Testing Your eBooks – Kobo Writing Life Help Centre</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了他们对 Adobe 不可靠性的挫败感，有人指出 Adobe 因糟糕的 QA 而浪费了 Flash 市场份额。另一个人提到甚至难以联系 Adobe 以获取 RMSDK 许可。一些人建议使用 Kobo 的 kepub 格式作为变通方案。

**标签**: `#EPUB`, `#Adobe`, `#eBooks`, `#Kobo`, `#software quality`

---

<a id="item-5"></a>
## [Salesforce 以 36 亿美元收购 Fin（前身为 Intercom）](https://www.salesforce.com/news/press-releases/2026/06/15/salesforce-signs-definitive-agreement-to-acquire-fin/?bc=HL) ⭐️ 8.0/10

Salesforce 已签署最终协议，以约 36 亿美元收购 Fin（前身为 Intercom）这一 AI 客服平台。该交易旨在利用 Fin 的 AI 智能体技术增强 Salesforce 的 Agentforce 平台。 此次收购加剧了 AI 驱动客服市场的竞争，尤其是与估值 158 亿美元的 Sierra 和 45 亿美元的 Decagon 的竞争。这也标志着 Salesforce CEO Marc Benioff 的战略举措，旨在对抗由前联席 CEO Bret Taylor 创立的 Sierra，并防止独立的 AI 支持智能体成为 CRM 生态系统之外的控制点。 Fin 在收购前一个月才从 Intercom 更名。Salesforce 计划利用 Fin 的团队和技术改进 Agentforce，这是其用于构建自定义 AI 智能体以自动化任务的企业平台。

hackernews · colesantiago · 6月15日 12:08 · [社区讨论](https://news.ycombinator.com/item?id=48540126)

**背景**: Fin 是一个 AI 客服平台，可连接各种系统，通过 API 和数据连接器个性化回复并执行操作。Salesforce 的 Agentforce 是一个用于构建自定义 AI 智能体的企业平台。客户支持 AI 智能体领域快速增长，Sierra 和 Decagon 等竞争对手已获得高估值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/06/15/salesforce-acquires-ai-customer-service-platform-fin-for-3-6b/">Salesforce acquires AI customer service platform Fin for $3.6 ...</a></li>
<li><a href="https://www.cnbc.com/2026/06/15/salesforce-ai-customer-service-fin-acquistion.html">Salesforce to buy AI customer service platform Fin for $3.6 ...</a></li>
<li><a href="https://www.siliconrepublic.com/business/salesforce-buys-fin-formerly-intercom-for-3-6bn">Salesforce buys Fin, formerly Intercom, for $3.6bn</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了不同观点：一些人称赞执行良好的 AI 支持智能体（例如 Starlink），而另一些人则质疑 Intercom 等客服公司的长期可行性，指出企业现在可以训练自己的 AI 智能体。还有人担心 AI 智能体可能编造理由拒绝帮助客户。

**标签**: `#acquisition`, `#AI`, `#customer support`, `#Salesforce`, `#SaaS`

---

<a id="item-6"></a>
## [Anthropic 的安全超能力受质疑](https://stratechery.com/2026/anthropics-safety-superpower/) ⭐️ 8.0/10

一篇 Stratechery 文章认为，Anthropic 谨慎发布其 Mythos 模型是出于安全考虑，但社区评论通过强调蒸馏风险和 ITAR 出口管制，质疑了“安全超能力”的说法。 这场辩论意义重大，因为它质疑了 AI 实验室在模型发布后能否真正控制其安全性，尤其是考虑到蒸馏攻击可能剥离安全防护，而 ITAR 法规可能迫使实施更广泛的限制。 评论者指出，模型蒸馏可以在没有安全护栏的情况下复制能力，而 ITAR 出口管制现已适用于 Mythos，仅限美国公民和绿卡持有者访问，Anthropic 无法在内部执行这一限制。

hackernews · swolpers · 6月15日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=48539078)

**背景**: Anthropic 是一家 AI 安全公司，开发像 Claude 这样的大型语言模型。模型蒸馏是一种让较小模型从较大模型学习的技术，可能绕过安全措施。ITAR（国际武器贸易条例）控制国防相关物品的出口，最近已应用于先进 AI 模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks">Detecting and preventing distillation attacks \ Anthropic</a></li>
<li><a href="https://www.kiteworks.com/regulatory-compliance/itar-ai-agents-compliance-gap/">AI and ITAR: Unseen Compliance Risks - kiteworks.com</a></li>

</ul>
</details>

**社区讨论**: 社区评论大多不同意文章的观点，认为蒸馏使安全控制无效，而 ITAR 限制证明 Anthropic 缺乏真正的控制力。一些评论者认为该公司对 AI 权力的渴望令人不安。

**标签**: `#AI Safety`, `#Anthropic`, `#Export Controls`, `#Model Distillation`, `#ITAR`

---

<a id="item-7"></a>
## [为何 AI 不会取代软件工程师](https://simonwillison.net/2026/Jun/14/why-ai-hasnt-replaced-software-engineers/#atom-everything) ⭐️ 8.0/10

Arvind Narayanan 和 Sayash Kapoor 发表了一篇文章，认为证据并不支持 AI 将导致软件工程大规模失业的说法，并引用纽约 WARN 法案数据，显示第一年没有报告任何与 AI 相关的裁员。 这挑战了 AI 将很快取代知识工作者（尤其是被认为特别脆弱的软件工程领域）的主流叙事。如果软件工程师是安全的，那么其他职业可能更不容易受到 AI 驱动的就业替代的影响。 作者指出了软件工程中抗拒自动化的三个真正瓶颈：决定构建什么、验证交付的内容，以及对代码库、业务和环境的深度人类理解。AI 加快了输入代码的速度，但并未解决这些瓶颈。

rss · Simon Willison · 6月14日 23:54

**背景**: 纽约 WARN 法案要求雇主披露 AI 是否导致了裁员；在第一年，超过 160 家公司提交了通知，但没有一家勾选 AI 选项。Narayanan 和 Kapoor 是普林斯顿大学的计算机科学家，以“AI 作为正常技术”的视角而闻名，该视角将 AI 视为具有变革性但并非超级智能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.hunton.com/hunton-employment-labor-perspectives/new-york-warn-act-no-ai-related-layoffs-reported-in-first-year-of-adding-ai-related-disclosure-to-the-system">New York WARN Act: No AI-Related Layoffs Reported in First Year of Adding AI-Related Disclosure to the System</a></li>
<li><a href="https://cyber.harvard.edu/story/2025-04/ai-normal-technology">AI as Normal Technology | Berkman Klein Center</a></li>

</ul>
</details>

**标签**: `#AI`, `#software engineering`, `#job displacement`, `#labor economics`

---

<a id="item-8"></a>
## [AGI 时代来临，治理体系尚未就绪](https://www.interconnects.ai/p/welcome-to-the-agi-era-of-ai-governance) ⭐️ 8.0/10

文章指出，AGI 时代的能力已经到来，这是一个不可逆转的转变，而治理体系尚未做好准备。 这之所以重要，是因为对 AGI 的治理不足可能导致重大社会风险，而该文章引发了关于紧迫政策改革的必要讨论。 作者将当前形势描述为‘单向门’，强调这一转变是永久性的，而现有的治理框架不足以应对。

rss · Interconnects · 6月14日 17:43

**背景**: 人工通用智能（AGI）是一种假设的 AI，能在几乎所有认知任务上达到或超越人类能力。当前的 AI 系统是窄领域的，但快速进展使一些人声称 AGI 能力正在显现。国际 AI 治理一直难以跟上步伐，存在协调僵局以及部署与监管之间的治理差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Artificial_general_intelligence">Artificial general intelligence - Wikipedia</a></li>
<li><a href="https://www.chathamhouse.org/sites/default/files/2026-03/2026-03-30-breaking-the-deadlock-AI-governance-wilkinsonr-et-al.pdf">2026-03-30-breaking-ai-governance-deadlock-wilkinson-et-al</a></li>
<li><a href="https://www.gcaie.org/post/the-ai-governance-gap-why-oversight-is-lagging-behind-deployment">The AI Governance Gap: Why Oversight Is Lagging Behind Deployment</a></li>

</ul>
</details>

**标签**: `#AGI`, `#AI governance`, `#AI policy`, `#ethics`

---

<a id="item-9"></a>
## [Xavier Leroy 出版控制结构新书](https://xavierleroy.org/control-structures/book/index.html) ⭐️ 8.0/10

著名计算机科学家、OCaml 创始人 Xavier Leroy 发布了一本关于编程中控制结构的新书，可在线免费获取。 这本书是对编程语言理论和实践的重要贡献，提供了该领域最具影响力人物之一的深刻见解。 该书涵盖基础和高级控制流机制，借鉴了 Leroy 在函数式编程和形式化方法方面的专业知识。

rss · Lobsters · 6月15日 12:36

**背景**: 控制结构决定了程序指令的执行顺序。Xavier Leroy 是法兰西学院教授，也是编程语言、编译器和认证软件领域的顶尖专家。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://xavierleroy.org/">Xavier Leroy - Home page</a></li>
<li><a href="https://en.wikipedia.org/wiki/Xavier_Leroy">Xavier Leroy - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Control_flow">Control flow - Wikipedia</a></li>

</ul>
</details>

**标签**: `#programming languages`, `#control structures`, `#book`, `#Xavier Leroy`

---

<a id="item-10"></a>
## [Diplomat：为 Rust 库生成多语言 FFI 绑定的工具](http://manishearth.github.io/blog/2026/06/14/diplomat-multi-language-ffi-for-rust-libraries/) ⭐️ 8.0/10

Diplomat 是一款新的 Rust 工具，能够从带注解的 Rust API 自动生成面向 C、C++ 和 JavaScript 的高级 FFI 绑定，从而减少样板代码和安全风险。 这大大降低了将 Rust 库集成到多语言项目中的门槛，使 Rust 在跨语言开发中更易使用，并可能加速其在多语言环境中的采用。 Diplomat 支持单向绑定（外部代码调用 Rust），并且可扩展以支持更多语言。它托管在 GitHub 的 rust-diplomat 组织下，并有《Diplomat 手册》提供文档。

rss · Lobsters · 6月15日 05:53

**背景**: 外部函数接口（FFI）允许一种语言调用另一种语言编写的函数，但手动编写 FFI 绑定容易出错且繁琐。虽然已有 Mozilla 的 UniFFI 和 SuperFFI 等工具，但 Diplomat 专注于以 Rust 为中心的方法，强调简单性和安全性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/rust-diplomat/diplomat">GitHub - rust-diplomat/diplomat: Rust tool for generating FFI ...</a></li>
<li><a href="https://rust-diplomat.github.io/diplomat/">Introduction - The Diplomat Book - rust-diplomat.github.io</a></li>
<li><a href="https://lib.rs/crates/diplomat-tool">diplomat-tool — Rust utility // Lib.rs Introduction - The Diplomat Book - rust-diplomat.github.io diplomat - crates.io: Rust Package Registry rust-diplomat/diplomat | DeepWiki Mix in Rust with C: Delegating FFI definitions to Diplomat diplomat-tool 0.7.0 on Cargo - Libraries.io</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论称赞 Diplomat 是对常见痛点设计良好的解决方案，一些评论者将其与 UniFFI 进行有利比较，并指出其扩展支持更多语言的潜力。

**标签**: `#Rust`, `#FFI`, `#multi-language`, `#tooling`

---

<a id="item-11"></a>
## [DROP TABLE：Postgres 中唯一可扩展的删除操作](https://planetscale.com/blog/the-only-scalable-delete) ⭐️ 8.0/10

文章指出，由于 MVCC 和 VACUUM 的开销，PostgreSQL 中的标准 DELETE 操作不可扩展，而 DROP TABLE 是唯一真正可扩展的删除策略。 这一见解对于管理大规模 Postgres 数据库的开发者和 DBA 至关重要，它揭示了基本的可扩展性限制，并为批量数据删除提供了实用的解决方案。 文章解释了 Postgres 中的 DELETE 会创建死元组，需要 VACUUM 来回收空间，这可能导致膨胀和性能下降。而 DROP TABLE 可以立即释放所有空间，没有这种开销。

rss · Lobsters · 6月15日 05:55

**背景**: PostgreSQL 使用多版本并发控制（MVCC）来处理并发事务，这意味着 DELETE 操作不会物理删除行，而是将其标记为死元组。这些死元组会累积并需要定期执行 VACUUM 来清理，这在大表上可能成为瓶颈。DROP TABLE 通过移除整个表结构及其关联的数据文件完全绕过了这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nemanjatanaskovic.com/blog/postgresql-mvcc-vacuum-internals">PostgreSQL MVCC and Vacuum: Why Your 10GB Table Uses 50GB</a></li>
<li><a href="https://www.postgresql.org/docs/current/routine-vacuuming.html">PostgreSQL: Documentation: 18: 24.1. Routine Vacuuming</a></li>
<li><a href="https://opensource-db.com/optimizing-postgresql-delete-operations-a-deep-dive-into-performance-troubleshooting/">Optimizing PostgreSQL Delete Operations: A Deep Dive into ...</a></li>

</ul>
</details>

**社区讨论**: Lobsters 上的讨论可能围绕使用 DROP TABLE 作为删除策略的实用性展开，一些人建议使用分区或 TRUNCATE 作为替代方案，而另一些人则认同 DELETE 的基本可扩展性问题。

**标签**: `#PostgreSQL`, `#database`, `#scalability`, `#performance`

---

<a id="item-12"></a>
## [利用 C++26 静态反射在编译时解析 JSON](https://lemire.me/blog/2026/06/14/parsing-json-at-compile-time-with-c26-static-reflection/) ⭐️ 8.0/10

一种利用 C++26 的静态反射和#embed 的新方法，使得 JSON 可以在编译时完全解析，并直接生成原生 C++结构体。 该技术消除了运行时解析开销并提高了类型安全性，可能改变 C++应用程序处理配置和数据交换的方式。 该方法依赖于 GCC 16 对#embed 的支持以及 simdjson 库的 consteval JSON 解析器，该解析器利用静态反射在编译时将 JSON 字段映射到结构体成员。

rss · Lobsters · 6月15日 06:07

**背景**: C++26 引入了静态反射（P2996），允许在编译时对类型进行内省。结合#embed（在编译时将文件内容作为字节数组包含），可以在没有运行时开销的情况下解析像 JSON 这样的结构化数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lemire.me/blog/2026/06/14/parsing-json-at-compile-time-with-c26-static-reflection/">Parsing JSON at compile time with C+ + 26 static reflection</a></li>
<li><a href="https://www.linkedin.com/pulse/c26-almost-here-reflection-going-change-everything-chorfa-issam-pmp--fiche">C+ + 26 Is Almost Here And Reflection Is Going to Change Everything</a></li>
<li><a href="https://zread.ai/simdjson/simdjson">Overview | simdjson/simdjson | Zread</a></li>

</ul>
</details>

**标签**: `#C++`, `#compile-time`, `#JSON`, `#reflection`, `#performance`

---

<a id="item-13"></a>
## [Typst 0.15 带来排版系统重大升级](https://typst.app/blog/2026/typst-0.15/) ⭐️ 8.0/10

Typst 0.15 已发布，为这款开源排版系统带来了重大改进，包括增强的功能和易用性。 此版本巩固了 Typst 作为 LaTeX 现代替代品的地位，可能加速其在寻求更快、更易用排版方案的学术界和出版界的采用。 此次更新包含一系列新功能和改进，但公告中未提供具体技术细节；Lobsters 上的社区讨论提供了更多信息。

rss · Lobsters · 6月15日 17:14

**背景**: Typst 是一种基于标记的排版系统，旨在拥有与 LaTeX 相同的强大功能，但语法更简单、编译速度更快，使用 Rust 构建。它旨在解决 LaTeX 常见的痛点，如复杂语法和编译缓慢。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/typst/typst">GitHub - typst / typst : A markup-based typesetting system that is...</a></li>
<li><a href="https://typst.app/docs/">Typst Documentation</a></li>
<li><a href="https://www.underleaf.ai/blog/typst-vs-latex">Typst vs LaTeX: Which Should You Use in 2026? | Underleaf</a></li>

</ul>
</details>

**社区讨论**: 帖子中链接的 Lobsters 讨论可能包含用户反应和技术评论，但提供的内容中未包含具体评论。

**标签**: `#typesetting`, `#open-source`, `#Typst`, `#LaTeX alternative`

---

<a id="item-14"></a>
## [谷歌 2009 年研究：延迟损害搜索参与度](https://services.google.com/fh/files/blogs/google_delayexp.pdf) ⭐️ 8.0/10

谷歌发布了一项 2009 年的研究，显示在搜索结果中增加 100-400 毫秒的延迟会导致用户查询量下降 0.2%-0.6%，并造成可衡量的收入下降。 这项研究成为网络性能优化的基础参考，证明即使是亚秒级延迟也会直接影响用户行为和业务指标。 该实验通过在谷歌搜索结果页面中人为注入延迟，并在数周内测量点击量、每位用户的查询次数以及每位用户的收入变化。

rss · Lobsters · 6月15日 03:24

**背景**: 在 2000 年代末，网络性能通常被视为次要问题。谷歌的研究是首批大规模严格量化延迟成本的研究之一，影响了整个行业对性能预算和速度优化的采纳。

**标签**: `#web performance`, `#latency`, `#user experience`, `#Google`

---

<a id="item-15"></a>
## [福克斯以 220 亿美元收购 Roku](https://www.wsj.com/business/deals/fox-roku-deal-f6e564f9) ⭐️ 7.0/10

福克斯公司已同意以 220 亿美元收购 Roku，将福克斯的体育、新闻和娱乐内容与 Roku 的联网电视平台及 Roku 频道相结合。 此次收购使一家大型内容提供商直接接触到约 30-50%美国家庭的电视硬件，引发反垄断担忧，并可能改变流媒体和电视硬件的竞争格局。 福克斯和 Roku 承诺将 Roku 作为开放、对合作伙伴友好的平台运营，但批评者担心利益冲突和用户体验下降。合并后的公司将成为美国电视收视份额第三大的参与者。

hackernews · thm · 6月15日 12:50 · [社区讨论](https://news.ycombinator.com/item?id=48540499)

**背景**: Roku 是领先的流媒体平台，为智能电视和流媒体设备提供支持，拥有庞大的安装基础。福克斯是一家大型内容提供商，拥有体育、新闻和娱乐资产，包括流媒体服务 Tubi。这笔交易将内容分发与硬件访问相结合，类似于过去的媒体与技术整合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fandomwire.com/biggest-concerns-after-foxs-22b-roku-acquisition/">5 Biggest Concerns After Fox's $22 Billion Roku Acquisition</a></li>
<li><a href="https://investor.foxcorporation.com/news/corp-press-releases/2026/fox-corporation-to-acquire-roku-inc/">Fox Corporation to Acquire Roku, Inc. - Fox Corp Investor</a></li>
<li><a href="https://www.hollywoodreporter.com/business/business-news/fox-acquires-roku-streaming-tech-deal-lachlan-murdoch-1236621853/">Fox to Acquire Roku in $22 Billion Deal - The Hollywood Reporter</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍悲观，用户担心 Roku 失去其服务无关的架构，并偏向福克斯内容。一些用户将此视为转向 Apple TV 等替代品的理由，并提到 Roku 现有的性能和广告问题。

**标签**: `#acquisition`, `#antitrust`, `#streaming`, `#hardware`, `#media`

---

<a id="item-16"></a>
## [苹果将 Claude 集成到 Foundation Models 框架](https://platform.claude.com/docs/en/cli-sdks-libraries/libraries/apple-foundation-models) ⭐️ 7.0/10

苹果发布了一个 Swift 包，将 Anthropic 的 Claude 作为服务器端语言模型集成到其 Foundation Models 框架中，该消息在 WWDC 2026 上宣布。 此举标志着苹果在保持对用户体验控制的同时，将 LLM 商品化的战略，可能影响开发者采用率以及苹果平台上未来 AI 生态系统的格局。 该集成并非 Claude 独有；开发者也可以通过同一框架调用 Google 的 Gemini 模型。苹果还宣布将在今年夏天晚些时候开源 Foundation Models 框架。

hackernews · MehrdadKhnzd · 6月15日 04:55 · [社区讨论](https://news.ycombinator.com/item?id=48536776)

**背景**: 苹果的 Foundation Models 框架提供对大语言模型的访问，用于执行智能任务。在 WWDC 2026 上，苹果通过新的公共 LanguageModel 协议向第三方云模型提供商开放了该框架，允许 Claude 和 Gemini 等模型在服务器端使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.apple.com/documentation/foundationmodels">Foundation Models | Apple Developer Documentation</a></li>
<li><a href="https://www.macrumors.com/2026/06/08/apple-unveils-xcode-and-models-improvements/">Apple Unveils Xcode and Foundation Models Framework ...</a></li>
<li><a href="https://rits.shanghai.nyu.edu/ai/apple-open-sources-its-foundation-models-framework-adds-claude-and-gemini/">Apple Open-Sources Its Foundation Models Framework, Adds ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论反应不一：有人认为苹果在将 LLM 商品化的同时控制用户体验，也有人希望支持本地模型而非仅限服务器端。有评论担心多个应用下载相同的设备端模型会导致存储膨胀，还有人猜测苹果正在构建抽象层，以便最终让开发者过渡到其自有模型。

**标签**: `#Apple`, `#LLM`, `#Foundation Models`, `#Claude`, `#AI Ecosystem`

---

<a id="item-17"></a>
## [OpenRouter Fusion API：多模型查询的权衡](https://openrouter.ai/openrouter/fusion) ⭐️ 7.0/10

OpenRouter 推出了 Fusion API，该 API 将提示并行发送给多个 LLM，并使用一个评判模型合成最终响应，声称以一半的成本达到接近 Fable 级别的性能。 Fusion 引入了一种通过聚合多个模型来提升 LLM 输出质量的新方法，但早期评估显示，与直接调用相比，延迟显著增加（慢 7 倍）且成本更高（高 4 倍），因此仅适用于对质量要求极高的场景。 Fusion 将请求分发到一组配备网络搜索和 bash 工具的模型，然后由评判模型提取共识、矛盾和独特见解。它拥有 128,000 个 token 的上下文窗口，定价为每百万 token 0 美元（目前免费）。

hackernews · tdchaitanya · 6月15日 07:10 · [社区讨论](https://news.ycombinator.com/item?id=48537641)

**背景**: 大型语言模型（LLM）通常各有优劣。多模型聚合技术旨在结合多个 LLM 的输出，以产生更稳健的答案。OpenRouter 是一个通过单一 API 提供对多个 LLM 统一访问的平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/openrouter/fusion">Fusion - API Pricing & Providers | OpenRouter</a></li>
<li><a href="https://aiengineerguide.com/til/openrouter-model-fusion-api/">OpenRouter's Model Fusion API - aiengineerguide.com</a></li>
<li><a href="https://explainx.ai/blog/openrouter-fusion-api-fable-5-alternative-2026">OpenRouter Fusion API: Fable-Level AI Guide 2026 | explainx ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论褒贬不一：一些用户构建了类似系统，发现让一个模型评判另一个模型并不能得到更好的答案；另一些用户进行的评估显示性能慢 7 倍、成本高 4 倍。少数人指出，Fusion 可能仅在质量至关重要时才有用。

**标签**: `#LLM`, `#API`, `#multi-model`, `#performance`, `#evaluation`

---

<a id="item-18"></a>
## [科技界书呆子身份的稀释](https://mrmarket.lol/what-the-fuck-happened-to-nerds/) ⭐️ 7.0/10

这反映了科技行业更广泛的文化转变，即真实性正被地位信号所取代，可能影响社区价值观和创新。 该文章获得了很高的社区参与度（638 分，436 条评论），评论者们在辩论这种变化是科技行业独有的，还是在任何重视地位的行业中都很常见。

hackernews · vrnvu · 6月15日 08:23 · [社区讨论](https://news.ycombinator.com/item?id=48538229)

**背景**: “书呆子”一词历史上用来描述对智力或技术主题（尤其是计算）有深厚、常常是痴迷兴趣的人。近几十年来，随着科技变得有利可图，这个标签被那些更关注财富和地位的人所采用，导致了一种真实性的丧失。

**社区讨论**: 评论者普遍认为这种转变是真实的，一些人指出这在任何重视价值和地位的行业都会发生。其他人则认为“书呆子”从来不是道德行为的保证，当前的讨论是由参与度经济和意识形态冲突塑造的。

**标签**: `#tech culture`, `#nerd identity`, `#social dynamics`, `#community discussion`

---

<a id="item-19"></a>
## [Kage：将任意网站打包成单个二进制文件供离线浏览](https://github.com/tamnd/kage) ⭐️ 7.0/10

Kage 是一款新的开源工具，能将任意网站克隆成单个二进制文件供离线浏览，去除所有脚本和跟踪，生成静态可浏览的镜像。 该工具通过将整个网站打包成一个可执行文件，提供了一种新颖的网页存档方式，无需服务器或网络即可轻松离线访问和携带。 Kage 使用无头 Chrome 渲染页面并去除所有 JavaScript，生成无脚本的镜像，可通过 'kage serve' 命令在本地 HTTP 服务器上提供浏览。

hackernews · Lobsters · 6月14日 17:25 · [社区讨论](https://news.ycombinator.com/item?id=48529990)

**背景**: 网页存档通常将页面保存为 HTML、PDF 或 WARC 文件，往往需要复杂配置。Kage 通过创建包含整个站点的单个二进制文件简化了这一过程，克隆后无需外部依赖或网络访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/tamnd/kage">GitHub - tamnd/ kage : Shadow any website for offline viewing, with the...</a></li>
<li><a href="https://getaninsight.com/general/technology-operations-signal-monitor-show-hn-kage-shadow-any-website-to-a-single/">Technology operations signal monitor: Show HN: Kage – Shadow any...</a></li>

</ul>
</details>

**社区讨论**: 社区成员讨论了使用 ascii-gif 生成演示 GIF、离线公司 Wiki 等潜在用例，以及与 SingleFile 等工具的比较。有人质疑查看静态内容是否需要服务器，而其他人则欣赏其无跟踪的承诺。

**标签**: `#offline`, `#archiving`, `#static-site`, `#tool`, `#web`

---

<a id="item-20"></a>
## [将 SQLite 结果列映射回源表](https://simonwillison.net/2026/Jun/13/sqlite-column-provenance/#atom-everything) ⭐️ 7.0/10

Simon Willison 探索了将 SQL 查询结果中的每一列映射回其源 table.column 的编程技术，并使用 Claude Code (Opus 4.8) 原型化了多种解决方案，包括 APSW、通过 ctypes 访问 SQLite 的 C API 以及分析 EXPLAIN 输出。 这一能力将使 Datasette 能够为任意 SQL 查询结果渲染更丰富的元数据，例如列特定的格式或工具提示，从而显著改善数据探索体验。同时，它也展示了 AI 辅助编程如何加速解决小众但有影响力的技术问题。 SQLite 内部会计算列的血缘关系，并通过 sqlite3_column_table_name() C 函数暴露，但该函数在 Python 的标准 sqlite3 模块中并未暴露。该研究发现了三种可行的方法：使用 APSW 库、通过 ctypes 直接调用 C 函数，或者解析 EXPLAIN 输出。

rss · Simon Willison · 6月13日 23:05

**背景**: Datasette 是一个用于探索和发布数据的开源工具，严重依赖 SQLite。当用户编写自定义 SQL 查询时，Datasette 目前无法知道每个结果列来自哪个源表，这限制了高级渲染功能。列血缘关系就是追踪这一来源的元数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/13/sqlite-column-provenance/">Research: Mapping SQLite result columns back to their source ...</a></li>

</ul>
</details>

**标签**: `#SQLite`, `#Datasette`, `#SQL`, `#AI-assisted programming`

---

<a id="item-21"></a>
## [OpenAI 推出合作伙伴网络，投资 1.5 亿美元](https://openai.com/index/introducing-openai-partner-network) ⭐️ 7.0/10

OpenAI 宣布推出 OpenAI 合作伙伴网络，并投入 1.5 亿美元支持全球合作伙伴加速企业级 AI 的采用和部署。 这一举措标志着 OpenAI 战略性地推动企业级 AI 的普及，可能重塑企业整合 AI 解决方案的方式，并为全球合作伙伴创造新的机遇。 1.5 亿美元的投资将用于为合作伙伴提供资源、专业知识和支持，帮助他们为企业客户构建和扩展 AI 解决方案。

rss · OpenAI Blog · 6月14日 17:00

**背景**: OpenAI 是一家领先的人工智能研究机构，以开发 GPT-4 等先进模型而闻名。企业级 AI 采用是指将 AI 技术整合到企业运营中，以提高效率和创新能力。合作伙伴网络在科技行业中很常见，用于扩展覆盖范围和能力。

**标签**: `#OpenAI`, `#Enterprise AI`, `#Partnership`, `#AI Adoption`

---

<a id="item-22"></a>
## [pyinfra：用纯 Python 实现无代理基础设施自动化](https://pyinfra.com/) ⭐️ 7.0/10

pyinfra 是一个开源工具，它将 Python 代码作为 shell 命令在 SSH 服务器、本地机器和 Docker 容器上执行，实现无代理基础设施自动化。 它提供了基于 YAML 的工具（如 Ansible）的 Python 原生替代方案，执行速度更快（最高 6 倍），并利用 Python 的全部能力处理复杂逻辑，使基础设施即代码更易用、更灵活。 pyinfra 支持幂等操作、实时调试、跨数千台主机的并行执行，并通过连接器与 Docker、Terraform 和 Vagrant 集成。

rss · Lobsters · 6月15日 11:05

**背景**: 像 Ansible 和 Chef 这样的基础设施自动化工具通常使用 YAML 或 DSL 来定义状态。pyinfra 则使用纯 Python，允许开发者直接使用循环、条件语句和库。其无代理方法意味着目标机器上无需安装任何软件，只需 SSH 访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pyinfra.com/">pyinfra — agentless infrastructure automation, in plain Python</a></li>
<li><a href="https://github.com/pyinfra-dev/pyinfra">GitHub - pyinfra-dev/pyinfra: pyinfra turns Python code ... Automating Infrastructure Management with Pyinfra - Medium pyinfra · PyPI pyinfra-dev/pyinfra | DeepWiki Infrastructure as code with pyinfra - cusy Dive into Pyinfra - mmap.page</a></li>

</ul>
</details>

**标签**: `#infrastructure automation`, `#Python`, `#devops`, `#agentless`

---

<a id="item-23"></a>
## [解构 Datalog：深入技术探讨](https://www.rntz.net/post/my-thesis.html) ⭐️ 7.0/10

文章《解构 Datalog》对 Datalog 编程语言进行了详细的技术探讨，可能涵盖其基础、实现和评估策略。 这项分析对于对逻辑编程、数据库和查询语言感兴趣的开发者和研究人员意义重大，因为 Datalog 提供了一种与 Prolog 不同的、采用自底向上评估的声明式方法。 Datalog 在语法上是 Prolog 的子集，但采用自底向上的评估模型，使其适用于查询关系数据库和知识图谱。文章可能深入探讨其理论基础和实际实现。

rss · Lobsters · 6月14日 17:07

**背景**: Datalog 是一种声明式逻辑编程语言，源于逻辑编程范式。与 Prolog 的自顶向下评估不同，Datalog 通常采用自底向上的评估，这保证了终止性，非常适合数据库查询。它被用于演绎数据库、数据集成和静态分析等领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Datalog">Datalog - Wikipedia</a></li>
<li><a href="https://datalog.dev/article/Introduction_to_Datalog_programming_language.html">Introduction to Datalog Programming Language</a></li>

</ul>
</details>

**标签**: `#Datalog`, `#programming languages`, `#databases`, `#logic programming`

---

<a id="item-24"></a>
## [Zinnia：用 Rust 编写的模块化 64 位类 Unix 内核](https://zinnia-os.org/) ⭐️ 7.0/10

Zinnia 是一个几乎完全用 Rust 编写的模块化 64 位类 Unix 内核，旨在最小化不安全代码并实现 POSIX 2024 兼容性。该项目始于 2024 年，已能使用 Limine 引导加载程序在真实 x86_64 硬件上启动。 Zinnia 展示了 Rust 在内核级系统编程中的可行性，有望提升安全性和可靠性。其模块化架构以及对移植 Linux 驱动的支持，可能加速基于 Rust 的内核在生产环境中的采用。 该内核使用 Rust 编写，仅含极少量不安全代码，并力求完全符合 POSIX 2024 标准。它采用模块化设计，组件可在运行时加载，支持 x86_64 架构并通过 Limine 实现 UEFI 启动。

rss · Lobsters · 6月14日 21:05

**背景**: 内核是操作系统的核心，负责管理硬件和系统资源。模块化内核允许系统部分作为模块在运行时加载，兼顾性能与灵活性。Rust 是一种注重内存安全且无需垃圾回收的系统编程语言，因此对内核开发颇具吸引力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/zinnia-os/zinnia">GitHub - zinnia-os/zinnia: Modular Unix-like 64-bit kernel</a></li>
<li><a href="https://news.ycombinator.com/item?id=48532705">Zinnia: A modular 64-bit Unix-like kernel written in Rust ...</a></li>
<li><a href="https://ecosistemastartup.com/zinnia-kernel-en-rust-que-es-y-por-que-importa-en-2026/">Zinnia kernel en Rust: qué es y por qué importa en 2026</a></li>

</ul>
</details>

**标签**: `#Rust`, `#kernel`, `#Unix-like`, `#systems programming`

---

<a id="item-25"></a>
## [Clojure 通过优化接近 C 语言性能](https://ertu.dev/posts/4_clojure-reaching-c-performance/) ⭐️ 7.0/10

一篇博客文章展示了基于 JVM 的函数式语言 Clojure 可以通过类型提示、原始算术和避免反射等技术优化，达到接近 C 语言的性能。 这挑战了动态函数式语言天生缓慢的普遍看法，表明 Clojure 在保持其表现力的同时，可以胜任对性能要求苛刻的应用。 该文章可能使用了 `(set! *unchecked-math* :warn-on-boxed)` 和类型提示等技术来消除装箱和反射开销，在特定数值计算任务中达到与 C 相当的速度。

rss · Lobsters · 6月15日 04:44

**背景**: Clojure 是一种运行在 JVM 上的动态函数式语言，通常由于装箱、反射和垃圾回收而带来额外开销。然而，通过利用 JVM 的即时编译并应用 Clojure 特定的优化，开发者可以显著缩小与 C 等静态编译语言之间的性能差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://softwarepatternslexicon.com/clojure/clojure-language-features-and-best-practices/performance-optimization-tips/">Performance Optimization Tips | Software Patterns Lexicon</a></li>
<li><a href="https://practical.li/clojure/reference/performance/">Clojure Performance - Practicalli Clojure Improve Speed and Performance in Your Clojure Development ... A performance optimization workflow - Clojure - CodeScene Functional Optimization in Clojure | Functional Programming ... Clojure Speed: Evaluating the Performance of Clojure Improving the performance of the popular Clojure development ...</a></li>
<li><a href="https://www.freshcodeit.com/blog/clojure-speed-evaluating-the-performance-of-clojure">Clojure Speed Comparison: Evaluating the Performance of ...</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论可能包含专家对这类优化实用性的评论、与代码可读性的权衡，以及与其他 JVM 语言（如 Java 或 Kotlin）的比较。

**标签**: `#Clojure`, `#performance`, `#optimization`, `#JVM`

---

<a id="item-26"></a>
## [MONOLITH：面向 x86 的实验性非 Unix 操作系统](https://codeberg.org/MONOLITH-Project/MONOLITH) ⭐️ 7.0/10

MONOLITH 是一个面向 x86 架构的实验性非 Unix 操作系统，旨在探索替代性的操作系统设计原则。 该项目挑战了类 Unix 设计的主导地位，可能为操作系统结构和性能提供新颖的见解。 MONOLITH 托管在 Codeberg 上，处于早期开发阶段，尚未有稳定版本。它专注于 x86 硬件，该硬件广泛应用于个人电脑和服务器。

rss · Lobsters · 6月15日 16:54

**背景**: 大多数现代操作系统（如 Linux、Windows、macOS）都是类 Unix 或受 Unix 设计影响。非 Unix 系统（如微软的 Singularity）已表明，通过重新思考基本假设，替代设计可以提高可靠性和安全性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Unix-like">Unix-like - Wikipedia</a></li>
<li><a href="https://dev.to/viz-x/singularity-a-non-posix-operating-system-built-by-microsoft-42k7">Singularity: A Non-POSIX Operating System Built By Microsoft</a></li>
<li><a href="https://en.wikipedia.org/wiki/X86">x86 - Wikipedia</a></li>

</ul>
</details>

**标签**: `#operating systems`, `#x86`, `#experimental`, `#systems programming`

---