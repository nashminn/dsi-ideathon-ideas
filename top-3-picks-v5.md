# Top 3 Picks (v5) — DSI Ideathon 2026

Scored across all 39 ideas. Weighted criteria: Business & Strategic Value (30%), Problem Clarity (25%), Originality (25%), Feasibility (20%). Adjusted for competition context: 300+ DSI engineers with domain knowledge across logistics (ODMS), education (IPEMIS), civil registration (OpenCRVS), and enterprise software security.

Additional filter applied in v5: ideas where the primary user has a direct incentive to lie to or game the agent were deprioritised. Robust ideas are those where dishonesty either cannot occur (data from external sources), gets caught downstream (bank verifies independently), or backfires on the liar (student misreports their own eligibility).

---

## #1 — Idea 24: FieldLedger — Microfinance Field Operations Agent

**Why:** No incumbent software. No DSI product collision. Uses DSI's exact AI stack (LangGraph, Bangla NLU). The borrower confirmation loop creates a two-sided audit trail that a dishonest officer cannot falsify alone — this is the core mechanism that makes the pitch defensible under scrutiny. Fraud detection and MRA compliance reporting accumulate as data moat over time.

**Dishonesty resistance:** Officer logs a payment → borrower receives a receipt and must confirm → entry only commits on confirmation. Officer pocketing cash now faces a borrower who got no receipt. Neither party controls the record alone.

**Strategic edge:** Deepest data moat of all 39 ideas. Every month of history increases switching cost and opens premium fraud analytics and MRA audit reporting features. Microfinance field collection is a global problem — scales to Kenya, Philippines, India without rebuilding.

---

## #2 — Idea 32: LoanReady — Bank Loan Application Preparation Agent

**Why:** Banks are enterprise clients — fits DSI's enterprise sales profile. The non-obvious insight (bank as buyer, not the applicant) shows business thinking DSI leadership will respect. No BD-specific competitor. Clean, demonstrable pitch scenario. No API dependencies in MVP.

**Dishonesty resistance:** An applicant who lies about their document readiness only hurts themselves — the bank verifies everything independently. The agent makes no credit decision and stores no sensitive data. There is nothing to game.

**Strategic edge:** Bank partnership gives distribution without a sales team. Internationally valid — same loan preparation gap exists in every emerging market.

---

## #3 — Idea 39: AdmitPath — University Admission Guidance Agent

**Why:** 1.3 million HSC candidates annually. Coaching centres (50,000+ in BD) are the B2B distribution channel — they pay to offer this as a value-added service to enrolled students, white-labelled under their brand. No conversational Bangla admission guidance tool exists. Knowledge base updates once a year — low maintenance. Highly original in a room of engineers who won't think about HSC admissions.

**Dishonesty resistance:** A student who misreports their HSC GPA to get a more favourable eligibility result only misleads themselves — the university verifies at admission. The knowledge base (university requirements) is external and fixed. There is no data the agent holds that is worth gaming.

**Strategic edge:** Coaching centre distribution is immediate and requires no consumer marketing. 50,000 coaching centres each serving hundreds of students is a large channel. Freemium student tier runs in parallel for direct growth.

---

## What changed from v4

| v4 Pick | v5 Pick | Reason |
|---|---|---|
| #24 FieldLedger | #24 FieldLedger | Unchanged in rank. Agent Idea rewritten — borrower confirmation loop added as core fraud-resistance mechanism. |
| #35 GreenPass | #39 AdmitPath | GreenPass dropped: factory compliance manager self-reports all data (energy, waste, worker incidents) with strong incentive to lie to retain buyer contracts. No verification layer exists in the agent — it would enable greenwashing. AdmitPath replaces it: external knowledge base, no incentive to game, strong B2B coaching centre channel. |
| #32 LoanReady | #32 LoanReady | Unchanged. |

---

## Collision risk reference — ideas to avoid

| Idea | Collision risk |
|---|---|
| #23 Cargo/Import Documentation | ODMS team — 40% BD container market |
| #25 School Fee Collection | IPEMIS team — 130,000 schools already in their product. Note: could be positioned as a sister product sold alongside IPEMIS rather than a standalone submission — DSI already has the client relationship and distribution channel. Worth flagging to IPEMIS product team separately. |
| #12/#13 Govt Service Navigation / SLA Watchdog | OpenCRVS team — civil registration is their domain |
| #33 FilterFirst (CV Screening) | Most common AI demo idea — multiple submissions expected |
| #30 Legal Document Drafting | Common AI idea — multiple submissions expected |
| #38 DealPulse (Sales Pipeline) | "AI sales assistant" is globally saturated — high collision risk among engineers |
| #35 GreenPass | Self-reported data with no verification layer — defensibility collapses under scrutiny |
