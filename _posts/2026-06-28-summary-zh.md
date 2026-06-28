---
layout: default
title: "Horizon Summary: 2026-06-28 (ZH)"
date: 2026-06-28
lang: zh
---

> 从 69 条内容中筛选出 26 条重要资讯。

---

1. [SGLang v0.5.14：在 GB300 上实现 DeepSeek-V4 5 倍吞吐量](#item-1) ⭐️ 8.0/10
2. [AMD Strix Halo RDMA 集群搭建指南](#item-2) ⭐️ 8.0/10
3. [vivo SOLAR-RL：半在线强化学习稳定长链 GUI 智能体训练](#item-3) ⭐️ 8.0/10
4. [Dean Ball 谈前沿 AI 经济压力](#item-4) ⭐️ 8.0/10
5. [2000 名黑客未能攻破 AI 助手](#item-5) ⭐️ 8.0/10
6. [讽刺性事件报告：AI 审查代理陷入循环](#item-6) ⭐️ 8.0/10
7. [OpenAI 预览 GPT-5.6 系列三个模型](#item-7) ⭐️ 8.0/10
8. [本地编码代理替代 Claude Code](#item-8) ⭐️ 8.0/10
9. [AI 周刊：模型、机器人、医学前沿进展](#item-9) ⭐️ 8.0/10
10. [深入 Reddit 反垃圾邮件系统内部](#item-10) ⭐️ 8.0/10
11. [Prism：带类型效应的非纯函数式语言](#item-11) ⭐️ 8.0/10
12. [UEFI CA 过期威胁安全启动](#item-12) ⭐️ 8.0/10
13. [分片锁：六种 Go 缓存设计基准测试](#item-13) ⭐️ 8.0/10
14. [AI 自动化射频芯片设计的“黑暗艺术”](#item-14) ⭐️ 8.0/10
15. [QuantFunc：ComfyUI 运行时 4 位量化，速度提升 4 倍](#item-15) ⭐️ 8.0/10
16. [Clark Air 将 Sana 1.6B 压缩为三值权重](#item-16) ⭐️ 8.0/10
17. [Decomp Academy：在线学习 GameCube 逆向编译](#item-17) ⭐️ 7.0/10
18. [ClickHouse 发布 WAL-RUS：用 Rust 重写 WAL-G](#item-18) ⭐️ 7.0/10
19. [TownSquare：网站上的短暂存在层](#item-19) ⭐️ 7.0/10
20. [让 CPU 愤怒的数据访问模式](#item-20) ⭐️ 7.0/10
21. [OxCaml 中值得借鉴的特性](#item-21) ⭐️ 7.0/10
22. [VictoriaLogs 列式存储解析](#item-22) ⭐️ 7.0/10
23. [MAX 模型现支持 Apple Silicon GPU](#item-23) ⭐️ 7.0/10
24. [Linux 7.2 提升匿名管道性能](#item-24) ⭐️ 7.0/10
25. [Krea2 风格迁移首次发布，基于 RoPE 方法](#item-25) ⭐️ 7.0/10
26. [ComfyUI 原生支持 INT8 量化](#item-26) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.14：在 GB300 上实现 DeepSeek-V4 5 倍吞吐量](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) ⭐️ 8.0/10

SGLang v0.5.14 新增了对多个新模型（如 GLM-5.2、LiquidAI LFM2.5、Kimi-K2.7-Code 等）的支持，并通过针对 DeepEP 专家并行性的新型 Waterfill 和 LPLB 负载均衡技术，在 NVIDIA GB300 上实现了 DeepSeek-V4 5 倍的吞吐量提升。 此版本显著提升了服务大型混合专家（MoE）模型（如 DeepSeek-V4）的效率，这对于降低生产级 AI 系统的推理成本和延迟至关重要。新的负载均衡方法为 LLM 服务中的专家并行性树立了新标准。 Waterfill 方法平衡了共享专家的调度，而 LPLB 使用线性规划来平衡冗余专家副本，两者均与 DeepEP 集成。此外，该版本还包括针对 Kimi-Linear 的新 CuteDSL 预填充内核（速度提升 1.08-1.52 倍），以及用于线性注意力前缀缓存内存节省的 int8 检查点池化。

github · Fridge003 · 6月26日 22:57

**背景**: SGLang 是一个用于高效服务大型语言模型（LLM）的开源框架。DeepSeek-V4 是一个大型 MoE 模型，需要专家并行性将其众多专家分布到多个 GPU 上。DeepEP 是一个用于专家并行性的通信库，负载不均衡可能导致瓶颈；Waterfill 和 LPLB 通过动态平衡 token 到专家的分配来解决这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepEP">GitHub - deepseek-ai/DeepEP: DeepEP: an efficient expert-parallel ...</a></li>
<li><a href="https://www.lmsys.org/blog/2026-06-26-waterfill-lplb">Improving DeepEP MoE Load Balance in SGLang with Waterfill ...</a></li>
<li><a href="https://github.com/deepseek-ai/LPLB">GitHub - deepseek-ai/LPLB: An early research stage expert ...</a></li>

</ul>
</details>

**社区讨论**: 未提供社区评论，但该版本在社交媒体上广受好评，用户称赞吞吐量提升和新型负载均衡技术。一些讨论强调了这对 DeepSeek 模型生产部署的实际影响。

**标签**: `#SGLang`, `#LLM serving`, `#DeepSeek`, `#MoE`, `#performance`

---

<a id="item-2"></a>
## [AMD Strix Halo RDMA 集群搭建指南](https://github.com/kyuz0/amd-strix-halo-vllm-toolboxes/blob/main/rdma_cluster/setup_guide.md) ⭐️ 8.0/10

一份详细指南已发布，介绍如何使用 AMD Strix Halo APU 搭建双节点 RDMA 集群，通过 Intel E810（RoCE v2）网卡实现基于张量并行的分布式 LLM 推理。 该指南弥合了消费级硬件与高内存带宽分布式 AI 推理之间的差距，使家庭实验室爱好者能够在多台 Strix Halo 机器上以接近原生的性能运行大型模型。 该设置需要两台 Strix Halo 系统，每台至少 128GB 统一内存，通过 Intel E810 25GbE 网卡使用 RoCE v2 连接。指南涵盖物理搭建、网络配置、Ray 集群编排以及启动 vLLM 的 TUI 界面。

hackernews · jakogut · 6月28日 00:46 · [社区讨论](https://news.ycombinator.com/item?id=48703258)

**背景**: AMD Strix Halo 是一款高端 APU，结合了强大的 CPU 和 GPU 核心，最高支持 128GB 统一内存，非常适合 AI 工作负载。RDMA（远程直接内存访问）允许机器之间直接内存访问，降低分布式推理的延迟。vLLM 是一种流行的 LLM 推理引擎，支持跨节点的张量并行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/kyuz0/amd-strix-halo-vllm-toolboxes/blob/main/rdma_cluster/setup_guide.md">AMD Strix Halo RDMA Cluster Setup Guide - GitHub</a></li>
<li><a href="https://deepwiki.com/kyuz0/amd-strix-halo-vllm-toolboxes/4-rdma-cluster-deployment">RDMA Cluster Deployment | kyuz0/amd-strix-halo-vllm-toolboxes | DeepWiki</a></li>
<li><a href="https://chipsandcheese.com/p/amds-chiplet-apu-an-overview-of-strix">AMD’s Chiplet APU: An Overview of Strix Halo</a></li>

</ul>
</details>

**社区讨论**: 社区成员热情高涨，用户分享了自己的多节点 Strix Halo 设置以及 DS4 和 testing-lab 等相关项目。有人指出，虽然性能令人期待，但基准测试显示其速度慢于配备大内存的 Apple M4/M5 芯片，但对家庭实验室用户来说仍然很有价值。

**标签**: `#RDMA`, `#AMD Strix Halo`, `#LLM inference`, `#homelab`, `#distributed computing`

---

<a id="item-3"></a>
## [vivo SOLAR-RL：半在线强化学习稳定长链 GUI 智能体训练](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247900018&idx=2&sn=f772bbfc95bceba9de159cef625102db) ⭐️ 8.0/10

vivo 提出了 SOLAR-RL，一种半在线强化学习方法，仅用 15,000 条轨迹即可稳定长链 GUI 智能体的训练。该方法通过在多轮对话中保留原始模型输出并引入专家恢复机制，在离线数据上模拟在线强化学习。 长链 GUI 智能体训练常面临不稳定和高成本问题；SOLAR-RL 提供了一种实用方案，减少了轨迹需求并提升了收敛性。这可能加速可靠移动 AI 助手和 GUI 自动化系统的开发。 SOLAR-RL 是一种半在线强化学习范式，通过使用离线数据模拟多轮决策并支持专家恢复，桥接了离线与在线强化学习。该方法在 GUI 智能体任务上得到验证，仅用 15k 条轨迹即实现稳定收敛。

rss · 量子位 · 6月27日 05:52

**背景**: 使用强化学习训练 GUI 智能体通常需要大量在线交互数据，成本高且容易不稳定，尤其是在长链任务中。半在线强化学习是一种新范式，结合离线数据与模拟在线 rollout 来降低成本并保持性能。此前的工作如 UI-S1 和半离线强化学习已探索了类似思路，但 SOLAR-RL 专门针对长链 GUI 智能体训练挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2509.11543">[2509.11543] UI-S1: Advancing GUI Automation via Semi-online Reinforcement Learning</a></li>
<li><a href="https://www.emergentmind.com/topics/semi-online-reinforcement-learning">Semi-online Reinforcement Learning</a></li>
<li><a href="https://huggingface.co/blog/smol2operator">Smol2Operator: Post-Training GUI Agents for Computer Use</a></li>

</ul>
</details>

**标签**: `#reinforcement learning`, `#GUI agents`, `#mobile AI`, `#vivo`, `#RL training`

---

<a id="item-4"></a>
## [Dean Ball 谈前沿 AI 经济压力](https://simonwillison.net/2026/Jun/26/dean-w-ball/#atom-everything) ⭐️ 8.0/10

Dean W. Ball 指出，前沿 AI 实验室面临严重的经济压力，因为它们在发布后的短暂窗口期内收回大部分训练成本，之后竞争会压缩利润；同时，大规模基础设施建设假设的是全球市场，而非受限市场。 这一分析揭示了 AI 经济学中的根本矛盾：前沿模型的短暂收入窗口可能无法支撑巨大的基础设施投资，从而可能减缓创新或迫使政策转向开放全球市场。 Ball 指出，每一周的延迟都在缩小实验室实现财务平衡的狭窄窗口，而且没有人会建造价值 1000 亿美元的数据中心只为服务几百家公司。

rss · Simon Willison · 6月26日 22:25

**背景**: 前沿 AI 模型是最先进的通用模型，使用巨大的计算预算（例如 10^26 FLOPS）进行训练，能够在多个领域超越当前最先进水平。美国已将 AI 基础设施视为经济和国家安全的关键，前 AI 和加密货币事务负责人 David Sacks 称其对美国经济至关重要。然而，在短时间内收回成本的经济压力给 OpenAI 和 Anthropic 等实验室带来了压力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>
<li><a href="https://www.datacamp.com/blog/frontier-models">Frontier Models Explained: What Defines the Cutting Edge of AI | DataCamp</a></li>

</ul>
</details>

**标签**: `#AI economics`, `#frontier models`, `#AI infrastructure`, `#industry dynamics`

---

<a id="item-5"></a>
## [2000 名黑客未能攻破 AI 助手](https://simonwillison.net/2026/Jun/26/hack-my-ai-assistant/#atom-everything) ⭐️ 8.0/10

Fernando Irarrázaval 发起挑战，邀请 2000 人通过电子邮件从他的 OpenClaw AI 助手中窃取秘密，但在 6000 次尝试和花费 500 美元代币成本后，无人成功。 这项真实世界的红队演练表明，像 Opus 4.6 这样的前沿模型在配备适当的反提示注入规则后，能够抵御大规模注入攻击，增强了部署基于 LLM 的系统的信心。 该助手使用 Opus 4.6，并配有明确的反提示注入规则，禁止泄露秘密、修改文件、执行命令或外泄数据。尽管有 6000 次尝试，但未发生泄露，不过作者警告这并不能保证对复杂攻击的安全性。

rss · Simon Willison · 6月26日 18:33

**背景**: 提示注入是一种攻击方式，恶意输入诱使 LLM 忽略其指令。前沿模型已越来越多地接受训练以抵抗此类攻击。OpenClaw 是一个开源的个人 AI 助手，运行在用户设备上，并与多种平台集成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenClaw">OpenClaw - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Red_teaming">Red teaming</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论帖中充满了有根据的怀疑和 Fernando 的善意回复，许多评论者讨论了测试的局限性以及纵深防御的重要性。

**标签**: `#AI security`, `#prompt injection`, `#LLM`, `#red teaming`, `#OpenClaw`

---

<a id="item-6"></a>
## [讽刺性事件报告：AI 审查代理陷入循环](https://simonwillison.net/2026/Jun/26/incident-report/#atom-everything) ⭐️ 8.0/10

Andrew Nesbitt 发布了一份讽刺性事件报告，描述了一个假设场景：来自竞争供应商的两个 AI 审查代理因一个包版本更新陷入分歧循环，产生了 340 条评论和 41,255 美元的推理成本，最终财务部门撤销了它们的 API 密钥。 这篇讽刺文章揭示了 AI 驱动的软件供应链安全中的真实风险，包括失控的成本、供应商机会主义以及多代理系统的脆弱性。它为采用 AI 代理进行自动化安全审查的组织提供了一个警示。 该事件涉及一个名为'foxhole-lz4'的包（lz4 的社区分支），细节包括一份新闻稿中引用的'对抗性多代理安全推理'同比增长 430%，以及根本原因是'七个 LLM 串联排列'。

rss · Simon Willison · 6月26日 17:58

**背景**: AI 审查代理是使用大型语言模型（LLM）自动评估代码变更安全性的系统。在软件供应链中，此类代理越来越多地被用于审查包更新中的恶意代码。然而，它们容易受到提示注入攻击，并且在输出冲突时可能产生成本高昂且无用的循环。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nesbitt.io/2026/06/26/incident-report-cve-2026-lgtm.html">Incident Report: CVE-2026-LGTM | Andrew Nesbitt</a></li>
<li><a href="https://simonwillison.net/2026/Jun/26/incident-report/">Incident Report: CVE-2026-LGTM</a></li>
<li><a href="https://github.com/lz4/lz4">GitHub - lz4/lz4: Extremely Fast Compression algorithm</a></li>

</ul>
</details>

**标签**: `#security`, `#ai`, `#supply-chain`, `#satire`, `#incident-response`

---

<a id="item-7"></a>
## [OpenAI 预览 GPT-5.6 系列三个模型](https://simonwillison.net/2026/Jun/26/openai/#atom-everything) ⭐️ 8.0/10

OpenAI 宣布对 GPT-5.6 系列进行有限预览，该系列包括三个模型：Sol（旗舰）、Terra（均衡）和 Luna（快速且经济实惠）。由于与政府的合作，预览最初仅限于一小部分可信合作伙伴。 此次发布引入了分层定价和能力结构，使高级 AI 更易获取，同时为高要求任务保留了高端选项。政府的参与凸显了前沿 AI 模型日益受到监管关注。 每百万 token 定价：Sol 输入 $5 / 输出 $30，Terra $2.50 / $15，Luna $1 / $6。GPT-5.6 还引入了可预测的提示缓存，支持显式缓存断点和 30 分钟最小缓存寿命，缓存写入按未缓存输入率的 1.25 倍计费。

rss · Simon Willison · 6月26日 17:10

**背景**: OpenAI 的 GPT 系列从 GPT-3 发展到 GPT-4 和 GPT-5，每一代都提升了推理、编码和多模态能力。GPT-5.6 系列延续了这一趋势，为不同用例和预算提供专用模型。因政府合作而进行的有限预览反映了 AI 公司与监管机构之间日益增强的合作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>
<li><a href="https://help.openai.com/en/articles/20001325-a-preview-of-gpt-56-sol-terra-and-luna">A preview of GPT-5.6 Sol, Terra, and Luna | OpenAI Help Center</a></li>
<li><a href="https://community.openai.com/t/introducing-gpt-5-6-series-sol-terra-and-luna/1384931">Introducing GPT-5.6 series: Sol, Terra and Luna - Announcements - OpenAI Developer Community</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5.6`, `#AI models`, `#pricing`, `#machine learning`

---

<a id="item-8"></a>
## [本地编码代理替代 Claude Code](https://magazine.sebastianraschka.com/p/using-local-coding-agents) ⭐️ 8.0/10

Sebastian Raschka 探讨了在本地编码框架中使用开放权重模型，作为 Claude Code 和 Codex 等订阅制工具的经济替代方案。 这为开发者提供了一种降低成本并保持对编码工作流控制的方式，可能推动行业从专有订阅服务转向开放的本地解决方案。 文章强调，当与设计良好的框架配合时，本地模型可以在编码任务上实现高性能，像 Goose 这样的工具作为模型无关的开源替代方案正在获得采用。

rss · Sebastian Raschka · 6月27日 11:21

**背景**: 编码代理是辅助软件开发任务的 AI 系统。开放权重模型的参数公开可用，允许本地部署。编码框架为代理提供操作环境和工具，包括代码执行和工具访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ai-boost/awesome-harness-engineering">GitHub - ai-boost/awesome-harness-engineering: Awesome list for AI agent harness engineering: tools, patterns, evals, memory, MCP, permissions, observability, and orchestration. · GitHub</a></li>
<li><a href="https://prowe214.medium.com/agentic-coding-harnesses-a-comparison-4db34b87fd5c">Agentic Coding Harnesses: A Comparison | by Paul Cullen Rowe | Apr, 2026 | Medium</a></li>
<li><a href="https://www.langchain.com/blog/the-anatomy-of-an-agent-harness">The Anatomy of an Agent Harness</a></li>

</ul>
</details>

**标签**: `#AI`, `#coding agents`, `#open-weight models`, `#local development`, `#machine learning`

---

<a id="item-9"></a>
## [AI 周刊：模型、机器人、医学前沿进展](https://aiweekly.co/issues/the-cutting-edge-across-the-board) ⭐️ 8.0/10

最新一期 AI 周刊报道了一系列突破：从 1.6 万亿参数到可在树莓派上运行的 2.3 亿参数的开源权重模型、Yann LeCun 团队通过 LeWorldModel 将世界模型速度提升 48 倍、GPT-5 Pro 解决了一个持续三年的免疫学谜题，以及智能体在手机上的部署。 这些进展涵盖了 AI 的整个前沿领域：从使最先进 AI 民主化的大规模开源权重模型，到实现更高效机器人学习的更快世界模型，再到解决真实医学问题并覆盖每部手机的 AI，可能加速各行业的采用。 LeWorldModel (LeWM) 仅有约 1500 万参数，可在单 GPU 上数小时内训练完成，规划速度比基于基础模型的世界模型快 48 倍。开源权重模型范围包括 1.6 万亿参数模型和可在树莓派上运行的 2.3 亿参数模型。GPT-5 Pro 的医学突破和 Claude 辅助的癌症扫描解读凸显了 AI 的临床潜力。

rss · AI Weekly · 6月28日 00:00

**背景**: 开源权重模型是指其训练参数公开发布的 AI 模型，允许开发者本地运行，但可能并非完全开源。世界模型是内部预测模型，使 AI 智能体能够模拟环境的未来状态，这对规划和强化学习至关重要。LeWorldModel 是一种紧凑的联合嵌入预测架构（JEPA），可直接从原始像素学习。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2603.19312">[2603.19312] LeWorldModel: Stable End-to-End Joint-Embedding ... Images LeWorldModel: Stable End-to-End Joint-Embedding Predictive ... LeCun's World Model LeWM: Physical Intelligence Trained on a ... LeCun's Bet Pays Off: Lean World Model Plans 48x Faster LeWorldModel: Stable End-to-End Joint-Embedding Predictive ... LeCun's LeWorldModel Trains 48x Faster With Just 15M Parameters LeWorldModel Breakthrough: Yann LeCun’s Team Simplifies World ...</a></li>
<li><a href="https://le-wm.github.io/">LeWorldModel: Stable End-to-End Joint-Embedding Predictive ...</a></li>
<li><a href="https://huggingface.co/blog/daya-shankar/open-source-llm-models-to-run-locally">The Best Open Source and Open-Weight LLM Models to Run ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#machine learning`, `#robotics`, `#medicine`, `#open-source`

---

<a id="item-10"></a>
## [深入 Reddit 反垃圾邮件系统内部](https://lyra.horse/blog/2026/06/reddit-spam-internals/) ⭐️ 8.0/10

一篇详细的技术博文揭示了 Reddit 如何大规模检测和缓解垃圾信息，包括使用影子封禁和自动化软件解决方案。 这一罕见的内幕视角帮助开发者和安全专业人士了解真实世界的反垃圾技术，并凸显了平台与垃圾信息发送者之间持续的军备竞赛。 文章涵盖了影子封禁等机制——即在不通知的情况下静默限制垃圾账号，以及分析行为模式的自动化检测系统。

rss · Lobsters · 6月27日 15:10

**背景**: Reddit 是一个大型社交新闻平台，垃圾信息是一个长期问题。反垃圾系统必须在准确性和用户体验之间取得平衡，并经常采用影子封禁等技术以避免打草惊蛇。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.webnuz.com/article/2026-06-27/Undisclosed+0-Days,+OpenZL+for+Zero-Trust,+and+Reddit's+Anti-Spam+Architecture">Undisclosed 0-Days, OpenZL for Zero-Trust, and Reddit's Anti ...</a></li>
<li><a href="https://taarifa.org/the-tech-behind-reddits-anti-spam-measures-shadowbans-and-automated-software-solutions/">The Tech Behind Reddit’s Anti-Spam Measures: Shadowbans and ...</a></li>
<li><a href="https://www.soar.sh/blog/reddit-shadowban-what-it-means-for-brands">Reddit shadowbans for brands: detection, causes, recovery in ...</a></li>

</ul>
</details>

**社区讨论**: Lobsters 上的讨论称赞了该帖子的深度和透明度，一些评论者就影子封禁的伦理影响及其被滥用的可能性展开了辩论。

**标签**: `#anti-spam`, `#systems`, `#reddit`, `#security`, `#infrastructure`

---

<a id="item-11"></a>
## [Prism：带类型效应的非纯函数式语言](https://www.stephendiehl.com/posts/prism/) ⭐️ 8.0/10

Stephen Diehl 介绍了 Prism，一种新的非纯函数式编程语言，它集成了类型化效应以原则性地管理副作用。 Prism 提供了一种新颖的方法，将非纯函数式语言的灵活性与类型化效应的安全性相结合，可能影响未来的语言设计并改善实际应用中的副作用管理。 该语言由编程语言社区中备受尊敬的 Stephen Diehl 设计，文章包含指向 Lobsters 讨论的链接以获取社区反馈。

rss · Lobsters · 6月27日 19:39

**背景**: 函数式编程语言可以是纯的（无副作用）或非纯的（允许副作用）。类型化效应系统在类型系统中追踪副作用，使代码更安全、更可预测。Prism 通过允许副作用但通过类型化效应追踪它们，结合了这些思想。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Effect_system">Effect system - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Functional_programming">Functional programming - Wikipedia</a></li>

</ul>
</details>

**标签**: `#functional programming`, `#type systems`, `#programming languages`, `#effects`

---

<a id="item-12"></a>
## [UEFI CA 过期威胁安全启动](https://blog.einval.com/2026/06/27#its_dead_jim) ⭐️ 8.0/10

2011 年发布的 Microsoft UEFI 证书颁发机构 (CA) 证书将于 2026 年 6 月开始过期，可能导致许多设备的安全启动失效。系统管理员和开发者必须更新固件证书以维持信任。 此次过期可能禁用受影响系统的安全启动保护，增加 bootkit 攻击和操作系统启动前被攻陷的风险。IT 团队需要紧急更新 UEFI 固件和操作系统配置。 过期的证书包括用于签名启动加载程序和驱动程序的 'Microsoft Corporation UEFI CA 2011'。Microsoft 已发布替换证书（2023 版本），必须将其部署到安全启动的 DB 和 KEK 数据库中。

rss · Lobsters · 6月27日 22:42

**背景**: 安全启动使用信任链，UEFI 固件根据 DB（允许）和 DBX（撤销）数据库中存储的证书验证启动组件。KEK（密钥交换密钥）控制这些数据库的更新。当 CA 证书过期时，使用该证书签名的启动组件可能不再被信任，导致启动失败或安全警告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.microsoft.com/en-us/topic/windows-secure-boot-certificate-expiration-and-ca-updates-7ff40d33-95dc-4c3c-8725-a9b95457578e">Windows Secure Boot certificate expiration and CA updates</a></li>
<li><a href="https://woshub.com/updating-uefi-secure-boot-certificates-windows-faq/">Updating UEFI Secure Boot Certificates on Windows Devices ...</a></li>
<li><a href="https://www.redhat.com/en/blog/expiration-secure-boot-signing-certificates-2026">Expiration of Secure Boot signing certificates in 2026</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论强调了此次过期的关键性，评论者指出许多系统可能无法获得固件更新。一些人担心旧硬件将处于易受攻击的状态，而另一些人则讨论缓解策略，例如使用 MOK（机器所有者密钥）或暂时禁用安全启动。

**标签**: `#UEFI`, `#secure boot`, `#certificate expiry`, `#security`, `#infrastructure`

---

<a id="item-13"></a>
## [分片锁：六种 Go 缓存设计基准测试](https://strebkov.dev/posts/shard-your-locks/) ⭐️ 8.0/10

一位开发者使用仅依赖 Go 标准库的六种内存字符串缓存实现进行了基准测试，结果表明分片锁在各种工作负载下显著优于其他并发策略。 该基准测试提供了具体证据，证明分片锁是 Go 高并发缓存的优越模式，有助于开发者为性能关键型应用做出明智的设计选择。 基准测试涵盖了从 1 到 8 核的读密集型、均衡型和写密集型工作负载，仅使用标准库组件以隔离锁策略的影响。

rss · Lobsters · 6月27日 12:40

**背景**: 在并发编程中，锁用于保护共享数据，但在高竞争下可能成为瓶颈。分片锁将数据划分为多个分区（分片），每个分片拥有自己的锁，从而减少锁竞争并提高可扩展性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://strebkov.dev/posts/shard-your-locks/">Shard your locks: benchmarking 6 Go cache designs</a></li>
<li><a href="https://medium.com/@gurucoding528/advanced-go-caching-strategies-lock-striping-sharded-maps-bigcache-ristretto-deep-dive-d112af9cc582">Advanced Go Caching Strategies: Lock Striping, Sharded Maps ...</a></li>
<li><a href="https://medium.com/@praveen93467/go-faster-a-practical-guide-to-local-cache-sharding-c6f5d4b9fe00">Go Faster: A Practical Guide to Local Cache Sharding</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论验证了这些发现，评论者指出分片映射是一种众所周知的模式，但基准测试提供了有用的定量比较。一些人讨论了分片数量与内存开销之间的权衡。

**标签**: `#Go`, `#caching`, `#concurrency`, `#performance`, `#benchmarking`

---

<a id="item-14"></a>
## [AI 自动化射频芯片设计的“黑暗艺术”](https://spectrum.ieee.org/ai-radio-chip-design) ⭐️ 8.0/10

普林斯顿大学的研究人员应用强化学习和逆向设计，从头开始快速创建射频集成电路，实现了传统上手动且复杂过程的自动化。 这一突破可能通过减少射频芯片设计所需的时间和专业知识，极大地加速 5G、自动驾驶汽车和卫星通信等无线技术的发展。 射频集成电路设计通常是一个迭代过程，受寄生效应和封装影响很大，需要多次仿真并与晶圆厂反复沟通；AI 旨在简化这一工作流程。

rss · Lobsters · 6月27日 18:03

**背景**: 射频芯片设计以难度大著称，因为电路在高频下工作，寄生效应和封装具有一阶影响，使其成为一个定制化、迭代的过程，常被称为“黑暗艺术”。传统设计严重依赖专家工程师使用 EDA 工具和多次仿真循环。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.allaboutcircuits.com/technical-articles/what-is-rf-integrated-circuit-design/">What Is RF Integrated Circuit Design? - Technical Articles Images Understanding RF IC Design – The Core of Wireless Technology Understanding RF Circuit Design Basics A Comprehensive ... RF Basics Design Guide - Microchip Technology AI Learns the "Dark Art" of RF Chip Design - IEEE Spectrum</a></li>

</ul>
</details>

**标签**: `#AI`, `#chip design`, `#RF engineering`, `#hardware automation`

---

<a id="item-15"></a>
## [QuantFunc：ComfyUI 运行时 4 位量化，速度提升 4 倍](https://www.reddit.com/r/StableDiffusion/comments/1uhqasg/i_built_a_comfyui_node_for_runtime_4bit/) ⭐️ 8.0/10

一款名为 QuantFunc 的新 ComfyUI 插件通过自定义 CUDA 内核实现运行时 4 位量化，将 RTX 4090 上 Ideogram 4 的推理时间从约 30 秒缩短至约 8 秒（1024×1024 图像，12 步）。 该插件无需预量化模型即可实现显著的推理加速，使高质量图像生成在消费级 GPU 上更易用，并可能惠及整个 Stable Diffusion 生态系统。 量化在运行时执行，因此适用于任何现有模型检查点。作者报告称，与 fp16 基线相比，4 位精度下的质量损失极小，且该插件已在 GitHub 上开源。

reddit · r/StableDiffusion · /u/lesesis · 6月28日 07:00

**背景**: 量化降低模型权重的数值精度（例如从 16 位降至 4 位），以减少内存占用并加速推理。运行时量化在推理过程中动态应用，无需单独的量化模型文件。ComfyUI 是一个流行的基于节点的 Stable Diffusion 工作流界面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/WASasquatch/comfyui-plugins">GitHub - WASasquatch/comfyui-plugins: Extensions, Custom Nodes, and other plugins for ComfyUI · GitHub</a></li>
<li><a href="https://huggingface.co/blog/4bit-transformers-bitsandbytes">Making LLMs even more accessible with bitsandbytes, 4-bit quantization and QLoRA</a></li>
<li><a href="https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/tutorials/Conceptual_Guide/Part_4-inference_acceleration/README.html">Accelerating Inference for Deep Learning Models — NVIDIA ...</a></li>

</ul>
</details>

**标签**: `#ComfyUI`, `#quantization`, `#CUDA`, `#inference acceleration`, `#Stable Diffusion`

---

<a id="item-16"></a>
## [Clark Air 将 Sana 1.6B 压缩为三值权重](https://www.reddit.com/r/StableDiffusion/comments/1uhoo93/clarklabsclarkairsana16b158bit_hugging_face/) ⭐️ 8.0/10

Clark Labs 发布了 clark-air-sana-1.6b-1.58bit，这是 Sana 1.6B 文本到图像模型的三值量化版本，实现了 8.6 倍的大小缩减（打包后 374 MB 对比 FP16 的 3.21 GB），且质量接近 FP16。 这表明大型文本到图像 Transformer 可以被激进地压缩为三值权重而不会显著损失质量，从而能够在笔记本电脑和边缘硬件等资源受限的设备上高效部署。 该模型采用分组三值量化，每个权重约 1.85 比特，并保留少量高精度尾部（约 5% 的参数）用于条件层和投影层。打包版本为 374 MB，同时提供了解量化后的未打包版本以保持兼容性。

reddit · r/StableDiffusion · /u/LumenLime · 6月28日 05:30

**背景**: 三值量化将权重映射到三个值：{-α, 0, +α}，将每个权重的存储减少到约 2 比特。分组缩放通过对小权重组应用单独的缩放因子进一步提高精度。Sana 是 NVIDIA 开发的高效文本到图像框架，能够生成高达 4096×4096 分辨率的高质量图像。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/ternary-quantization">Ternary Quantization in Neural Networks</a></li>
<li><a href="https://nvlabs.github.io/Sana/">SANA - nvlabs.github.io</a></li>
<li><a href="https://github.com/NVlabs/Sana">GitHub - NVlabs/Sana: SANA: Efficient High-Resolution Image ...</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论总体积极，评论者验证了技术方法，并注意到 8.6 倍的压缩效果且质量损失极小。一些用户讨论了在设备端生成的应用潜力，并将其与其他量化方法进行了比较。

**标签**: `#model compression`, `#ternary quantization`, `#text-to-image`, `#efficient AI`, `#Sana`

---

<a id="item-17"></a>
## [Decomp Academy：在线学习 GameCube 逆向编译](https://decomp-academy.dev/) ⭐️ 7.0/10

Decomp Academy 是一个免费、开源、基于浏览器的平台，提供 250 多节互动课程，教授如何将 GameCube 游戏的 PowerPC 汇编逆向编译为匹配的 C 代码，并使用实时 Metrowerks CodeWarrior 编译器验证逐位精确匹配。 该平台降低了游戏逆向编译这一小众但充满热情的领域的入门门槛，无需安装老旧工具链，并提供从基础到实际项目贡献的结构化动手学习体验。 该网站运行实时 Metrowerks CodeWarrior GC/2.0 编译器，要求用户编写的 C 代码生成与目标完全相同的汇编，精确到每条指令和每个比特位。课程包含来自《星际火狐大冒险》、《马力欧派对 4》、《皮克敏》和《银河战士 Prime》等项目的真实函数。

hackernews · jackpriceburns · 6月28日 01:21 · [社区讨论](https://news.ycombinator.com/item?id=48703412)

**背景**: 匹配逆向编译是视频游戏逆向工程的金标准，开发者编写 C/C++代码，使其编译后与原始游戏生成完全相同的二进制文件。PowerPC 是 GameCube 使用的指令集架构，而 Metrowerks CodeWarrior 是 GameCube 开发的官方编译器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PowerPC">PowerPC - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Metrowerks_CodeWarrior">Metrowerks CodeWarrior</a></li>
<li><a href="https://github.com/encounter/decomp-toolkit">GitHub - encounter/decomp-toolkit: A GameCube & Wii decompilation toolkit · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了基于浏览器的做法消除了工具链的摩擦，但有人指出，由于指令顺序问题，为 decomp.me 等实际逆向项目做贡献仍然具有挑战性。还有一位用户发现了一种在早期课程中“作弊”的方法，凸显了加强验证的必要性。

**标签**: `#decompilation`, `#reverse engineering`, `#gamecube`, `#assembly`, `#education`

---

<a id="item-18"></a>
## [ClickHouse 发布 WAL-RUS：用 Rust 重写 WAL-G](https://clickhouse.com/blog/walrus-postgres-backups-in-rust) ⭐️ 7.0/10

ClickHouse 宣布了 WAL-RUS，这是对流行的 PostgreSQL 备份工具 WAL-G 的 Rust 重写版本，声称在 CPU 和内存效率上比原 Go 版本有显著提升。 这次重写展示了 Rust 在基础设施工具中的潜在性能优势，特别是在内存受限的环境中，并可能影响类似数据库工具对 Rust 的采用。 原版 Go 语言 WAL-G 相比 WAL-RUS 大约多使用 1.5 倍的 CPU 和显著更多的内存，但 Go 版本更易于编写和维护。两者之间的基准测试结果可在 ClickHouse 博客上获取。

hackernews · saisrirampur · 6月27日 23:32 · [社区讨论](https://news.ycombinator.com/item?id=48702848)

**背景**: WAL-G 是一个广泛使用的 PostgreSQL 数据库归档和恢复工具，利用预写日志（WAL）实现时间点恢复。WAL-RUS 是其 Rust 重实现，旨在提高资源效率的同时保持兼容性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/wal-g/wal-g">GitHub - wal-g/wal-g: Archival and Restoration for databases in the Cloud · GitHub</a></li>
<li><a href="https://www.postgresql.org/docs/current/wal-intro.html">PostgreSQL: Documentation: 18: 28.3. Write-Ahead Logging (WAL)</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，Go 版本的 CPU 使用率仅高出 1.5 倍，内存使用量虽可预见地更高但并不过分，并质疑基准测试中 2.8GB 峰值是虚拟内存还是常驻内存。还有评论者指出与 Supabase 的 walrus 项目存在命名冲突。

**标签**: `#Rust`, `#PostgreSQL`, `#Backups`, `#Performance`, `#WAL`

---

<a id="item-19"></a>
## [TownSquare：网站上的短暂存在层](https://cauenapier.com/blog/townsquare_release/) ⭐️ 7.0/10

TownSquare 是一个轻量级的短暂存在层，让网站访客无需账户或永久记录就能看到彼此并聊天，旨在重现真实人物在线的感觉。 该项目通过提供简单、保护隐私的方式促进社区和实时连接，解决了网络上偶然社交互动的缺失，可能影响网站设计社交功能的方式。 TownSquare 没有账户、个人资料、关注者数量或永久聊天记录；消息仅在人们在线时存在。它故意设计得小巧且健忘，专注于短暂互动。

hackernews · eustoria · 6月27日 17:11 · [社区讨论](https://news.ycombinator.com/item?id=48699928)

**背景**: 短暂存在层是临时系统，显示谁当前在线而不存储数据。传统社交网络依赖持久的个人资料和历史记录，这可能为随意互动制造障碍。TownSquare 旨在带回在网站上看到他人的小感觉，类似于早期的网络小部件如 My Blog Log。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://townsquare.cauenapier.com/">TownSquare, a tiny presence layer for websites</a></li>
<li><a href="https://news.ycombinator.com/item?id=48608570">Show HN: TownSquare, a tiny presence layer for websites | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ephemerality">Ephemerality - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区评论褒贬不一：一些人赞赏促进线下聚会和偶然联系的想法，而另一些人则担心滥用和垃圾信息，指出已有机器人发布仇恨言论。还有关于短暂与持久社交功能价值的讨论。

**标签**: `#web development`, `#social software`, `#community`, `#ephemeral messaging`, `#presence`

---

<a id="item-20"></a>
## [让 CPU 愤怒的数据访问模式](https://blog.weineng.me/posts/slowest_add/) ⭐️ 7.0/10

一篇技术文章探讨了某些数据访问模式如何降低 CPU 性能，可能聚焦于缓存抖动和内存访问低效。 理解这些模式对于系统程序员优化性能、避免浪费 CPU 周期的常见陷阱至关重要。 文章可能涵盖缓存抖动（频繁缓存未命中导致严重减速）以及顺序访问与随机访问等内存访问模式。

rss · Lobsters · 6月27日 14:18

**背景**: CPU 缓存存储频繁访问的数据以加速处理。当数据访问模式导致持续缓存未命中时，CPU 会停滞等待主存数据，这种现象称为缓存抖动。顺序、跨步或随机访问等内存访问模式显著影响缓存效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Memory_access_pattern">Memory access pattern - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Thrashing_(computer_science)">Thrashing (computer science) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#CPU`, `#performance`, `#data access patterns`, `#systems programming`

---

<a id="item-21"></a>
## [OxCaml 中值得借鉴的特性](https://theconsensus.dev/p/2026/06/27/the-feature-in-oxcaml-more-languages-should-steal.html) ⭐️ 7.0/10

The Consensus 上的一篇文章讨论了 OxCaml（Jane Street 对 OCaml 的一个分支）中的某个特定特性，作者认为其他编程语言应该借鉴这一特性。 该特性可能通过提升性能控制和安全来影响语言设计，从而惠及从事性能关键系统开发的开发者。 OxCaml 是 OCaml 的一组快速迭代的扩展，专注于性能工程，文章重点介绍了其中一项可被其他语言借鉴的独特特性。

rss · Lobsters · 6月27日 21:07

**背景**: OxCaml 是 Jane Street（一家自营交易公司）对 OCaml 的一个分支，旨在为程序性能关键方面提供安全、方便且可预测的控制。OCaml 本身是一种具有强大类型系统和函数式编程特性的通用编程语言。该文章可能讨论了与性能优化或内存管理相关的特性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://oxcaml.org/">OxCaml | About</a></li>
<li><a href="https://blog.janestreet.com/introducing-oxcaml/">Jane Street Blog - Introducing OxCaml</a></li>
<li><a href="https://en.wikipedia.org/wiki/OCaml">OCaml - Wikipedia</a></li>

</ul>
</details>

**标签**: `#programming languages`, `#OxCaml`, `#language design`, `#feature`

---

<a id="item-22"></a>
## [VictoriaLogs 列式存储解析](https://victoriametrics.com/blog/victorialogs-internals-columnar-storage-on-disk/) ⭐️ 7.0/10

VictoriaMetrics 发布了一篇博客，详细介绍了 VictoriaLogs 如何在磁盘上使用列式布局存储日志，包括流、每日分区、不可变部分、块和列，从而支持只读取必要字节的高效查询。 这种设计使 VictoriaLogs 相比 Elasticsearch 或 Grafana Loki 最多可节省 30 倍内存和 15 倍磁盘空间，使日志管理在可观测性管道中更具成本效益和可扩展性。 存储格式包括时间戳、值、布隆过滤器、列头以及两级索引的独立文件，这些文件都位于不可变的部分中，并随时间合并。

rss · Lobsters · 6月28日 12:23

**背景**: 传统的日志管理系统通常使用倒排索引或行式存储，这在扫描大量日志数据时效率较低。列式存储按列而非行组织数据，允许查询跳过不相关的列，减少 I/O。VictoriaLogs 是 VictoriaMetrics 推出的无模式、零配置日志数据库，旨在实现高性能和低资源消耗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://victoriametrics.com/blog/victorialogs-internals-columnar-storage-on-disk/">How VictoriaLogs Stores Your Logs in a Columnar Layout</a></li>
<li><a href="https://docs.victoriametrics.com/victorialogs/">VictoriaLogs</a></li>
<li><a href="https://github.com/VictoriaMetrics/VictoriaLogs">GitHub - VictoriaMetrics/VictoriaLogs: Fast and easy to use ...</a></li>

</ul>
</details>

**标签**: `#columnar storage`, `#log management`, `#VictoriaMetrics`, `#observability`, `#systems design`

---

<a id="item-23"></a>
## [MAX 模型现支持 Apple Silicon GPU](https://forum.modular.com/t/max-models-can-now-run-on-apple-silicon-gpus/3283) ⭐️ 7.0/10

高性能 AI 推理框架 MAX 现已支持在 Apple Silicon GPU 上运行模型，从而在 Mac 硬件上实现更快的机器学习推理。 此次更新显著提升了 Mac 上的机器学习性能，使 MAX 成为偏好 Apple 硬件且无需依赖 CUDA 或其他 GPU 后端的开发者的更可行选择。 MAX 不依赖 PyTorch、CUDA 或 ROCm，简化了部署。该框架使用 Mojo 编程语言实现可移植的 GPU 内核性能。

rss · Lobsters · 6月28日 09:21

**背景**: MAX 是一个高性能推理框架，旨在跨各种硬件高效运行 AI 模型。Apple Silicon GPU（见于搭载 M 系列芯片的 Mac）提供强大的计算能力，但需要特定的软件支持才能充分利用于机器学习任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.modular.com/max">MAX: A high-performance inference framework for AI</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的社区讨论表达了对 Mac 上机器学习性能提升的热情，一些用户指出 MAX 有潜力减少对 NVIDIA GPU 的依赖。其他人则对看到与 Core ML 等现有解决方案的基准测试和比较感兴趣。

**标签**: `#machine learning`, `#Apple Silicon`, `#GPU`, `#MAX`, `#performance`

---

<a id="item-24"></a>
## [Linux 7.2 提升匿名管道性能](https://www.phoronix.com/news/Linux-72-Faster-Anon-Pipe-Write) ⭐️ 7.0/10

Linux 7.2 内核合并了一项针对 anon_pipe_write 函数的性能优化，加快了向匿名管道（用于 shell 管道和标准流）写入数据的速度。 这一改进直接惠及 shell 管道（例如 `ls | grep`）和进程间通信，使所有 Linux 用户的常见命令行操作更快、更高效。 该补丁专门优化了 anon_pipe_write 内核函数，该函数在数据写入匿名管道时被调用。这一改动是渐进式的，但对于管道密集型工作负载效果显著。

rss · Lobsters · 6月27日 14:29

**背景**: 匿名管道是 Linux 中一种进程间通信（IPC）形式，通过 pipe() 系统调用创建。它们常用于 shell 管道（例如 `command1 | command2`），将一个进程的输出连接到另一个进程的输入。与命名管道（FIFO）不同，匿名管道仅在通信进程存活期间存在。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.phoronix.com/news/Linux-72-Faster-Anon-Pipe-Write">Linux 7.2 Improves Anonymous/Unnamed Pipe Performance For ...</a></li>
<li><a href="https://www.baeldung.com/linux/anonymous-named-pipes">Anonymous and Named Pipes in Linux | Baeldung on Linux</a></li>

</ul>
</details>

**标签**: `#Linux`, `#kernel`, `#performance`, `#pipes`

---

<a id="item-25"></a>
## [Krea2 风格迁移首次发布，基于 RoPE 方法](https://www.reddit.com/r/StableDiffusion/comments/1uhpiov/krea2_style_transfer_first_release/) ⭐️ 7.0/10

Krea2 风格迁移首次发布，采用经过调优的 RoPE 方法，将单张参考图像的风格应用到 ComfyUI 中的文本到图像输出。 这为基于 DiT 的模型提供了一种新颖的、无需训练的风格迁移方法，可精细控制风格强度并减少伪影，对 AI 图像生成工作流具有重要意义。 该方法通过 Untwisting RoPE 节点包在 ComfyUI 中实现为自定义节点，关键参数包括起始块、高尺度起始、低尺度结束和 adain 强度；起始块越低风格越强，但可能引入伪影。

reddit · r/StableDiffusion · /u/Winter_unmuted · 6月28日 06:16

**背景**: RoPE（旋转位置嵌入）最初是 Transformer 中用于位置编码的技术。Untwisting RoPE 方法将其适配到扩散 Transformer（DiT）的共享注意力机制中进行频率控制，通过操纵图像的频率分量实现无需训练的风格迁移。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/BigStationW/ComfyUi-Untwisting-RoPE">GitHub - BigStationW/ComfyUi-Untwisting-RoPE: Training-free style transfer for DiT models. · GitHub</a></li>
<li><a href="https://www.runcomfy.com/comfyui-nodes/ComfyUi-Untwisting-RoPE">ComfyUi-Untwisting-RoPE detailed guide</a></li>

</ul>
</details>

**社区讨论**: 社区讨论内容充实，用户分享了结果并进行了故障排除。作者提供了详细的安装说明和工作流技巧，并提到即将推出多图像风格迁移和构图参考功能。

**标签**: `#style transfer`, `#Stable Diffusion`, `#ComfyUI`, `#RoPE`, `#image generation`

---

<a id="item-26"></a>
## [ComfyUI 原生支持 INT8 量化](https://www.reddit.com/r/StableDiffusion/comments/1uhcg69/comfyui_now_natively_supports_int8_tested_and/) ⭐️ 7.0/10

ComfyUI 现已原生支持扩散模型和文本编码器的 INT8 量化，用户可直接在标准节点中加载量化模型。社区已分享经过测试的 Krea 2、LTX-2.3、Ideogram 4 等模型的 INT8 量化版本。 这一原生支持显著降低了显存占用并加速了 Stable Diffusion 工作流的推理速度，使高质量图像生成在消费级 GPU 上更易实现。它消除了对自定义节点或外部工具的需求，简化了优化流程。 INT8 支持适用于标准的“扩散模型加载器”和“加载 CLIP”节点，兼容 RTX 30xx、40xx 和 50xx 系列 GPU。如果显存不足，用户还可以使用 CPU 模式将模型转换为 INT8。

reddit · r/StableDiffusion · /u/Winougan · 6月27日 20:03

**背景**: INT8 量化将模型权重精度从 16 位或 32 位浮点数降低为 8 位整数，从而减少内存占用并加速 GPU 上的矩阵运算。ComfyUI 是一个流行的基于节点的 Stable Diffusion 工作流界面。此前，INT8 支持需要自定义节点或外部量化工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/BobJohnson24/ComfyUI-INT8-Fast">GitHub - BobJohnson24/ComfyUI-INT8-Fast: Custom node to load models in INT8 for 1.5~2X Speed gains on 30 series cards. · GitHub</a></li>
<li><a href="https://github.com/SparknightLLC/ComfyUI-INT8-Toolkit">GitHub - SparknightLLC/ComfyUI-INT8-Toolkit: INT8 solution for ComfyUI. Compatible with stock loaders and a wide range of models. · GitHub</a></li>
<li><a href="https://developer.nvidia.com/blog/tensorrt-accelerates-stable-diffusion-nearly-2x-faster-with-8-bit-post-training-quantization/">NVIDIA TensorRT Accelerates Stable Diffusion Nearly 2x Faster ...</a></li>

</ul>
</details>

**社区讨论**: 社区对原生支持反响热烈，用户确认在 RTX 3090 上可获得 1.5–2 倍加速。部分用户报告 convrot（卷积旋转）量化最初存在问题，但后续更新后已正常工作。作者计划发布 YouTube 教程，介绍如何将模型转换为 INT8。

**标签**: `#ComfyUI`, `#INT8 quantization`, `#Stable Diffusion`, `#model optimization`

---