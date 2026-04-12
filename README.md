# GEO Toolkit — AI CLI Skill

Generative Engine Optimization (GEO) skill for AI CLI agents (Claude Code, Codex, Gemini CLI). Audit and improve your brand's visibility in AI-generated answers — Perplexity, ChatGPT Search, Google AI Overviews, Bing Copilot, and more.

> **GEO vs SEO:** Traditional SEO gets you on the list. GEO gets you in the answer.

## What It Does

Five modules that cover the full GEO workflow:

| Module | Input | Output |
|--------|-------|--------|
| **M1 AI Visibility Audit** | Brand name or URL | Citation rate across AI platforms |
| **M2 Citability Analysis** | Target URL | Structured score (0-100) + fix list |
| **M3 Competitor AI Presence** | Competitor URLs | Content gap + citation strategy |
| **M4 Content GEO Rewrite** | URL or article text | AI-optimized content + Schema code |
| **M5 Entity Building** | Brand name | Entity checklist + action plan |

## Quick Start

```
/geo-toolkit https://your-site.com
```

Auto-routing by input:

| What you say | What runs |
|-------------|-----------|
| Just a URL | M1 audit → M2 citability |
| Brand name or keyword | M1 audit → M3 competitor |
| "Content optimization" + URL | M2 → M4 rewrite |
| "Entity optimization" | M5 entity building |
| "Full GEO analysis" | M1 → M2 → M3 → M4 → M5 |

## Key Data (2026 Research)

- AI-referred sessions grew **527% year-over-year** in 2025
- **31.3%** of US population uses generative AI search
- Multi-platform content distribution increases AI citations by up to **325%**
- YouTube mentions are the **#1 strongest single external signal** for AI citation
- Pages with semantic completeness score 8.5/10+ are **4.2× more likely** to be cited
- Schema-marked content gets **73% higher** selection rate
- Pages loading under 0.4s are **3× more likely** to be cited by ChatGPT
- **40-60% of cited sources change month-to-month** — GEO requires ongoing monitoring

## How It Audits AI Visibility

Claude tests representative queries across platforms:

```
Brand queries:    "[Brand] review" / "[Brand] vs [Competitor]"
Category queries: "Best [product type]" / "[Industry] top tools"
Problem queries:  "How to [user pain point]"
```

Then records: cited (✓/✗), position in answer, source URL cited, sentiment (positive/neutral/negative).

## Citation Score Dimensions

M2 scores content across six dimensions (0-100 total):

| Dimension | Max Score | Key Factor |
|-----------|-----------|-----------|
| Semantic Completeness | 20 | 134-167 word self-contained answer units |
| Fact Density | 20 | Stats every 150-200 words with sources |
| Content Structure | 20 | Tables, lists, short paragraphs, page speed |
| E-E-A-T Signals | 20 | Author info, dates, authoritative citations |
| Schema Markup | 10 | FAQPage, Article, Organization, HowTo |
| Entity Clarity | 10 | Wikidata, sameAs, clear brand definition |

## Media Distribution Strategy

GEO depends on where your content appears, not just what's on your site.

### Overseas (English AI engines)

| Tier | Platforms |
|------|-----------|
| Must-have | YouTube, Reddit, Wikipedia/Wikidata, Forbes/TechCrunch, LinkedIn |
| High-value | G2, Product Hunt, Crunchbase, GitHub, Quora |

### China (Chinese AI engines: Ernie/Doubao/Kimi/Tongyi/DeepSeek)

| Tier | Platforms |
|------|-----------|
| Must-have | 百度百科, 知乎, B站, 36氪, 微信公众号 |
| High-value | 虎嗅, 少数派, CSDN/掘金, 企查查/天眼查 |

Full media landscape: [`references/media-landscape.md`](references/media-landscape.md)

## Schema Templates

M4 outputs ready-to-use JSON-LD code for:
- `FAQPage` — question-answer content
- `Article` + `BlogPosting` — editorial content with author signals
- `Organization` — brand entity foundation
- `HowTo` — tutorial/process content

Templates: [`references/content-patterns.md`](references/content-patterns.md)

## File Structure

```
geo-toolkit/
├── SKILL.md                         Main workflow definition (5 modules)
└── references/
    ├── citation-signals.md          6 AI citation signal dimensions + scoring
    ├── content-patterns.md          Schema templates + content rewrite patterns
    ├── media-landscape.md           Domestic vs. overseas media distribution map
    └── tools.md                     GEO tools (free & paid) + best practices
```

## Tools Referenced

| Tool | Purpose | Cost |
|------|---------|------|
| [Perplexity](https://www.perplexity.ai/) | Primary AI citation test | Free |
| [ChatGPT](https://chatgpt.com/) | ChatGPT Search citation test | Free |
| [Otterly.AI](https://otterly.ai/) | Multi-platform AI visibility tracking | Free tier |
| [Profound](https://www.profound.co/) | Enterprise AI monitoring (10+ engines) | Paid |
| [Google Rich Results Test](https://search.google.com/test/rich-results) | Schema validation | Free |
| [Wikidata](https://www.wikidata.org/) | Brand entity creation | Free |
| [HubSpot AEO Grader](https://www.hubspot.com/) | Quick brand evaluation | Free |

Full tool guide: [`references/tools.md`](references/tools.md)

## Installation

### For Claude Code
```bash
git clone https://github.com/jiaweifreshair/geo-toolkit ~/.claude/skills/geo-toolkit
```
Then use `/geo-toolkit` or ask Claude directly.

### For Codex
```bash
git clone https://github.com/jiaweifreshair/geo-toolkit ~/.codex/skills/geo-toolkit
```
Then ask Codex: "帮我用 geo-toolkit 分析品牌"

### For Gemini CLI
```bash
git clone https://github.com/jiaweifreshair/geo-toolkit ~/.agents/skills/geo-toolkit
```
Then ask Gemini: "请运行 geo-toolkit 分析品牌"

## License

MIT
