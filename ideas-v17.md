# DSI Ideathon 2026 — Ideas (v17) — Current Events Response

Two ideas generated in direct response to live crises: Strait of Hormuz blockade driving fuel shortages, and US tariffs on Bangladesh exports disrupting the RMG sector.

---

## Idea 49

**Title**
GenWatch — Generator Fuel Inventory & Runtime Management Agent

**The Problem**
Bangladesh imports nearly all its fuel through shipping routes that pass the Strait of Hormuz. With the strait blocked, diesel supply is constrained and prices are spiking. Every factory, hospital, cold storage facility, and office building in Bangladesh that runs a backup generator is now managing a fuel inventory problem they were not designed to handle.

The default approach: a supervisor checks the tank level by eye, makes a phone call when it looks low, and hopes the fuel truck arrives before the generator dies. Under normal supply conditions this works poorly. Under a fuel shortage it fails completely — procurement windows are narrow, prices fluctuate daily, and a factory that runs out mid-shift loses an entire production run.

Most facilities have no system to track actual fuel consumption rates, predict remaining runtime, or plan procurement with enough lead time for current market conditions. A 500-person garment factory running three generators across two shifts consumes diesel at a rate that varies with production load. The facility manager does not know that rate. They guess. When supply is tight, guessing wrong is catastrophic.

Hospitals face this at a different level of severity — a generator failure during surgery or ICU operation is not a production loss, it is a patient safety incident. Cold storage operators managing temperature-sensitive medicine or food face full inventory loss. Telecom tower operators face network outage. The stakes vary but the problem is identical: nobody knows exactly how much fuel they have, how long it will last, or when they need to move.

**The Agent Idea**
A WhatsApp agent for facility managers. The agent is set up once with each generator's fuel tank capacity and typical load profile. From there, management is two daily messages: fuel intake ("received 300L diesel, tank now 800L") and generator runtime ("gen A on since 7am, off at 6pm"). The agent maintains a running fuel ledger, calculates actual consumption rate from the last 7 days of logs, and projects runtime on current inventory: "বর্তমান ব্যবহারের হারে আপনার ডিজেল আরও ৩.২ দিন চলবে। আগামীকালের মধ্যে অর্ডার করুন।"

When inventory drops below a configurable threshold — set higher during shortage periods — the agent sends an escalating alert: facility manager first, then the admin head, then the building owner. It also tracks fuel cost per operating hour over time, giving procurement a trend line to negotiate against suppliers.

For multi-site operators — a factory group running 5 plants, a hospital chain, a telecom tower operator managing 200 sites — the agent aggregates across all locations, flags which sites are critical, and generates a priority procurement list. The manager makes one procurement decision covering all sites instead of receiving five panicked phone calls from five site supervisors.

Typical interaction: Supervisor: "জেনারেটর A সকাল ৭টায় চালু, বিদ্যুৎ এলে বন্ধ হবে।" Evening: "বিদ্যুৎ এসেছে, জেন A বন্ধ — ১১ ঘণ্টা চলেছে।" Agent logs 11 operating hours, updates consumption rate, recalculates projection. 8pm summary to facility manager: "আজ ১৮৫ লিটার খরচ হয়েছে। মজুদ: ৬১৫ লিটার। প্রজেকশন: ৩.৩ দিন।"

**Who Benefits**
Factory owners and facility managers at manufacturing units — garment, pharmaceuticals, food processing, printing — are the immediate buyers. The crisis makes willingness to pay acute: a single avoidable production halt costs more than years of subscription. Hospital management at private facilities (Square, Evercare, United, Ibn Sina) have patient safety motivation on top of cost motivation. Cold storage operators managing medicine or frozen food face total inventory loss from an unmanaged fuel-out. BTRC-licensed telecom tower operators (Edotco, Summit Tower) managing hundreds of diesel-powered towers need exactly this multi-site aggregation.

Revenue: BDT 1,000–3,000/month per facility for single-site; BDT 10,000–30,000/month for multi-site operators covering all locations. At 2,000 single-site clients and 50 multi-site operators: BDT 2.5–7.5M/month. The crisis creates the initial market; the habit of data-driven fuel management persists after supply normalises.

**Why Now**
The Strait of Hormuz blockade is not a future scenario — it is the current operational reality Bangladesh's fuel-dependent businesses are navigating today. Procurement windows are narrow. Prices are volatile. A tool that gives facility managers accurate runtime projections and early procurement alerts has immediate, quantifiable value right now. Every week without it is a week of guessing. The product sells itself in the current environment without a single cold call.

**Feasibility & Scope**
Generator setup (one-time: tank capacity, load profile) → daily fuel intake log → runtime log → consumption rate calculation → runtime projection → threshold alert → weekly cost summary.

Pure arithmetic — no heavy LLM inference required per interaction. LLM handles message parsing only ("received 300L" → intake event). POC: single factory with 2 generators, 1 week to build. Multi-site aggregation adds 1 week. Needs: WhatsApp Business API, LLM API (light, for message parsing). No hardware integration required — all inputs are human-logged.

Biggest unknown: supervisor discipline in logging consistently. Addressed by: (1) the agent sends a daily 8pm prompt if no runtime log was received that day — missed logs are visible gaps that alert the manager, (2) inconsistent logging produces obviously wrong projections that motivate the supervisor to log correctly.

**Tag:** Quick Build

---

## Idea 50

**Title**
PivotPath — Export Market Diversification Agent for RMG Factories

**The Problem**
The United States imposed a 37% tariff on Bangladesh's garment exports in 2025. Bangladesh sends roughly $8–9 billion in RMG goods to the US annually — approximately 18% of total garment exports. A 37% tariff does not reduce that trade gradually. It stops it. Buyers who sourced from Bangladesh for US-bound orders have already or will shortly move those orders to Vietnam, Cambodia, or India, where tariff exposure is lower.

Factory owners and export managers who built their order books around US buyers now face two choices: find replacement buyers in alternative markets, or lose the capacity utilisation that keeps their factory financially viable.

Alternative markets exist. The EU gives Bangladesh near-zero duty access under EBA (Everything But Arms). Japan's EPA with Bangladesh provides preferential rates. Australia and Canada have similar frameworks. These markets are large, they buy the same product categories, and Bangladesh's cost structure remains competitive in them. The problem is that most factory export managers do not know the specific duty rates, compliance requirements, and active sourcing patterns in these markets in enough detail to act on them. They know US buyers. They built relationships with US buyers. The alternative market landscape is unfamiliar territory.

Simultaneously: EU buyers sourcing for European retail have specific compliance requirements that US buyers did not — REACH chemical compliance, mandatory supply chain traceability under CSDDD, specific social audit frameworks. A factory pivoting from US to EU buyers needs to know its compliance gaps before it pitches a European buyer, or it will spend months in a sourcing conversation that ends at the compliance check.

**The Agent Idea**
A WhatsApp agent for factory export managers and buying house sourcing teams. The factory registers its product categories (woven bottoms, knitwear, denim, activewear), current certifications held (OEKO-TEX, GOTS, SEDEX, BSCI), and target price tier. The agent does three things:

First, it answers specific market intelligence questions on demand: "EU duty rate for HS 6109.10?" "What certifications does Inditex require for new BD suppliers?" "Which trade shows in Q3 2026 are most relevant for European knitwear buyers?" Answers drawn from a curated knowledge base of preferential trade agreements, major buyer compliance requirements, and sourcing event calendars — all publicly available information, assembled into one place.

Second, it runs a compliance gap analysis: given the factory's current certification profile, what is missing to approach EU buyers vs Japan buyers vs Australian buyers? For each gap, what is the certification pathway, cost estimate, and timeline? The factory knows exactly what to fix before entering a new market conversation.

Third, it sends a weekly digest: which EU and Japanese brands have publicly announced increased Bangladesh sourcing commitments, which sustainability certifications are becoming table-stakes in target markets, which sourcing events are upcoming with registration deadlines.

Typical interaction: Export manager: "H&M-এ নতুন সাপ্লায়ার হতে কী কী লাগবে?" Agent: "H&M-এর জন্য HIGG FEM, SEDEX SMETA 4-pillar, এবং ZDHC MRSL compliance লাগবে। আপনার কাছে OEKO-TEX আছে — সেটা ZDHC-র অর্ধেক পথ। বাকি গ্যাপ এবং খরচ দেখতে চান?"

**Who Benefits**
Factory export managers and owners at Bangladesh's 4,500+ export-oriented garment factories facing US tariff exposure are the immediate buyers — the crisis creates urgent demand for exactly this intelligence. Buying houses managing multi-factory sourcing for international brands are equally affected and have budget to pay for market intelligence tools.

BGMEA and BKMEA are natural collective buyers — they can distribute this to their member base as a crisis response service, the same way they distributed COVID recovery guidance. At BDT 3,000–8,000/month per factory for individual subscription, or BDT 500,000–1,000,000/month for a BGMEA-distributed license covering member factories, the revenue case is immediate.

Internationally: every tariff shock creates the same pivot need. If Vietnam faces a future tariff escalation, or if Cambodia's GSP access is restricted, the same product applies without rebuilding.

**Why Now**
The tariff shock is not coming — it already happened. Factories that were 30–40% US-exposed are operating under an existential constraint today. The window to pivot is now, before order books are empty and production lines are idle. A factory that successfully pivots to EU buyers in the next 6 months survives. One that waits loses the capacity utilisation that makes the pivot possible. The urgency is already in the market — DSI does not need to create demand, it needs to show up while demand is acute.

**Feasibility & Scope**
Knowledge base of preferential trade agreements (EBA, Japan EPA, Canada PTA), major buyer compliance requirements (H&M, Inditex, PVH, Fast Retailing), certification pathways and costs, sourcing event calendar → certification gap analysis per factory profile → weekly digest generation → on-demand Q&A.

Knowledge base is entirely publicly available: WTO tariff schedules, buyer sustainability portals, BGMEA compliance guides. POC: EU market pivot guidance for knitwear factories, covering 5 major EU buyers, 2 weeks. Needs: WhatsApp Business API, LLM API, curated knowledge base. No API integrations required.

Biggest unknown: knowledge base currency — buyer requirements update quarterly. Addressed by: a quarterly review cycle and, once BGMEA partnership is in place, a direct feed from their trade intelligence team who track this already. US tariff reversal would reduce urgency but not eliminate it — market diversification is sound strategy regardless of tariff status.

**Tag:** Quick Build
