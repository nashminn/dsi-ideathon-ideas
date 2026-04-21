# Submission-Ready Answers — DSI Ideathon 2026 (v4)

Copy-paste directly into the form. Three ideas: GenWatch (#49), HajjReady (#47), FieldLedger (#24).
All five fields covered per idea, in form order.

Changes from v3: FieldLedger unchanged. LoanReady and ClaimStart replaced by GenWatch and HajjReady — GenWatch scores highest in the full pool of 50 ideas; HajjReady scores highest on originality and retains second place.

---

# IDEA 1 — GenWatch: Generator Fuel Inventory & Runtime Agent

## Title
GenWatch — Generator Fuel Inventory & Runtime Agent

## The Problem
Bangladesh imports nearly all its fuel through shipping routes passing the Strait of Hormuz. With that route disrupted, diesel is scarce, prices are spiking, and every factory, hospital, cold storage facility, and office building running a backup generator is managing a fuel inventory problem they were not designed for.

The default approach: a supervisor checks the tank level by eye and calls someone when it looks low. Under normal supply conditions this works poorly. Under a shortage it fails — procurement windows are narrow, prices shift daily, and a factory that runs out mid-shift loses an entire production run. A hospital that loses power during a procedure faces something worse.

Most facilities have no system to track actual consumption rates, predict remaining runtime, or plan procurement with enough lead time. A factory running three generators across two shifts consumes diesel at a rate that varies with production load. The facility manager does not know that rate precisely. They guess. Right now, guessing wrong is catastrophic.

This is not a new problem — Bangladesh has had rolling load shedding for thirty years. The crisis has made it acute. Every enterprise in the country with a generator is living this today.

## The Agent Idea
A WhatsApp agent for facility managers. Set up once with each generator's tank capacity and typical load. From there, two daily inputs: fuel intake ("received 300L diesel") and generator runtime ("gen A on since 7am, off at 6pm"). The agent maintains a running fuel ledger, calculates actual consumption rate from the past 7 days, and projects runtime on current inventory: "বর্তমান ব্যবহারের হারে আপনার ডিজেল আরও ৩.২ দিন চলবে। আগামীকালের মধ্যে অর্ডার করুন।"

When inventory drops below a configurable threshold, the agent sends escalating alerts — facility manager first, then the admin head, then the owner. It tracks fuel cost per operating hour, giving procurement a trend line to negotiate against.

For multi-site operators — a factory group running five plants, a hospital chain, a telecom tower operator managing hundreds of sites — the agent aggregates across all locations, flags which sites are critical, and generates a priority procurement list. Five panicked phone calls from five site supervisors become one structured summary.

Typical interaction: Supervisor logs generator start in the morning, shutdown in the evening. Agent calculates hours run, updates fuel projection, sends an 8pm summary: "আজ ১৮৫ লিটার খরচ হয়েছে। মজুদ: ৬১৫ লিটার। প্রজেকশন: ৩.৩ দিন।" Facility manager orders fuel the next morning with two days to spare.

The agent is pure arithmetic — no AI complexity per interaction. The LLM handles only message parsing. Everything else is addition and division.

## Who Benefits
Factory owners and facility managers at manufacturing units are the immediate buyers — a single avoidable production halt costs more than years of subscription. Private hospital management (Square, Evercare, United, Ibn Sina) has patient safety motivation on top of cost. Cold storage operators managing medicine or frozen food face total inventory loss from an unmanaged fuel-out. Telecom tower operators (Edotco, Summit Tower) need multi-site aggregation across hundreds of diesel-powered sites.

Revenue: BDT 1,000–3,000/month per single facility; BDT 10,000–30,000/month for multi-site operators. At 2,000 single-site clients and 50 multi-site operators: BDT 3.5–7.5M/month. The crisis creates initial adoption; the habit of data-driven fuel management persists after supply normalises.

## Why Now
The Strait of Hormuz disruption is not a future scenario — it is the current operational reality Bangladesh's fuel-dependent businesses are navigating today. Every week without a fuel runtime system is a week of guessing under shortage conditions. The product does not need to be sold — facility managers are already looking for exactly this. DSI shows up while demand is acute, builds the client base, and retains it permanently.

Beyond the crisis: Bangladesh has had chronic power instability for three decades. Generator management is a permanent operational reality for every industrial and commercial facility in the country. The crisis created the market entry window; the structural problem sustains the revenue.

## Feasibility & Scope
Generator setup (one-time: tank capacity, load profile) → daily fuel intake log → runtime log → consumption rate calculation → runtime projection → threshold alert → weekly cost summary.

POC: single factory with 2 generators, 1 week to build. Multi-site aggregation adds 1 week. Needs: WhatsApp Business API, LLM API (light — message parsing only). No hardware integration, no government system, no third-party API required.

Biggest unknown: supervisor discipline in logging consistently. Addressed by: the agent sends a daily prompt if no runtime log is received — missing logs appear as visible gaps in the projection, which motivates the supervisor to log correctly. Inconsistent logging produces obviously wrong projections that self-correct adoption.

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
Hajj agencies are the buyers. Bangladesh has 500+ licensed Hajj agencies, each handling hundreds of pilgrims per season. An agency distributing this agent to enrolled pilgrims differentiates from competitors offering the same paper briefing. A pilgrim who arrives prepared does not call the agency in a panic the night before departure — that alone has direct value to the agency's operations team.

At BDT 500–1,500 per pilgrim per travel cycle, an agency handling 500 pilgrims per season = BDT 250,000–750,000 per Hajj season per agency. 100 agencies = BDT 25–75M/year. Umrah operates year-round — same product, continuous revenue outside the Hajj window.

White-labelling (the agent answers as "XYZ Travels Hajj Assistant") is a 1-day configuration change. Agencies with strong brands will pay a premium for branded delivery.

## Why Now
(1) **Saudi Arabia's Vision 2030 Hajj digitisation** is tightening documentation standards and reducing tolerance for manual errors at the border — the preparation bar is rising, not falling. (2) **Bangladesh's Hajj quota has expanded** in recent years — more first-time pilgrims, more variation in agency preparation quality, higher error rate from families navigating this for the first time. (3) **No Bangla-language Hajj preparation tool exists** — the gap is currently filled by agency pamphlets, YouTube videos, and Facebook groups, none of which are personalised to the pilgrim's specific travel date and situation. The knowledge base (vaccination requirements, visa specifications, airline rules) is publicly available and updates once per season.

## Feasibility & Scope
Pilgrim registration (travel date, Hajj or Umrah) → preparation timeline generation → deadline reminder per requirement → document checklist walkthrough → completion confirmation per item → pre-departure readiness summary.

Knowledge base: Ministry of Religious Affairs circulars, Saudi embassy visa requirements, WHO vaccination requirements for Saudi Arabia, airline baggage policies — all public, updated annually. POC covers Umrah preparation for a single agency in 2 weeks (year-round travel, simpler checklist than Hajj). Full Hajj workflow is v1 production.

Biggest unknown: religious content sensitivity. Addressed by: the agent covers practical preparation only — no religious rulings, no scholarly guidance, no fiqh questions. It explicitly directs pilgrims to their imam or agency scholar for religious questions. This keeps the agent out of religious authority territory entirely.

## Self-Categorization Tag
Quick Build

---

# IDEA 3 — FieldLedger: Microfinance Collection Agent

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
