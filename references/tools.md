# GEO 工具指南

免费工具优先，按使用场景分类。

---

## AI 可见性监测

| 工具 | 地址 | 用途 | 费用 |
|------|------|------|------|
| **Perplexity** | https://www.perplexity.ai/ | 测试品牌在 Perplexity 的引用情况，最直观的 AI 搜索测试入口 | 免费 |
| **ChatGPT** | https://chatgpt.com/ | 测试 ChatGPT Search 是否引用你的品牌和内容 | 免费 |
| **Otterly.AI** | https://otterly.ai/ | 多平台 AI 可见性追踪（Perplexity/ChatGPT/Gemini），可设置品牌词监控 | 免费 tier |
| **Profound** | https://www.profound.co/ | 企业级 AI 监控，覆盖 10+ AI 引擎，支持批量关键词和竞品对比 | 付费 |
| **Brandwatch AI** | https://www.brandwatch.com/ | 社交 + AI 引用综合监控 | 付费 |

**使用建议：**
- 个人/初创：Perplexity + ChatGPT 手动测试（M1 模块）
- 成长期品牌：Otterly.AI 设置自动监控
- 企业级：Profound 批量覆盖主要 AI 引擎

---

## Schema 验证

| 工具 | 地址 | 用途 | 费用 |
|------|------|------|------|
| **Google Rich Results Test** | https://search.google.com/test/rich-results | 验证 FAQPage、Article、HowTo、Organization Schema 是否正确 | 免费 |
| **Schema.org Validator** | https://validator.schema.org/ | 更宽松的 Schema 验证，支持 JSON-LD/Microdata/RDFa | 免费 |
| **JSON-LD Playground** | https://json-ld.org/playground/ | 在线调试 JSON-LD 结构，实时预览解析结果 | 免费 |

**使用建议：**
- 每次添加或修改 Schema 后，必须用 Google Rich Results Test 验证
- JSON-LD Playground 用于快速调试结构，不用上线就能看结果

---

## 实体建设

| 工具 | 地址 | 用途 | 费用 |
|------|------|------|------|
| **Wikidata** | https://www.wikidata.org/ | 创建品牌实体词条，AI 引擎直接读取结构化实体数据 | 免费 |
| **Wikipedia** | https://en.wikipedia.org/ | 英文百科词条（需达到"可关注度"标准才能创建） | 免费 |
| **百度百科** | https://baike.baidu.com/ | 中文 AI 引擎核心知识库，可自行提交申请 | 免费 |
| **Crunchbase** | https://www.crunchbase.com/ | 公司档案，AI 引擎常引用为品牌事实来源 | 免费基础版 |
| **Google Knowledge Panel** | https://business.google.com/ | 触发 Google 知识面板，提升品牌实体识别 | 免费 |

**使用建议：**
- 优先级：Wikidata（可自建）> Crunchbase（填完整）> Wikipedia（有门槛）
- Wikidata 词条创建后，在官网 Organization Schema 的 `sameAs` 字段中引用对应 Q 编号

---

## 内容可引用性分析

| 工具 | 地址 | 用途 | 费用 |
|------|------|------|------|
| **HubSpot AEO Grader** | https://www.hubspot.com/marketing/ai-search-grader | 快速评估品牌 AI 搜索可见度，输出改进建议 | 免费 |
| **Screaming Frog** | https://www.screamingfrog.co.uk/seo-spider/ | 批量检查页面 Schema、H 结构、内容密度 | 免费 500 URL |
| **PageSpeed Insights** | https://pagespeed.web.dev/ | 检查页面加载速度（<0.4s 被 ChatGPT 引用概率 3×）| 免费 |

---

## 关键词与内容挖掘

| 工具 | 地址 | 用途 | 费用 |
|------|------|------|------|
| **AnswerThePublic** | https://answerthepublic.com/ | 挖掘用户真实问题语言，用于 FAQ 区块选题 | 免费额度 |
| **AlsoAsked** | https://alsoasked.com/ | Google "People Also Ask" 问题聚合，发现长尾问答机会 | 免费 3 次/天 |
| **Perplexity Discover** | https://www.perplexity.ai/discover | 直接观察 AI 常回答哪些话题，反向推导选题方向 | 免费 |

---

## 使用优先级（按阶段）

### 第一阶段：摸底（M1 + M5）
1. 手动在 [Perplexity](https://www.perplexity.ai/) 和 [ChatGPT](https://chatgpt.com/) 测试品牌词查询
2. 检查 [Wikidata](https://www.wikidata.org/) 和 [Crunchbase](https://www.crunchbase.com/) 是否有品牌词条
3. 用 [Google Rich Results Test](https://search.google.com/test/rich-results) 检查官网 Schema

### 第二阶段：内容优化（M2 + M4）
1. 用 [PageSpeed Insights](https://pagespeed.web.dev/) 检查页面速度
2. 用 [AnswerThePublic](https://answerthepublic.com/) 找 FAQ 素材
3. 添加 Schema 后用 [Google Rich Results Test](https://search.google.com/test/rich-results) 验证

### 第三阶段：持续监控（M1 循环）
1. 用 [Otterly.AI](https://otterly.ai/) 设置品牌词自动监控
2. 每月用 Perplexity/ChatGPT 手动抽查核心查询
3. 关注 AI 引用来源变化（40-60% 月度变动率为正常）
