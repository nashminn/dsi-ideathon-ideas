# Submission-Ready Answers — DSI Ideathon 2026 (v8)

Three ideas: LoanWatch (#61), Cargo Documentation (#23), HajjReady (#47).

---

# IDEA 1 — LoanWatch: Loan Portfolio Delinquency Monitor

## Title
LoanWatch — Automated Loan Portfolio Delinquency Monitor

## The Problem
Banks don't lose loans overnight. They lose them because a missed payment at day 3 becomes a classified loan at day 90 — and nobody acted in between. Loan officers managing 200+ accounts can't track each one daily. By the time a delinquency is noticed, recovery is hard and the credit bureau damage is done.

The data to catch this early exists in every bank's core banking system. What's missing is a system that watches it continuously and acts without waiting for a human to notice.

## The Agent Idea
A daily scheduled agent that runs against the bank's loan repayment data and manages the entire early warning ladder automatically — no one needs to trigger it.

- **DPD 1–7**: LLM-generated reminder sent directly to the borrower via WhatsApp or SMS — contextual, referencing their specific loan and payment channel.
- **DPD 7–30**: Loan officer receives a structured account brief — borrower contact, outstanding amount, payment history, suggested call script. Ready to act immediately.
- **DPD 30–60**: Branch manager gets a consolidated list of all accounts in this bracket, across all officers. No manual compilation.
- **DPD 90**: Compliance team receives a pre-classification alert with CIB reporting preparation.

Beyond reaction: every week the agent runs a predictive pass over the portfolio — flagging accounts showing early behavioral signals (partial payments, irregular timing, decreasing amounts) before they miss a payment. Proactive outreach before DPD 1 is the highest-value intervention.

## Who Benefits
Risk and collections heads at banks and NBFIs are the buyers. Bangladesh has 61 scheduled banks and 35 NBFIs — all under Bangladesh Bank pressure to reduce NPL ratios. The same product works identically in Kenya, Nigeria, Pakistan, and the Philippines. NPL is a global banking problem; the escalation logic and LLM messaging are language-configurable.

Pricing per active loan account (BDT 20–50/account/month) scales with portfolio size. A bank with 50,000 accounts at BDT 30 = BDT 1.5M/month per client.

## Why Now
Bangladesh Bank has been pushing formal NPL reduction targets since 2023 — this is now a regulatory obligation, not just a best practice. Core banking data exports are standard at every scheduled bank. LLM-generated outreach messages are production-quality and cost-effective at per-account scale. The tool that helps a bank hit its NPL target has a board-level argument behind it.

## Feasibility & Scope
Daily repayment data export → DPD calculation per account → LLM message generation → WhatsApp/SMS dispatch → weekly predictive risk scoring → management dashboard.

POC: one bank, one loan product, DPD 1–7 automated reminders only — 3 weeks. Full escalation ladder and predictive scoring is v1 production. No core banking write access required — read-only data export is sufficient.

## Self-Categorization Tag
Big Bet

---

# IDEA 2 — TradeReady: Import & Cargo Documentation Agent

## Title
TradeReady — AI-Powered Import & Cargo Documentation Agent

## The Problem
Every shipment entering Bangladesh generates a stack of documents — Bill of Lading, commercial invoice, packing list, certificate of origin, LC. Someone has to read all of them, classify the goods under the correct HS code, calculate applicable duties, check for discrepancies, and generate a customs declaration. This is done manually by clearing agents, and it is slow, error-prone, and expensive.

A wrong HS code means a customs penalty. A discrepancy between the invoice and the packing list means a hold. A delayed clearance means demurrage charges accumulating by the day. The stakes are high and the process is entirely manual.

## The Agent Idea
A triggered agent that acts the moment shipping documents arrive — via email or document upload — without anyone initiating it.

The agent reads the full document set using multimodal LLM: extracts structured data from the B/L (consignee, vessel, port, cargo description), commercial invoice (line items, unit prices, total value), and packing list (quantities, weights, dimensions). It cross-checks figures across documents and flags any discrepancy before the shipment reaches customs.

From the cargo description, it classifies the applicable HS code, calculates the import duty, VAT, and AIT applicable under the current NBR schedule, and generates a draft customs declaration ready for submission. It also tracks shipment milestones — ETA, port arrival, customs examination schedule — and sends alerts when action is required.

What takes a clearing agent half a day of manual work happens in minutes, with a full audit trail.

## Who Benefits
Freight forwarders, customs clearing agents, importers, and banks processing Letters of Credit are the buyers. Bangladesh processes billions in imports annually — the clearing agent industry alone has thousands of licensed firms. Banks with trade finance operations need the same document extraction for LC compliance checking.

This is not a Bangladesh-only product. HS codes are WTO-standardized globally. The same agent works for any importer in any country — the duty rate tables and regulatory rules change per country, the document processing pipeline does not. DSI can expand to any trade-active market without rebuilding.

## Why Now
Multimodal LLMs can now reliably extract structured data from arbitrary document formats — printed PDFs, scanned invoices, mixed-language documents — without per-vendor template configuration. This capability is new. Previously, document automation required expensive OCR template setup per document type; now a single model handles all formats. Bangladesh's import volumes are growing and NBR is tightening customs compliance enforcement.

## Feasibility & Scope
Document intake (email/upload) → LLM multimodal extraction → cross-document discrepancy check → HS classification → duty calculation → customs declaration generation → shipment milestone alerts.

POC: one clearing agent, one commodity type, email intake — 3 weeks. Expansion to full document set and multi-commodity HS classification is v1 production. No government system integration required — declaration is generated as a draft for the agent to submit through existing channels.

## Self-Categorization Tag
Quick Build

---

# IDEA 3 — HajjReady: Hajj & Umrah Preparation Agent

## Title
HajjReady — Hajj & Umrah Preparation Agent

## The Problem
Bangladesh sends over 100,000 pilgrims to Saudi Arabia for Hajj annually — and a larger number for Umrah year-round. For most families this is a once-in-a-lifetime journey saved for over a decade.

The preparation is document-heavy: vaccinations with specific timing windows, medical fitness certificates, passport validity rules, mahram documentation for women, visa processing, baggage restrictions. Every year, pilgrims are turned away at the airport for preventable errors. For a family that saved ten years for this, that failure is devastating — and entirely avoidable.

## The Agent Idea
A WhatsApp agent that Hajj agencies distribute to every registered pilgrim. The pilgrim registers once — travel date, Hajj or Umrah, passport issue date, travelling with or without mahram — and the agent generates a personalised preparation timeline with conditional logic.

A passport issued within 6 months triggers a Saudi entry advisory. A woman travelling without a male relative follows a different document flow. A pilgrim with a pre-existing condition gets routed to additional medical screening. Hajj and Umrah have different preparation sequences — the agent handles both without conflating them.

Reminders fire automatically at each deadline. The agency gets a live dashboard: all enrolled pilgrims, completion percentage per person, automatic risk flag for anyone with departure inside 30 days and a critical item outstanding. At T-7, the agent sends each pilgrim a personalised pre-departure document — confirmed vaccinations, baggage rules, emergency contacts — over WhatsApp automatically.

The agency's job becomes exception management, not status chasing.

## Who Benefits
Hajj agencies are the buyers. Bangladesh has 500+ licensed agencies, each handling hundreds of pilgrims per season. An agency using this differentiates from competitors offering the same paper briefing — and has fewer last-minute crises.

The international case: Indonesia, Malaysia, Pakistan, and Egypt send even larger pilgrim volumes to the same Saudi system with identical requirements. The knowledge base doesn't change; only the language layer does.

At BDT 500–1,500 per pilgrim per cycle, 100 agencies × 500 pilgrims = BDT 25–75M/year. Umrah runs year-round — revenue is continuous, not seasonal.

## Why Now
Saudi Arabia's Vision 2030 Hajj digitisation is raising documentation standards and reducing tolerance for errors at the border. Bangladesh's Hajj quota has expanded — more first-time pilgrims, higher error rate. No Bangla-language personalised preparation tool exists. The knowledge base is public and updates once per season.

## Feasibility & Scope
Pilgrim registration → conditional timeline generation → automated milestone reminders → completion tracking → agency dashboard → T-7 pre-departure document generation.

POC: Umrah preparation, single agency, 2 weeks. Full Hajj workflow and agency dashboard is v1 production. Knowledge base is public — Ministry of Religious Affairs circulars, Saudi embassy requirements, WHO vaccination rules.

## Self-Categorization Tag
Quick Build
