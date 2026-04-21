# Submission-Ready Answers — DSI Ideathon 2026

Copy-paste directly into the form. Three ideas: MFI Field Ops (#24), GreenPass (#35), LoanReady (#32).
All five fields covered per idea, in form order.

---

# IDEA 1 — MFI Field Operations Agent

## Title
FieldLedger — Microfinance Collection Agent

## The Problem
Bangladesh's microfinance sector serves 30 million borrowers through tens of thousands of field officers who collect weekly loan repayments door-to-door. Every one of those officers manages their collections on paper — a handwritten register, sometimes a basic spreadsheet. Data reaches the head office with a 1–2 day lag. When a borrower starts missing payments, nobody knows until they've already missed several. Fraud — field officers pocketing cash, fabricating ghost borrower entries — is a known, ongoing problem that paper systems structurally cannot detect.

This isn't a niche edge case. It happens across hundreds of MFIs, every single week, at scale. The cost is absorbed in write-offs, fraud losses, and compliance failures that MRA audits increasingly flag.

## The Agent Idea
A WhatsApp agent used by field officers on their existing Android phones. After each collection visit the officer logs a receipt by typing or sending a voice note in Bangla: "রহিমা বেগম — ৫০০ টাকা জমা." The agent parses the entry, reads it back for confirmation, and appends it to that officer's live daily ledger. At the end of each day it generates a collection summary — total collected, borrowers visited, any missed payments — sent simultaneously to the officer and their branch supervisor. If a borrower misses a payment, the agent flags it immediately and prompts the officer to log a follow-up note.

Typical interaction: Officer finishes a home visit, sends a voice note. Agent transcribes, confirms "রহিমা বেগম, ৫০০ টাকা — ঠিক আছে?", officer replies "হ্যাঁ", entry is logged. At 5pm the supervisor receives a clean daily summary without making a single phone call.

The agent lives entirely in WhatsApp. No app to install. No training beyond what the officer already knows how to do.

## Who Benefits
MFI branch managers and operations heads at small and mid-sized MFIs — specifically those running 50–500 field officers who cannot afford enterprise loan management software. BRAC and Grameen have built custom systems; the underserved market is the next tier: hundreds of MFIs with BDT 50–500 crore portfolios and no digital field tooling.

Bangladesh has 700+ MRA-licensed MFIs. At BDT 200–400 per officer per month, a single 150-officer MFI generates BDT 30,000–60,000/month. At 50 clients: BDT 150–300M/year recurring. Beyond BD: microfinance field collection is a global problem — Kenya, Philippines, India, Cambodia all have the same paper notebook.

## Why Now
Three things converge: (1) **Bangla NLU via LLMs** — models can now reliably parse informal Bangla voice and text inputs into structured ledger entries, something rule-based systems never could. (2) **WhatsApp penetration** among field officers is near-universal — no behaviour change required, the agent lives inside the tool they already use every day. (3) **MRA compliance pressure** — reporting requirements for licensed MFIs are tightening, creating institutional demand for auditable digital records that paper cannot provide. The product replaces a process unchanged for 30 years. There is no incumbent software to displace.

## Feasibility & Scope
A 2-week POC: WhatsApp intake → LLM parsing of borrower name and amount → confirmation step → per-officer ledger append → end-of-day summary to officer and supervisor → missed payment flag.

Needs: WhatsApp Business API, LLM API for Bangla NLU, simple database per MFI (borrower roster, officer assignments). No government or banking system integration required in v1.

Biggest unknown: borrower name parsing accuracy for uncommon names in noisy voice input. Solved with the read-back confirmation step before any entry is committed. Delinquency trend detection and supervisor dashboard are v2.

## Tag
Quick Build

---

# IDEA 2 — GreenPass: ESG & Sustainability Compliance Agent

## Title
GreenPass — Factory ESG Data Collection Agent

## The Problem
International buyers — H&M, Walmart, IKEA, Marks & Spencer — now contractually require their Bangladesh suppliers to submit annual ESG reports: energy consumption, water usage, waste management, worker welfare metrics, carbon footprint. The EU's Corporate Sustainability Due Diligence Directive (CSDDD) comes into full enforcement by 2027 and will tighten requirements further.

Most BD factories — garment, leather, jute, pharmaceutical — have no system to collect this data. The compliance manager is typically one person managing this alongside everything else. Their current options: hire a consultant at BDT 200,000–500,000 per annual report cycle, or fail the audit and lose the buyer contract. Losing a single international buyer relationship costs multiples of any annual software fee. This pain is already happening today, and it gets worse every year until 2027.

## The Agent Idea
A WhatsApp agent that runs a monthly data collection routine with the factory's compliance manager. On the first Monday of each month it sends a structured prompt in Bangla: "এই মাসের বিদ্যুৎ বিল ছবি তুলে পাঠান।" The manager takes a photo of the utility bill and sends it. The agent extracts the figure, confirms it, logs it, and moves to the next data point — water consumption, waste disposal, worker headcount, incident log. At year end it auto-generates a buyer-ready ESG report in the format required by the Higg Index (the most widely adopted framework among BD garment buyers).

Typical interaction: Agent sends the monthly prompt. Manager photographs a crumpled electricity bill on their phone. Agent reads back "এই মাসে বিদ্যুৎ খরচ: ৪৮,৫০০ টাকা — ঠিক আছে?" Manager confirms. Twelve months of these exchanges produce a complete, audit-ready ESG report without a consultant, a spreadsheet, or a desktop computer.

## Who Benefits
Factory compliance managers and owners at Bangladesh's 4,500+ export-oriented factories pay for this. The ROI case writes itself: this agent costs less per year than a single consultant visit, and the consequence of not having it is losing the buyer contract.

At BDT 5,000–20,000/month per factory, even 500 clients = BDT 2.5–10M/month recurring. International expansion requires no product changes — Vietnam, Cambodia, and Sri Lanka face identical buyer pressure from the same global brands. DSI's existing RMG sector client relationships provide immediate distribution without cold outreach.

## Why Now
(1) **EU CSDDD enforcement deadline (2027)** — international buyers are pre-empting it with contractual requirements today. The market is being created by European regulation, not by a sales team. (2) **Multimodal LLMs** — extracting figures from a photo of a handwritten log or a utility bill taken on a basic Android phone is now reliable. This removes the last barrier: factory managers don't use computers, but they all have phones and WhatsApp. Previous ESG data collection tools required desktop software or complex forms. This doesn't. (3) No affordable tool exists for mid-sized BD factories — the market between "consultant" and "nothing" is entirely open.

## Feasibility & Scope
A 3-week POC: monthly WhatsApp prompt → photo and text intake → multimodal LLM extraction → metric logging → single-framework year-end report generation (Higg Index first).

Needs: WhatsApp Business API, multimodal LLM API, Higg Index framework template, per-factory data store. No government or buyer API required — the output is a generated document, not a filed submission.

Biggest unknown: extraction accuracy from low-quality photos of handwritten or crumpled documents. Addressed with a confirmation step after every extraction and a manual override option. Multi-framework support (Higg vs. SEDEX vs. UNGC) is v2 — MVP locks to one framework.

## Tag
Quick Build

---

# IDEA 3 — LoanReady: Bank Loan Application Preparation Agent

## Title
LoanReady — Bank Loan Preparation Agent

## The Problem
Thousands of small business owners and individuals apply for bank loans in Bangladesh every month and get rejected — not because they don't qualify, but because their application is incomplete, their documents are in the wrong format, or a required item is missing. Bank loan officers spend significant time returning incomplete applications and chasing applicants for corrections. Applicants spend weeks resubmitting without understanding what was wrong.

Both sides lose time on a fully preventable problem. The applicant doesn't know what "complete" looks like. The bank gets a flood of defective applications that consume officer hours without producing approved loans. Nobody wins.

## The Agent Idea
A WhatsApp agent that walks a loan applicant through preparation before they visit the bank. The user states the bank name and loan type: "Islami Bank SME loan দরকার." The agent responds with the exact document checklist for that bank and product, then assesses readiness one item at a time: "আপনার ট্রেড লাইসেন্স কি আপ টু ডেট?" Based on each answer it explains what's missing, what format the bank requires, and what to fix. It ends with a readiness summary: "আপনি ৭টার মধ্যে ৫টা ডকুমেন্ট রেডি। বাকি ২টা হলো: ..." The applicant arrives at the bank prepared. The loan officer receives a complete application.

The agent lives in WhatsApp. It doesn't apply on the applicant's behalf — it makes sure they're ready before they go. Banks are the primary buyer: they embed or distribute the agent to reduce incomplete application volume across their branches.

## Who Benefits
Banks and NBFIs are the paying customers — a bank embedding this agent on their website or distributing it through branch staff reduces incomplete applications and lowers the per-approved-loan processing cost across thousands of branches. Bangladesh has 60+ scheduled banks and hundreds of NBFIs. At BDT 50,000–200,000/month per institution, even 30 bank clients represents significant recurring revenue.

Secondary beneficiaries: millions of SME owners and individuals who apply for loans annually and lose weeks to rejection cycles caused by preventable document errors. They save time; banks save cost; both have strong motivation to use and distribute the agent.

## Why Now
(1) **LLM multi-turn reasoning** is now reliable enough to conduct a contextual document readiness assessment — asking the right follow-up question based on what the applicant already has, not reciting a static list. (2) **Bangladesh Bank's financial inclusion mandate** gives banks regulatory incentive to approve more qualified applicants, not just process fewer bad ones — this agent serves both goals simultaneously. (3) **No API dependency in MVP** — the entire first version runs on a manually curated knowledge base of bank-specific requirements built from publicly available information. Zero technical risk in the first build.

## Feasibility & Scope
A 2-week POC: user states bank and loan type → agent loads requirements for that combination → conversational readiness check, one item at a time → gap summary at the end.

Needs: WhatsApp Business API, LLM API, a structured knowledge base of document requirements (5 banks × 3 loan types to start, built manually from bank websites and branch brochures). No bank API, no government system, no user data stored.

Biggest unknown: keeping the knowledge base current as banks update requirements. Solved with a quarterly review cycle and, once a bank partnership is in place, a direct feed from their product team.

## Tag
Quick Build
