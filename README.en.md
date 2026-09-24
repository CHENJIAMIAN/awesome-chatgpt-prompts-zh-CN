[中文](./README.md)

<!-- codex-github-rules:bilingual-summary -->
> **English summary**: A Chinese ChatGPT prompt collection with additional AIPRM prompts
>
> **中文简介**：ChatGPT 提示词中文合集，新增 AIPRM 提示词

---

# 🧠 awesome-chatgpt-prompts-zh-CN

![Prompts](https://img.shields.io/badge/prompts-2172-blue?style=flat-square)
![Upstream sync](https://img.shields.io/badge/upstream%20sync-2026--09--25-green?style=flat-square)
![License](https://img.shields.io/badge/license-CC0--1.0-lightgrey?style=flat-square)

**A complete Simplified-Chinese edition of [f/prompts.chat](https://github.com/f/prompts.chat)** (formerly `awesome-chatgpt-prompts`, 170k+ stars): all **2169 upstream prompts translated into Chinese**, published as Markdown, CSV and JSON, plus a **1,536-prompt AIPRM library snapshot** (bilingual, captured in 2023).

Start here → **[PROMPTS.zh-CN.md](PROMPTS.zh-CN.md)** (index of all Chinese prompts, split into `prompts/part-NN.md` volumes).  
Chinese readers: the default entry point is the [Chinese README](./README.md).

## ✨ What changed in the 2026-09-25 update

| Item | Before | After |
| --- | --- | --- |
| Prompts | 152 | **2172** (full upstream set + 3 legacy entries) |
| Chinese text | 2023 machine translation | fully re-translated, preserving Markdown / code blocks / `{placeholders}` / URLs |
| English source data | Feb-2023 snapshot | synced with upstream (Sep-2026) |
| Browsing | one huge README | [PROMPTS.zh-CN.md](PROMPTS.zh-CN.md) index + `prompts/part-NN.md` volumes with collapsible sections |
| Data files | legacy CSV/JSON | rebuilt CSV (zh/en) and JSON (zh/en), columns aligned with upstream |
| Repo metadata | no topics | topics/description added so the repo is discoverable in GitHub search |

## 📦 Repository layout

| File | Description | Entries |
| --- | --- | --- |
| [PROMPTS.zh-CN.md](PROMPTS.zh-CN.md) | index of all Chinese prompts; full text split into `prompts/part-NN.md` | 2172 |
| [prompts_zh-CN.csv](prompts_zh-CN.csv) | Chinese CSV — `行动`,`提示` | 2172 |
| [prompts.csv](prompts.csv) | upstream English CSV — `act`,`prompt`,`for_devs`,`type`,`contributor` | 2169 |
| [chatgpt_prompts-zh-CN.json](chatgpt_prompts-zh-CN.json) | Chinese JSON — `cmd`,`act`,`tags`,`enable`,`prompt` | 2172 |
| [chatgpt_prompts.json](chatgpt_prompts.json) | English JSON (same schema) | 2169 |
| `Aiprm_Prompts*.json` / `*.yml` / `*_txt*.txt` | AIPRM prompt-library snapshot, English and bilingual | 1,536 |
| [CONTRIBUTING.md](CONTRIBUTING.md) / [LICENSE](LICENSE) | inherited from upstream (CC0-1.0) | — |

## 🚀 Usage

- Browse/copy: open the [PROMPTS.zh-CN.md](PROMPTS.zh-CN.md) index, jump into a `prompts/part-NN.md` volume and use `Ctrl+F` to search (e.g. "面试", "SEO", "代码审查").
- As a dataset:

```bash
curl -O https://raw.githubusercontent.com/CHENJIAMIAN/awesome-chatgpt-prompts-zh-CN/main/prompts_zh-CN.csv
curl -O https://raw.githubusercontent.com/CHENJIAMIAN/awesome-chatgpt-prompts-zh-CN/main/chatgpt_prompts-zh-CN.json
```

- Paste into any chat model (ChatGPT, Claude, Gemini, DeepSeek, Qwen, Grok) and replace the placeholders (`[PROMPT]`, `{like this}`, …) with your own input.
- Entries typed as image prompts target Midjourney/DALL·E-style models; entries mentioning Suno target music models.

## 📊 Stats

| Metric | Value |
| --- | --- |
| Prompts | 2172 (upstream 2169 + 3 legacy) |
| Types | text 1836 · structured 312 · image 21 |
| Upstream contributors | 1045 |
| English source size | 5,501,347 characters |
| Chinese translation size | 2,699,655 characters |

## ⚠️ Notes on the translation

- Translations were produced with **AI assistance** (Qwen `qwen-plus` / `qwen3-max`) under strict instructions to keep the original structure intact: Markdown, code fences, URLs, `{placeholders}` and literal format markers stay as in the source.
- **`prompts.csv` is the source of truth**; rows are aligned by index with the Chinese files.
- The upstream list is community-curated and uneven: duplicate, placeholder-ish or low-quality entries (`Test`, `reviews`, …) are kept as-is rather than silently dropped. `STRUCTURED` entries are JSON/YAML-style specs; `IMAGE` entries target image models.
- Corrections and new Chinese prompts are welcome via [issues](https://github.com/CHENJIAMIAN/awesome-chatgpt-prompts-zh-CN/issues) / PRs.
- The AIPRM snapshot dates from January 2023 (later library contents require a logged-in account).

## 🔗 Links

- Upstream: [f/prompts.chat](https://github.com/f/prompts.chat) · [prompts.chat](https://prompts.chat/prompts) · [Hugging Face dataset](https://huggingface.co/datasets/fka/prompts.chat)
- Desktop app: [lencx/ChatGPT](https://github.com/lencx/ChatGPT)

## 📜 License

Prompt content and data follow upstream: **CC0-1.0** (public domain dedication), see [LICENSE](LICENSE). The Chinese translations in this repository are released under the same terms.

## 🙏 Credits

Thanks to [@f](https://github.com/f) and the 1045 upstream prompt contributors, as well as the AIPRM community authors. A ⭐ is appreciated if this Chinese collection helps you.
