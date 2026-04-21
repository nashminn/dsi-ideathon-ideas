# DSI Ideathon 2026 — Alternative Ideas (v9)

Focus: evaluation-weighted for Business & Strategic Value (30%) above all. Standalone products with durable revenue.

---

## Idea 25 — School Fee Collection & Parent Communication Agent

**Tag:** Quick Build

**1. Problem being solved**
Bangladesh has over 100,000 private schools, madrasas, and coaching centers — virtually all of which chase monthly fees manually via phone calls, paper notices, and in-person reminders. Finance staff spend days every month calling defaulting families, tracking payments in notebooks, and preparing collection reports for principals. Parents miss deadlines not from refusal but from forgetfulness. This is a universally painful, universally unsolved administrative problem that repeats every single month without exception.

**2. The AI agent concept**
A WhatsApp agent the school configures once with its student list, fee schedule, and payment deadline. Each month it automatically sends fee reminders to parents, accepts payment confirmation replies (manual confirmation or bKash/Nagad reference number), marks the student as paid, and sends the finance manager a real-time collection dashboard summary. For overdue accounts it escalates — day 3, day 7, day 14 — with progressively direct messages. At month end it generates a full collection report by class. Parents interact in Bangla; the school gets structured data.

**3. Beneficiary audience**
Private school administrators and coaching center owners — a market of 100,000+ institutions across Bangladesh. The primary buyer is the school principal or owner, not a tech team. The agent replaces a process so painful and universal that demonstrating it to any school owner is an immediate sale.

**4. Why now**
bKash and Nagad have made digital payment confirmation frictionless for parents. WhatsApp and SMS penetration among parents is near-universal. No affordable school management SaaS exists for sub-200-student institutions — existing products (like Shikho, School management software) target larger, more tech-forward schools. The bottom 90% of the market is unserved.

**5. Feasibility / Business model**
Student database upload (CSV or manual entry) → monthly trigger → WhatsApp reminder broadcast → payment confirmation intake → collection tracking → report generation. Zero complex inference — primarily scheduling and state management. **Revenue: BDT 500–1,500/month per institution. At 5,000 institutions: BDT 2.5–7.5M/month recurring.** Coaching centers (estimated 50,000+ in BD) are an equally large parallel market. Extremely low churn — once a school's student data and payment history are in the system, switching cost is high. Annual contracts with pre-monsoon (June) enrollment cycles make revenue predictable.

---

## Idea 26 — Pharmaceutical Expiry & Distributor Stock Agent

**Tag:** Quick Build

**1. Problem being solved**
Bangladesh's pharmaceutical sector is one of the largest in South/Southeast Asia — over 300 licensed manufacturers, thousands of distributors, depot holders, and retail pharmacies. Expired or near-expiry medicine stock is a direct public health risk and a major financial loss for distributors and pharmacies who must return or destroy it. Managing expiry dates across hundreds of SKUs is done manually — handwritten ledgers, memory, or basic Excel — and near-expiry stock routinely slips through. Meanwhile, fast-moving items go out of stock without warning. Both failures cost money and, in the case of expiry, cost lives.

**2. The AI agent concept**
A WhatsApp agent for medicine distributors, depot holders, and pharmacy owners. Stock entries come in as simple text ("received 200 Napa 500mg, expiry 12/2026") — the agent maintains a running inventory with expiry tracking per batch. It sends automated alerts: 90-day expiry warning (time to push to retailers), 30-day warning (time to return to manufacturer), and out-of-stock alerts for fast movers based on sales velocity. For distributors managing multiple retail pharmacy accounts, it tracks which batches went where — critical for targeted recalls. Sold as a monthly subscription per outlet.

**3. Beneficiary audience**
~3,000 licensed wholesale medicine distributors, ~20,000 depot holders, and ~150,000 retail pharmacies in Bangladesh. The primary pain point is sharpest for distributors and depot holders managing large, multi-SKU inventories with manufacturer return windows. Secondary market: hospital pharmacy departments managing their own procurement.

**4. Why now**
DGDA (Directorate General of Drug Administration) is tightening enforcement on expired medicine. Manufacturer return policies have strict windows — missing the window means the loss is absorbed by the distributor, not recovered. The financial incentive to track expiry is direct and quantifiable. No affordable mobile-first tool exists for small and mid-sized distributors; they operate entirely on paper or basic spreadsheets that offer no proactive alerts.

**5. Feasibility / Business model**
Text-based stock entry → SKU + batch + expiry parsing via LLM → expiry calendar per batch → threshold-based alert generation → optional sales velocity tracking for reorder nudges. **Revenue: BDT 500–2,000/month per outlet depending on SKU count. At 10,000 outlets: BDT 5–20M/month.** The data moat is powerful: a distributor's full inventory and movement history makes switching nearly impossible. Over time, aggregated (anonymized) stock data across distributors becomes a market intelligence asset — which SKUs are overstocked nationally, where near-expiry stock is concentrated — valuable to manufacturers and potentially monetizable as a separate data product.

---

## Idea 27 — Property Due Diligence & Ownership Verification Agent

**Tag:** Big Bet

**1. Problem being solved**
Land and property disputes are the single most litigated category in Bangladesh's courts — hundreds of thousands of active cases. The core cause is consistently the same: buyers purchase property without verifying the full ownership chain, outstanding mortgages, mutation status, or pending litigation. This happens not from negligence but because verification requires visiting multiple offices (Sub-registrar, AC Land, DC office), knowing the right forms, and often paying brokers. A fraudulent sale of the same plot to multiple buyers — or of encumbered property — is shockingly common. The damage is permanent and the legal recovery process takes decades.

**2. The AI agent concept**
A WhatsApp + web agent where a buyer, seller, or lawyer submits a property's Mouza, JL number, and Khatian number. The agent guides them through a structured due diligence checklist: how to pull the RS/CS/BS khatian from land.gov.bd, what to look for in the mutation record, how to check for encumbrance at the Sub-registrar's office, how to verify the seller's NID against the khatian owner name, and what court record searches to run. For each step it explains what a red flag looks like in plain Bangla. It maintains a case file per property — documents uploaded by the user are logged against the checklist. Sold per-verification or as a monthly subscription to real estate agents, lawyers, and developers.

**3. Beneficiary audience**
Individual property buyers (high willingness to pay — transactions are BDT 20L to several crore), real estate developers doing land acquisition, lawyers handling property transactions, and banks doing mortgage due diligence. The Real Estate & Housing Association of Bangladesh (REHAB) members are a high-value B2B channel.

**4. Why now**
land.gov.bd has digitized a significant portion of khatian records. NID verification APIs are increasingly accessible. Property transaction volume in Bangladesh is growing rapidly with urbanization. Legal fees for a property dispute dwarf any due diligence subscription cost by orders of magnitude — the ROI conversation with buyers is trivially easy. No consumer-facing due diligence product exists in this market.

**5. Feasibility / Business model**
Guided checklist logic per verification step → land record lookup guidance (not API-dependent in MVP — agent guides the user to pull records themselves) → document upload and checklist tracking → red flag explanation via LLM → case file generation. MVP requires no government API access — it operates as a guided intelligence layer over publicly available processes. **Revenue: BDT 500–2,000 per verification (transactional) or BDT 5,000–15,000/month for real estate agent/law firm subscriptions. High-value market: even 1,000 verifications/month at BDT 1,000 = BDT 1M/month.** Big Bet due to the need for accurate, jurisdiction-specific legal knowledge and the liability implications of errors — requires legal review of content and clear disclaimers.
