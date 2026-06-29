---
layout: default
title: "Horizon Summary: 2026-06-29 (ZH)"
date: 2026-06-29
lang: zh
---

> 从 66 条内容中筛选出 30 条重要资讯。

---

1. [Longinus：单个漏洞穿透 Chrome 渲染器和 V8 沙箱](#item-1) ⭐️ 9.0/10
2. [混淆：密码学的终极挑战](#item-2) ⭐️ 9.0/10
3. [火箭实验室以 80 亿美元收购铱星公司](#item-3) ⭐️ 8.0/10
4. [HackerRank 开源 ATS 显示 LLM 评分不一致](#item-4) ⭐️ 8.0/10
5. [声誉管理公司滥用 DMCA，谷歌同谋](#item-5) ⭐️ 8.0/10
6. [索尼删除已购 Studio Canal 电影且不退款](#item-6) ⭐️ 8.0/10
7. [年龄验证是言论归因的滑坡起点](#item-7) ⭐️ 8.0/10
8. [ChatGPT 推翻陈立杰苦研 7 年的计算几何难题](#item-8) ⭐️ 8.0/10
9. [Ornith-1.0：面向智能体编程的开源权重大模型系列](#item-9) ⭐️ 8.0/10
10. [Jon Udell：将“人在回路中”重构为“代理在回路中”](#item-10) ⭐️ 8.0/10
11. [AI 周报：模型、机器人、医学前沿进展](#item-11) ⭐️ 8.0/10
12. [Ante 融合借用检查与引用计数](#item-12) ⭐️ 8.0/10
13. [Typst 演讲：为增量性而设计](#item-13) ⭐️ 8.0/10
14. [新核心演算形式化文档操作](#item-14) ⭐️ 8.0/10
15. [WATaBoy：将 Game Boy 指令 JIT 编译为 Wasm，性能超越原生解释器](#item-15) ⭐️ 8.0/10
16. [Autocrypt v2 引入后量子加密与可靠删除功能](#item-16) ⭐️ 8.0/10
17. [ISC'26 公布新超算榜首](#item-17) ⭐️ 8.0/10
18. [桑迪亚国家实验室的辐射加固 8085 CPU 揭秘](#item-18) ⭐️ 7.0/10
19. [Tidal 发布 AI 音乐政策，强调内容诚信](#item-19) ⭐️ 7.0/10
20. [三星、SK 海力士、美光因 DRAM 价格操纵被起诉](#item-20) ⭐️ 7.0/10
21. [逆向工程苹果新稀疏映像格式](#item-21) ⭐️ 7.0/10
22. [惠普扩大与 OpenAI 的 Frontier 合作伙伴关系，推动企业 AI 应用](#item-22) ⭐️ 7.0/10
23. [当性能提升不再重要](#item-23) ⭐️ 7.0/10
24. [Datalog 中的求值顺序与非终止性](#item-24) ⭐️ 7.0/10
25. [欧盟聊天控制威胁加密，活动重启](#item-25) ⭐️ 7.0/10
26. [优化 LLVM 的 bump 分配器](#item-26) ⭐️ 7.0/10
27. [扫描线清扫器：一种新型字形渲染算法](#item-27) ⭐️ 7.0/10
28. [一种带类型的代数解析方法（2019）](#item-28) ⭐️ 7.0/10
29. [VictoriaLogs 列式存储原理解析](#item-29) ⭐️ 7.0/10
30. [量子计算威胁卫星加密安全](#item-30) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Longinus：单个漏洞穿透 Chrome 渲染器和 V8 沙箱](https://nebusec.ai/research/v8-cve-2026-6307-writeup/) ⭐️ 9.0/10

一篇关于 CVE-2026-6307（代号 Longinus）的详细分析揭示了一个单一漏洞，该漏洞同时绕过了 Chrome 的渲染器沙箱和 V8 堆沙箱，实现了对浏览器的完全控制。 这意义重大，因为它展示了一种新颖的攻击向量，用一个漏洞突破了两层安全边界，可能影响数百万 Chrome 用户，并凸显了当前沙箱设计中的关键弱点。 该漏洞存在于 V8 的 JIT 编译器中，允许攻击者在渲染器进程内实现任意代码执行，然后逃逸 V8 沙箱以获得完全的系统访问权限。该漏洞被分配为 CVE-2026-6307，并在最近的 Chrome 更新中已修复。

rss · Lobsters · 6月29日 15:00

**背景**: Chrome 使用多层沙箱来隔离不受信任的代码。渲染器沙箱限制了受损渲染器进程可以访问的系统资源，而 V8 堆沙箱则保护 V8 运行时的内部内存免受破坏。一个能同时突破这两层的漏洞非常罕见，属于高严重性安全问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nvd.nist.gov/vuln/detail/CVE-2026-6307">CVE-2026-6307 Detail - NVD</a></li>
<li><a href="https://chromium.googlesource.com/chromium/src/+/HEAD/docs/design/sandbox.md">Chromium Docs - Sandbox</a></li>

</ul>
</details>

**社区讨论**: Lobsters 上的讨论称赞了这篇分析的技术深度，并指出该漏洞利用的巧妙之处。一些评论者表达了对浏览器安全影响的担忧，以及防御此类跨边界攻击的难度。

**标签**: `#security`, `#browser`, `#v8`, `#chrome`, `#cve`

---

<a id="item-2"></a>
## [混淆：密码学的终极挑战](https://vitalik.eth.limo/general/2026/06/29/obfuscation1.html) ⭐️ 9.0/10

Vitalik Buterin 发表了一篇关于密码学混淆的深度文章，探讨其作为通用程序隐藏原语的潜力，可能彻底改变区块链和隐私技术。 如果实现，密码学混淆将能在保留功能的同时隐藏任意程序的逻辑，为智能合约、投票系统等提供前所未有的隐私和安全性。 文章讨论了理论基础，包括不可区分混淆（iO），以及效率和安全性证明等实际挑战。

rss · Lobsters · 6月29日 12:46

**背景**: 密码学混淆旨在使程序代码难以理解，同时保持其功能完整，类似于对软件进行加密。由于其广泛的应用，它长期以来被视为密码学中的“圣杯”，但构建安全且高效的混淆器仍然极其困难。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cryptographic_obfuscation">Cryptographic obfuscation</a></li>
<li><a href="https://www.esat.kuleuven.be/cosic/blog/program-obfuscation/">Co6GC: Program Obfuscation - COSIC</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论可能包括对 iO 可行性的技术分析、与零知识证明等现有隐私技术的比较，以及关于实际时间表的辩论。

**标签**: `#cryptography`, `#obfuscation`, `#blockchain`, `#privacy`, `#Vitalik Buterin`

---

<a id="item-3"></a>
## [火箭实验室以 80 亿美元收购铱星公司](https://investors.rocketlabcorp.com/news-releases/news-release-details/rocket-lab-acquire-iridium-historic-deal-creating-fully) ⭐️ 8.0/10

火箭实验室宣布以 80 亿美元收购卫星通信公司铱星，旨在成为一家完全垂直整合的端到端太空公司。 此次收购为火箭实验室提供了来自铱星卫星网络替换的稳定发射需求，类似于 SpaceX 利用 Starlink 确保基础发射量，并使火箭实验室成为太空行业的主要竞争者。 该交易价值 80 亿美元，包括铱星现有的卫星星座及其未来的替换订单，火箭实验室可以利用自己的卫星制造能力来建造这些卫星。

hackernews · everfrustrated · 6月29日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=48719485)

**背景**: 火箭实验室于 2006 年在新西兰成立，是一家发射服务和卫星制造公司，一直在扩展成为端到端的太空公司。铱星运营着一个全球卫星通信网络，在低地球轨道上有 75 颗升级后的 Iridium NEXT 卫星，提供全球语音和数据连接。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Iridium_satellite_constellation">Iridium satellite constellation - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Iridium_Communications">Iridium Communications - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rocket_Lab">Rocket Lab - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区评论强调了与 SpaceX 利用 Starlink 作为发射杠杆的战略相似性，火箭实验室确保了最低发射频率。一些人表达了对太空垃圾的担忧，以及铱星较旧的网络相对于 SpaceX 的 Starlink 的竞争可行性。

**标签**: `#space`, `#acquisition`, `#satellite`, `#Rocket Lab`, `#Iridium`

---

<a id="item-4"></a>
## [HackerRank 开源 ATS 显示 LLM 评分不一致](https://danunparsed.com/p/hackerrank-open-source-ats) ⭐️ 8.0/10

HackerRank 开源了其申请人跟踪系统（ATS），允许用户用 LLM 测试简历评分。作者发现同一份简历在重复提交时得分差异巨大（如 90、74、88、83），揭示了随机行为。 这暴露了基于 LLM 的简历筛选中的关键缺陷，包括不一致性和潜在偏见，可能导致不公平的招聘决策。它还引发了反歧视法（尤其是在欧盟）下的法律担忧。 该 ATS 使用 0.1 的低温度，但仍然产生高度可变的分数，表明即使是低温度的 LLM 也不是确定性的。评分系统还严重偏向个人项目和开源贡献，这可能使某些候选人处于不利地位。

hackernews · sambellll · 6月29日 01:44 · [社区讨论](https://news.ycombinator.com/item?id=48713832)

**背景**: 申请人跟踪系统（ATS）被雇主用来筛选简历。最近，一些 ATS 集成了大型语言模型（LLM）来自动评分简历。然而，LLM 本质上是随机的，这意味着即使输入相同，其输出也可能变化，这可能导致不公平且不一致的筛选结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://danunparsed.com/p/hackerrank-open-source-ats">HackerRank open sourced its ATS. My resume scored 90/100. Oh wait 74/100. No — 88/100. Actually 83/100.</a></li>
<li><a href="https://arxiv.org/html/2509.04404v1">No Thoughts Just AI: Biased LLM Recommendations Limit Human Agency in Resume Screening</a></li>
<li><a href="https://www.holisticai.com/blog/assessing-biases-in-llms">Assessing Biases in LLMs: From Basic Tasks to Hiring Decisions</a></li>

</ul>
</details>

**社区讨论**: 评论者对基于 LLM 的筛选的随机性表示担忧，有人指出此类系统可能违反欧盟反歧视法。另一位评论者指出，35%的通过率对于大批量招聘实际上很高效，但承认有效的候选人很可能被筛掉。

**标签**: `#LLM`, `#hiring`, `#bias`, `#ATS`, `#discrimination`

---

<a id="item-5"></a>
## [声誉管理公司滥用 DMCA，谷歌同谋](https://blog.pragmaticengineer.com/pollen-tried-to-remove-my-article-about-callum-negus-fancey-and-google-is-assisting-to-it/) ⭐️ 8.0/10

一家名为 Pollen 的声誉管理公司试图通过虚假的 DMCA 删除通知，欺诈性地删除一篇关于 Callum Negus-Fancey 的批评文章，而谷歌未经核实就处理了该请求。 这一事件暴露了声誉管理公司对 DMCA 删除程序的系统性滥用，而谷歌未能追究其责任，威胁到言论自由和在线信息的完整性。 该虚假通知是在伪证处罚下提交的，但谷歌在删除内容前未核实索赔人身份或版权主张的有效性。

hackernews · taubek · 6月29日 09:28 · [社区讨论](https://news.ycombinator.com/item?id=48716902)

**背景**: DMCA（数字千年版权法）规定了版权所有者请求删除侵权内容的通知-删除程序。然而，该程序常被声誉管理公司滥用，以压制负面信息，因为谷歌等平台很少核实索赔或惩罚虚假提交。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Notice_and_take_down">Notice and take down - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reputation_management">Reputation management - Wikipedia</a></li>
<li><a href="https://copyrightalliance.org/education/copyright-law-explained/the-digital-millennium-copyright-act-dmca/dmca-notice-takedown-process/">DMCA Notice & Takedown Process | Copyright Alliance</a></li>

</ul>
</details>

**社区讨论**: 评论者对这一滥用行为表示愤怒，许多人呼吁对删除通知强制要求政府身份验证，并对轻率索赔进行处罚。一些人指出，这一尝试反而通过斯特赖桑德效应增加了文章的可见度。

**标签**: `#DMCA`, `#content moderation`, `#Google`, `#reputation management`, `#free speech`

---

<a id="item-6"></a>
## [索尼删除已购 Studio Canal 电影且不退款](https://www.playstation.com/en-gb/legal/psvideocontent/) ⭐️ 8.0/10

索尼宣布将于 2026 年 9 月 1 日从 PlayStation 用户库中删除 551 部 Studio Canal 电影，理由是许可协议，且不会为这些购买提供退款。 这一事件凸显了数字所有权的脆弱性，消费者可能在没有补偿的情况下失去对已购内容的访问权限，引发了重大的消费者权益和数字保存问题。 受影响的电影包括《终结者 2》、《帕丁顿熊》和《月光男孩》等热门影片。索尼的服务条款规定购买的是许可而非所有权，可随时撤销。

hackernews · kugelblitz · 6月29日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=48718967)

**背景**: 在 PlayStation Store 等平台上的数字购买通常是许可而非所有权，即用户购买的是可被撤销的访问权。这与提供永久所有权的实体媒体形成对比。类似问题在其他平台也曾发生，加剧了关于数字权利和消费者保护的辩论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thecybersecguru.com/news/playstation-studiocanal-content-removal-2026/">PlayStation Removes 551 Purchased StudioCanal Movies with No...</a></li>
<li><a href="https://gamingpromax.com/playstation-store-studiocanal-movies-delisted-september-2026/">PlayStation Store Is Delisting 551 StudioCanal Movies in September...</a></li>
<li><a href="https://www.playstation.com/en-us/legal/terms-of-service/">PLAYSTATION TERMS OF SERVICE (US)</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了不满，认为索尼本应为已购内容谈判永久许可。一些人主张购买无 DRM 内容或自建媒体库作为替代方案，而另一些人则质疑从游戏平台购买数字电影的合理性。

**标签**: `#digital rights`, `#consumer protection`, `#DRM`, `#PlayStation`, `#licensing`

---

<a id="item-7"></a>
## [年龄验证是言论归因的滑坡起点](https://nonogra.ph/age-verification-is-just-a-precursor-to-attribution-of-speech-06-29-2026) ⭐️ 8.0/10

一篇评论文章指出，年龄验证强制要求是政府控制言论归属和许可制互联网访问的前奏，警告其系统性风险远超保护儿童范畴。 这很重要，因为年龄验证法律正在全球范围内讨论，文章揭示了监控、设备认证和匿名言论侵蚀等二阶效应，可能从根本上改变互联网自由。 文章指出，年龄验证常与设备认证结合，要求使用未修改的政府批准操作系统和与用户 ID 关联的应用，从而创建许可制互联网。它还警告网站面临责任风险及不可避免的数据泄露。

hackernews · arkhiver · 6月29日 03:42 · [社区讨论](https://news.ycombinator.com/item?id=48714529)

**背景**: 年龄验证法律旨在限制未成年人访问成人内容，但批评者认为这需要身份证件或生物识别信息，从而促成监控并压制言论。设备认证确保硬件和软件完整性，常用于 DRM 或企业安全，但当政府强制要求时，它可以控制哪些应用和操作系统被允许使用。

**社区讨论**: 评论者表示强烈赞同，许多人强调二阶效应如政府越权和许可制互联网。有人建议直接避开要求身份证件的网站，另一些人则指出数据泄露和责任风险的必然性。讨论还提及设备认证作为并行威胁。

**标签**: `#age verification`, `#surveillance`, `#internet freedom`, `#systems thinking`, `#privacy`

---

<a id="item-8"></a>
## [ChatGPT 推翻陈立杰苦研 7 年的计算几何难题](https://mp.weixin.qq.com/s?__biz=MzI3MTA0MTk1MA==&mid=2652709773&idx=2&sn=68bde762eb0070f5bd61518728971232) ⭐️ 8.0/10

OpenAI 宣布其模型解决了 Erdős 单位距离问题，这是离散几何中一个长期未解的猜想，陈立杰曾为此研究 7 年。 这标志着 AI 驱动数学发现的一个里程碑，表明大型语言模型能够解决此前被认为需要人类直觉的深奥理论问题。 该模型否定了离散几何中一个与 Erdős 单位距离问题相关的核心猜想，该猜想已悬而未决 80 年。

rss · 新智元 · 6月29日 05:01

**背景**: Erdős 单位距离问题询问平面上 n 个点之间单位距离的最大数量。陈立杰是清华姚班出身的著名理论计算机科学家，现任加州大学伯克利分校教授。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/model-disproves-discrete-geometry-conjecture/">An OpenAI model has disproved a central conjecture in... | OpenAI</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/openai-paul-erdos-geometry-problem-cracked">80-year-old geometry puzzle cracked by OpenAI using number theory</a></li>

</ul>
</details>

**标签**: `#AI`, `#computational geometry`, `#OpenAI`, `#Erdős conjecture`, `#machine learning`

---

<a id="item-9"></a>
## [Ornith-1.0：面向智能体编程的开源权重大模型系列](https://simonwillison.net/2026/Jun/29/ornith/#atom-everything) ⭐️ 8.0/10

DeepReinforce 发布了 Ornith-1.0，这是一个采用 MIT 许可证的开源权重大模型系列，提供 9B、31B、35B MoE 和 397B MoE 四种尺寸，基于 Gemma 4 和 Qwen 3.5 构建。在同等规模的开源模型中，它在编程基准测试中达到了最先进的性能。 此次发布为开源社区带来了具有竞争力的智能体编程能力，使开发者能够在本地或自有基础设施上运行强大的编程助手。宽松的 MIT 许可证和多种模型尺寸降低了实验和部署的门槛。 这些模型基于 Gemma 4（Apache 2.0）和 Qwen 3.5（Apache 2.0）构建，确保了许可证兼容性。提供了 GGUF 量化版本，可使用 LM Studio 和 Ollama 等工具轻松进行本地推理。

rss · Simon Willison · 6月29日 16:17

**背景**: 智能体编程是指 AI 系统自主执行多步骤软件开发任务（如代码生成、调试和测试），只需极少的人工干预。自脚手架是一种技术，大模型通过生成显式的逐步分解来解决复杂任务，从而提高可靠性和性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48709744">Ornith-1.0: Self - Scaffolding LLMs for Agentic Coding | Hacker News</a></li>
<li><a href="https://ornith.site/">Ornith 1 . 0 — Open-Source Agentic Coding Models</a></li>
<li><a href="https://huggingface.co/deepreinforce-ai/Ornith-1.0-9B-GGUF">deepreinforce -ai/ Ornith - 1 . 0 -9B-GGUF · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: Hacker News 和 Simon Willison 博客上的初步社区反应是积极的，用户称赞该模型在编程任务上的性能以及通过 GGUF 进行本地部署的便捷性。一些用户对 DeepReinforce 作为新玩家以及自脚手架技术表示好奇。

**标签**: `#LLM`, `#open-source`, `#coding`, `#agentic`, `#model release`

---

<a id="item-10"></a>
## [Jon Udell：将“人在回路中”重构为“代理在回路中”](https://simonwillison.net/2026/Jun/28/jon-udell/#atom-everything) ⭐️ 8.0/10

Jon Udell 提议将“人在回路中”重构为“代理在回路中”，认为代理应被邀请进入人类主导的流程，而非人类屈从于机器。 这种重构将叙事从人类监督 AI 转向 AI 辅助人类，在代理式软件开发中保留了人类的主体性和控制权。 Udell 强调代理辅助流程不应是黑箱；相反，它们应透明且可审查，人类保留对回路的权威。

rss · Simon Willison · 6月28日 21:57

**背景**: 代理式软件开发涉及自主 AI 代理在整个软件开发生命周期中与人类协作。传统的“人在回路中”概念将人类置于 AI 行动的监督者位置，Udell 认为这会将权威让渡给机器。他的“代理在回路中”翻转了这一概念，将人类定位为主要驱动者，邀请代理协助。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ness.com/blog/what-is-agentic-software-development/">Agentic Software Development : Beyond Metrics and Speed</a></li>
<li><a href="https://waxell.ai/blog/human-in-the-loop-vs-human-on-the-loop-ai-agents">Human - in - the - Loop vs Human-on- the - Loop for AI Agents</a></li>

</ul>
</details>

**标签**: `#agentic software development`, `#human-in-the-loop`, `#AI agents`, `#software engineering`, `#Jon Udell`

---

<a id="item-11"></a>
## [AI 周报：模型、机器人、医学前沿进展](https://aiweekly.co/issues/the-cutting-edge-across-the-board) ⭐️ 8.0/10

本周 AI 进展包括一个 1.6 万亿参数的开源权重模型、Yann LeCun 团队将世界模型速度提升 48 倍、GPT-5 Pro 破解一个持续三年的免疫学谜题，以及智能体在手机上的部署。 这些进展跨越多个 AI 前沿领域，从推动更广泛研究的大型开源权重模型，到提升机器人和现实模拟速度的世界模型，同时医学突破展示了 AI 对人类健康的实际影响。 1.6 万亿参数模型是迄今发布的最大开源权重模型之一，而世界模型 48 倍的速度提升可大幅缩短具身 AI 的训练时间。GPT-5 Pro 的医学诊断凸显了 LLM 在医疗领域日益重要的作用。

rss · AI Weekly · 6月28日 00:00

**背景**: 开源权重模型公开 AI 模型参数，使研究人员能够自由微调和部署。世界模型是学习环境内部表征的 AI 系统，对机器人和模拟至关重要。GPT-5 Pro 是一种具有高级推理能力的大型语言模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/11870455-openai-open-weight-models-gpt-oss">OpenAI open - weight models (gpt-oss) | OpenAI Help Center</a></li>
<li><a href="https://medium.com/@kimanited73/open-weight-models-f504be677b1c">Open Weight Models . What are they, and why should you... | Medium</a></li>
<li><a href="https://deepmind.google/models/">Models — Google DeepMind</a></li>

</ul>
</details>

**标签**: `#AI`, `#large language models`, `#world models`, `#robotics`, `#medicine`

---

<a id="item-12"></a>
## [Ante 融合借用检查与引用计数](https://verdagon.dev/blog/ante-blending-borrowing-rc) ⭐️ 8.0/10

低级函数式语言 Ante 引入了一种新方法，将借用检查与引用计数相结合进行内存管理，旨在融合 Rust 借用检查器的安全性与引用计数的灵活性。 这可能会影响未来的系统编程语言设计，在严格的编译时安全性与运行时垃圾回收之间提供中间地带，可能使安全内存管理更易用。 该方法使用“约束引用”，结合了引用计数和单一所有权，每个对象有一个唯一所有者和一个引用计数器，但与 Rust 意义上的借用检查无关。

rss · Lobsters · 6月29日 01:37

**背景**: 借用检查（如 Rust）在编译时通过跟踪引用并防止数据竞争来保证内存安全，而引用计数（RC）在运行时通过跟踪对象的引用数量来管理内存。Ante 旨在弥合 C++/Rust 等低级语言与 Java 或 Haskell 等高级垃圾回收语言之间的差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://verdagon.dev/grimoire/grimoire">Borrow checking , RC, GC, and the Eleven (!) Other Memory Safety...</a></li>
<li><a href="https://antelang.org/">Ante</a></li>
<li><a href="https://news.ycombinator.com/item?id=48718589">Ante: A New Way to Blend Borrow Checking and Reference Counting</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论可能包含对编译时与运行时内存安全性之间权衡的技术见解，一些评论者可能质疑该方法的新颖性或实用性。

**标签**: `#programming languages`, `#memory management`, `#borrow checking`, `#reference counting`, `#systems programming`

---

<a id="item-13"></a>
## [Typst 演讲：为增量性而设计](https://youtu.be/yWWVhbyOWWE) ⭐️ 8.0/10

一场题为“Typst：为增量性而设计”的演讲展示了 Typst 排版系统如何围绕增量编译构建，以实现快速重新编译和响应式编辑体验。 这很重要，因为 Typst 旨在通过提供更现代、更易用且编译速度显著更快的系统来取代 LaTeX 在学术出版中的地位，解决研究人员和学生长期以来的痛点。 该演讲可能涵盖 Typst 的增量编译引擎（仅重新编译文档中更改的部分）及其基于标记的语法，与 LaTeX 的命令密集型方法相比，该语法简化了文档创建。

rss · Lobsters · 6月29日 13:57

**背景**: Typst 是一种新的基于标记的排版系统，旨在与 LaTeX 一样强大，但更易于学习和使用。增量编译是一种仅重新编译程序中已修改部分的技术，可减少构建时间。LaTeX 是当前学术文档的标准，以其陡峭的学习曲线和大型项目的缓慢编译而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/typst/typst">GitHub - typst / typst : A markup-based typesetting system that is...</a></li>
<li><a href="https://typst.app/docs/">Overview - Typst Documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Incremental_compilation">Incremental compilation</a></li>

</ul>
</details>

**标签**: `#typesetting`, `#programming languages`, `#incremental compilation`, `#academic publishing`

---

<a id="item-14"></a>
## [新核心演算形式化文档操作](https://dl.acm.org/doi/pdf/10.1145/3632865) ⭐️ 8.0/10

Will Crichton 和 Shriram Krishnamurthi 在 2024 年 ACM 论文中提出了一种文档核心演算，为编程语言中的文档操作提供了形式化框架。 这项工作弥合了被动文档与主动程序之间的鸿沟，有望催生更简洁、更规范的文档语言，并改进文档在代码中的嵌入方式。 该演算定义了从纯文本到完全可编程文档的层次结构，可作为设计新文档语言或分析现有语言的分类法。

rss · Lobsters · 6月28日 20:12

**背景**: 现代文档语言（如 LaTeX、带扩展的 Markdown）越来越多地包含编程特性，而编程语言（如带模板字面量的 JavaScript）则嵌入文档符号。然而，缺乏统一这些概念的形式化理论。文档演算旨在为文档提供类似 lambda 演算之于函数的理论基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2310.04368">[2310.04368] A Core Calculus for Documents</a></li>
<li><a href="https://cel.cs.brown.edu/paper/document-calculus/">A Core Calculus for Documents</a></li>
<li><a href="https://blog.brownplt.org/2023/12/28/document-calculus.html">A Core Calculus for Documents</a></li>

</ul>
</details>

**标签**: `#programming languages`, `#type theory`, `#documents`, `#research`

---

<a id="item-15"></a>
## [WATaBoy：将 Game Boy 指令 JIT 编译为 Wasm，性能超越原生解释器](https://humphri.es/blog/WATaBoy/) ⭐️ 8.0/10

一篇博文介绍了 WATaBoy，这是一个即时（JIT）编译器，将 Game Boy 指令翻译为 WebAssembly，性能优于原生解释器。 这表明将代码 JIT 编译为 WebAssembly 可以超越原生解释器，有望提升模拟器性能，并展示 WebAssembly 在动态代码生成方面的能力。 WATaBoy 在运行时将 Game Boy CPU 指令编译为 WebAssembly 模块，利用浏览器中 WebAssembly 的 JIT 编译实现接近原生的速度。该项目开源，可在 GitHub 上获取。

rss · Lobsters · 6月29日 15:07

**背景**: 传统的 Game Boy 模拟器使用解释执行或动态重编译为原生代码。WebAssembly 是一种低级二进制格式，旨在 Web 浏览器中高效执行，通常带有 JIT 编译。WATaBoy 将 JIT 应用于动态生成 WebAssembly，这是一种新颖的模拟方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/topics/game-boy">game - boy · GitHub Topics · GitHub</a></li>
<li><a href="https://www.cs.cornell.edu/courses/cs6120/2019fa/blog/wasm/">Bringing You Up to Speed on How Compiling WebAssembly is Faster</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论强调了这种方法的巧妙之处，一些人指出 WebAssembly 的 JIT 可以胜过简单的解释器。其他人讨论了潜在的局限性，例如运行时生成 WebAssembly 模块的开销。

**标签**: `#WebAssembly`, `#JIT`, `#emulation`, `#performance`, `#Game Boy`

---

<a id="item-16"></a>
## [Autocrypt v2 引入后量子加密与可靠删除功能](https://autocrypt2.org/) ⭐️ 8.0/10

Autocrypt v2 增加了混合后量子密码学（ML-KEM-768 + X25519）和用于可靠删除的自动密钥过期机制，这是对 2019 年 v1 规范的升级。 此次更新使电子邮件加密能够抵御量子计算机攻击，并通过确保密钥被可靠删除来应对“先存储后解密”的威胁，这对长期保密性至关重要。 后量子部分使用 NIST 标准化的 ML-KEM-768 算法，与 X25519 结合实现混合安全。可靠删除通过自动密钥过期和销毁实现，防止未来对存档消息的解密。

rss · Lobsters · 6月29日 10:22

**背景**: Autocrypt 是一种自动端到端电子邮件加密标准，自 2019 年 v1 发布以来已在多个邮件客户端中广泛实现。后量子密码学旨在保护通信免受未来量子计算机的攻击，因为量子计算机可能破解当前的公钥算法。可靠删除确保即使加密邮件被存储，解密所需的密钥也会在设定时间后被永久移除。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://autocrypt2.org/">Autocrypt v2 - Post-Quantum and Reliable Deletion for Internet...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Post-quantum_cryptography">Post - quantum cryptography - Wikipedia</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#post-quantum`, `#security`, `#email`

---

<a id="item-17"></a>
## [ISC'26 公布新超算榜首](https://chipsandcheese.com/p/top500-at-isc26-we-have-a-new-number) ⭐️ 8.0/10

在 ISC High Performance 2026 大会上，一台新的超级计算机登顶 TOP500 榜单，标志着高性能计算领域的一个重要里程碑。 新的榜首超算代表了计算能力的飞跃，将影响科学研究、人工智能和国家竞争力，并为未来的 HPC 发展树立标杆。 TOP500 榜单使用高性能 LINPACK（HPL）基准测试对全球最快超算进行排名。目前提供的内容中尚未披露新榜首的具体身份和性能数据。

rss · Lobsters · 6月28日 22:59

**背景**: TOP500 榜单是全球公认的最强超算排名，每年在 ISC 和 SC 会议上更新两次。ISC High Performance 成立于 1986 年，是最古老的超算会议，也是欧洲最大的 HPC 盛会。新的榜首通常意味着重大技术进步，例如新架构或浮点运算性能的大幅提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High-performance_computing">High-performance computing - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/ISC_High_Performance">ISC High Performance - Wikipedia</a></li>
<li><a href="https://isc-hpc.com/">Home - Welcome to ISC High Performance 2026</a></li>

</ul>
</details>

**社区讨论**: 提供的内容包含指向 Lobsters 评论的链接，但未提供实际评论，因此无法总结社区观点。

**标签**: `#HPC`, `#TOP500`, `#supercomputing`, `#ISC`

---

<a id="item-18"></a>
## [桑迪亚国家实验室的辐射加固 8085 CPU 揭秘](https://www.cpushack.com/2026/06/03/sandia-national-labs-sa3000-8085-cpu/) ⭐️ 7.0/10

桑迪亚国家实验室在 1980 年代利用内部制造工艺开发了 SA3000，这是 Intel 8085 CPU 的辐射加固版本。该芯片曾用于伽利略号探测器等关键太空任务。 这展示了美国政府历史上具备内部设计和制造辐射加固集成电路的能力，而这一能力如今已十分罕见。它突显了为太空和国防关键任务进行本土生产的重要性。 SA3000 采用 n-on-n+外延衬底制造以防止闩锁效应，并使用了大量保护环和硬化氧化物。桑迪亚还使用相同工艺为伽利略探测器重新制造了 RCA 1802 处理器。

hackernews · rbanffy · 6月29日 10:20 · [社区讨论](https://news.ycombinator.com/item?id=48717287)

**背景**: 辐射加固是使电子设备抵抗电离辐射的过程，对太空和核应用至关重要。Intel 8085 是 1976 年推出的 8 位微处理器，广泛用于嵌入式系统。桑迪亚国家实验室是美国专注于国家安全的政府研究实验室。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cpushack.com/2026/06/03/sandia-national-labs-sa3000-8085-cpu/">Sandia National Labs SA3000 8085 CPU | The CPU Shack Museum</a></li>
<li><a href="https://en.wikipedia.org/wiki/Radiation_hardening">Radiation hardening - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Intel_8085">Intel 8085 - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了其历史意义和技术细节，有人指出需要更多政府内部能力。其他人讨论了现代辐射加固 CPU，如 MOOG BRE440 和 BAE RAD5500，它们采用 IBM POWER 架构。

**标签**: `#hardware`, `#retrocomputing`, `#radiation hardening`, `#government R&D`, `#CPU`

---

<a id="item-19"></a>
## [Tidal 发布 AI 音乐政策，强调内容诚信](https://tidal.com/ai-policy) ⭐️ 7.0/10

Tidal 宣布了一项新政策，接受 AI 生成的音乐，但要求更高的内容诚信标准，禁止利用艺术家姓名或形象以及欺骗行为。 该政策为流媒体平台如何在 AI 创新与艺术家保护之间取得平衡树立了先例，可能影响行业标准，并引发关于 AI 在音乐中角色的辩论。 该政策特别针对欺骗听众或降低服务质量的 AI 生成音乐，并对此类内容提出比传统音乐更高的诚信标准。

hackernews · hn8726 · 6月29日 13:09 · [社区讨论](https://news.ycombinator.com/item?id=48718840)

**背景**: AI 生成的音乐在流媒体平台上越来越常见，引发了关于版权侵权、艺术家冒充和听众欺骗的担忧。Tidal 的政策旨在解决这些问题，同时仍允许 AI 音乐在其平台上存在。

**社区讨论**: 社区评论反应不一：一些人称赞该政策是对 AI 版权的合理处理方式，而另一些人则希望有纯人类音乐平台或能够选择退出 AI 生成内容。还强调了 AI 音乐充斥信息流和冒充艺术家的担忧。

**标签**: `#AI`, `#music`, `#policy`, `#copyright`, `#streaming`

---

<a id="item-20"></a>
## [三星、SK 海力士、美光因 DRAM 价格操纵被起诉](https://en.sedaily.com/international/2026/06/29/samsung-sk-hynix-micron-sued-in-us-over-memory-price-fixing) ⭐️ 7.0/10

2026 年 6 月 25 日，美国加州北区联邦地区法院提起了一项集体诉讼反垄断案，指控三星、SK 海力士和美光合谋限制传统 DRAM 供应并操纵价格。 这起诉讼可能扰乱已经面临供应短缺和价格上涨的内存芯片市场，并可能导致巨额罚款或行业惯例的改变。 案件编号为 3:26-cv-06345，主要针对传统 DRAM（不包括 HBM）。此前 2022 年的类似尝试因缺乏协议证据而失败。

hackernews · donohoe · 6月29日 11:58 · [社区讨论](https://news.ycombinator.com/item?id=48718102)

**背景**: DRAM（动态随机存取存储器）是用于计算机和服务器的内存类型。三星、SK 海力士和美光这三家公司主导了全球 DRAM 市场，其中三星在 2026 年第一季度占据约 38%的收入份额。价格操纵指控此前也曾发生，包括 21 世纪初导致罚款的丑闻。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://allthings.how/samsung-sk-hynix-and-micron-face-dram-price-fixing-class-action-in-california/">Samsung, SK Hynix, and Micron Face DRAM Price - Fixing Class...</a></li>
<li><a href="https://en.yna.co.kr/view/AEN20260625005400320">Samsung Electronics maintains No. 1 spot in global DRAM market in...</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，2022 年曾有类似尝试但失败，一些人质疑本案的力度，特别是关于停产 DDR3 和 DDR4 等旧型 DRAM 的指控。其他人则强调了行业对高利润率的偏好，以及如果三星和 SK 海力士停止向美国销售可能带来的地缘政治影响。

**标签**: `#memory`, `#price fixing`, `#antitrust`, `#semiconductors`, `#legal`

---

<a id="item-21"></a>
## [逆向工程苹果新稀疏映像格式](https://schamper.dev/dissecting-apples-sparse-image-format-asif/) ⭐️ 7.0/10

一篇关于苹果稀疏映像格式（ASIF）的详细逆向工程分析已发布，解释了其内部结构以及与旧版稀疏映像格式的区别。该分析使用基于 Python 的工具直接从代码中解析 C 结构体定义。 该分析为数字取证、存储工程师以及使用 macOS 26 Tahoe 的开发者提供了宝贵见解，因为 ASIF 是一种新的单文件稀疏磁盘映像格式，可格式化为任意文件系统。理解其结构对于兼容性和数据恢复工具至关重要。 ASIF 是 macOS 26 Tahoe 中引入的单文件稀疏磁盘映像，不同于旧版的多文件稀疏包。逆向工程揭示 ASIF 使用自定义磁盘布局，通过二进制文件中嵌入的 C 结构体定义进行解析。

hackernews · supermatou · 6月28日 16:10 · [社区讨论](https://news.ycombinator.com/item?id=48708644)

**背景**: 稀疏磁盘映像是虚拟磁盘，仅占用实际写入数据的空间，而非完整标称容量。苹果历史上使用稀疏包（一个包含多个带文件的文件夹）来实现此功能。ASIF 将其整合为单个文件，简化了管理并可能提升性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.helpnetsecurity.com/2025/10/03/apple-disk-image-format/">Apple strengthens storage flexibility with new disk image formats</a></li>
<li><a href="https://www.linkedin.com/pulse/macos-26-tahoe-introduces-new-image-formats-what-examiners-whalen-hrncc">macOS 26 Tahoe Introduces New Image Formats : What Examiners...</a></li>
<li><a href="https://en.shiftdelete.net/macos-26-tahoe-introduces-a-new-disk-image-format-asif/">macOS 26 Tahoe introduces a new disk image format : ASIF ! - SDN</a></li>

</ul>
</details>

**社区讨论**: 评论者注意到 ASIF 与 Qcow2 的相似性，并质疑苹果为何不采用现有格式而创建新格式。有人指出分析工具使用了从 Python 字符串解析 C 结构体的不寻常方法，而其他人则提供了关于 ASIF 差异和替代工具的额外资源。

**标签**: `#reverse engineering`, `#file formats`, `#Apple`, `#storage`, `#forensics`

---

<a id="item-22"></a>
## [惠普扩大与 OpenAI 的 Frontier 合作伙伴关系，推动企业 AI 应用](https://openai.com/index/hp-frontier-partnership) ⭐️ 7.0/10

惠普公司宣布与 OpenAI 建立战略合作伙伴关系，将在 2026 年 2 月试点后，在其全球业务中部署 Frontier 平台，将 AI 整合到客户体验、软件开发和内部运营中。 这一合作标志着企业 AI 应用迈出重要一步，像惠普这样的财富 500 强公司将智能体 AI 作为连接层嵌入其系统，可能为其他大型组织树立先例。 OpenAI 于 2026 年 2 月 5 日推出的 Frontier 平台是一个企业级平台，用于构建、部署和管理具有共享上下文、入职、权限和治理功能的 AI 智能体。惠普将在客户支持、软件开发和内部运营中部署智能体 AI。

rss · OpenAI Blog · 6月28日 17:00

**背景**: OpenAI Frontier 是一个企业级平台，旨在帮助大型组织构建、部署和管理 AI 智能体群，使其作为具有共享上下文和治理功能的“AI 同事”。它提供了一个“上下文+控制”层，使 AI 能够在企业系统中安全运行。惠普的合作是该平台的首次大规模部署之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://beyondtmrw.org/article/hp-inc-launches-frontier-strategic-partnership-with-openai">HP Inc . launches Frontier strategic partnership with OpenAI</a></li>
<li><a href="https://openai-dotcom-git-main-openai.vercel.app/index/introducing-openai-frontier/">Introducing OpenAI Frontier | OpenAI</a></li>

</ul>
</details>

**标签**: `#AI`, `#Enterprise`, `#Partnership`, `#OpenAI`, `#HP`

---

<a id="item-23"></a>
## [当性能提升不再重要](https://blog.colinbreck.com/when-impressive-performance-gains-do-not-matter/) ⭐️ 7.0/10

一篇博文指出，令人印象深刻的性能提升并不总是值得追求，这取决于具体背景和权衡。 这挑战了性能提升总是至关重要的普遍假设，为软件工程师提供了宝贵的见解，尤其是那些在权衡取舍至关重要的系统上工作的工程师。 文章强调，开发成本、可维护性和用户感知延迟等因素可能超过原始性能提升。它鼓励工程师评估优化是否与整体项目目标一致。

rss · Lobsters · 6月29日 13:15

**背景**: 性能优化是软件工程中的一个常见关注点，但它通常伴随着权衡，例如增加复杂性或降低可读性。这篇文章提供了一个细致的视角，提醒工程师在投入优化之前考虑更广泛的背景。

**标签**: `#performance`, `#software engineering`, `#trade-offs`, `#optimization`

---

<a id="item-24"></a>
## [Datalog 中的求值顺序与非终止性](https://www.rntz.net/post/2026-06-11-datalog-nontermination.html) ⭐️ 7.0/10

该文章探讨了求值顺序如何影响 Datalog 查询语言中的非终止性，指出在特定递归查询中，自底向上的求值可能导致无限循环。 理解非终止性对于设计安全高效的 Datalog 引擎至关重要，尤其是在 Datalog 越来越多地用于静态分析和数据库系统的背景下。 文章指出，传统上用于建模非终止性的域理论已不再流行，使得该主题难以理解。文章呼吁重新关注求值顺序的语义。

rss · Lobsters · 6月29日 14:47

**背景**: Datalog 是一种声明式逻辑编程语言，通常采用自底向上的求值方式，与 Prolog 的自顶向下方法不同。自底向上求值在递归规则生成无限事实时可能导致非终止。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Datalog">Datalog - Wikipedia</a></li>
<li><a href="https://www.rntz.net/post/2026-06-11-datalog-nontermination.html">Evaluation order and nontermination in query languages</a></li>

</ul>
</details>

**标签**: `#Datalog`, `#query languages`, `#evaluation order`, `#nontermination`, `#programming languages`

---

<a id="item-25"></a>
## [欧盟聊天控制威胁加密，活动重启](https://www.patrick-breyer.de/en/double-threat-to-private-communications-undemocratic-chat-control-backroom-deals-and-imminent-concessions-spark-relaunch-of-fightchatcontrol-eu/) ⭐️ 7.0/10

Patrick Breyer 重新启动了 fightchatcontrol.eu 活动，反对欧盟要求扫描私人通信以查找非法内容的提案，该提案可能破坏端到端加密。 欧盟的聊天控制提案要求平台扫描消息中的儿童性虐待材料，这在技术上与端到端加密不兼容。由于多个成员国不支持，欧洲理事会推迟了投票。

rss · Lobsters · 6月28日 19:48

**背景**: 端到端加密（E2EE）确保只有发送者和预期接收者能读取消息，甚至服务提供商也无法访问内容。欧盟的聊天控制提案旨在打击儿童性虐待，但需要破坏 E2EE，引发了隐私担忧。类似的辩论在全球范围内进行，一些国家已通过削弱加密的法律。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tuta.com/blog/chat-control-criticism">Huge Victory: Chat Control no longer forces us to break... | Tuta</a></li>
<li><a href="https://www.privateinternetaccess.com/blog/chat-control-eus-plan-for-real-time-mass-surveillance-takes-a-dramatic-turn/">Chat Control , EU ’s Plan for Real-Time Mass Surveillance, Takes...</a></li>
<li><a href="https://en.wikipedia.org/wiki/End-to-end_encryption">End-to-end encryption</a></li>

</ul>
</details>

**社区讨论**: lobste.rs 上的讨论强烈反对这些提案，用户强调加密的重要性并批评欧盟的幕后交易。一些评论者对活动的有效性表示怀疑，而另一些人则呼吁更多技术解决方案来保护隐私。

**标签**: `#privacy`, `#encryption`, `#EU policy`, `#surveillance`

---

<a id="item-26"></a>
## [优化 LLVM 的 bump 分配器](https://maskray.me/blog/2026-06-28-optimizing-llvm-bump-allocator) ⭐️ 7.0/10

一篇关于 LLVM 的 BumpPtrAllocator 优化详细分析的文章已发布，涵盖了提升内存分配性能的技术。 这很重要，因为 LLVM 是许多编译器和工具的关键基础设施，改进其分配器可以加快编译速度并降低所有用户的内存开销。 优化包括减少分支、使用更大的 slab 以及更高效地对齐分配，基准测试显示吞吐量显著提升。

rss · Lobsters · 6月29日 04:25

**背景**: bump 分配器（arena 分配器）通过在预分配的 slab 内递增指针来分配内存，并在分配器销毁时一次性释放所有内存。LLVM 的 BumpPtrAllocator 广泛用于其编译器 pass 和工具中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://maskray.me/blog/2026-06-28-optimizing-llvm-bump-allocator">Optimizing LLVM's bump allocator | MaskRay</a></li>
<li><a href="https://os.phil-opp.com/allocator-designs/">Allocator Designs | Writing an OS in Rust</a></li>
<li><a href="https://coredumped.dev/2024/03/25/bump-allocation-up-or-down/">Bump Allocation: Up or Down? • Core Dumped</a></li>

</ul>
</details>

**社区讨论**: Lobsters 上的讨论（文章中有链接）可能包含编译器工程师对提议优化的权衡见解，但此处未提供具体评论。

**标签**: `#LLVM`, `#compiler`, `#memory allocation`, `#optimization`, `#systems programming`

---

<a id="item-27"></a>
## [扫描线清扫器：一种新型字形渲染算法](https://youtu.be/B9bztU1sTFA) ⭐️ 7.0/10

一种名为“扫描线清扫器”的新型字形渲染算法被提出，为传统的扫描线渲染或 Bresenham 算法提供了替代方案。 该算法可能提升计算机图形学和排版中的文本渲染性能与质量，从而影响字体在屏幕和印刷品上的显示方式。 该算法以视频形式呈现，可能限制了技术解释的深度，但它引入了一种不同于传统扫描线方法的字形渲染新思路。

rss · Lobsters · 6月29日 13:13

**背景**: 字形渲染是将字体轮廓转换为显示像素的过程。传统方法包括逐行处理图像的扫描线渲染，以及用于高效画线的 Bresenham 算法。扫描线清扫器提出了一种可能在速度或质量上具有优势的新技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Scanline_rendering">Scanline rendering - Wikipedia</a></li>

</ul>
</details>

**标签**: `#computer graphics`, `#typography`, `#rendering`, `#algorithm`

---

<a id="item-28"></a>
## [一种带类型的代数解析方法（2019）](https://www.cl.cam.ac.uk/~nk480/parsing.pdf) ⭐️ 7.0/10

Neelakantan R. Krishnaswami 和 Jeremy Yallop 在 PLDI 2019 上发表了一篇论文，提出了一种带类型的代数解析框架，该框架为 μ-正则表达式赋予了语义类型概念，并推导出解析器组合子，保证线性时间解析、无回溯和单符号前瞻。 这项工作通过提供类型安全、可组合的方法，解决了传统解析器组合子的基本限制——回溯和指数级时间复杂度，确保了效率和正确性，对编程语言实现和形式化方法具有重要意义。 该论文在 PLDI 2019 上获得了杰出论文奖和杰出工具体验奖。该框架将词法分析和语法分析融合为一个阶段，解析器组合子通过类型检查确保线性时间执行且无回溯。

rss · Lobsters · 6月28日 15:45

**背景**: 解析是根据形式文法的规则分析符号串的过程。传统的解析器组合子虽然优雅，但常常面临回溯和指数级最坏时间复杂度的问题。该论文基于 μ-正则表达式理论以及 Brüggemann-Klein 和 Wood 对无歧义正则表达式的刻画，提供了带类型的代数基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cl.cam.ac.uk/~nk480/parsing.pdf">A Typed , Algebraic</a></li>
<li><a href="https://github.com/joelburget/typed-algebraic-parsing">GitHub - joelburget/ typed - algebraic - parsing : An implementation of...</a></li>
<li><a href="https://www.repository.cam.ac.uk/items/cbe9137d-d047-420e-99e0-33f4812d5e5b">A Typed, Algebraic Approach to Parsing</a></li>

</ul>
</details>

**标签**: `#parsing`, `#algebraic approach`, `#type theory`, `#programming languages`, `#formal methods`

---

<a id="item-29"></a>
## [VictoriaLogs 列式存储原理解析](https://victoriametrics.com/blog/victorialogs-internals-columnar-storage-on-disk/) ⭐️ 7.0/10

VictoriaMetrics 发布了一篇详细博客，解释 VictoriaLogs 如何在磁盘上实现列式存储，将每个日志字段存储在单独的列中以优化查询性能。 这种方法通过仅读取查询所需的列来减少 I/O，使日志分析更高效且成本更低，尤其是在大规模场景下。 VictoriaLogs 是一个无模式、零配置的日志数据库，支持垂直和水平扩展，其列式布局旨在处理高写入速率的同时保持存储紧凑。

rss · Lobsters · 6月28日 12:23

**背景**: 传统的日志管理系统通常使用行式存储或索引引擎，这对于扫描大量数据集的分析查询可能效率低下。列式存储（如 ClickHouse 等 OLAP 数据库所采用的）按列而非按行存储数据，可实现更快的扫描和更好的压缩。VictoriaLogs 将这一概念应用于日志数据，旨在提供一种轻量且高效的替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://victoriametrics.com/blog/victorialogs-internals-columnar-storage-on-disk/">How VictoriaLogs Stores Your Logs in a Columnar Layout</a></li>
<li><a href="https://victoriametrics.com/blog/victorialogs-architecture-basics/">VictoriaLogs Basics: What You Need to Know, with Examples & Visuals</a></li>
<li><a href="https://github.com/VictoriaMetrics/VictoriaLogs">GitHub - VictoriaMetrics/ VictoriaLogs : Fast and easy to use database...</a></li>

</ul>
</details>

**标签**: `#log management`, `#columnar storage`, `#VictoriaLogs`, `#database internals`

---

<a id="item-30"></a>
## [量子计算威胁卫星加密安全](https://spacenews.com/quantum-computing-is-about-to-become-a-national-security-problem-in-orbit/) ⭐️ 7.0/10

量子计算技术快速进步，直接威胁到依赖当前加密算法的卫星通信安全。航天行业必须紧急准备后量子密码学，以保护轨道上的国家安全资产。 卫星对通信、导航和监视至关重要，其加密可能被未来的量子计算机破解，危及国家安全。这凸显了航天行业在“Q-Day”到来之前采用抗量子密码学的必要性。 文章提到了 ESA 的量子密钥分发卫星，它利用量子力学安全分发加密密钥。但主要担忧在于，运行 Shor 算法的足够强大的量子计算机可能破解广泛使用的公钥密码学，如 RSA 和 ECC。

rss · SpaceNews · 6月29日 13:00

**背景**: 后量子密码学（PQC）是指设计用于抵御量子计算机攻击的加密算法。当前的公钥算法依赖于整数分解或离散对数等数学问题，而 Shor 算法可以高效解决这些问题。NIST 已于 2024 年发布了首批三个 PQC 标准，以指导迁移。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Post-quantum_cryptography">Post-quantum cryptography</a></li>
<li><a href="https://en.wikipedia.org/wiki/Quantum_Experiments_at_Space_Scale">Quantum Experiments at Space Scale - Wikipedia</a></li>
<li><a href="https://csrc.nist.gov/projects/post-quantum-cryptography">Post - Quantum Cryptography | CSRC</a></li>

</ul>
</details>

**标签**: `#quantum computing`, `#national security`, `#space`, `#cryptography`, `#satellite`

---