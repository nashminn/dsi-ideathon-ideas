# DSI Ideathon 2026 — Alternative Ideas (v8)

Focus: standalone product potential, recurring B2B revenue, problems that don't go away.

---

## Idea 22 — SME Tax & VAT Compliance Agent

**Tag:** Quick Build

**1. Problem being solved**
Bangladesh's NBR has been aggressively expanding the VAT net and pushing digital filing via iBAS++ and the VAT Online system. Small and medium businesses — garment accessories suppliers, distributors, small manufacturers, service firms — are legally required to file monthly VAT returns, annual income tax, and TDS deductions but most have no in-house accountant. They either hire expensive CA firms, rely on informal tax agents who make errors, or simply miss deadlines and pay penalties. The compliance calendar is fixed and recurring — the pain never goes away.

**2. The AI agent concept**
A WhatsApp-based agent that a business owner registers with their BIN (Business Identification Number) and business type. The agent maintains their compliance calendar: monthly VAT return deadlines, quarterly advance tax, annual return, TDS deposit dates. It sends deadline reminders 7 days and 1 day before each due date, walks them through what data to collect (sales register, purchase register, applicable rates), helps calculate the payable amount via a guided chat, and — for businesses ready for it — generates a pre-filled return summary they can hand to a filing agent or upload themselves. Sold as a monthly subscription per BIN.

**3. Beneficiary audience**
~800,000 VAT-registered businesses in Bangladesh, the majority of which are SMEs without dedicated finance staff. Also resellable through CA firms and tax consultants who manage multiple client BINs — a B2B2B channel that dramatically accelerates distribution.

**4. Why now**
NBR's VAT Online system mandate is expanding. Penalties for late filing are increasing. The compliance burden is rising faster than SME capacity to handle it. No affordable, Bangla-language compliance assistant exists for this market. The product sells itself every month when the deadline reminder lands — churn is structurally low because the problem recurs on a fixed calendar.

**5. Feasibility / Business model**
Compliance calendar logic + deadline reminders + guided data collection chat + return summary generation. No integration with NBR systems required in MVP — the agent produces a human-readable summary, not a filed return. **Revenue: BDT 300–500/month per BIN subscription. At 10,000 subscribers: BDT 3–5M/month recurring.** CA firms managing 50+ clients become high-value accounts. Data moat: over time the agent learns each business's typical filing patterns and can detect anomalies before an audit.

---

## Idea 23 — Import & Cargo Documentation Agent for C&F Agents

**Tag:** Big Bet

**1. Problem being solved**
Bangladesh processes ~$70B in annual imports, almost entirely through Chittagong Port. Every shipment requires a precisely sequenced set of documents — LC, Bill of Lading, packing list, certificate of origin, customs assessment (HS code classification), duty calculation, and clearance filing — each with strict deadlines. Missing a deadline triggers demurrage charges that compound daily. C&F (Clearing & Forwarding) agents manage dozens of shipments simultaneously, tracking deadlines manually in spreadsheets or from memory. Errors are expensive — a miscalculated duty or missed document costs their clients real money and damages the relationship.

**2. The AI agent concept**
A WhatsApp + lightweight web agent for C&F firms. When a new shipment arrives, the agent is given the Bill of Lading and basic shipment details. It extracts key fields, generates the full document checklist for that shipment type, sets a deadline calendar for each step (customs assessment, duty payment, gate pass), and sends daily status nudges to the responsible handler. For common HS code lookups it provides an instant classification suggestion with the applicable duty rate. When a deadline is within 24 hours it escalates to the firm owner. Sold per-seat to C&F firms and importers with in-house clearance teams.

**3. Beneficiary audience**
~3,500 licensed C&F agents in Bangladesh and their staff, plus mid-to-large importers who handle their own clearance. Also relevant to freight forwarders and buying houses managing multiple client shipments. High willingness to pay because the cost of a single demurrage incident or duty error vastly exceeds a year's subscription fee.

**4. Why now**
Chittagong Port's Automated System for Customs Data (ASYCUDA) is digitizing but the C&F agent workflow remains manual and error-prone. Port congestion makes deadline management more critical than ever. No vertical SaaS product exists for BD's C&F sector — the market is served by generic spreadsheets and WhatsApp groups.

**5. Feasibility / Business model**
Document intake (PDF/photo of BL) → field extraction via LLM → deadline calendar generation → daily nudge logic → HS code lookup against NBR tariff schedule. The HS classification suggestion is the most technically interesting piece. **Revenue: BDT 3,000–8,000/month per C&F firm seat. At 500 firms: BDT 1.5–4M/month.** Data moat builds over time: historical shipment data per importer enables predictive duty estimation and anomaly detection that becomes a premium feature.

---

## Idea 24 — Microfinance Field Operations Agent

**Tag:** Quick Build

**1. Problem being solved**
Bangladesh has the world's largest microfinance sector — BRAC, ASA, Grameen, and hundreds of smaller MFIs collectively serve ~30 million borrowers through armies of field officers. Each officer manages 200–400 borrowers, collects weekly repayments, conducts loan assessments, and prepares daily collection reports — almost entirely on paper or in basic spreadsheets. Data reaches the head office with a 1–2 day lag. Delinquency signals are invisible until a borrower has already missed multiple payments. Fraud by field officers (pocketing collections, ghost borrowers) is a known, ongoing problem that paper systems can't detect.

**2. The AI agent concept**
A WhatsApp agent used by field officers on their existing Android phones. After each collection session the officer logs receipts by typing or voice note in Bangla: "রহিমা বেগম — ৫০০ টাকা জমা" — the agent parses, confirms, and appends to that officer's daily ledger in real time. At end of day it generates a collection summary sent simultaneously to the officer and their branch supervisor. If a borrower misses a payment, the agent flags it immediately and prompts a follow-up note. Supervisors get a live dashboard view. Sold to MFIs as a per-officer monthly SaaS — no hardware, no training beyond basic WhatsApp use.

**3. Beneficiary audience**
MFI branch managers and operations teams at small and mid-sized MFIs (50–500 field officers) that cannot afford enterprise loan management software but need better field data than paper provides. BRAC and Grameen have custom systems; the underserved market is the next tier down — hundreds of MFIs with BDT 50–500 crore portfolios.

**4. Why now**
Smartphone penetration among field officers is now near-universal. WhatsApp is their primary communication tool. MRA (Microcredit Regulatory Authority) compliance reporting requirements are tightening, increasing demand for reliable digital records. The product replaces a paper process that has been unchanged for 30 years — switching cost is low because there is no incumbent software to displace, only a notebook.

**5. Feasibility / Business model**
Voice/text intake → Bangla NLU for borrower name + amount parsing → per-officer ledger append → daily summary generation → delinquency flag logic → supervisor alert. No complex ML. **Revenue: BDT 200–400/officer/month. A 100-officer MFI = BDT 20,000–40,000/month recurring.** With 50 MFI clients at average 150 officers each: BDT 150–300M/year. Extremely sticky — once an MFI's loan book history is in the system, switching cost is high. Audit trail data becomes a premium compliance feature over time.

**Note — Enterprise buyer angle**
Targeting bKash/Nagad as the buyer doesn't work — their field agents are cash-in/cash-out shopkeepers whose transactions are already handled by purpose-built apps, and both companies have large engineering teams that would build custom rather than buy. Better enterprise targets:
- **BRAC Bank / City Bank / Dutch Bangla Bank** — have active SME micro-loan arms with real field collection teams doing door-to-door recovery. Same workflow, larger procurement budgets.
- **Insurance companies (MetLife BD, Pragati Life, Delta Life)** — field agents collect premiums door-to-door, identical workflow to MFI collection, sector is growing, zero digital tooling exists at the field level. Potentially stronger angle than MFIs.
