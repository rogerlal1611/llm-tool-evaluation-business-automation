# LLM Tool Evaluation: Business Automation Use Cases

**Author:** Roger Lal  
**Date:** June 2025  
**Purpose:** Comparative evaluation of leading large language models (ChatGPT, Claude, Gemini) across three business automation scenarios relevant to wholesale distribution and supply chain operations. Findings are intended to support responsible AI adoption decisions for non-technical business leadership.

---

## Executive Summary

This report evaluates three frontier AI platforms — **OpenAI ChatGPT (GPT-4o)**, **Anthropic Claude (Sonnet 3.7)**, and **Google Gemini (1.5 Pro)** — across three real-world business automation tasks: drafting supplier RFQ emails, summarising product specification documents, and generating inventory reorder reports from structured data.

**Recommendation:** Claude performs most consistently across all three tasks for business writing and document summarisation. ChatGPT offers the strongest ecosystem for workflow integration via plugins and API tooling. Gemini excels when tasks involve large-volume document processing or integration with Google Workspace. For a wholesale distribution business beginning its AI adoption journey, a **Claude + ChatGPT hybrid approach** is recommended — Claude for internal communication drafting and document analysis, ChatGPT for API-driven workflow automation.

---

## Evaluation Methodology

Each model was given identical prompts across three task categories. Outputs were scored on a 1–5 scale across four dimensions:

| Dimension | Description |
|---|---|
| **Accuracy** | Factual correctness and relevance of output |
| **Format quality** | Structure, readability, and professional tone |
| **Instruction following** | How precisely the model followed the prompt |
| **Business readiness** | Whether the output could be used as-is with minimal editing |

All prompts were run on free or standard-tier access (no system prompt customisation). Results represent out-of-the-box capability, reflecting real-world conditions for a business evaluating these tools without dedicated AI engineering support.

---

## Task 1: Drafting Supplier RFQ Emails

### Prompt Used

```
You are a procurement coordinator at a dental supply distribution company.
Draft a professional Request for Quotation (RFQ) email to a new supplier
for the following items: nitrile examination gloves (size M, box of 100),
disposable face masks (Type IIR), and dental mirror handles (stainless steel,
autoclavable). We need pricing for 500 units of each, delivery to our
warehouse in Markham, Ontario, within 30 days. Include a deadline for
response and a professional closing.
```

### Outputs Summary

**ChatGPT (GPT-4o)**  
Produced a well-structured email with accurate item descriptions and a clear response deadline. Included a subject line unprompted. Tone was slightly formal but business-appropriate. Required minor edits to personalise the company name and contact details.

**Claude (Sonnet 3.7)**  
Generated the most natural-sounding email with the strongest professional tone. Correctly inferred context (e.g. added a note about preferred payment terms and delivery confirmation), which a procurement coordinator would typically include. Output was closest to what a human expert would write with minimal editing needed.

**Gemini (1.5 Pro)**  
Output was accurate but more generic in tone. Less contextual inference than Claude. Did not include a subject line. Formatting was clean but required more editing to reach professional standard.

### Scores

| Model | Accuracy | Format | Instruction Following | Business Readiness | **Total /20** |
|---|---|---|---|---|---|
| ChatGPT (GPT-4o) | 4 | 4 | 5 | 4 | **17** |
| Claude (Sonnet 3.7) | 5 | 5 | 5 | 5 | **20** |
| Gemini (1.5 Pro) | 4 | 3 | 4 | 3 | **14** |

---

## Task 2: Product Specification Summarisation

### Prompt Used

```
Summarise the following product specification into a 3-bullet executive
summary suitable for a non-technical purchasing manager. Focus on:
1. What the product is and its primary use
2. Key compliance or safety certifications
3. Key technical limitations or compatibility notes

[Simulated product spec: Dental X-Ray Sensor — Digital intraoral sensor,
USB 2.0 and USB 3.0 compatible, CMOS imaging technology, 20 x 30mm active
area, 25 lp/mm resolution, CE marked, FDA 510(k) cleared, compatible with
most major practice management software via TWAIN driver, not compatible
with Mac OS versions below 12.0, 2-year warranty, $1,200 MSRP per unit.]
```

### Outputs Summary

**ChatGPT (GPT-4o)**  
Produced accurate, concise bullets. Correctly flagged the Mac OS compatibility issue as a risk. Slight tendency to over-explain technical terms even when asked for a non-technical audience.

**Claude (Sonnet 3.7)**  
Best balance of brevity and clarity. Translated technical specs into plain business language without losing critical information. Explicitly framed the compatibility caveat as an action item ("verify current OS version before purchasing"), which adds practical value for a purchasing manager.

**Gemini (1.5 Pro)**  
Accurate summarisation. Output was slightly longer than instructed (4 bullets instead of 3). Good handling of compliance certifications but did not flag the OS compatibility limitation prominently.

### Scores

| Model | Accuracy | Format | Instruction Following | Business Readiness | **Total /20** |
|---|---|---|---|---|---|
| ChatGPT (GPT-4o) | 5 | 4 | 4 | 4 | **17** |
| Claude (Sonnet 3.7) | 5 | 5 | 5 | 5 | **20** |
| Gemini (1.5 Pro) | 4 | 4 | 3 | 4 | **15** |

---

## Task 3: Inventory Reorder Report Generation

### Prompt Used

```
Based on the following inventory data, generate a reorder priority report
for a warehouse manager. Flag any item below its reorder threshold and
suggest an order quantity based on average weekly usage.

Item: Nitrile Gloves M | Stock: 120 units | Reorder threshold: 200 | Avg weekly usage: 80
Item: Face Masks Type IIR | Stock: 350 units | Reorder threshold: 150 | Avg weekly usage: 60
Item: Dental Mirrors | Stock: 45 units | Reorder threshold: 100 | Avg weekly usage: 30
Item: Sterilisation Pouches | Stock: 800 units | Reorder threshold: 500 | Avg weekly usage: 120
Item: Prophy Paste (mint) | Stock: 90 units | Reorder threshold: 120 | Avg weekly usage: 40

Format the output as a table with columns: Item, Status, Weeks of Stock Remaining, Recommended Order Quantity.
```

### Outputs Summary

**ChatGPT (GPT-4o)**  
Produced a correctly formatted table with accurate calculations. Correctly identified all three flagged items and calculated weeks of stock remaining. Recommended order quantities were reasonable (4-week coverage). No errors.

**Claude (Sonnet 3.7)**  
Matched ChatGPT on accuracy. Additionally added a brief plain-English paragraph above the table summarising the urgency tier (critical vs. low stock), which was not asked for but added genuine business value. Calculations were correct.

**Gemini (1.5 Pro)**  
Table format was accurate. One calculation error: Sterilisation Pouches listed as 6.67 weeks remaining rather than rounding to a clean figure. Also flagged Sterilisation Pouches as low stock despite it being above threshold — a reasoning error.

### Scores

| Model | Accuracy | Format | Instruction Following | Business Readiness | **Total /20** |
|---|---|---|---|---|---|
| ChatGPT (GPT-4o) | 5 | 5 | 5 | 5 | **20** |
| Claude (Sonnet 3.7) | 5 | 5 | 5 | 5 | **20** |
| Gemini (1.5 Pro) | 3 | 4 | 4 | 3 | **14** |

---

## Overall Scorecard

| Model | Task 1 /20 | Task 2 /20 | Task 3 /20 | **Total /60** | **Rank** |
|---|---|---|---|---|---|
| ChatGPT (GPT-4o) | 17 | 17 | 20 | **54** | 2nd |
| Claude (Sonnet 3.7) | 20 | 20 | 20 | **60** | 1st |
| Gemini (1.5 Pro) | 14 | 15 | 14 | **43** | 3rd |

---

## Platform Comparison: Key Differentiators

| Factor | ChatGPT | Claude | Gemini |
|---|---|---|---|
| Best for | Workflow integration, coding, API automation | Business writing, document analysis, nuanced instructions | Google Workspace integration, large document volumes |
| API access | ✅ Mature, widely supported | ✅ Available, strong rate limits | ✅ Available via Google Cloud |
| Context window | 128k tokens | 200k tokens | 1M tokens |
| Data privacy (free tier) | Data used for training by default | Data not used for training by default | Data used for training by default |
| Workflow automation tools | ChatGPT plugins, GPTs, Zapier integration | Claude for Work, API | Gemini for Workspace, AppSheet |
| Pricing (as of Jun 2025) | GPT-4o: ~$5 / 1M input tokens | Sonnet 3.7: ~$3 / 1M input tokens | 1.5 Pro: ~$3.50 / 1M input tokens |
| Ease of use (non-technical) | High | High | Medium |
| Responsible AI documentation | OpenAI Usage Policies | Anthropic Acceptable Use Policy | Google AI Principles |

---

## Risk & Compliance Considerations

All three platforms operate as cloud-based services, meaning business data submitted in prompts may be transmitted to and processed on third-party servers. Key considerations for responsible adoption:

- **Data sensitivity:** Do not submit personally identifiable information (PII), protected health information (PHI), confidential pricing agreements, or customer data to any of these platforms via the free or standard tiers without reviewing the provider's data processing terms.
- **Output verification:** LLM outputs should be treated as drafts, not authoritative sources. All generated emails, reports, and summaries must be reviewed by a qualified team member before external use.
- **Vendor lock-in:** Building workflows that depend entirely on a single LLM provider creates a dependency risk if pricing, availability, or terms change. A multi-model strategy (as recommended above) reduces this exposure.
- **Hallucination risk:** All three models are capable of generating plausible but incorrect information, particularly for numerical calculations and compliance claims. Task 3 demonstrated this with Gemini's calculation error. Human review of any data-driven outputs is essential.

---

## Recommendations for Phased AI Adoption

### Phase 1 — Immediate (0–30 days, no budget required)
- Pilot ChatGPT (free tier) or Claude (free tier) for internal email drafting and meeting summarisation
- Identify 2–3 repetitive documentation workflows suitable for AI assistance
- Establish a basic responsible use policy: what data is allowed in prompts

### Phase 2 — Proof of Concept (30–90 days, low cost)
- Subscribe to Claude Pro or ChatGPT Plus (~$20/month) for a pilot team
- Build 1–2 automation POCs using the API: e.g. auto-generating weekly inventory summary reports from exported CSV data
- Measure time saved vs. manual process

### Phase 3 — Scale (90+ days)
- Evaluate enterprise tiers for data privacy guarantees (Claude for Enterprise, ChatGPT Enterprise)
- Integrate chosen platform into existing workflow tools (ERP, inventory management, email)
- Train staff on prompt engineering basics to maximise output quality

---

## Conclusion

For a wholesale distribution business in the dental supply sector, **Claude is the strongest out-of-the-box choice** for business communication and document automation tasks. **ChatGPT** is the recommended platform for any workflow that requires API integration or automation pipeline development. **Gemini** is best reserved for organisations already embedded in the Google Workspace ecosystem.

The highest-ROI starting point is email drafting automation (Task 1), which requires no technical setup, delivers immediate time savings, and carries low risk when a human review step is maintained.

---

*This report was produced as part of an independent AI capability evaluation. All prompt outputs were generated in June 2025 using standard-access tiers of each platform. Scores reflect the author's assessment based on the defined rubric.*

*Roger Lal | AI/ML Engineering | roger.lal1611@gmail.com | [linkedin.com/in/rogerlal16](https://linkedin.com/in/rogerlal16)*
