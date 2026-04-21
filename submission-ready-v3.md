# Submission-Ready Answers — DSI Ideathon 2026 (v3)

Copy-paste directly into the form. Three ideas: FieldLedger (#24), LoanReady (#32), ClaimStart (#34).
All five fields covered per idea, in form order.

Changes from v2: #39 AdmitPath replaced by #34 ClaimStart — coaching centres (primary distribution channel for AdmitPath) are in structural decline; DSI management would not invest in a product whose buyer market is contracting. ClaimStart replaces it: insurance companies as enterprise buyers, simple product nobody built in BD, IDRA regulatory tailwind.

---

# IDEA 1 — FieldLedger: Microfinance Collection Agent

## Title
FieldLedger — Microfinance Collection Agent

## The Problem
At a weekly center meeting, a field officer collects 500 taka from Rohima Begum, writes 300 in the register, and pockets the difference. He fills in her passbook to match — he controls both records. Rohima assumes it's correct. The branch manager sees 300. Nobody knows.

This happens because the officer is the sole source of truth. The paper register says whatever they write. There is no second input. Cash skimming and ghost borrower entries — fabricated borrowers whose "repayments" the officer keeps — are known, ongoing problems across Bangladesh's microfinance sector. Paper systems cannot structurally detect them.

Bangladesh has 700+ MRA-licensed MFIs collectively serving over 30 million borrowers. The fraud cost is absorbed in write-offs and MRA audit failures, every week, at scale.

## The Agent Idea
A WhatsApp agent that creates a two-sided audit trail — one input from the officer, one confirmation from the borrower — so neither party can falsify the record alone.

At each weekly center meeting, the officer collects from 20–40 borrowers seated together. After each payment they log a receipt by typing or voice note in Bangla: "রহিমা বেগম — ৫০০ টাকা জমা." The agent immediately sends Rohima Begum a WhatsApp message: "আপনার ৫০০ টাকা আজকে জমা হয়েছে। ঠিক আছে?" She confirms or disputes on her phone. Only a confirmed entry commits to the ledger. The officer moves to the next borrower.

This replaces the existing passbook system, where the officer writes in both the center register and each borrower's passbook — meaning they control both records. The WhatsApp confirmation goes directly to the borrower's phone, bypassing the officer entirely.

At the end of each day the agent sends the branch supervisor a collection summary — total collected, confirmed entries, any disputed or unconfirmed payments — without a single phone call. A field officer who under-records a payment now faces a borrower who received the wrong receipt amount. The fraud vector closes.

Typical interaction: Center meeting, 8am. Officer collects from 30 borrowers, logs each by voice note. Agent sends each borrower a receipt as entries come in. By 9am the officer has a confirmed ledger for the full center. At 5pm the supervisor sees confirmed and disputed transactions across all 40 officers in the branch.

The agent lives entirely in WhatsApp. No app to install. No training required beyond what officers already do.

## Who Benefits
MFI branch managers and operations heads are the buyers — they pay because this is a management control system, not a convenience tool. MFI management at small and mid-sized MFIs (50–500 field officers) currently has no way to detect cash skimming until it accumulates into an audit finding. This agent gives them real-time visibility and a tamper-resistant record.

BRAC and Grameen have built custom systems; the underserved market is the next tier: hundreds of MFIs with BDT 50–500 crore portfolios and no digital field tooling.

Bangladesh has 700+ MRA-licensed MFIs. At BDT 200–400 per officer per month, a single 150-officer MFI generates BDT 30,000–60,000/month. At 50 clients: BDT 150–300M/year recurring. Beyond BD: microfinance field collection is a global problem — Kenya, Philippines, India, Cambodia all have the same paper notebook and the same fraud problem.

## Why Now
Three things converge: (1) **Bangla NLU (LLM reasoning)** — models now reliably parse informal Bangla voice and text into structured ledger entries; rule-based systems never could. (2) **WhatsApp penetration** among field officers and borrowers is now high enough that a two-way confirmation interaction is practical, not hypothetical. (3) **MRA compliance pressure** — reporting requirements are tightening, creating institutional demand for auditable digital records that paper cannot provide. No incumbent software exists to displace.

## Feasibility & Scope
A 2-week POC: officer WhatsApp intake → LLM parsing of borrower name and amount → borrower confirmation message → conditional ledger commit on confirmation → end-of-day summary to officer and supervisor → disputed entry flag to supervisor.

Needs: WhatsApp Business API (two-way messaging to both officer and borrower numbers), LLM API for Bangla NLU, simple database per MFI (borrower roster with phone numbers, officer assignments). No government or banking system integration required in v1.

Biggest unknowns: (1) Borrower WhatsApp availability — MFIs already collect borrower phone numbers; SMS fallback covers the rest with no additional engineering. (2) Officer adoption — an officer who doesn't log shows zero visits to their supervisor; non-use is self-incriminating. (3) Name parsing accuracy for uncommon names — addressed by the borrower confirmation step before any entry commits. Delinquency trend detection and supervisor dashboard are v2.

## Self-Categorization Tag
Quick Build

---

# IDEA 2 — LoanReady: Bank Loan Preparation Agent

## Title
LoanReady — Bank Loan Preparation Agent

## The Problem
An SME owner walks into Islami Bank to apply for a loan. The officer reviews the file and sends them home — trade licence is expired, the bank statement format is wrong, one document is missing entirely. The applicant had no idea. They come back three weeks later. The officer sends them home again.

This cycle repeats across thousands of applications every month at every bank in Bangladesh. Applicants are rejected not because they don't qualify but because nobody told them exactly what "complete" looks like for that bank and that loan type. Loan officers spend significant time on returns that are entirely preventable. Both sides lose weeks on a process that should take one visit.

## The Agent Idea
A WhatsApp agent that walks a loan applicant through preparation before they visit the bank. The user states the bank name and loan type: "Islami Bank SME loan দরকার." The agent responds with the exact document checklist for that bank and product, then assesses readiness one item at a time: "আপনার ট্রেড লাইসেন্স কি আপ টু ডেট?" Based on each answer it explains what's missing, what format the bank requires, and what to fix. It ends with a readiness summary: "আপনি ৭টার মধ্যে ৫টা ডকুমেন্ট রেডি। বাকি ২টা হলো: ..."

The applicant arrives at the bank prepared. The loan officer receives a complete application.

The agent lives in WhatsApp. It doesn't apply on the applicant's behalf — it makes sure they're ready before they go. Banks are the primary buyer: they embed or distribute the agent to reduce incomplete application volume across their branches.

Importantly, an applicant who lies to this agent — claiming they have documents they don't — only hurts themselves. The bank verifies everything independently. The agent makes no credit decision and stores no sensitive data. There is nothing to game.

## Who Benefits
Banks and NBFIs are the paying customers — a bank embedding this agent on their website or distributing it through branch staff reduces incomplete applications and lowers the per-approved-loan processing cost across thousands of branches. Bangladesh has 60+ scheduled banks and hundreds of NBFIs. At BDT 50,000–200,000/month per institution, even 30 bank clients represents significant recurring revenue.

Secondary beneficiaries: millions of SME owners and individuals who apply for loans annually and lose weeks to rejection cycles caused by preventable document errors. They save time; banks save cost; both have strong motivation to use and distribute the agent.

## Why Now
(1) **LLM multi-turn reasoning** — reliable enough to conduct a contextual readiness assessment, asking the right follow-up based on what the applicant already has rather than reciting a static list. A PDF checklist cannot do this. (2) **Bangladesh Bank's financial inclusion mandate** — banks have regulatory incentive to approve more qualified applicants, not just reject incomplete ones faster; this agent serves both goals. (3) **Zero API dependency in MVP** — runs entirely on a manually curated knowledge base built from public bank websites. No integration risk in the first build.

## Feasibility & Scope
A 2-week POC: user states bank and loan type → agent loads requirements for that combination → conversational readiness check, one item at a time → gap summary at the end.

Needs: WhatsApp Business API, LLM API, a structured knowledge base of document requirements (5 banks × 3 loan types to start, built manually from bank websites and branch brochures). No bank API, no government system, no user data stored.

Biggest unknowns: (1) "Why not just a better PDF checklist?" — a static checklist can't ask follow-up questions; if a trade licence expired last month, the agent tells the applicant exactly what to do about it, a PDF cannot. (2) Knowledge base currency — quarterly review cycle; bank partnership replaces this with a direct documentation feed from their product team.

## Self-Categorization Tag
Quick Build

---

# IDEA 3 — ClaimStart: Insurance First Notice of Loss Agent

## Title
ClaimStart — Insurance First Notice of Loss Agent

## The Problem
When a Bangladeshi policyholder has an incident — a vehicle accident, a shop fire, a hospitalisation — they have to visit the insurance office in person, fill out a paper form, and wait days for an adjuster to contact them. In the meantime, evidence degrades, receipts get lost, and the claimant has no idea what stage their claim is at.

On the insurer's side, claims teams receive incomplete FNOL (First Notice of Loss) reports that require multiple follow-up calls before an adjuster can be dispatched. Adjusters arrive at incidents without a full picture. The result: slow claims cycles, high administrative cost per claim, and a sector with one of the lowest customer trust ratings in Bangladesh.

Bangladesh has 80+ registered insurance companies. None has a functional digital FNOL channel. The problem exists at every insurer, for every claim, every day — and it has a straightforward fix.

## The Agent Idea
A WhatsApp agent that insurance companies embed as their claims intake channel. When a policyholder has an incident, they message the agent. It guides them through structured FNOL intake: policy number, incident type, date and location, brief description, and photo evidence. The agent validates the policy number, checks coverage, and asks claim-type specific follow-up questions — for a vehicle accident: is the vehicle driveable? any injuries? — then generates a complete, structured FNOL report delivered to the insurer's claims team within minutes. The policyholder gets a reference number and knows what happens next.

The adjuster arrives at the scene with a complete dossier, not a blank form.

Typical interaction: Policyholder texts "আমার গাড়ি এক্সিডেন্ট হয়েছে।" Agent asks for policy number, incident details, location, photos. 8 minutes later the claims team has a structured report with photos attached and policy coverage confirmed. Adjuster is dispatched the same day.

An applicant who exaggerates on intake faces an adjuster who sees the actual scene. The agent makes no coverage decision — it only captures what the policyholder reports. The insurer verifies everything on-site. There is nothing to gain by lying to the intake agent.

## Who Benefits
Insurance companies are the buyers — sold as a SaaS intake layer per claim processed or monthly subscription. Bangladesh has 80+ registered insurance companies with millions of active policies across life, health, motor, and fire lines. Faster, complete FNOL reduces total claims cycle time, which directly reduces the insurer's loss adjustment expense. The cost reduction is measurable per claim.

At BDT 50–150 per claim processed, or BDT 30,000–80,000/month per insurer on subscription, even 30 insurer clients at mid-range subscription = BDT 1–2.4M/month recurring. Same model scales globally — the FNOL problem is identical in every insurance market.

## Why Now
(1) **WhatsApp multimodal input** — photo and text at the point of incident is now practical on any Android phone; a policyholder can photograph vehicle damage on the roadside and submit it in seconds. Previous digital FNOL attempts required desktop portals nobody used. (2) **LLM structured extraction** — converting a conversational incident description into a structured claims report is now reliable without manual processing. (3) **IDRA digitisation mandate** — the Insurance Development and Regulatory Authority is actively pushing insurers toward digital operations; there is regulatory incentive to adopt a digital intake channel. No BD insurer has built one.

## Feasibility & Scope
A 2-week POC: policyholder WhatsApp message → policy number validation → claim type routing → structured Q&A per claim type → photo intake and logging → FNOL report generation → delivery to claims team via email.

MVP covers motor claims only — highest volume claim type in BD. Needs: WhatsApp Business API, multimodal LLM API, per-insurer policy number lookup (manual in MVP, replaced by API in production). No government system integration required.

Biggest unknowns: (1) Policy database access — MVP uses manual lookup; insurer partnership replaces this with a direct API feed, which is a standard integration any insurer can provide. (2) Photo quality from low-end phones — addressed with a confirmation step after every extraction and a manual override option. Life and health claim types are v2.

## Self-Categorization Tag
Quick Build
