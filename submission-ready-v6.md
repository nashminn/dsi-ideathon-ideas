# Submission-Ready Answers — DSI Ideathon 2026 (v6)

Copy-paste directly into the form. Three ideas: FieldLedger (#24), HajjReady (#47), LoanReady (#32).
All five fields covered per idea, in form order.

Changes from v5:
- FieldLedger: insurance field agents added as adjacent market in Who Benefits; Why Now #3 sharpened with specific MRA digital reporting obligation.
- HajjReady: Agent Idea expanded to make conditional intelligence explicit — addresses "just a reminder app" challenge directly in the submission.
- LoanReady: "PDF vs agent" argument moved from Feasibility into Agent Idea as a positive statement; NBFIs foregrounded as easier first sale; defensive framing in Feasibility removed.

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

Bangladesh has 700+ MRA-licensed MFIs. At BDT 200–400 per officer per month, a single 150-officer MFI generates BDT 30,000–60,000/month. At 50 clients: BDT 150–300M/year recurring.

Adjacent market: insurance company field agents — MetLife BD, Pragati Life, Delta Life, Green Delta — collect premiums door-to-door with an identical workflow: agent visits policyholder, collects cash, logs it manually, supervisor has no real-time visibility. The fraud vector is identical; the agent architecture is identical; insurance IT budgets are larger than small MFIs. The same product serves both sectors without rebuilding.

Beyond BD: microfinance and insurance premium field collection is a global problem — Kenya, Philippines, India, Cambodia all run the same paper notebook.

## Why Now
Three things converge: (1) **Bangla NLU (LLM reasoning)** — models now reliably parse informal Bangla voice and text into structured ledger entries; rule-based systems never could. (2) **WhatsApp penetration** among field officers and borrowers is now high enough that a two-way confirmation interaction is practical, not hypothetical. (3) **MRA's digital reporting obligation** — MRA now requires licensed MFIs to maintain auditable electronic records of field collections. Most MFIs cannot currently meet this requirement on paper. This agent is the compliance solution, not just an efficiency tool. No incumbent software exists to displace.

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

The preparation process is one of the most document-intensive undertakings a Bangladeshi family will ever manage: meningitis and other vaccinations with specific timing windows, medical fitness certificates from designated hospitals, passport validity requirements, visa processing through the registered Hajj agency, mahram documentation for women travelling without a close male relative, specific baggage restrictions, and pre-departure religious preparation. Each step has its own deadline, its own office, and its own format requirement.

Most pilgrims piece this together from what their agency tells them, what relatives who went before remember, and what Facebook groups say. Agencies vary enormously in how thoroughly they communicate requirements. Every year, pilgrims are turned away at the airport or have visas rejected for preventable errors — a missed vaccination window, a recently renewed passport rejected by Saudi authorities, a missing document. For a family that saved for this for ten years, that failure is a devastation.

## The Agent Idea
A WhatsApp agent that Hajj and Umrah agencies distribute to every registered pilgrim. The pilgrim registers once: travel date, whether Hajj or Umrah, passport issue date, and whether they are travelling with a mahram. The agent maps their specific profile against a preparation timeline with conditional logic — this is not a generic reminder broadcast.

A passport issued within the last 6 months triggers a specific advisory about Saudi entry requirements that a 3-year-old passport does not. A woman registering without a male relative follows a different document flow — the agent identifies which family relationships qualify for the mahram exemption under Saudi regulations and what paperwork each requires. A pilgrim with a pre-existing medical condition flagged during registration is routed to additional health screening steps not on the standard checklist. A Hajj pilgrim has a different and more complex preparation sequence than an Umrah pilgrim; the agent handles both without conflating them.

As each window opens, the agent sends a contextual reminder: "মেনিনজাইটিস টিকার উইন্ডো শুরু হয়েছে — শেষ তারিখ ১৫ দিন পরে। অনুমোদিত হাসপাতাল: ..." It confirms completion as each step is done. At 30, 14, and 7 days before departure it sends a full readiness check — what is complete, what is outstanding, what can still be fixed.

The pilgrim arrives at the airport prepared. The agency has fewer last-minute crises.

Typical interaction: Pilgrim registers in April for a July Umrah. Agent generates their specific timeline. Mid-May: "আপনার পাসপোর্ট ইস্যু তারিখ ৫ মাস আগে — সৌদি কর্তৃপক্ষ সর্বনিম্ন ৬ মাসের বৈধতা চায়। ভ্রমণের আগে পাসপোর্ট নবায়ন করতে হবে।" That's not a reminder — that's a personalised catch that a paper briefing misses entirely.

A pilgrim who misreports their document status only misleads themselves — Saudi immigration verifies everything at the border.

## Who Benefits
Hajj agencies are the buyers. Bangladesh has 500+ licensed Hajj agencies, each handling hundreds of pilgrims per season. An agency distributing this agent to enrolled pilgrims differentiates from competitors offering the same paper briefing. A pilgrim who arrives prepared does not call the agency in a panic the night before departure.

At BDT 500–1,500 per pilgrim per travel cycle, an agency handling 500 pilgrims per Hajj season = BDT 250,000–750,000 per season per agency. 100 agencies = BDT 25–75M/year. Umrah operates year-round — same product, continuous revenue outside the Hajj window.

White-labelling (the agent answers as "XYZ Travels Hajj Assistant") is a 1-day configuration change. Agencies with strong brands pay a premium for branded delivery.

## Why Now
(1) **Saudi Arabia's Vision 2030 Hajj digitisation** is tightening documentation standards and reducing tolerance for manual errors at the border — the preparation bar is rising, not falling. (2) **Bangladesh's Hajj quota has expanded** in recent years — more first-time pilgrims, more agencies, higher error rate from families navigating this for the first time. (3) **No Bangla-language Hajj preparation tool exists** — the gap is filled by agency pamphlets and Facebook groups, none of which are personalised to the pilgrim's specific travel date, passport situation, or travel companion status. The knowledge base (vaccination requirements, visa specifications, airline rules) is publicly available and updates once per season.

## Feasibility & Scope
Pilgrim registration (travel date, Hajj or Umrah, passport issue date, mahram status) → conditional preparation timeline generation per pilgrim profile → deadline reminder per requirement → document checklist walkthrough → completion confirmation per item → pre-departure readiness summary.

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

The difference from a PDF checklist is the follow-up. A checklist tells the applicant their trade licence must be valid — the agent asks if it is, and when the answer is "it expired last month," it tells them exactly which city corporation window to visit, how long renewal takes, and to come back when it's done. The intelligence is in the conditional response to what the applicant actually has, not the list of what they need.

The agent doesn't apply on the applicant's behalf — it makes sure they're ready before they go. Banks are the primary buyer: they embed or distribute the agent to reduce incomplete application volume across their branches.

An applicant who lies to this agent — claiming they have documents they don't — only hurts themselves. The bank verifies everything independently. The agent makes no credit decision and stores no sensitive data. There is nothing to game.

## Who Benefits
NBFIs are the natural first sales target — hundreds of non-bank financial institutions in Bangladesh operate SME and personal loan products with the same document requirements and the same incomplete application problem, but shorter procurement cycles than scheduled banks. The first 10 NBFI clients build the case for the bank sales conversation.

Banks and NBFIs together are the paying customers — a bank embedding this agent on their website or distributing it through branch staff reduces incomplete applications and lowers the per-approved-loan processing cost. Bangladesh has 60+ scheduled banks and hundreds of NBFIs. At BDT 50,000–200,000/month per institution, 30 clients generates BDT 1.5–6M/month recurring.

Secondary beneficiaries: millions of SME owners and individuals who apply for loans annually and lose weeks to rejection cycles caused by preventable document errors. They save time; institutions save processing cost; both have strong motivation to use and distribute the agent.

## Why Now
(1) **LLM multi-turn reasoning** — reliable enough to conduct a contextual readiness assessment, asking the right follow-up based on what the applicant already has. This became practical in the last 18 months; it was not before. (2) **Bangladesh Bank's financial inclusion mandate** — institutions have regulatory incentive to approve more qualified applicants, not just reject incomplete ones faster; this agent serves both goals simultaneously. (3) **Zero API dependency in MVP** — runs entirely on a manually curated knowledge base built from public bank websites and branch brochures. No integration risk, no bank system access required to launch.

## Feasibility & Scope
A 2-week POC: user states bank and loan type → agent loads requirements for that combination → conversational readiness check, one item at a time → gap summary at the end.

Needs: WhatsApp Business API, LLM API, a structured knowledge base of document requirements (5 institutions × 3 loan types to start). No bank API, no government system, no user data stored.

Biggest unknown: knowledge base currency as institutions update requirements. Quarterly review cycle covers this in MVP; an institutional partnership replaces it with a direct documentation feed, converting a maintenance liability into a distribution asset.

## Self-Categorization Tag
Quick Build
