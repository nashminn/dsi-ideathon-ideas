# Submission-Ready Answers — DSI Ideathon 2026 (v5)

Copy-paste directly into the form. Three ideas: FieldLedger (#24), HajjReady (#47), LoanReady (#32).
All five fields covered per idea, in form order.

Changes from v4: GenWatch dropped — doesn't use DSI's AI stack meaningfully, not a platform investment. LoanReady returns as #3 — bank enterprise buyers, LLM multi-turn reasoning as core differentiator, durable regardless of external events.

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

# IDEA 2 — HajjReady: Hajj & Umrah Preparation Agent

## Title
HajjReady — Hajj & Umrah Preparation Agent

## The Problem
Bangladesh sends over 100,000 pilgrims to Saudi Arabia for Hajj annually, and a larger number for Umrah year-round. For most families, this is the most significant journey of their lives — often saved for over a decade.

The preparation process is one of the most document-intensive undertakings a Bangladeshi family will ever manage: meningitis and other vaccinations with specific timing windows, medical fitness certificates from designated hospitals, passport validity requirements, visa processing through the registered Hajj agency, mahram documentation for women, specific baggage restrictions, and pre-departure religious preparation. Each step has its own deadline, its own office, and its own format requirement.

Most pilgrims piece this together from what their agency tells them, what relatives who went before remember, and what Facebook groups say. Agencies vary enormously in how thoroughly they communicate requirements. Every year, pilgrims are turned away at the airport or have visas rejected for preventable errors — a missed vaccination window, a recently renewed passport rejected by Saudi authorities, a missing mahram document. For a family that saved for this for ten years, that failure is not an inconvenience. It is a devastation.

## The Agent Idea
A WhatsApp agent that Hajj and Umrah agencies distribute to every registered pilgrim. The pilgrim registers once: travel date, whether Hajj or Umrah, and passport details. The agent becomes their personal preparation calendar.

It maps every required step to a deadline and sends reminders as each window opens: "মেনিনজাইটিস টিকার উইন্ডো শুরু হয়েছে — শেষ তারিখ ১৫ দিন পরে। অনুমোদিত হাসপাতাল: ..." It walks through each document requirement in plain Bangla, explains what each means and where to get it, and confirms completion as each step is done.

For women: it explains the mahram requirement, which family relationships qualify, and what documentation Saudi authorities require. For first-time pilgrims: what ihram rules mean practically, what to pack, what is prohibited. Not religious instruction — practical preparation.

At 30, 14, and 7 days before departure it sends a full readiness check: what is confirmed complete, what is still outstanding, what can still be fixed. The pilgrim arrives at the airport prepared. The agency has fewer last-minute crises the night before departure.

Typical interaction: Pilgrim registers with travel date. Agent maps their preparation timeline. Three weeks before departure: "আপনার ভিসা আবেদনের জন্য ২টি ডকুমেন্ট এখনও কনফার্ম হয়নি — মেডিকেল ফিটনেস সার্টিফিকেট এবং ব্যাংক স্টেটমেন্ট। বিস্তারিত দেখতে 'লিস্ট' লিখুন।"

A pilgrim who misreports their document status only misleads themselves — Saudi immigration verifies everything at the border.

## Who Benefits
Hajj agencies are the buyers. Bangladesh has 500+ licensed Hajj agencies, each handling hundreds of pilgrims per season. An agency distributing this agent to enrolled pilgrims differentiates from competitors offering the same paper briefing. A pilgrim who arrives prepared does not call the agency in a panic the night before departure.

At BDT 500–1,500 per pilgrim per travel cycle, an agency handling 500 pilgrims per Hajj season = BDT 250,000–750,000 per season per agency. 100 agencies = BDT 25–75M/year. Umrah operates year-round — same product, continuous revenue outside the Hajj window.

White-labelling (the agent answers as "XYZ Travels Hajj Assistant") is a 1-day configuration change.

## Why Now
(1) **Saudi Arabia's Vision 2030 Hajj digitisation** is tightening documentation standards — the preparation bar is rising, not falling. (2) **Bangladesh's Hajj quota has expanded** in recent years — more first-time pilgrims, higher error rate from families navigating this for the first time. (3) **No Bangla-language Hajj preparation tool exists** — the gap is filled by agency pamphlets and Facebook groups, none of which are personalised to the pilgrim's specific travel date. The knowledge base updates once per season.

## Feasibility & Scope
Pilgrim registration (travel date, Hajj or Umrah) → preparation timeline generation → deadline reminder per requirement → document checklist walkthrough → completion confirmation per item → pre-departure readiness summary.

Knowledge base: Ministry of Religious Affairs circulars, Saudi embassy visa requirements, WHO vaccination requirements, airline baggage policies — all public, updated annually. POC covers Umrah preparation for a single agency in 2 weeks. Full Hajj workflow is v1 production.

Biggest unknown: religious content sensitivity. Addressed by the agent covering practical preparation only — no religious rulings, no fiqh questions. Pilgrims are explicitly directed to their imam or agency scholar for religious guidance.

## Self-Categorization Tag
Quick Build

---

# IDEA 3 — LoanReady: Bank Loan Preparation Agent

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
