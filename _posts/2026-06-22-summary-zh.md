---
layout: default
title: "Horizon Summary: 2026-06-22 (ZH)"
date: 2026-06-22
lang: zh
---

> 从 57 条内容中筛选出 25 条重要资讯。

---

1. [Claude Code 的扩展思考是丢失信息的摘要，并非真实推理](#item-1) ⭐️ 8.0/10
2. [Deno Desktop 支持用 Deno 构建桌面应用](#item-2) ⭐️ 8.0/10
3. [Mitchell Hashimoto 承诺向 Zig 软件基金会捐赠 40 万美元](#item-3) ⭐️ 8.0/10
4. [Codex 日志漏洞可能导致本地 SSD 写入数 TB 数据](#item-4) ⭐️ 8.0/10
5. [GLM-5.2 标志着开放智能体的重大飞跃](#item-5) ⭐️ 8.0/10
6. [OpenAI 推出 Daybreak 自动化安全工具](#item-6) ⭐️ 8.0/10
7. [三星向员工部署 ChatGPT Enterprise 和 Codex](#item-7) ⭐️ 8.0/10
8. [中美 AI 出口战升级：中国将 56 家美国公司列入黑名单](#item-8) ⭐️ 8.0/10
9. [2.4 亿域名自动补全实现 P99 零毫秒延迟](#item-9) ⭐️ 8.0/10
10. [Nix 需要可重定位二进制文件](#item-10) ⭐️ 8.0/10
11. [早期研究表明，使用 AI 可能削弱人类技能](#item-11) ⭐️ 8.0/10
12. [Linux 安全启动证书即将到期](#item-12) ⭐️ 8.0/10
13. [1991 年慕尼黑：当前 AI 热潮的根源](#item-13) ⭐️ 8.0/10
14. [我过去的工作只是因欺诈而存在吗？](#item-14) ⭐️ 7.0/10
15. [Apertus：面向主权 AI 的开放基础模型](#item-15) ⭐️ 7.0/10
16. [为何绘图板品牌回避 Linux 开源驱动](#item-16) ⭐️ 7.0/10
17. [sqlite-utils 4.0rc1 引入迁移和嵌套事务](#item-17) ⭐️ 7.0/10
18. [Cloudflare 推出临时 Workers 部署功能](#item-18) ⭐️ 7.0/10
19. [切斯特顿的中指：对盲目遵循的批判](#item-19) ⭐️ 7.0/10
20. [在 PostgreSQL 中管理时区变更](#item-20) ⭐️ 7.0/10
21. [postmarketOS v26.06 Alpen Avocado 发布](#item-21) ⭐️ 7.0/10
22. [不到 100 行代码实现 Nix 构建](#item-22) ⭐️ 7.0/10
23. [内存安全的内联汇编提案](#item-23) ⭐️ 7.0/10
24. [PivCo-Huffman 合并操作](#item-24) ⭐️ 7.0/10
25. [美国可能将非洲航天产业拱手让给中国](#item-25) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Claude Code 的扩展思考是丢失信息的摘要，并非真实推理](https://patrickmccanna.net/the-text-in-claude-codes-extended-thinking-output-is-not-authentic/) ⭐️ 8.0/10

一项批判性分析指出，Claude Code 的“扩展思考”功能输出的只是模型实际推理过程的丢失信息的摘要，而非真实的思维链。这引发了关于透明度、安全性以及有效优化提示能力的担忧。 这一点很重要，因为 AI 模型中的隐藏推理（尤其是以丢失信息的方式摘要）可能掩盖提示注入攻击，并使开发者更难调试或优化提示。它还削弱了对 AI 透明度的信任，因为用户无法验证模型的真实决策过程。 该分析将输出比作将 JPEG 转换为 BMP 再转换回来，过程中会发生数据丢失。此外，隐藏推理阶段可能包含函数调用，攻击者有可能在摘要中不被察觉地窃取数据。

hackernews · 0o_MrPatrick_o0 · 6月22日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=48630535)

**背景**: 扩展思考是 Claude Code 中的一项功能，允许模型在响应前花费更多时间进行推理，但推理过程并未完全向用户展示。提示注入是一种安全漏洞，恶意输入可操纵 LLM 的行为，而隐藏推理会使此类攻击更难被检测到。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gist.github.com/intellectronica/58571dda3581eec3e17a77741e8c858a">Claude Extended Thinking: The Ultimate Guide · GitHub</a></li>
<li><a href="https://platform.claude.com/docs/en/build-with-claude/extended-thinking">Building with extended thinking - Claude API Docs</a></li>
<li><a href="https://genai.owasp.org/llmrisk/llm01-prompt-injection/">LLM01:2025 Prompt Injection - OWASP Gen AI Security Project</a></li>

</ul>
</details>

**社区讨论**: 社区评论对隐藏推理表达了强烈担忧，用户指出所有主要的美国 AI 模型（Anthropic、OpenAI、Google）都隐藏推理，这使得提示优化更加困难并增加了安全风险。一些评论者将其与人类的事后合理化相类比，而另一些人则批评 Anthropic 在隐藏自身推理的同时却大量收集用户数据。

**标签**: `#AI transparency`, `#LLM reasoning`, `#prompt injection`, `#Anthropic`, `#security`

---

<a id="item-2"></a>
## [Deno Desktop 支持用 Deno 构建桌面应用](https://docs.deno.com/runtime/desktop/) ⭐️ 8.0/10

Deno 推出了 Deno Desktop 新功能，允许开发者使用 Deno 构建桌面应用，并支持多种渲染后端，包括 CEF、Webview 和 Raw。 这扩展了 Deno 的能力，从服务器端和 CLI 应用进入桌面开发领域，提供了 Electron 的现代替代方案，并通过共享 CEF 运行时有望减小二进制文件大小。 Deno Desktop 支持多种后端：CEF（Chromium Embedded Framework）、Webview（系统 Webview）和 Raw（无 UI）。共享 CEF 运行时已在路线图中，可将每个应用的二进制文件大小从数百 MB 减少到几 MB。

hackernews · Lobsters · 6月22日 05:38 · [社区讨论](https://news.ycombinator.com/item?id=48626137)

**背景**: Deno 是一个基于 V8 和 Rust 的现代 JavaScript、TypeScript 和 WebAssembly 运行时，由 Ryan Dahl（也是 Node.js 的创建者）创建。CEF 是一个用于在应用中嵌入 Chromium 浏览器的开源框架，通常被 Electron 使用，但每个应用通常需要单独捆绑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Deno_(software)">Deno (software) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Chromium_Embedded_Framework">Chromium Embedded Framework - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对 Deno Desktop 感到兴奋，称赞其与 Deno 权限系统的集成以及共享 CEF 运行时减小二进制文件大小的潜力。有人建议增加“在浏览器中启动”选项以简化使用场景。

**标签**: `#Deno`, `#Desktop`, `#CEF`, `#Webview`, `#Runtime`

---

<a id="item-3"></a>
## [Mitchell Hashimoto 承诺向 Zig 软件基金会捐赠 40 万美元](https://mitchellh.com/writing/zig-donation-2026) ⭐️ 8.0/10

HashiCorp 和 Ghostty 的创始人 Mitchell Hashimoto 承诺在 2024 年捐赠 40 万美元的基础上，再向 Zig 软件基金会 (ZSF) 捐赠 40 万美元（2026 年），两年内总承诺支持金额达到 80 万美元。 这笔巨额个人捐款彰显了业界对 Zig 作为系统编程语言的信心日益增强，并凸显了可持续资助对开源基金会的重要性。它还引发了社区关于大额捐赠者在塑造项目方向和政策（例如 Zig 对 LLM 生成贡献的立场）中所扮演角色的讨论。 这笔捐款专门针对 2026 年，Hashimoto 指出 ZSF 目前的资金可持续到 2026 年。他还重申支持 Zig 不接受 LLM 生成贡献的政策，这一政策在社区中一直存在争议。

hackernews · tosh · 6月22日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=48630020)

**背景**: Zig 是一种通用系统编程语言，旨在作为 C 语言的现代替代品，专注于健壮性、优化和可读性。Zig 软件基金会 (ZSF) 是一家非营利组织，支持该语言的发展，由 Zig 创始人 Andrew Kelley 于 2020 年创立。Mitchell Hashimoto 是开发者工具领域的知名人物，以联合创立 HashiCorp 和创建 Ghostty 终端模拟器而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language) - Wikipedia</a></li>
<li><a href="https://ziglang.org/zsf/">Zig Software Foundation Zig Programming Language</a></li>
<li><a href="https://ziglang.org/">Home Zig Programming Language</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了对 Hashimoto 慷慨解囊以及言行一致的钦佩。一些用户强调了他的其他项目（如 Ghostty）的更广泛影响，而另一些用户则就 Zig 的 LLM 贡献政策进行了细致讨论，一位评论者认为谨慎的设计考量证明了该政策的合理性。

**标签**: `#Zig`, `#open-source`, `#funding`, `#programming-languages`

---

<a id="item-4"></a>
## [Codex 日志漏洞可能导致本地 SSD 写入数 TB 数据](https://github.com/openai/codex/issues/28224) ⭐️ 8.0/10

OpenAI 的 Codex CLI 存在一个漏洞，错误配置的日志接收器以 TRACE 级别将调试日志写入本地 SQLite 数据库，每年可能写入高达 640 TB 的数据，迅速消耗 SSD 寿命。 该漏洞可能导致使用 Codex（一款广泛使用的 AI 编码工具）的开发者的 SSD 过早损坏、数据丢失和性能下降。该问题已开放近六个月，尚未有官方修复，削弱了用户对 OpenAI 产品质量的信任。 该漏洞在 GitHub issue #28224 中跟踪，影响位于 ~/.codex/logs_2.sqlite 的 SQLite 数据库。社区提供的临时解决方案包括使用 SQLite 触发器阻止日志插入，或运行 VACUUM FULL 将数据库从 27 GB 缩小到 73 MB。

hackernews · vantareed · 6月22日 07:30 · [社区讨论](https://news.ycombinator.com/item?id=48626930)

**背景**: Codex 是 OpenAI 的 AI 编码助手，通过 CLI 在本地运行。它使用 SQLite 记录反馈和调试信息。SSD 寿命以总写入字节数（TBW）衡量；典型消费级 SSD 的 TBW 为 150–600 TB，因此每年 640 TB 的写入量可在一年内损坏硬盘。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openai/codex/issues/28224">Codex SQLite feedback logs can write ~640 TB/year and rapidly consume SSD endurance · Issue #28224 · openai/codex</a></li>
<li><a href="https://www.reddit.com/r/OpenAI/comments/1ucf4px/openai_codex_has_a_bug_that_could_kill_your_ssd/">r/OpenAI on Reddit: OpenAI Codex has a bug that could kill your SSD in under a year</a></li>
<li><a href="https://www.notebookcheck.net/OpenAI-Codex-has-a-bug-that-could-kill-your-SSD-in-under-a-year.1326191.0.html">OpenAI Codex has a bug that could kill your SSD in under a year - Notebookcheck News</a></li>

</ul>
</details>

**社区讨论**: 社区情绪高度批评，用户称 Codex 为“垃圾软件”，并批评 OpenAI 缺乏回应。一些用户提供了临时解决方案，而另一些用户则对 OpenAI 没有使用自己的 AI 工具自动修复该问题表示失望。

**标签**: `#OpenAI`, `#Codex`, `#bug`, `#logging`, `#AI tools`

---

<a id="item-5"></a>
## [GLM-5.2 标志着开放智能体的重大飞跃](https://www.interconnects.ai/p/glm-52-is-the-step-change-for-open) ⭐️ 8.0/10

智谱 AI 发布了最新的旗舰模型 GLM-5.2，在开放智能体能力上实现了显著跃升，尤其在长周期任务和编码方面，并支持 100 万 token 的上下文窗口。 此次发布跨越了开放智能体能力的一个关键门槛，以极低的成本提供了接近 Claude Opus 的性能，这可能使开发者和研究人员能够更广泛地使用先进的 AI 智能体。 GLM-5.2 的定价为每百万 token 输入/输出 1.4/4.4 美元，远低于 Anthropic 的 Opus（5/25 美元）甚至 Haiku（1/5 美元），同时在一次性 3D 平台游戏编码任务上据称与 Opus 相当。

rss · Interconnects · 6月22日 14:52

**背景**: 开放智能体指能够通过与环境及工具交互来自主执行复杂任务的 AI 系统。GLM 是智谱 AI 开发的一系列大语言模型。该模型已在 Hugging Face 和 openlm.ai 上发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/GLM-5.2 · Hugging Face</a></li>
<li><a href="https://openlm.ai/glm-5.2/">GLM-5.2 - openlm.ai</a></li>

</ul>
</details>

**社区讨论**: 社区评论对一次性提示作为基准表示怀疑，用户强调可靠性、可操控性和协作用例的重要性，而非单次提示演示。一些用户注意到 GLM-5.2 相比 Anthropic 模型的成本优势。

**标签**: `#AI`, `#open source`, `#agents`, `#GLM`, `#research`

---

<a id="item-6"></a>
## [OpenAI 推出 Daybreak 自动化安全工具](https://openai.com/index/daybreak-securing-the-world) ⭐️ 8.0/10

OpenAI 宣布了 Daybreak 计划，推出了 Codex Security 和 GPT-5.5-Cyber，用于大规模自动化漏洞发现、验证和修复，同时推出了面向开源维护者的 Patch the Planet 项目。 这标志着 AI 驱动网络安全的重要一步，通过使高级漏洞管理变得可访问和可扩展，可能改变组织防御威胁的方式。 Codex Security 逐个提交扫描 GitHub 仓库并构建项目特定的威胁模型，而 GPT-5.5-Cyber 是一个经过网络调优的模型，仅限经过审查的防御者用于渗透测试和恶意软件分析。

rss · OpenAI Blog · 6月22日 10:00

**背景**: OpenAI 的 Daybreak 计划旨在将 AI 安全能力直接嵌入软件开发工作流。Codex Security 是一个应用安全代理，于 2026 年 3 月 6 日发布研究预览版，而 GPT-5.5-Cyber（代号 'Spud'）是一个专门用于网络防御任务的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Codex_(AI_agent)">Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://www.axios.com/2026/05/07/openai-gpt-55-cybersecurity-model">OpenAI makes GPT - 5 . 5 more widely available to cyber defenders</a></li>
<li><a href="https://openai.com/index/patch-the-planet/">Patch the Planet: a Daybreak initiative to support open... | OpenAI</a></li>

</ul>
</details>

**标签**: `#AI Security`, `#Vulnerability Management`, `#OpenAI`, `#Cybersecurity`, `#Codex`

---

<a id="item-7"></a>
## [三星向员工部署 ChatGPT Enterprise 和 Codex](https://openai.com/index/samsung-electronics-chatgpt-codex-deployment) ⭐️ 8.0/10

三星电子正在向全球员工部署 ChatGPT Enterprise 和 Codex，这标志着 OpenAI 最大规模的企业 AI 部署之一。 此次部署标志着企业大规模采用 AI 工具，可能提升这家全球科技领导者的生产力和创新能力，并验证了 OpenAI 的企业级产品。 ChatGPT Enterprise 提供企业级安全、隐私、无限制的 GPT-4 访问和高级数据分析，而 Codex 是一个 AI 编程伙伴，可加速工程工作。

rss · OpenAI Blog · 6月21日 23:00

**背景**: ChatGPT Enterprise 是 OpenAI 面向企业的 ChatGPT 版本，专为组织使用设计，具有增强的安全性和集成能力。Codex 是一个 AI 工具，可帮助开发者进行规划、构建功能、重构等。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-chatgpt-enterprise/">Introducing ChatGPT Enterprise | OpenAI</a></li>
<li><a href="https://openai.com/codex/">Codex | AI Coding Partner from OpenAI | OpenAI</a></li>

</ul>
</details>

**标签**: `#AI`, `#Enterprise`, `#Samsung`, `#OpenAI`, `#Codex`

---

<a id="item-8"></a>
## [中美 AI 出口战升级：中国将 56 家美国公司列入黑名单](https://aiweekly.co/issues/washington-blocked-one-ai-lab-china-blacklisted-56-companies) ⭐️ 8.0/10

中国将 56 家美国公司列入黑名单，以报复华盛顿对 Anthropic 最新 AI 模型 Fable 5 和 Mythos 5 的出口管制，该管制迫使 Anthropic 阻止外国国民访问这些模型。微软 CEO 萨提亚·纳德拉警告称，将 AI 权力集中在少数几家公司手中在政治上是不可持续的。 这标志着中美 AI 出口战显著升级，从单向变为双向，可能扰乱全球 AI 供应链和合作。纳德拉的警告凸显了政治和行业对 AI 垄断日益增长的担忧，可能影响未来的监管。 美国商务部利用国家安全出口管制，禁止 Anthropic 向外国国民分发 Fable 5 和 Mythos 5，即使在美国境内也不行。中国的黑名单包括国防承包商和稀土公司，并另外针对 46 家美国公司。

rss · AI Weekly · 6月22日 00:00

**背景**: 出口管制是政府对向外国实体转让敏感技术的限制。美国越来越多地利用这些措施限制中国获取先进 AI 芯片和模型，而中国则控制着对国防和科技制造至关重要的稀土矿物。Anthropic 的模型因一次常规编码请求被视为国家安全威胁而受到限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fortune.com/2026/06/13/anthropic-disables-fable-mythos-export-controls-national-security-threat/">Anthropic disables Fable and Mythos AI models following U.S. government export ban | Fortune</a></li>
<li><a href="https://www.presstv.ir/Detail/2026/06/22/770883/China-US-sanctions-retaliation-">China sanctions 56 US companies in retaliation for military-linked...</a></li>
<li><a href="https://www.firstpost.com/tech/you-cant-call-it-progress-microsoft-ceo-satya-nadella-warns-against-concentration-of-ai-power-14025004.html">'You can't call it progress': Microsoft CEO Satya Nadella ...</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#geopolitics`, `#export controls`, `#Anthropic`, `#Microsoft`

---

<a id="item-9"></a>
## [2.4 亿域名自动补全实现 P99 零毫秒延迟](https://ruurtjan.com/articles/p99-0ms-autocomplete-for-240-million-domain-names) ⭐️ 8.0/10

一个系统通过巧妙的数据结构和缓存策略，实现了对 2.4 亿个域名的自动补全，p99 延迟为零毫秒。 这证明了在大规模数据下实现极致性能是可能的，为自动补全系统树立了新标杆，并激励其他领域进行类似优化。 该系统可能使用了 trie 或压缩 trie（Patricia trie）结合激进缓存来实现 p99 零毫秒延迟，即 99%的请求在 1 毫秒内完成。

rss · Lobsters · 6月22日 11:31

**背景**: P99 延迟指响应时间的第 99 百分位数；p99 为零毫秒意味着几乎所有请求都能即时响应。自动补全系统传统上使用 trie 数据结构进行快速前缀匹配，但扩展到数亿条目需要仔细优化内存和缓存局部性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://redis.io/blog/p99-latency/">P99 Latency: What It Means & How to Fix It - Redis</a></li>
<li><a href="https://yalinpala.dev/blog/building-an-autocomplete-system-with-trie">Building an Autocomplete System with Trie - yalinpala.dev</a></li>
<li><a href="https://www.linkedin.com/pulse/trie-optimization-techniques-autocomplete-systems-vallabhaneni-bgm9c">Trie Optimization Techniques for Autocomplete Systems</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论可能赞扬了这一工程成就，并探讨了内存使用与延迟之间的权衡，一些人质疑域名自动补全实现零毫秒的实际必要性。

**标签**: `#autocomplete`, `#performance`, `#systems design`, `#search`, `#engineering`

---

<a id="item-10"></a>
## [Nix 需要可重定位二进制文件](https://fzakaria.com/2026/06/21/nix-needs-relocatable-binaries) ⭐️ 8.0/10

一篇博客文章指出，Nix 无法生成可重定位二进制文件是一个关键缺陷，阻碍了其实用性，必须加以解决。 这一限制影响了 Nix 的可用性和采用率，尤其是在需要将二进制文件移动到不同环境或共享而无需重新编译的场景中。 可重定位二进制文件可以从任何目录运行，无需硬编码路径，这对于 Nix 的纯函数式包模型至关重要。缺乏此功能迫使使用包装脚本或修补等变通方法。

rss · Lobsters · 6月22日 11:54

**背景**: Nix 是一个纯函数式包管理器，将包视为不可变值，从而实现可重现构建和声明式系统配置。可重定位二进制文件是指可以移动到文件系统上任何位置并仍能正常运行的二进制文件，因为它使用相对路径或运行时路径解析，而不是硬编码的绝对路径。许多包管理器和构建系统支持可重定位二进制文件，但 Nix 目前不支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://softwareengineering.stackexchange.com/questions/314327/what-is-a-relocatable-binary/314331">What is a Relocatable Binary ? - Software Engineering Stack Exchange</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nix_(package_manager)">Nix (package manager)</a></li>
<li><a href="https://nixos.org/">Nix & NixOS | Declarative builds and deployments</a></li>

</ul>
</details>

**标签**: `#Nix`, `#relocatable binaries`, `#package management`, `#software engineering`, `#systems research`

---

<a id="item-11"></a>
## [早期研究表明，使用 AI 可能削弱人类技能](https://www.nature.com/articles/d41586-026-01947-1) ⭐️ 8.0/10

《自然》杂志的一篇文章报道，早期研究结果表明，依赖 AI 工具可能会削弱人类的认知技能，如批判性思维和解决问题的能力。 这项研究引发了对 AI 对人类能力长期影响的重大担忧，可能对教育、劳动力培训以及我们如何将 AI 融入日常生活产生深远影响。 该文章基于早期阶段的研究，技能退化的具体机制和程度仍在调查中。研究结果强调需要平衡 AI 整合，以保护人类专业知识。

rss · Lobsters · 6月21日 10:41

**背景**: 随着 ChatGPT 和 GitHub Copilot 等 AI 工具的普及，人们越来越担心过度依赖 AI 可能导致基本人类技能的退化。这反映了过去关于技术对记忆和注意力影响的讨论。

**标签**: `#AI`, `#human skills`, `#cognitive effects`, `#research`, `#education`

---

<a id="item-12"></a>
## [Linux 安全启动证书即将到期](https://lwn.net/Articles/1029767/) ⭐️ 8.0/10

微软 2011 年安全启动签名证书将于 2026 年 6 月 27 日到期，影响依赖该证书进行启动完整性验证的 Linux 系统。 如果未及时更新，此证书到期可能导致启用了安全启动的 Linux 系统无法启动，给企业和个人用户带来广泛的安全和运营风险。 Red Hat 等发行版正在发布使用微软 2023 UEFI CA 证书签名的新版 shim，以确保安全启动的持续兼容性。

rss · Lobsters · 6月22日 12:37

**背景**: 安全启动是 UEFI 固件的一项功能，它验证引导加载程序和内核的数字签名，以防止未经授权的代码在系统启动时运行。第一阶段的引导加载程序称为 shim，由微软的证书签名，然后验证后续组件如 GRUB 和内核。当签名证书到期时，shim 的签名将失效，导致安全启动拒绝加载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lwn.net/Articles/1029767/">Linux and Secure Boot certificate expiration [LWN.net]</a></li>
<li><a href="https://developers.redhat.com/articles/2026/02/04/secure-boot-certificate-changes-2026-guidance-rhel-environments">Secure Boot certificate changes in 2026: Guidance for RHEL environments | Red Hat Developer</a></li>
<li><a href="https://www.redhat.com/en/blog/expiration-secure-boot-signing-certificates-2026">Expiration of Secure Boot signing certificates in 2026</a></li>

</ul>
</details>

**标签**: `#Linux`, `#Secure Boot`, `#Security`, `#Certificate Expiration`

---

<a id="item-13"></a>
## [1991 年慕尼黑：当前 AI 热潮的根源](https://people.idsia.ch/~juergen/ai-boom-roots-munich-1991.html) ⭐️ 8.0/10

Jürgen Schmidhuber 发表文章，将当前 AI 热潮的起源追溯至其团队 1991 年在慕尼黑的工作，重点介绍了 1991 年 3 月至 8 月的关键论文。 这位 AI 先驱研究者的历史视角为理解现代深度学习和生成式 AI 的基础提供了关键背景。 文章引用了慕尼黑工业大学 1991 年的具体出版物，包括一篇关于通过人工好奇心训练世界模型的 GAN 会议论文，并指出当时的计算成本比现在贵数百万倍。

rss · Lobsters · 6月22日 12:09

**背景**: Jürgen Schmidhuber 是一位德国计算机科学家，被公认为人工神经网络和深度学习领域的先驱。他在 1990 年代初的工作为现代 AI 奠定了概念基础，包括首个在交通中行驶的自动驾驶汽车和早期的 GAN。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://people.idsia.ch/~juergen/ai-boom-roots-munich-1991.html">Munich 1991 : the Roots of the Current AI Boom</a></li>
<li><a href="https://digg.com/tech/akhwgaiu">Jürgen Schmidhuber argues his Munich team's 1991 papers...</a></li>

</ul>
</details>

**社区讨论**: 该文章在 Lobsters 上引发了讨论，评论可能围绕 Schmidhuber 关于优先权和影响力的主张展开辩论，但未提供具体评论内容。

**标签**: `#AI`, `#history`, `#deep learning`, `#research`

---

<a id="item-14"></a>
## [我过去的工作只是因欺诈而存在吗？](https://david.newgas.net/did-my-old-job-only-exist-because-of-fraud/) ⭐️ 7.0/10

一篇个人文章和社区讨论探讨了政府及企业技术合同中的欺诈和低效如何创造不必要的岗位，评论者分享了账单欺诈和合同注水的真实案例。 这引发了对技术合同实践诚信的质疑，可能影响数百万软件工程师以及为这些项目纳税的公众。 评论者描述了承包商通过外包公司以更高费率重新入职，以及经理篡改工时表以耗尽预算的情况，凸显了政府和私营部门项目中的系统性问题。

hackernews · advisedwang · 6月21日 21:40 · [社区讨论](https://news.ycombinator.com/item?id=48622867)

**背景**: 政府及大型企业技术项目通常涉及复杂的合同链，多层供应商和分包商可能掩盖真实成本和责任。欺诈形式包括对未完成工作收费、虚报工时或创造不必要的岗位以消耗预算盈余。

**社区讨论**: 评论者普遍认为此类欺诈普遍存在，分享了个人经历中的账单操纵和承包商更替。一些人表示管理层往往忽视这些做法，另一些人则指出私营部门也存在类似低效。

**标签**: `#tech industry`, `#fraud`, `#government contracting`, `#software engineering`

---

<a id="item-15"></a>
## [Apertus：面向主权 AI 的开放基础模型](https://apertvs.ai/) ⭐️ 7.0/10

由苏黎世联邦理工学院领导的瑞士联盟开发的 Apertus，一个完全开放、透明且多语言的基础模型，已发布以促进 AI 主权。 该倡议解决了对数据主权和依赖美国 AI 提供商日益增长的担忧，为政府和组织提供了构建主权 AI 能力的透明替代方案。 Apertus 是少数几个在其规模上完全开放的 LLM 之一，发布了完整的训练流程和数据集，但社区基准测试表明它落后于 Nvidia Nemotron 和 Llama 3.1 等模型。

hackernews · T-A · 6月21日 21:29 · [社区讨论](https://news.ycombinator.com/item?id=48622778)

**背景**: 主权 AI 指国家或组织对其 AI 生态系统的控制，包括数据、模型和治理。Apertus 旨在提供一个透明、多语言的基础模型，可适应各种应用，减少对外国 AI 系统的依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ethz.ch/en/news-and-events/eth-news/news/2025/09/press-release-apertus-a-fully-open-transparent-multilingual-language-model.html">Apertus: a fully open, transparent, multilingual language model | ETH Zurich</a></li>
<li><a href="https://www.techtarget.com/whatis/feature/Sovereign-AI-explained">Sovereign AI explained: Everything you need to know - TechTarget</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-sovereignty">What is AI sovereignty? - IBM</a></li>

</ul>
</details>

**社区讨论**: 社区评论对 Apertus 的竞争力表示怀疑，指出其进展缓慢，且其指令模型基于去年的 Llama 3.1。一些用户强调团队经验不足，而另一些则指出多语言任务的可靠性问题。

**标签**: `#open source`, `#LLM`, `#AI sovereignty`, `#foundation model`

---

<a id="item-16"></a>
## [为何绘图板品牌回避 Linux 开源驱动](https://www.davidrevoy.com/article1154/why-drawing-tablet-brands-wont-collaborate-on-linux-floss-drivers) ⭐️ 7.0/10

David Revoy 的一篇文章解释称，绘图板品牌拒绝合作开发 Linux 自由开源驱动，部分原因是主要驱动仓库以 Wacom 命名，让竞争对手觉得是在帮助对手。 这一命名问题阻碍了 Linux 上通用开源绘图板驱动的发展，限制了硬件支持和用户选择。解决它可能促进合作，改善数字艺术家的 Linux 生态。 linuxwacom 项目及其仓库历史上以 Wacom 命名，尽管通过 DIGImend 等项目支持其他品牌。简单的重命名可以消除这种利益冲突感。

hackernews · Lobsters · 6月22日 12:09 · [社区讨论](https://news.ycombinator.com/item?id=48629064)

**背景**: FLOSS 代表自由/开源软件。Linux 绘图板驱动由 linux-wacom（支持 Wacom）和 DIGImend（支持其他品牌）等项目维护。OpenTabletDriver 是另一个跨平台开源替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.davidrevoy.com/article1154/why-drawing-tablet-brands-wont-collaborate-on-linux-floss-drivers">Why Drawing Tablet Brands Won't Collaborate on Linux FLOSS ...</a></li>
<li><a href="https://github.com/DIGImend/digimend-kernel-drivers">GitHub - DIGImend/digimend-kernel-drivers: DIGImend graphics tablet drivers for the Linux kernel · GitHub</a></li>
<li><a href="https://opentabletdriver.net/">OpenTabletDriver</a></li>

</ul>
</details>

**社区讨论**: 评论者大多同意重命名仓库是一个简单的修复，有人指出从'master'到'main'的重命名更具破坏性。其他人建议分叉并重命名项目以鼓励厂商贡献。

**标签**: `#Linux`, `#open-source`, `#drivers`, `#graphics-tablets`, `#community-collaboration`

---

<a id="item-17"></a>
## [sqlite-utils 4.0rc1 引入迁移和嵌套事务](https://simonwillison.net/2026/Jun/21/sqlite-utils-40rc1/#atom-everything) ⭐️ 7.0/10

sqlite-utils 4.0rc1 于 2026 年 6 月 21 日发布，新增了内置的数据库迁移功能（从 sqlite-migrate 包移植而来）以及通过新的 db.atomic 上下文管理器实现的嵌套事务。这是 4.0 主版本的第一个候选发布版，包含少量不兼容的变更。 这些功能简化了使用 SQLite 的 Python 开发者的数据库模式演进和事务控制，使 sqlite-utils 成为更完整的 CLI 和库工具。迁移系统已在 LLM 等项目中得到验证，减少了对外部迁移工具的依赖。 迁移被定义为 migrations.py 文件中的装饰器 Python 函数，仅支持前向变更，不提供反向迁移。嵌套事务通过 SQLite 保存点模拟，允许在事务块内部分回滚。

rss · Simon Willison · 6月21日 23:35

**背景**: sqlite-utils 是 Simon Willison 开发的 Python 库和 CLI 工具，为 SQLite 数据库提供高级操作。SQLite 本身不支持真正的嵌套事务，但可以使用保存点来模拟。新的迁移功能移植自成熟的 sqlite-migrate 包，该包已在生产环境中使用多年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/21/sqlite-utils-40rc1/">sqlite-utils 4.0rc1 adds migrations and nested transactions</a></li>
<li><a href="https://sqlite-utils.datasette.io/en/latest/migrations.html">Database migrations - sqlite-utils</a></li>
<li><a href="https://github.com/simonw/sqlite-migrate">GitHub - simonw/sqlite-migrate: A simple database migration ... GitHub - simonw/sqlite-utils: Python CLI utility and library ... sqlite-utils 4.0rc1 adds migrations and nested transactions sqlite-migrate · PyPI sqlite-utils · PyPI</a></li>

</ul>
</details>

**标签**: `#sqlite`, `#python`, `#database`, `#migrations`

---

<a id="item-18"></a>
## [Cloudflare 推出临时 Workers 部署功能](https://simonwillison.net/2026/Jun/21/temporary-cloudflare-accounts/#atom-everything) ⭐️ 7.0/10

Cloudflare 为 Wrangler CLI 新增了 `--temporary` 标志，无需账户即可部署 Workers 项目，部署内容将保持在线 60 分钟。 该功能大幅降低了尝试 Cloudflare Workers 的门槛，为 AI 代理和开发者提供了快速原型设计和临时部署的能力。 `--temporary` 标志仅适用于未认证用户；如果已配置凭据，则会返回错误。部署可通过链接认领，以保留超过 60 分钟。

rss · Simon Willison · 6月21日 22:01

**背景**: Cloudflare Workers 是一个无服务器边缘计算平台，在 Cloudflare 的 CDN 上运行 JavaScript。Wrangler 是用于开发和部署 Workers 的官方命令行工具。此前，部署 Worker 需要创建 Cloudflare 账户并进行身份验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/21/temporary-cloudflare-accounts/">Temporary Cloudflare Accounts for AI agents</a></li>
<li><a href="https://developers.cloudflare.com/workers/platform/claim-deployments/">Claim deployments ( temporary accounts) · Cloudflare Workers docs</a></li>
<li><a href="https://hono.dev/docs/getting-started/cloudflare-workers">Cloudflare Workers - Hono</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（文中已链接）可能对易用性持积极态度，但此处未提供具体评论。

**标签**: `#cloudflare`, `#serverless`, `#devtools`, `#ai-agents`, `#deployment`

---

<a id="item-19"></a>
## [切斯特顿的中指：对盲目遵循的批判](https://www.arp242.net/chestersons-finger.html) ⭐️ 7.0/10

一篇题为《切斯特顿的中指》的文章批判性地审视了切斯特顿栅栏原则，认为应深思熟虑地应用而非盲目遵循。它挑战了常见的解读，即改变任何事物前必须理解其原始目的。 这一批判对经常引用切斯特顿栅栏来抵制变化、可能扼杀创新的软件工程师和决策者具有重要意义。它鼓励一种更平衡的方法，既考虑过去的智慧，也考虑进步的需要。 文章可能使用“竖中指”的比喻来强调对教条式遵循的反叛。它可能提供例子，说明盲目遵循该原则导致次优结果。

rss · Lobsters · 6月22日 09:02

**背景**: 切斯特顿栅栏是一个归功于 G.K.切斯特顿的原则，指出在移除或改变某物之前，应首先理解它最初为何存在。在软件工程中，它常被用来警告不要仓促重构或移除看似不必要的代码。文章批判了这一原则，认为它可能被滥用来为不作为辩护或保留过时的做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fs.blog/chestertons-fence/">Chesterton ’ s Fence : A Lesson in Thinking</a></li>
<li><a href="https://generalist-thinkbox.medium.com/chestertons-fence-why-understanding-the-past-can-help-us-build-a-better-future-a2afdce03f63">Chesterton ’ s Fence : Why Understanding the Past Can Help... | Medium</a></li>
<li><a href="https://www.linkedin.com/pulse/chestertons-fence-understanding-why-behind-decisions-belk-olson-msc-6u6lc">Chesterton ' s Fence and Understanding The Why Behind Decisions</a></li>

</ul>
</details>

**标签**: `#software engineering`, `#principles`, `#critical thinking`, `#Chesterton's fence`

---

<a id="item-20"></a>
## [在 PostgreSQL 中管理时区变更](https://www.crunchydata.com/blog/british-columbia-and-time-zone-changes) ⭐️ 7.0/10

Crunchy Data 发布了一篇技术指南，以不列颠哥伦比亚省可能从太平洋时间改为山地时间为例，讲解如何在 PostgreSQL 中处理时区变更。 时区变更虽然罕见，但处理不当可能导致数据损坏或时间戳错误；本指南为数据库管理员提供了在过渡期间确保数据完整性的实用步骤。 文章涵盖了使用 PostgreSQL 的时区数据库、更新系统时区数据以及使用历史数据进行测试以验证正确性。

rss · Lobsters · 6月22日 11:18

**背景**: PostgreSQL 内部使用 UTC 存储带时区的时间戳，并在显示时转换为会话的时区。时区变更需要更新操作系统的时区文件和 PostgreSQL 的时区数据以反映新规则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cybertec-postgresql.com/en/time-zone-management-in-postgresql/">Time zone management in PostgreSQL | CYBERTEC PostgreSQL</a></li>
<li><a href="https://en.wikipedia.org/wiki/Time_in_Canada">Time in Canada - Wikipedia</a></li>

</ul>
</details>

**标签**: `#PostgreSQL`, `#time zones`, `#database`, `#engineering`

---

<a id="item-21"></a>
## [postmarketOS v26.06 Alpen Avocado 发布](https://postmarketos.org/blog/2026/06/21/v26.06-release/) ⭐️ 7.0/10

postmarketOS v26.06（Alpen Avocado）已发布，基于 Alpine Linux 3.24，包含 GNOME 50、KDE Plasma Mobile 6.6.5、Phosh 0.55.0、systemd 261 以及新的基于 Plymouth 的启动动画。 此版本继续推动 postmarketOS 成为可行的移动 Linux 发行版，延长智能手机的使用寿命，并为用户提供最新的软件和改进的无障碍功能。 值得注意的变化包括 Phosh 从 tinydm 切换到 greetd/phrog、启动时振动无障碍支持，以及用 sudo-rs 替代 sudo 作为默认权限提升工具。

rss · Lobsters · 6月21日 15:08

**背景**: postmarketOS 是一个基于 Alpine Linux 的免费开源 Linux 发行版，专为智能手机和其他移动设备设计。它旨在通过提供长期软件支持和多种用户界面（如 Plasma Mobile、GNOME 和 Phosh）来为设备提供十年的生命周期。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://postmarketos.org/blog/2026/06/21/v26.06-release/">postmarketOS // v26.06: Alpen Avocado</a></li>
<li><a href="https://en.wikipedia.org/wiki/PostmarketOS">PostmarketOS</a></li>
<li><a href="https://daily.dev/posts/v26-06-alpen-avocado-fq0f6x1ib">v26.06: Alpen Avocado - daily.dev</a></li>

</ul>
</details>

**标签**: `#postmarketOS`, `#Linux`, `#mobile`, `#open source`, `#release`

---

<a id="item-22"></a>
## [不到 100 行代码实现 Nix 构建](https://fzakaria.com/2026/06/21/nix-build-in-under-100-lines) ⭐️ 7.0/10

一位开发者发布了不到 100 行代码的 nix-build 最小实现，展示了 Nix 构建系统背后的核心逻辑。 这个简洁的实现有助于开发者理解 Nix 的构建隔离和可重现性原则，可能降低学习 Nix 的门槛。 该实现捕获了核心构建逻辑，无需外部依赖，专注于使 Nix 独特的函数式编程方面。

rss · Lobsters · 6月22日 00:21

**背景**: Nix 是一个跨平台的包管理器和构建系统，使用函数式语言定义包，并在隔离环境中进行构建。它通过沙盒构建过程和内容寻址存储确保可重现的构建。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nixos.org/">Nix & NixOS | Declarative builds and deployments</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nix_(package_manager)">Nix ( package manager ) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Nix`, `#build systems`, `#functional programming`, `#software engineering`

---

<a id="item-23"></a>
## [内存安全的内联汇编提案](https://fil-c.org/inlineasm) ⭐️ 7.0/10

Fil-C 实现了首个针对 x86_64 的内存安全内联汇编，支持数百条指令，包括 x87、SIMD、位运算和栅栏指令。该提案定义了安全边界和允许的指令白名单。 内联汇编长期以来一直是底层编程中内存安全漏洞的主要来源。这项工作可以在保持性能的同时显著减少此类错误，对系统编程和编译器设计产生影响。 该实现遵循“垃圾进，内存安全出”模型，即任何输入都会被清理以确保内存安全。它涵盖在此模型下安全的指令，排除了可能绕过内存保护的指令。

rss · Lobsters · 6月22日 03:49

**背景**: 内存安全是一种关键属性，可防止缓冲区溢出和释放后使用等错误。像 C 和 C++ 这样的底层语言通常依赖内联汇编来提升性能，但这类代码通常内存不安全。Fil-C 是一个探索内存安全系统编程的研究项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fil-c.org/inlineasm">Memory Safe Inline Assembly - fil-c.org</a></li>
<li><a href="https://news.ycombinator.com/item?id=48606096">Memory Safe Inline Assembly | Hacker News</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论强调了该方法的新颖性以及对允许指令的精心筛选。一些评论者质疑安全检查的性能开销，而另一些则赞赏所定义的正式边界。

**标签**: `#memory safety`, `#inline assembly`, `#systems programming`, `#compiler`

---

<a id="item-24"></a>
## [PivCo-Huffman 合并操作](https://fgiesen.wordpress.com/2026/06/21/pivco-huffman-merge-operations/) ⭐️ 7.0/10

一篇新论文提出了 PivCo-Huffman，它将霍夫曼解码从串行过程转变为一系列可并行化的列表合并操作，可能提高压缩效率。 这种方法可以在现代并行硬件上实现更快的霍夫曼解码，从而惠及数据存储、网络和多媒体中使用的压缩算法。 该合并操作被描述为一种通用的任意字节到任意字节的洗牌操作，该技术基于小波树中的数据结构。

rss · Lobsters · 6月22日 01:27

**背景**: 霍夫曼编码是一种经典的无损压缩方法，根据符号频率分配可变长度码。传统的霍夫曼解码本质上是串行的，限制了其在并行硬件上的性能。PivCo-Huffman 旨在通过将解码重新表述为可并行执行的合并操作来克服这一限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.05765">[2606.05765] PivCo-Huffman - arXiv.org</a></li>
<li><a href="https://fgiesen.wordpress.com/2026/06/21/pivco-huffman-merge-operations/">PivCo- Huffman “ merge ” operations | The ryg blog</a></li>
<li><a href="https://daily.dev/posts/pivco-huffman-merge-operations-ypm0kxiih">PivCo-Huffman “merge” operations - daily.dev</a></li>

</ul>
</details>

**标签**: `#compression`, `#algorithms`, `#data structures`, `#Huffman coding`

---

<a id="item-25"></a>
## [美国可能将非洲航天产业拱手让给中国](https://spacenews.com/america-is-about-to-cede-africas-space-industry-to-china-and-nobodys-talking-about-it/) ⭐️ 7.0/10

一篇 SpaceNews 文章指出，由于缺乏战略重点，美国正在将非洲日益增长的航天产业影响力拱手让给中国，而中国则通过投资和合作积极介入。 这一转变可能重塑全球航天格局，因为非洲在卫星通信、地球观测和发射服务方面正成为关键参与者，可能更倾向于与中国合作。 文章指出，美国的“美国优先在非洲”政策缺乏具体的航天举措，而中国已经启动了联合卫星项目并为非洲工程师提供培训。

rss · SpaceNews · 6月22日 13:00

**背景**: 非洲航天产业正在快速增长，尼日利亚、南非和肯尼亚等国正在开发自己的卫星。美国历史上曾是合作伙伴，但中国的“一带一路”倡议包含航天合作，提供资金和技术转让。

**标签**: `#space industry`, `#Africa`, `#geopolitics`, `#China`, `#US policy`

---