# DSI Ideathon 2026 — Ideas (v21) — Banking/Fintech Depth

Three ideas built specifically for the DSI management panel profile — technical backgrounds, banking client awareness, preference for clear enterprise business models.

---

## Idea 70

**Title**
CreditPulse — SME Alternative Credit Scoring Platform

**The Problem**
Bangladesh has over 7 million SMEs. Banks cannot lend to most of them because they have no formal credit history — no audited financials, no CIB record, no collateral documentation. Bangladesh Bank's financial inclusion mandate pushes banks to grow SME lending, but the underwriting infrastructure to actually do this at scale does not exist. Banks currently either refuse these loans or underwrite them manually at a per-file cost that makes small-ticket SME lending economically unviable.

Meanwhile, every one of those SMEs has a digital footprint: mobile money transaction history (bKash Business, Nagad), bank account flows, utility payment records, mobile recharge patterns, business registration data, supply chain records. The data exists to underwrite them — it just isn't being used.

**The Product Idea**
An AI credit scoring platform that banks and NBFIs deploy for SME loan underwriting. The platform ingests alternative digital data from multiple sources (with the SME's consent, through open banking / account aggregator APIs), runs ML models trained on historical repayment outcomes, and generates a credit score plus structured underwriting narrative.

The scoring is not a single number — it's a structured assessment: cash flow volatility, revenue trend, supplier payment reliability, customer concentration risk, seasonal patterns. The loan officer receives an underwriting package ready to approve, decline, or escalate — not a raw score. As loan outcomes come in (repayment, default), the models retrain continuously.

For the bank: SME lending becomes profitable at smaller ticket sizes. For the SME: borrowing becomes possible without a formal credit history. For Bangladesh Bank: financial inclusion targets become achievable, not aspirational.

**Who Benefits**
Banks and NBFIs doing SME lending are the buyers. 61 scheduled banks, 35 NBFIs, plus a growing digital lending segment (iFarmer, ShopUp Credit). Sold as an annual platform license with per-decision pricing or tiered subscription. Globally: alternative credit scoring for SMEs is a multi-billion dollar market — Lenddo, Tala, Branch operate internationally. Bangladesh has no local player.

**Why Now**
Bangladesh Bank's financial inclusion mandate is now measured, not aspirational. Mobile money transaction data is massive — bKash alone processes billions of transactions annually. Open banking frameworks are emerging. ML models for alternative data underwriting are now production-grade and battle-tested in other markets. The gap between regulatory pressure and execution capability is exactly the space DSI can fill.

**Feasibility & Scope**
Data ingestion (mobile money APIs, bank core exports, utility records) → feature engineering → ML credit scoring model → underwriting narrative generation → bank loan origination system integration.

POC: single bank, SME segment, mobile money + bank flow data only — 6 weeks. Full multi-source model and continuous retraining: 4–6 months. Biggest unknown: alternative data access agreements. Addressed by: initial partnership with one MFS provider (bKash is the natural first choice) creates the reference implementation.

**Dishonesty Filter**
SMEs cannot fabricate mobile money history or bank flows — the data comes from verified digital sources, not self-reporting. This is exactly the system designed to underwrite borrowers who cannot be trusted on their word.

**Tag:** Big Bet

---

## Idea 71

**Title**
FraudPulse — Real-time Mobile Financial Services Fraud Detection

**The Problem**
Bangladesh has one of the highest mobile financial services (MFS) penetration rates globally. bKash alone has 70+ million users; Nagad, Rocket, Upay collectively add tens of millions more. Transaction volumes are in the billions. Fraud is growing faster than any provider can manually monitor — mule account networks, account takeover attacks, transaction layering to evade AML thresholds, social engineering scams targeting the vulnerable.

The providers' current fraud detection relies on rule-based alerts and reactive investigation. Rules catch known patterns; they miss emerging fraud typologies. Reactive investigation catches fraud after the money has moved. The average time between fraud occurrence and detection is often measured in days — by which time the mule accounts have been drained and the funds are gone.

**The Product Idea**
A real-time ML fraud detection platform that sits inside the MFS provider's transaction stream. Every transaction is scored for fraud risk as it occurs — in milliseconds — based on behavioral patterns, network graph analysis (who transacts with whom), velocity patterns, and deviation from the user's normal activity. High-risk transactions are flagged for immediate hold and review; medium-risk patterns trigger background investigation.

Beyond individual transactions: the platform maintains a live mule account graph. When one account is identified as a mule, its counterparties are scored for participation probability. New mule networks are identified by clustering analysis rather than waiting for victim complaints.

For the MFS provider: fraud losses drop. Regulatory reporting to Bangladesh Bank's payment systems division is generated automatically. Customer trust — the product's core asset — is preserved.

**Who Benefits**
MFS providers (bKash, Nagad, Rocket, Upay) are the primary buyers. Banks with agent banking operations face the same problem. Payment processors. Sold as an annual platform license priced by transaction volume or AUM. Globally: every MFS provider in every market has this problem — M-Pesa, GCash, Paytm, Wave all fight the same fight.

**Why Now**
MFS penetration in BD has reached saturation for basic services — providers now compete on trust, security, and premium services. Fraud losses directly erode the trust asset. Bangladesh Bank's payment systems department is tightening oversight of MFS fraud reporting. Real-time ML inference on transaction streams is now cost-feasible at MFS scale.

**Feasibility & Scope**
Transaction stream integration → real-time feature extraction → ML fraud scoring model → graph-based network analysis → alert routing → investigation dashboard.

POC: single MFS provider, subset of transaction types (cash-out, P2P transfer), historical data model training — 8 weeks. Production real-time scoring requires integration with provider's transaction processing systems. Biggest unknown: MFS provider willingness to grant transaction data access. Addressed by: positioning as a deployed-inside solution where DSI's platform runs inside the provider's infrastructure, not as a data-sharing model.

**Dishonesty Filter**
The entire product exists to detect dishonesty. The fraudsters are the adversaries, not the users. The institutional buyer (MFS provider) is fully aligned with the product's goal.

**Tag:** Big Bet

---

## Idea 72

**Title**
ReportReady — Automated Bangladesh Bank Regulatory Reporting Agent

**The Problem**
Every scheduled bank and NBFI in Bangladesh must file a dense calendar of regulatory reports to Bangladesh Bank: CIB updates, classified loan statements, CAR (Capital Adequacy Ratio) computations, SLR/CRR compliance, deposit classification, branch-wise lending reports, liquidity coverage ratios, and more. Each has a specific format, a specific submission deadline, and specific penalties for late or incorrect filing.

Currently this is compiled manually by compliance and accounting teams — extracting data from core banking systems, reconciling across branches, computing required ratios, formatting into the Bangladesh Bank prescribed templates. Errors carry financial penalties. The work is repetitive, rules-based, and consumes significant team time every month and quarter.

**The Product Idea**
A scheduled agent that connects to the bank's core banking system, runs regulatory report generation on the appropriate cadence (daily, monthly, quarterly), and produces submission-ready reports in Bangladesh Bank's exact formats.

The agent maintains a rules engine encoding Bangladesh Bank's current reporting requirements — updated as regulations change (connecting to RegulatoryRadar-style regulatory change intelligence). For each scheduled report: pull data from core banking → apply classification rules → compute required metrics → validate against submission template → generate final report → route for human approval → submit through Bangladesh Bank's electronic filing portal.

Beyond routine reports: when Bangladesh Bank issues ad-hoc data calls (e.g., "all banks submit stressed-loan exposure analysis within 10 days"), the agent templates the data call, pulls from core banking, and drafts the response.

**Who Benefits**
Compliance heads, CFOs, and CROs at banks and NBFIs are the buyers. Every scheduled bank and NBFI needs this — the cost of manual reporting is a line item everyone wants to eliminate. Sold as an annual platform license. Internationally: every central bank has regulatory reporting requirements. The same product architecture serves banks in Kenya, Nigeria, Philippines, Pakistan — only the rules engine and templates change per jurisdiction.

**Why Now**
Bangladesh Bank's regulatory reporting volume has grown substantially since 2020 — new stress testing requirements, enhanced AML reporting, granular lending disclosures. Banks complain but cannot reduce the compliance burden. LLM-based rules interpretation and document generation is now reliable enough for production regulatory reporting.

**Feasibility & Scope**
Core banking data integration → regulatory rules engine → data extraction and classification → metric computation → template-based report generation → approval workflow → submission.

POC: single bank, three specific reports (CL statement, CAR report, SLR/CRR) — 8 weeks. Full regulatory calendar coverage: 4 months. Biggest unknown: core banking data access varies across institutions. Addressed by: modular data connectors for each major core banking platform used in BD (Flexcube, Temenos T24, Finacle, local systems).

**Dishonesty Filter**
The bank is the buyer and the subject of regulatory compliance — there is no incentive to misreport to BD Bank through this tool; that would only create regulatory exposure the tool is designed to reduce.

**Tag:** Big Bet

---

*Pool total: 72 ideas*
