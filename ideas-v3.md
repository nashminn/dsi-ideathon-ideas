# DSI Ideathon 2026 — Alternative Ideas (v3)

---

## Idea 7 — Hiring Bias Audit Agent

**Tag:** Quick Build

**1. Problem being solved**
Unconscious bias seeps into hiring at every stage — gendered language in job descriptions, inconsistent scoring rubrics, patterns in who gets rejected at each round — yet most companies only audit this annually, manually, and superficially. Biased hiring is both an ethical failure and a talent pipeline problem that compounds over time.

**2. The AI agent concept**
An agent that continuously audits the hiring pipeline: it scans job descriptions for exclusionary or biased language and suggests neutral rewrites, analyzes interview feedback forms for inconsistency (same candidate rated differently by different interviewers with no justification), and tracks funnel drop-off patterns across demographic proxies (school tier, name origin, gap years) to surface statistically anomalous rejection rates. Monthly reports go to HR leadership with flagged decisions for review — not to override decisions, but to prompt reflection.

**3. Beneficiary audience**
HR directors, talent acquisition leads, and DEI officers at companies hiring more than ~50 people per year. Also relevant to recruiting agencies and staffing firms managing client pipelines.

**4. Why now**
ESG and DEI reporting requirements are tightening globally. ATS platforms (Greenhouse, Lever, Workday) now expose structured data via API. LLMs are strong at language bias detection. Companies are under increasing legal and reputational pressure to demonstrate fair hiring — and most have no systematic tooling for it.

**5. Feasibility scope**
ATS API integration → JD language analysis → interview feedback clustering → funnel drop-off analysis with demographic proxies → report generation. No proprietary data beyond what the company already holds. Quick Build for the JD audit and feedback consistency layers; the funnel analysis is more complex but additive.

---

## Idea 8 — Support Ticket Root Cause Clustering Agent

**Tag:** Quick Build

**1. Problem being solved**
Support teams drown in individual tickets while the underlying product bugs causing them go undetected for weeks. A product issue affecting 200 users generates 200 separate tickets — each handled one-by-one by a human — when a single engineering fix would have resolved all of them. The link between ticket volume and root cause is invisible without manual analysis nobody has time to do.

**2. The AI agent concept**
An agent that runs nightly over the support ticket queue, clusters semantically similar tickets that likely share a root cause, estimates how many customers are affected, ranks clusters by impact, and auto-creates a single engineering bug ticket with a synthesized description, affected user count, and representative verbatims. It also drafts a templated bulk response for support agents to send to all affected users once the fix is shipped. The loop closes: ticket → cluster → bug → fix → bulk reply.

**3. Beneficiary audience**
Support leads and product managers at SaaS companies and digital platforms with high ticket volume. Particularly valuable for startups where support and engineering share bandwidth and triage is informal.

**4. Why now**
Embedding-based clustering of support text is now fast and cheap. LLMs can synthesize a coherent bug report from 50 fragmented user complaints. No mainstream helpdesk tool (Zendesk, Intercom, Freshdesk) has shipped this as a native feature — they surface keywords and tags but not semantic root cause clusters.

**5. Feasibility scope**
Nightly batch pull from helpdesk API → embedding + clustering → LLM synthesis of cluster summary → Jira/Linear bug creation + draft bulk reply. Entirely achievable with existing APIs. The main design challenge is tuning cluster granularity to avoid over-splitting or over-merging.

---

## Idea 9 — R&D Literature Monitoring Agent

**Tag:** Big Bet

**1. Problem being solved**
Researchers and product teams at tech, pharma, materials, and agri-science companies need to track relevant academic papers and patent filings continuously — but the volume of publications is overwhelming. Relevant breakthroughs get missed, competitive patents go unnoticed, and teams waste time doing manual literature reviews that could have been automated. Missing a prior art citation or a competitor's patent filing can cost millions.

**2. The AI agent concept**
An agent that accepts a company's research focus areas as a structured brief (domains, keywords, competitor names, technology terms), then monitors arXiv, PubMed, Google Scholar, and patent databases (USPTO, EPO) on a weekly cadence. It filters for relevance, scores papers by likely impact on the company's work, summarizes key findings in plain language, flags potential prior art conflicts, and delivers a curated digest to the relevant team — with direct links, author details, and a "why this matters to you" explanation generated per paper.

**3. Beneficiary audience**
R&D leads, IP counsel, and product strategists at companies in pharma, biotech, materials science, AI/ML, semiconductors, and agri-tech. Also useful to university technology transfer offices and venture capital firms doing technical due diligence.

**4. Why now**
arXiv alone publishes 20,000+ papers per month. LLMs can now do domain-aware relevance filtering and plain-language summarization at a quality that rivals a junior research analyst. Patent database APIs are publicly accessible. The combination — automated ingestion + LLM relevance scoring + synthesis — is newly practical and no affordable tool does it with agent-level customization.

**5. Feasibility scope**
Feed ingestion from arXiv/PubMed/patent APIs → embedding-based relevance filter against company brief → LLM summary + impact scoring → digest delivery via email or Slack. The ingestion and filtering pipeline is straightforward. The hard part is the relevance brief — getting domain specificity right without over-filtering. Big Bet due to breadth of data sources and need for high precision in regulated industries.
