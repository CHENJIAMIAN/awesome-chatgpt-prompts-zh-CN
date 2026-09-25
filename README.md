[English](./README.en.md)

<!-- codex-github-rules:bilingual-summary -->
> **中文简介**：ChatGPT 提示词中文合集，新增 AIPRM 提示词
>
> **English summary**: A Chinese ChatGPT prompt collection with additional AIPRM prompts

---

# 🧠 ChatGPT 提示词中文合集（Awesome ChatGPT Prompts 中文版）

![提示词](https://img.shields.io/badge/%E6%8F%90%E7%A4%BA%E8%AF%8D-2172-blue?style=flat-square)
![上游同步](https://img.shields.io/badge/%E4%B8%8A%E6%B8%B8%E5%90%8C%E6%AD%A5-2026--09--25-green?style=flat-square)
![许可](https://img.shields.io/badge/%E8%AE%B8%E5%8F%AF-CC0--1.0-lightgrey?style=flat-square)
[![Awesome](https://awesome.re/badge.svg)](https://github.com/sindresorhus/awesome)

**一句话说明**：把上游 [f/prompts.chat](https://github.com/f/prompts.chat)（原名 `awesome-chatgpt-prompts`，17 万+ stars）的**全部 2169 条提示词**翻译成简体中文，并把全部译文整理成 CSV / JSON / Markdown 三种可直接使用的形式；另外附上 **1536 条 AIPRM 提示词库快照**（2023 年抓取，中文译文已于 2026-09 重新翻译）。

打开 [PROMPTS.zh-CN.md](PROMPTS.zh-CN.md)（全量索引）即可按分卷浏览全部中文提示词。

## ✨ 本次更新（2026-09-25）

| 项目 | 更新前 | 更新后 |
| --- | --- | --- |
| 提示词条数 | 152 | **2172**（上游全量 + 3 条历史条目） |
| 中文译文 | 2023 年的旧版机翻 | **全部重新翻译**，保留 Markdown 结构 / 代码块 / `{占位符}` / URL |
| 英文源数据 | 2023-02 快照 | 与上游同步至 2026-09 |
| 浏览方式 | 只有超长 README | 新增 [PROMPTS.zh-CN.md](PROMPTS.zh-CN.md) 索引 + `prompts/part-NN.md` 分卷（每条 `<details>` 折叠，便于检索） |
| 数据文件 | 只有旧版 CSV/JSON | CSV（中/英）、JSON（中/英）全部重建，字段与上游对齐 |
| 仓库元数据 | 无 topics | 补齐 topics / 描述，便于在 GitHub 搜索中发现 |
| AIPRM 中文 | 2023 年旧机翻，且中文 YAML 行序错位、部分条目被截断 | **1536 条全部重译**，YAML 按英文文件行序重建（与 JSON 逐条对齐） |

## 📦 仓库内容

| 文件 | 说明 | 条目数 |
| --- | --- | --- |
| [PROMPTS.zh-CN.md](PROMPTS.zh-CN.md) | **全量中文提示词索引**，正文按体积分卷到 `prompts/part-NN.md` | 2172 |
| [prompts_zh-CN.csv](prompts_zh-CN.csv) | 中文数据表，列：`行动`,`提示`（UTF-8，全部字段加引号） | 2172 |
| [prompts.csv](prompts.csv) | 上游英文原文数据表，列：`act`,`prompt`,`for_devs`,`type`,`contributor` | 2169 |
| [chatgpt_prompts-zh-CN.json](chatgpt_prompts-zh-CN.json) | 中文 JSON，字段：`cmd`,`act`,`tags`,`enable`,`prompt` | 2172 |
| [chatgpt_prompts.json](chatgpt_prompts.json) | 英文 JSON（同上结构） | 2169 |
| [Aiprm_Prompts.json](Aiprm_Prompts.json) / [Aiprm_Prompts-Prompt-zh-CN.json](Aiprm_Prompts-Prompt-zh-CN.json) | AIPRM 提示词库快照（英 / 中英对照 JSON，含作者、分类、社区字段）；`PromptZh` 于 2026-09 重译 | 1536 |
| [Aiprm_Prompts Prompt-zh-CN.yml](Aiprm_Prompts%20Prompt-zh-CN.yml) / [Aiprm_Prompts_Prompt.yml](Aiprm_Prompts_Prompt.yml) | AIPRM 提示词的中文 / 英文 YAML（每行一条，中英行序一致） | 1536 |
| [Aiprm_Prompts_txt.txt](Aiprm_Prompts_txt.txt) / [Aiprm_Prompts_txt_zh.txt](Aiprm_Prompts_txt_zh.txt) | 2023 年抓取的「标题 + 摘要」纯文本清单（另一份快照，见下方说明） | 3652 |
| [CONTRIBUTING.md](CONTRIBUTING.md) / [LICENSE](LICENSE) | 沿用上游（CC0-1.0） | — |

## 🚀 怎么用

**1）直接找提示词**：打开 [PROMPTS.zh-CN.md](PROMPTS.zh-CN.md) 索引，进入某个分卷（`prompts/part-01.md` …）后点开条目复制；也可在本仓库页面按 `t` 打开文件搜索，或在分卷里用 `Ctrl+F` 搜关键词（例如「面试」「SEO」「代码审查」）。

**2）当成数据集用**：

```bash
# 中文 CSV
curl -O https://raw.githubusercontent.com/CHENJIAMIAN/awesome-chatgpt-prompts-zh-CN/main/prompts_zh-CN.csv

# 中文 JSON
curl -O https://raw.githubusercontent.com/CHENJIAMIAN/awesome-chatgpt-prompts-zh-CN/main/chatgpt_prompts-zh-CN.json
```

```python
import csv, io, urllib.request
url = "https://raw.githubusercontent.com/CHENJIAMIAN/awesome-chatgpt-prompts-zh-CN/main/prompts_zh-CN.csv"
text = urllib.request.urlopen(url).read().decode("utf-8")
rows = list(csv.DictReader(io.StringIO(text)))
print(len(rows), rows[0]["行动"])   # -> 2172 Linux 终端
```

**3）复制到 AI 对话框**：把「提示」正文整段粘贴给 ChatGPT / Claude / Gemini / 豆包 / DeepSeek / Grok 等任意对话模型，然后按提示词里的要求补充你的输入（例如把 `[PROMPT]` 换成你的主题）。

**4）图像 / 音乐类提示词**：`类型 = 图像生成提示词` 的条目适合 Midjourney / DALL·E / 即梦等；含 Suno 字样的条目适合音乐生成模型。

## 🔍 精选示例

### Linux Terminal（原文标题：`Linux Terminal`）

> 我需要你充当 Linux 终端。我会输入命令，而你将回复终端应该显示的内容。你只能在唯一的代码块中回复终端输出，除此之外什么都不要回复。不要写解释。除非我指示你这样做，否则不要输入任何命令。当我需要用英文告诉你一些事情时，我会将文字放在大括号内 {like this}。我的第一个命令是 pwd

### 代码审查专家（原文标题：`Code Review Specialist`）

> 扮演一名代码审查专家。你是一名经验丰富的软件开发人员，具有敏锐的细节洞察力，深入理解编码标准和最佳实践。
>
> 你的任务是审查所提供的代码，评估其质量、是否符合标准以及是否存在优化潜力。
>
> 你将：
> - 评估代码是否符合行业标准和最佳实践。
> - 识别潜在的优化区域并提出改进建议。
> - 检查逻辑错误、缺陷以及潜在的安全漏洞。
> - 向代码作者提供有建设性的反馈。
>
> 规则：
> - 在审查过程中保持客观和公正。
> - 关注代码的功能性和非功能性方面。
> - 在所有反馈中保持专业和尊重的语气。

### 面试官（原文标题：`Job Interviewer`）

> 我希望你扮演面试官的角色。我将作为候选人，而你将向我提出针对 ${Position:Software Developer} 职位的面试问题。你只能以面试官的身份回复。不要一次性写出整个对话。我只希望你和我进行面试。向我提问并等待我的回答。不要写解释。像真正的面试官一样逐个提问，并等待我的回答。
>
> 我的第一句话是 "Hi"

### SEO 专家（原文标题：`SEO specialist`）

> 我要你充当一名 SEO 专家。我将向你提供与搜索引擎优化（SEO）相关的查询或场景，而你将据此给出相应的 SEO 建议或推荐。你的回复应严格聚焦于 SEO 策略、技术与洞见。请勿在回复中提供通用营销建议或泛泛解释。"Your SEO Prompt"

### 图像编辑器（原文标题：`Image Editor`）

> 使用 HTML5 Canvas、CSS3 和 JavaScript 开发一个基于网页的图像编辑器。创建一个具备工具面板和预览区域的专业化界面。实现基础调整功能，包括亮度、对比度、饱和度和锐度。添加可自定义参数并支持实时预览的滤镜。包含带宽高比控制的裁剪与缩放功能。实现文本叠加功能，支持字体选择与样式设置。添加形状绘制工具，并提供填充与描边选项。包含图层管理功能，并支持混合模式。支持以多种格式与质量导出图像。创建响应式设计，使其能随屏幕尺寸自适应。添加支持历史状态的撤销/重做功能。

### MCP Builder（原文标题：`MCP Builder`）

> ---
> name: mcp-builder
> description: 指导如何创建高质量的 MCP（Model Context Protocol）服务器，使大语言模型（LLM）能够通过精心设计的工具与外部服务交互。在构建用于集成外部 API 或服务的 MCP 服务器时使用，无论是使用 Python（FastMCP）还是 Node/TypeScript（MCP SDK）。
> license: 完整条款见 LICENSE.txt
> ---
>
> # MCP 服务器开发指南
>
> ## 概述
>
> 创建 MCP（Model Context Protocol）服务器，使大语言模型（LLM）能够通过设计良好的工具与外部服务交互。MCP 服务器的质量取决于其在多大程度上帮助 LLM 完成真实世界任务的能力。
>
> ---
>
> # 流程
>
> ## 🚀 高层次工作流
>
> 创建高质量的 MCP 服务器包含四个主要阶段：
>
> ### 第一阶段：深入研究与规划
>
> #### 1.……


更多见 [PROMPTS.zh-CN.md](PROMPTS.zh-CN.md)。

## 📊 数据统计

| 指标 | 数值 |
| --- | --- |
| 提示词总数 | 2172（上游 2169 + 历史条目 3） |
| 类型分布 | 文本 1836 · 结构化 312 · 图像 21 |
| 贡献者 | 上游 1045 人 |
| 英文原文体量 | 5,501,347 字符 |
| 中文译文体量 | 2,699,655 字符 |
| 最长条目 | Socratic Lens（原文约 14.4 万字符） |

## ⚠️ 翻译与使用说明

- 本仓库的中文译文由 **AI 辅助批量翻译**（通义千问 `qwen-plus` / `qwen3-max`），翻译时强制保留 Markdown 结构、代码块、URL、`{占位符}` 与示例中的英文格式标记；术语（prompt=提示词、prompt engineering=提示词工程等）统一。
- **原文以 [prompts.csv](prompts.csv) 为准**；译文与原文逐条对应，同一个 `act` 字段可通过行序对齐。
- 上游是社区众包列表，条目质量参差、存在重复与低质量条目（例如占位用的 `Test`、`reviews`），本仓库如实保留，未做主观删减；`结构化提示词` 多为 JSON/YAML 形式的输入输出定义，`图像生成提示词` 面向绘图模型。
- 发现翻译错误、术语不一致或想补充新提示词：欢迎提交 [Issue](https://github.com/CHENJIAMIAN/awesome-chatgpt-prompts-zh-CN/issues) 或 PR（新增/修改中文译文即可）。
- AIPRM 部分：JSON 与 YAML 为 2023 年 1 月抓取的同一份快照（1536 条），其**中文译文于 2026-09-25 用 `deepseek-v4.1-flash` 全部重译**（替换 2023 年的旧机翻；中文 YAML 同时修正了行序错位与条目截断问题）。
- `Aiprm_Prompts_txt.txt` / `Aiprm_Prompts_txt_zh.txt` 是**另一份抓取结果**（3652 条「标题 + 摘要」清单，与上面 1536 条 JSON 无法逐条对应），因此保持 2023 年原样、未做改动。
- AIPRM 的提示词库后续需登录访问，故 1536 条快照未再扩充。

## 🔗 相关链接

- 上游项目：[f/prompts.chat](https://github.com/f/prompts.chat)（原 awesome-chatgpt-prompts）
- 在线浏览：[prompts.chat](https://prompts.chat/prompts)
- Hugging Face 数据集：[fka/prompts.chat](https://huggingface.co/datasets/fka/prompts.chat)
- 桌面客户端：[lencx/ChatGPT](https://github.com/lencx/ChatGPT)
- 其他中文合集：[L1Xu4n/Awesome-ChatGPT-prompts-ZH_CN](https://github.com/L1Xu4n/Awesome-ChatGPT-prompts-ZH_CN)

## 📜 许可

- 提示词内容与数据沿用上游，采用 **CC0-1.0**（公有领域贡献），见 [LICENSE](LICENSE)。
- 本仓库的中文译文同样以 CC0-1.0 发布，可自由使用、修改、商用。

## 🙏 致谢

感谢上游作者 [@f](https://github.com/f) 与 1045 位提示词贡献者，以及 AIPRM 社区的提示词作者。如果这个中文合集对你有帮助，欢迎点个 ⭐ Star。
