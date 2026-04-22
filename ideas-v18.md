# DSI Ideathon 2026 — Ideas (v18) — Internal DSI Tools + Non-Chatbot Platform Ideas

Ideas #51–#57 are internal DSI tools (DSI is the user, not the seller). Ideas #58–#60 are new platform ideas that are explicitly not chatbot products.

---

## Idea 51

**Title**
Bench-to-Bill Agent — Engineer Allocation Intelligence

**The Problem**
In service companies, engineers on the bench (unallocated) cost money every day. Matching them manually to leads, gaps, and training tracks is slow and often wrong.

**The Product Idea**
An AI agent that tracks bench capacity and matches available engineers to incoming leads, internal POCs, urgent client gaps, training tracks, and cross-sell opportunities. Predicts who can become billable fastest and suggests allocation actions.

**Who Benefits**
DSI delivery and resource management teams internally. If productised: other IT service firms and staffing companies.

**Why it Wins**
Direct revenue impact + utilisation improvement. "Reduce idle talent and turn capacity into revenue."

**Tag:** Internal DSI Tool

---

## Idea 52

**Title**
Proposal Intelligence Agent

**The Problem**
Winning international clients requires fast, customised proposals. RFP response quality is inconsistent and manual assembly is slow.

**The Product Idea**
An agent that reads RFPs and client inquiries and auto-generates tailored proposals, relevant case studies, team composition suggestions, timeline estimates, risk notes, and pricing drafts.

**Who Benefits**
DSI BD team internally. If productised: any IT services company or consultancy.

**Why it Wins**
Revenue growth engine. Faster, higher-quality proposals improve win rates.

**Tag:** Internal DSI Tool

---

## Idea 53

**Title**
Delivery Rescue Agent

**The Problem**
Projects look green until suddenly they fail. Warning signs exist but nobody is synthesising them.

**The Product Idea**
An agent that monitors Jira, commits, QA bugs, missed standups, blockers, and scope creep, then predicts project distress early and suggests rescue actions.

**Who Benefits**
DSI delivery managers internally. If productised: software delivery firms and IT departments.

**Why it Wins**
Protects reputation and margins.

**Caveat:** Competitive space — LinearB, Jellyfish exist internationally. BD local context and integration with DSI-specific workflows are the differentiator.

**Tag:** Internal DSI Tool

---

## Idea 54

**Title**
Knowledge Clone Agent

**The Problem**
Senior architects and managers become bottlenecks. Junior teams can't access their reasoning without scheduling time.

**The Product Idea**
An agent that learns from senior experts' decisions, docs, reviews, and patterns and becomes a searchable internal advisor for junior teams.

**Who Benefits**
DSI engineering and delivery teams internally.

**Why it Wins**
Scales expertise without adding headcount.

**Caveat:** Knowledge capture is notoriously hard to demonstrate and adoption is slow. Requires significant internal data curation investment before it becomes useful.

**Tag:** Internal DSI Tool

---

## Idea 55

**Title**
Client Expansion Agent

**The Problem**
Existing clients often have more needs but opportunities are missed because account managers are focused on delivery, not upsell.

**The Product Idea**
An agent that analyses current projects, client industries, and pain points and identifies upsell opportunities — mobile app, DevOps support, AI modernisation, cloud migration, QA automation.

**Who Benefits**
DSI account managers and BD team internally.

**Why it Wins**
Cheaper to grow existing accounts than acquire new ones.

**Tag:** Internal DSI Tool

---

## Idea 56

**Title**
Trust Score Agent for Outsourcing Clients

**The Problem**
International clients worry about offshore delivery reliability. DSI's sales team has no live transparency tool to share during deal negotiations.

**The Product Idea**
Creates live transparency dashboards using delivery metrics, quality trends, response speed, sprint health, and release confidence — shareable with international clients in real time.

**Who Benefits**
DSI BD and client success teams internally. The dashboard is shown to DSI's international clients.

**Why it Wins**
Competitive differentiator for DSI sales. Trust is the core blocker in offshore deals.

**Tag:** Internal DSI Tool

---

## Idea 57

**Title**
Talent Growth Navigator Agent

**The Problem**
Engineers stagnate or train randomly. Company pipeline needs and individual career development are never connected.

**The Product Idea**
Builds personalised growth plans based on market demand and company pipeline. Example: "Need more FastAPI engineers in 3 months — train these 12 people now."

**Who Benefits**
DSI HR and engineering leads internally. If productised: other IT companies and HR platforms.

**Why it Wins**
Future-ready workforce planning.

**Tag:** Internal DSI Tool

---

## Idea 58

**Title**
RegulatoryRadar — Autonomous Regulatory Change Intelligence Platform

**The Problem**
Every regulated institution in Bangladesh — banks, NBFIs, MFIs, insurance companies, factories, hospitals, telecom operators — must comply with regulations from a dozen bodies: Bangladesh Bank, IDRA, MRA, DIFE, DGDA, BTRC, BSEC, and others. These bodies issue circulars, gazette notifications, and policy updates continuously.

Currently, compliance officers manually visit each regulatory body's website or rely on professional networks to catch updates. This is unreliable. Missing a Bangladesh Bank circular on loan classification or a DIFE update on working-hour rules carries direct penalties — fines, license suspension, audit findings. The problem is not that regulations change; it is that no institution has a reliable, automated way to know when they change and what specifically has changed for their operations.

A bank with 40 branches, an insurance company, and a 500-worker factory each have different subsets of regulations that apply to them. A generic news feed is useless — they need changes mapped to their specific operational context.

**The Product Idea**
A SaaS platform that operates fully autonomously. There is no chatbot and no user conversation required. The platform:

1. **Monitors** all relevant regulatory body websites, official gazette portals, and Bangladesh Government notification feeds on a daily automated basis.
2. **Classifies** each update by regulatory body, sector applicability (banking, insurance, manufacturing, healthcare, telecom), and effective date — using LLM to read and extract structured meaning from unstructured PDF circulars and gazette text.
3. **Maps** each change to the client's specific operational profile (sector, size, licence type, active product lines) and generates an impact assessment: is this update applicable to this client? If yes, what specifically must change?
4. **Auto-generates** a compliance task for each applicable change: what action is required, by which team, by which deadline. These tasks are pushed to the client's dashboard and optionally to email or internal ticketing systems.

The client logs in to a structured dashboard that shows: new regulations this week, open compliance tasks, upcoming regulatory deadlines, and a searchable archive of all past updates. No manual monitoring required.

**Who Benefits**
Primary buyers are compliance and legal heads at regulated institutions. Bangladesh has 61 scheduled banks, 35 non-bank financial institutions, 750+ insurance companies and intermediaries, 80,000+ DIFE-registered factories, and growing private hospital networks — all of which face regulatory monitoring as a standing operational cost.

The enterprise sale is straightforward: one compliance head approves the subscription and the entire institution uses the dashboard. No fragmented end-user onboarding. Subscription pricing by institution type — smaller MFIs at BDT 5,000–10,000/month, banks and insurance companies at BDT 30,000–80,000/month. At 200 institutional clients across verticals: BDT 6–12M/month.

**Why Now**
Bangladesh Bank has been accelerating its digital compliance push since 2023. IDRA reformed its reporting framework in 2024. DIFE enforcement is intensifying under ILO-linked pressure from international apparel buyers. The volume and pace of regulatory change is increasing, making the manual monitoring model increasingly untenable. No Bangladesh-focused regulatory intelligence platform exists — this is a gap in the market that has not been filled precisely because building it requires LLM capability that did not exist at production cost two years ago.

**Feasibility & Scope**
Core pipeline: web crawler per regulatory body → LLM document classification and extraction → client profile matching → task generation → dashboard display.

This is not a chatbot and requires no conversational interface. The AI runs in the background; the user sees a structured dashboard. POC: Bangladesh Bank circulars only, one bank as pilot client, three weeks to build. Full vertical coverage adds 2–3 months of knowledge base and crawler configuration.

Biggest unknown: regulatory body website reliability — some use PDF portals, some gazette links break. Addressed by: redundant monitoring (official site + gazette + professional legal publisher feeds) and a human-in-the-loop flag when a known update is not automatically parsed.

**Dishonesty Filter**
Not applicable — all data comes from official government sources. No user is providing self-reported information that could be gamed.

**Tag:** Platform / Non-Chatbot | Recurring SaaS | Multi-vertical

---

## Idea 59

**Title**
TenderScope — AI Procurement Intelligence Platform for BD Government Tenders

**The Problem**
Bangladesh's government procurement runs through e-GP (Electronic Government Procurement), IMED, and dozens of sector-specific procurement portals. Thousands of tenders are published monthly across infrastructure, IT, health, education, and services.

Companies — IT firms, engineering consultancies, NGOs, construction companies — spend substantial manual effort scanning these portals daily to find relevant tenders. Most miss tenders they were qualified to win simply because they did not see them in time. When they do find a tender, they have no systematic way to assess their win probability against past award patterns, or to understand which technical and compliance requirements they need to address.

The opportunity cost is significant: a mid-size IT company submitting 40 bids per year might win 8. A better signal on which 40 to choose and how to position each bid translates directly to revenue.

DSI itself participates in government and institutional tenders — this is not a hypothetical buyer problem, it is an internal problem DSI already experiences.

**The Product Idea**
A web-based platform that operates as an intelligence layer over Bangladesh's procurement landscape. No conversational interface — the product is a structured dashboard and automated alerting system:

1. **Aggregation**: Monitors e-GP, IMED, sector portals, and UN/development bank procurement notices daily. All tenders in one place, updated automatically.
2. **Classification**: LLM reads each tender document and tags it by sector, scope, estimated value, eligibility requirements, and required certifications — so clients can filter by what they're actually qualified for rather than manually reading every notice.
3. **Relevance Scoring**: Each client sets a capability profile (sectors, past work, certifications, team sizes, geographic presence). The platform scores every incoming tender for relevance to that profile and surfaces only the high-signal ones.
4. **Historical Pattern Analysis**: For tenders in categories the client bids in, the platform shows historical award data — typical winning price bands, which firms have won previously, how many bids are typically submitted, what compliance documents were required. This replaces the guesswork in bid/no-bid decisions.
5. **Bid Checklist Generation**: LLM reads each tender document and auto-generates the submission checklist — documents required, format specifications, evaluation criteria weights — so bid teams spend time on substance, not document parsing.

Clients receive a daily digest email of new high-relevance tenders, and log in to the dashboard to track active bids and review historical data.

**Who Benefits**
Primary buyers: IT services companies (DSI included), engineering consultancies, development sector organisations (NGOs/INGOs), and large construction firms — all of which actively bid for public procurement.

The BD IT sector alone has 5,000+ registered companies. Development organisations (BRAC, CARE, Save the Children, RTI, Chemonics) submit dozens of bids per year for USAID, World Bank, and ADB-funded tenders. At BDT 10,000–25,000/month per company, 500 clients generates BDT 5–12.5M/month.

DSI's internal use creates an immediate pilot and live testimonial — the most credible sales asset possible.

**Why Now**
e-GP has been mandatory for most government procurement since 2018 and the volume of tenders is growing. The development sector is expanding as Bangladesh reaches LDC graduation and aid modalities shift. No local company offers this intelligence layer — the market reads tenders by hand. LLM-based tender document parsing is now cost-effective enough to run at scale.

**Feasibility & Scope**
e-GP has a structured portal — scraping is straightforward. IMED and sector portals vary. POC: e-GP IT-category tenders only, DSI as internal pilot, two weeks to build. Full coverage of development sector tenders and historical award data adds 6–8 weeks.

Biggest unknown: historical award data availability. e-GP publishes award notices but the data is not uniformly structured. Addressed by: building the award history database incrementally as new awards are published, with manual entry for key historical data in high-value categories.

**Dishonesty Filter**
Not applicable — all data comes from public procurement portals. Client capability profiles are self-reported but gaming them only harms the client (irrelevant tender alerts).

**Tag:** Platform / Non-Chatbot | Recurring SaaS | DSI Internal + External

---

## Idea 60

**Title**
ContractLens — AI Contract Risk Analysis Platform

**The Problem**
Every institution that signs contracts — banks, NBFIs, corporations, NGOs, factories — does so at significant legal and financial risk. Contract review is slow, expensive, and inconsistent. Large institutions can afford in-house legal teams; mid-size companies pay law firms by the hour; small companies sign contracts they do not fully understand.

The specific risks that matter most are also the ones most often buried in legal language: automatic renewal clauses, penalty and liability caps, jurisdiction terms that shift legal recourse to unfavourable courts, IP ownership clauses in vendor agreements, force majeure definitions that exclude the risks most relevant to Bangladesh (flooding, political unrest, power outages), and non-compete restrictions on key personnel.

Current practice: a procurement officer reads a 40-page vendor agreement, misses clause 31.4, and the company later discovers it waived its right to dispute resolution under Bangladesh law. Or a service agreement auto-renews at a 20% price increase because nobody was tracking the renewal window. These are not rare events — they are the standard consequence of underpowered contract review.

**The Product Idea**
A document analysis platform with no conversational interface. The workflow is: upload contract → AI analyses it → receive structured risk report. Specifically:

1. **Clause Extraction**: LLM reads the contract and identifies all materially significant clauses — payment terms, liability limits, IP ownership, termination rights, auto-renewal, jurisdiction, penalty clauses, data ownership (critical for tech vendor contracts), and non-compete.
2. **Risk Flagging**: Each extracted clause is rated against a configurable risk framework (institution type × sector). A payment default clause that is standard for a manufacturing supplier agreement is a red flag in a software development contract. The platform understands the difference.
3. **Benchmark Comparison**: For common contract types (vendor agreements, employment contracts, lease agreements, service level agreements), the platform compares extracted terms against market-standard templates and flags deviations that are unfavourable to the client.
4. **Obligation Calendar**: Extracts all time-sensitive obligations — payment milestones, renewal decision windows, reporting deadlines, audit rights windows — and generates a calendar that can be exported to the client's systems. Renewal deadlines never get missed.
5. **Summary Report**: Generates a plain-language executive summary of the contract's key terms and risk profile — readable by a procurement officer without a law degree.

The output is a structured PDF report and a dashboard entry. No legal advice is given — the platform surfaces information and flags risk; the client's legal or procurement team makes decisions.

**Who Benefits**
Primary buyers: legal and procurement heads at mid-to-large institutions — banks, NBFIs, insurance companies, large corporations, development organisations, and factory groups. 

NGOs and development sector organisations sign dozens of grant agreements, sub-grant contracts, and vendor agreements annually with international funders — these contracts are in English, complex, and unfavourable boilerplate from donors is common. Development sector buyers have both budget and acute pain.

Banks and NBFIs sign large vendor agreements (core banking, insurance tech, HR systems) and loan agreements that carry significant liability. At BDT 15,000–50,000/month per institution, or per-contract pricing at BDT 2,000–8,000 per analysis, the revenue model is flexible. 300 institutional clients on subscription: BDT 4.5–15M/month.

**Why Now**
The volume of digital transformation contracts being signed by Bangladeshi institutions — cloud services, fintech integrations, ERP systems — has surged since 2022 and the contracts are increasingly complex international agreements. At the same time, in-house legal capacity has not scaled proportionally. The gap between contract complexity and review capacity is widening. No local AI contract analysis tool exists in the Bangladesh market.

**Feasibility & Scope**
Core pipeline: document ingestion (PDF/Word) → LLM clause extraction → risk classification → benchmark comparison → report generation. No real-time data required, no API integrations with third parties, no user conversation flow.

POC: vendor agreement analysis for IT services contracts, targeting DSI's own procurement team as internal pilot, three weeks. Extension to loan agreements and grant contracts adds 4–6 weeks of template and risk framework configuration.

Biggest unknown: LLM accuracy on Bangla-language contracts. Addressed by: scoping the initial product to English-language contracts (the highest-value segment) and adding Bangla support in v2 after validating the core pipeline.

**Dishonesty Filter**
The contract document is the object of analysis — it cannot be gamed by the user. A client who uploads a different contract than the one they will sign harms only themselves.

**Tag:** Platform / Non-Chatbot | Document Intelligence | Recurring SaaS

---

*Pool total: 60 ideas*
