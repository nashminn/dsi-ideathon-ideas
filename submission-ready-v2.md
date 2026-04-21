# Submission-Ready Answers — DSI Ideathon 2026 (v2)

Copy-paste directly into the form. Three ideas: FieldLedger (#24), LoanReady (#32), AdmitPath (#39).
All five fields covered per idea, in form order.

Changes from v1: #24 rewritten with borrower confirmation loop (fraud-resistant framing). #35 GreenPass replaced by #39 AdmitPath — GreenPass relied entirely on self-reported data from users with strong incentive to lie.

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

# IDEA 3 — AdmitPath: University Admission Guidance Agent

## Title
AdmitPath — University Admission Guidance Agent

## The Problem
Every year, approximately 1.3 million Bangladeshi students navigate one of the most stressful and confusing admission processes in the world. Public university admissions — Dhaka University, BUET, medical colleges — run on separate, decentralised schedules with different exam dates, different eligibility criteria, different subject combinations, and different seat counts. Private university admissions layer on top with their own deadlines and scholarship criteria.

A Science group student misses the DU 'Ka' unit application deadline because they didn't know it opened two weeks before the 'Kha' unit. They find out from a Facebook comment three days after it closed. They sit out a year.

This is not unusual. Each university publishes its own circular on its own website on its own schedule. Eligibility criteria differ by unit, group, and GPA combination. Students piece this together from Facebook groups, coaching centre noticeboards, and rumour — all of which are noisy, unverified, and generic. A wrong assumption or a missed notification costs a full year. Approximately 1.3 million students go through this every year with no personalised, reliable information source.

## The Agent Idea
A WhatsApp agent that a student registers with once: their HSC result (GPA, group — Science/Commerce/Humanities), preferred subjects, and target university type. The agent becomes their personal admission calendar: it maps which universities and units they are eligible for, sends reminders before application deadlines and admit card download dates, and answers eligibility questions in plain Bangla — "বিজ্ঞান বিভাগ থেকে ঢাকা বিশ্ববিদ্যালয়ের 'খ' ইউনিটে আবেদন করতে কি লাগবে?"

It does not submit applications. It makes sure students know exactly what to do and when, so that no one loses a year to a missed deadline or an incorrect assumption.

Typical interaction: Student registers in July after HSC results. Agent maps their profile to eligible universities and units. In August when DU 'Ka' unit application opens: "ঢাকা বিশ্ববিদ্যালয় 'ক' ইউনিট আবেদন শুরু — শেষ তারিখ ১৫ আগস্ট। আপনার SSC ও HSC সনদের স্ক্যান কপি লাগবে।"

A student who misreports their GPA to get a more favourable eligibility result only misleads themselves — the university verifies at admission. There is nothing to game here.

## Who Benefits
Primary buyers are coaching centres, not individual students. Bangladesh has 50,000+ coaching centres, each serving hundreds of enrolled students going through exactly this process. Coaching centres already spend on student management tools, SMS broadcasts, and printed materials — this replaces a line item they have. A coaching centre offering personalised admission calendars differentiates from competitors offering the same generic WhatsApp broadcast. At BDT 5,000–20,000/month per coaching centre, 500 clients = BDT 2.5–10M/month recurring. The coaching centre channel provides immediate distribution without a consumer marketing budget.

Secondary beneficiaries: the 1.3 million HSC candidates annually and their families, who gain a reliable, personalised information source in a process currently served only by noise and rumour.

Freemium is also viable — basic deadline reminders free, premium tier (BDT 150–300/year per student) for personalised eligibility analysis and document checklists — but the coaching centre B2B channel is the faster path to revenue and fits DSI's enterprise sales model.

## Why Now
(1) **LLM reasoning over structured knowledge bases** — reliable enough to map a student's GPA and subject group against unit-specific eligibility rules with multiple conditional criteria. This required hand-coded rule engines before; now it's a knowledge base and a prompt. (2) **No Bangla-language conversational admission tool exists** — the gap is currently filled by Facebook groups and generic WhatsApp broadcasts, both unreliable. (3) **Annual update cycle** — the knowledge base refreshes once a year after HSC results and circular publication. Low maintenance, high stickiness.

## Feasibility & Scope
Student profile registration → eligibility mapping against university/unit criteria database → personalised deadline calendar → reminder push at configurable intervals → Q&A over eligibility knowledge base. POC covers 5 major public universities (DU, BUET, DMCH, Jahangirnagar, Rajshahi) in 2 weeks.

Needs: WhatsApp Business API, LLM API, structured eligibility and deadline database built from publicly available admission circulars. No government API required — all data sourced manually from published circulars and updated annually.

Biggest unknown: admission circular release timing varies year to year. Addressed with a lightweight web scraper on university admission portals that triggers a knowledge base update when a new circular is detected. Coaching centre white-labelling (agent answers as "XYZ Academy Admission Assistant") is a 1-day configuration change.

## Self-Categorization Tag
Quick Build
