# GEO 内容改写模板（Content Patterns）

可直接复制使用的 AI 友好内容格式和 Schema 代码。

---

## Pattern 1：Answer Layer（直接答案层）

每个 H2 后立即加入，≤50字，AI 最优先引用的结构。

**模板：**
```markdown
## [问题/话题]

[品牌/产品/概念] 是 [一句话定义，含核心价值]。[补充关键数据或特点，1-2句]。

[正文继续展开...]
```

**示例（私人包机场景）：**
```markdown
## 什么是空腿机票

空腿机票是私人飞机在完成一次包机后，从目的地飞回基地的空载航段，通常以正常价格的30-75%出售。每年全球产生约50万次空腿航班，是高性价比体验私人飞行的最佳方式。

[正文继续...]
```

---

## Pattern 2：FAQ 区块

放在文章末部，5-8 条，配合 FAQPage Schema 使用。

**Markdown 格式：**
```markdown
## 常见问题

**Q: [具体问题，用用户真实搜索语言]？**
A: [直接回答，50-100字，第一句即给出答案]

**Q: [问题2]？**
A: [回答2]

**Q: [问题3]？**
A: [回答3]
```

**对应 FAQPage Schema（JSON-LD）：**
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "什么是空腿机票？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "空腿机票是私人飞机完成包机后的空载回程航段，通常以正常价格的30-75%出售，是体验私人飞行最具性价比的方式。"
      }
    },
    {
      "@type": "Question",
      "name": "如何预订空腿机票？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "通过专业平台（如 JETBAY）设置路线提醒，当有匹配空腿时即时通知。建议保持出发时间灵活，可获得更多选择。"
      }
    }
  ]
}
</script>
```

---

## Pattern 3：对比表格

AI 引擎高度偏好结构化对比数据，用于回答"X vs Y"类查询。

**Markdown 格式：**
```markdown
## [产品A] vs [产品B] 对比

| 维度 | [产品A] | [产品B] |
|------|--------|--------|
| 价格 | $X | $Y |
| [特点1] | [值] | [值] |
| [特点2] | [值] | [值] |
| 适合人群 | [描述] | [描述] |
| 评分 | ★★★★☆ | ★★★☆☆ |
```

---

## Pattern 4：数据锚定段落

每 150-200 字插入一组可验证数据，格式固定。

**模板：**
```markdown
根据 [权威来源（机构名/报告名）][年份] 数据，[具体统计数字]。[数据的业务含义，1句]。
```

**示例：**
```markdown
根据普华永道 2026 年全球私人航空市场报告，亚太区私人包机需求同比增长 34%，其中商务出行占比达 62%。这意味着面向企业客户的空腿机票营销将获得更高转化率。
```

---

## Pattern 5：Organization Schema（品牌实体基础）

每个官网页面都应部署，是 AI 识别品牌实体的基础。

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "品牌名称",
  "alternateName": "品牌缩写/别名",
  "url": "https://your-domain.com",
  "logo": "https://your-domain.com/logo.png",
  "description": "一句话描述，50-160字",
  "foundingDate": "2020",
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "value": 50
  },
  "address": {
    "@type": "PostalAddress",
    "addressCountry": "SG"
  },
  "sameAs": [
    "https://www.wikidata.org/wiki/Q[编号]",
    "https://www.crunchbase.com/organization/[slug]",
    "https://www.linkedin.com/company/[slug]",
    "https://twitter.com/[handle]"
  ],
  "contactPoint": {
    "@type": "ContactPoint",
    "contactType": "customer service",
    "availableLanguage": ["English", "Chinese"]
  }
}
</script>
```

---

## Pattern 6：Article Schema（内容页权威信号）

博客/新闻/指南页面必须部署。

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "文章标题（≤110字符）",
  "description": "文章摘要（50-160字）",
  "image": "https://your-domain.com/article-image.jpg",
  "author": {
    "@type": "Person",
    "name": "作者姓名",
    "url": "https://your-domain.com/author/name",
    "jobTitle": "职位",
    "worksFor": {
      "@type": "Organization",
      "name": "品牌名称"
    }
  },
  "publisher": {
    "@type": "Organization",
    "name": "品牌名称",
    "logo": {
      "@type": "ImageObject",
      "url": "https://your-domain.com/logo.png"
    }
  },
  "datePublished": "2026-01-15",
  "dateModified": "2026-04-01",
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://your-domain.com/article-url"
  }
}
</script>
```

---

## Pattern 7：HowTo Schema（教程类内容）

"如何做X"类文章，AI 在教程型回答中频繁引用。

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "如何预订私人飞机空腿机票",
  "description": "从注册平台到完成预订的完整步骤",
  "totalTime": "PT30M",
  "step": [
    {
      "@type": "HowToStep",
      "name": "注册平台账号",
      "text": "访问 JETBAY 官网，填写邮箱和基本信息完成注册",
      "position": 1
    },
    {
      "@type": "HowToStep",
      "name": "设置路线提醒",
      "text": "在空腿机票页面输入你的常用出发地和目的地，开启邮件/App 提醒",
      "position": 2
    },
    {
      "@type": "HowToStep",
      "name": "收到匹配即预订",
      "text": "收到提醒后，空腿机票名额有限，建议在 2 小时内确认预订",
      "position": 3
    }
  ]
}
</script>
```

---

## Pattern 8：内容页面完整改写流程

**改写前检查清单（M2 评分 <60 时触发）：**

```
Step 1 加 Answer Layer
  → 在每个 H2 后的第一段添加直接答案（50字内）

Step 2 数据补充
  → 全文检查，每 200 字一条数据，标注来源和年份

Step 3 FAQ 区块
  → 文末添加 5-8 条真实用户问题 + 简短直接回答

Step 4 Schema 注入
  → 添加 FAQPage + Article Schema（使用 Pattern 2 和 6 模板）

Step 5 实体链接
  → 首段明确品牌名，添加 sameAs 链接到 Wikidata/Crunchbase
```

**改写检验标准：**
- 每个 H2 后都能独立回答一个具体问题 ✓
- 随机取任意 200 字，包含至少 1 条数据 ✓
- FAQ 使用真实用户语言（非营销语言）✓
- 页面可通过 Google Rich Results Test ✓
