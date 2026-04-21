# Top 3 Picks (v6) — DSI Ideathon 2026

Scored across all 39 ideas. Weighted criteria: Business & Strategic Value (30%), Problem Clarity (25%), Originality (25%), Feasibility (20%). Adjusted for competition context: 300+ DSI engineers with domain knowledge across logistics (ODMS), education (IPEMIS), civil registration (OpenCRVS), and enterprise software security.

Filters applied: (1) ideas where the primary user has a direct incentive to lie and can get away with it are deprioritised; (2) ideas where the primary buyer is not an enterprise — i.e. DSI cannot sell B2B at scale — are deprioritised; (3) declining buyer markets (e.g. coaching centres) are deprioritised regardless of problem clarity.

---

## #1 — Idea 24: FieldLedger — Microfinance Field Operations Agent

**Why:** No incumbent software. No DSI product collision. Uses DSI's exact AI stack (LangGraph, Bangla NLU). The borrower confirmation loop creates a two-sided audit trail that a dishonest officer cannot falsify alone. Fraud detection and MRA compliance reporting accumulate as data moat over time.

**Dishonesty resistance:** Officer logs a payment → borrower receives a receipt and must confirm → entry only commits on confirmation. Officer pocketing cash now faces a borrower who got no receipt. Neither party controls the record alone.

**Strategic edge:** Deepest data moat of all 39 ideas. Every month of history increases switching cost and opens premium fraud analytics and MRA audit reporting features. Microfinance field collection is a global problem — scales to Kenya, Philippines, India without rebuilding.

---

## #2 — Idea 32: LoanReady — Bank Loan Application Preparation Agent

**Why:** Banks are enterprise clients — fits DSI's enterprise sales profile exactly. The non-obvious insight (bank as buyer, not the applicant) shows business thinking DSI leadership will respect. No BD-specific competitor. Clean, demonstrable pitch scenario. No API dependencies in MVP.

**Dishonesty resistance:** An applicant who lies about their document readiness only hurts themselves — the bank verifies everything independently. The agent makes no credit decision and stores no sensitive data. There is nothing to game.

**Strategic edge:** Bank partnership gives distribution without a sales team. Internationally valid — same loan preparation gap exists in every emerging market.

---

## #3 — Idea 34: ClaimStart — Insurance First Notice of Loss Agent

**Why:** Bangladesh has 80+ registered insurance companies and none has a functional digital FNOL channel. Policyholders currently file claims in person on paper forms — adjusters arrive at incidents unprepared with incomplete information. The problem is embarrassingly basic and nobody built the product. Insurance companies are enterprise buyers with a direct cost-reduction motivation. IDRA is actively pushing sector digitisation — same regulatory tailwind as MRA for FieldLedger.

**Dishonesty resistance:** The agent handles intake only — it does not make coverage decisions. A policyholder who exaggerates on intake faces an adjuster who sees the actual scene. Lying on intake only undermines the policyholder's own claim. The insurer verifies independently.

**Strategic edge:** Per-claim revenue model scales with claims volume without DSI doing additional sales. Same FNOL problem exists in every insurance market globally — international expansion requires no product rebuild. Multimodal LLM capability (photo + text extraction at incident scene) is a natural showcase of DSI's AI stack.

---

## What changed from v5

| v5 Pick | v6 Pick | Reason |
|---|---|---|
| #24 FieldLedger | #24 FieldLedger | Unchanged. |
| #32 LoanReady | #32 LoanReady | Unchanged. |
| #39 AdmitPath | #34 ClaimStart | AdmitPath dropped: coaching centres (primary distribution channel) are in structural decline; people are slowly moving away from traditional education paths. Management at DSI would not invest in a product whose buyer market is contracting. ClaimStart replaces it: enterprise buyer (insurers), simple product nobody built, regulatory tailwind, globally applicable. |

---

## Collision risk reference — ideas to avoid

| Idea | Collision risk |
|---|---|
| #23 Cargo/Import Documentation | ODMS team — 40% BD container market |
| #25 School Fee Collection | IPEMIS team — 130,000 schools already in their product. Could be positioned as IPEMIS upsell/sister product — DSI already has the client relationship. |
| #12/#13 Govt Service Navigation / SLA Watchdog | OpenCRVS team — civil registration is their domain |
| #33 FilterFirst (CV Screening) | Most common AI demo idea — multiple submissions expected |
| #30 Legal Document Drafting | Common AI idea — multiple submissions expected |
| #38 DealPulse (Sales Pipeline) | "AI sales assistant" is globally saturated — high collision risk |
| #35 GreenPass | Self-reported data with no verification layer — defensibility collapses under scrutiny |
| #39 AdmitPath | Primary distribution channel (coaching centres) is in structural decline |
