# DSI Ideathon 2026 — Alternative Ideas (v2)

Note: Pick the best 3 across this file and ideas.md — max 3 submissions per person.

---

## Idea 4 — Internal Knowledge Decay Agent

**Tag:** Quick Build

**1. Problem being solved**
Company wikis and internal docs rot silently. A process doc written 18 months ago may reference a deprecated tool, a team that was restructured, or a workflow that no longer exists — and nobody knows until something breaks. Teams waste hours following stale runbooks or rediscovering tribal knowledge that was once written down.

**2. The AI agent concept**
An agent that cross-references internal documentation (Confluence, Notion, Google Drive) against signals of change — merged PRs, org chart updates, tool migrations, Slack announcements — and flags docs likely to be stale. It scores each doc by decay risk, generates a diff of what probably changed, drafts an updated version for human review, and routes it to the last editor for confirmation. Runs on a monthly cadence.

**3. Beneficiary audience**
Engineering and operations teams at companies with more than ~20 people. Particularly valuable for fast-growing startups, remote teams, and regulated environments where outdated SOPs are a compliance risk.

**4. Why now**
LLMs can now do semantic comparison between a doc and a set of change signals — something rule-based systems couldn't. Companies have accumulated years of wiki content that nobody has budget to manually audit. The cost of stale knowledge is invisible until it causes an incident.

**5. Feasibility scope**
Pull docs via Confluence/Notion API → pull change signals from GitHub, HRIS, and Slack → LLM cross-reference and decay scoring → draft update + route to owner. Achievable with existing APIs and no fine-tuning. Main challenge is calibrating false positive rate on the decay signal.

---

## Idea 5 — Supply Chain Disruption Early Warning Agent

**Tag:** Big Bet

**1. Problem being solved**
Procurement and operations teams at manufacturing, retail, and logistics companies react to supply chain disruptions after they happen — a port closure, a supplier factory fire, a trade policy change — instead of anticipating them days or weeks ahead. This reactive posture leads to costly emergency sourcing, production halts, and broken SLAs.

**2. The AI agent concept**
An agent that continuously monitors a configurable set of signals — news feeds, port status APIs, weather events, geopolitical risk databases, and commodity price feeds — and maps disruptions to a company's specific supplier graph. When a risk event is detected upstream of a critical supplier, it fires an alert with: severity score, affected SKUs/components, estimated lead time impact, and a shortlist of pre-vetted alternative suppliers to consider. Delivered as a daily digest or real-time Slack alert.

**3. Beneficiary audience**
Procurement managers, supply chain analysts, and COOs at mid-to-large manufacturers, importers, electronics firms, and retailers with multi-tier supplier dependencies. Also valuable to 3PL and logistics firms managing client supply chains.

**4. Why now**
Post-pandemic supply chain fragility is now a boardroom-level concern. Public signal sources (shipping APIs, news, weather, trade databases) are accessible and rich. LLMs can now do supplier-graph-aware risk mapping from unstructured news — a task that previously required expensive analyst teams or specialized enterprise software costing six figures annually.

**5. Feasibility scope**
Signal ingestion pipeline → supplier graph stored as structured data → LLM-based relevance mapping (does this event affect my suppliers?) → alert generation. The signal sourcing and graph maintenance are the hard parts. A scoped MVP for one industry vertical (e.g., garment manufacturing) is achievable. Full multi-industry coverage is a Big Bet.

---

## Idea 6 — Burnout Early Warning Agent

**Tag:** Quick Build

**1. Problem being solved**
Employee burnout costs organizations billions annually in turnover, sick leave, and productivity loss — yet managers typically only notice it after it has already peaked. The signals are there in the data (calendar density, after-hours activity, response latency, meeting-to-focus ratio) but no one is watching them systematically.

**2. The AI agent concept**
An agent that analyzes anonymized, consent-gated work pattern signals — calendar load, after-hours email/Slack activity, PR commit times, ticket throughput trends — to compute a per-employee burnout risk score over a rolling 4-week window. When a score crosses a threshold, it sends a private nudge to the employee ("your focus time has dropped 40% this month — here are some calendar suggestions") and a separate, anonymized alert to their manager suggesting a check-in. No message content is read — only metadata.

**3. Beneficiary audience**
HR teams, engineering managers, and people ops leads at companies with 50+ employees. Especially relevant to remote-first companies where passive signals (body language, visible exhaustion) are invisible to managers.

**4. Why now**
Workplace burnout is at a documented high post-pandemic. Calendar and productivity APIs (Google Workspace, Microsoft 365) now expose the metadata needed. Employees are increasingly open to employer wellness tooling if privacy is handled correctly. No mainstream HR platform has shipped this as a proactive agent — only retroactive surveys.

**5. Feasibility scope**
Metadata ingestion via Google/M365 APIs (no message content) → signal feature extraction → LLM-assisted pattern interpretation → tiered alert generation. Privacy architecture (consent flow, anonymization layer) is the critical design challenge, not the ML. A Quick Build for one platform (e.g., Google Workspace only) is realistic within weeks.
