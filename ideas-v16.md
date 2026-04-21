# DSI Ideathon 2026 — Ideas (v16)

---

## Idea 46

**Title**
VisitReady — Hospital Appointment & Patient Flow Coordination Agent

**The Problem**
A patient is told to arrive at the hospital by 6am for a scheduled radiotherapy session. They arrive on time. Then they wait two hours — not because the machine is busy, but because no one told them that arriving is only step one. Payment must be processed at the billing counter first. The receipt must be physically submitted to the radiology department. Only then is a serial number issued. Only then does the actual queue begin.

The hospital gave one arrival time. The actual workflow has three sequential steps with no feedback between them. The patient has no visibility into where they are in the process or how long each step takes. They sit in a corridor with no information.

This is the default experience at every high-volume outpatient department in Bangladesh — oncology, radiology, dialysis, physiotherapy, specialist OPD — departments where complex pre-treatment workflows mean the appointment time and the treatment time are never the same thing. The friction is not the wait itself. It is the invisible, unmanaged gap between arrival and readiness.

**The Agent Idea**
A WhatsApp agent that makes the patient's journey visible at every step, before they arrive and while they are there.

Pre-arrival: 24 hours before the appointment, the agent sends the patient the exact preparation sequence — what documents to bring, whether online payment is possible (and how), what counter to go to first, what to expect at each step. The patient arrives knowing the workflow, not discovering it on the day.

Day-of: after the patient completes billing and submits their receipt, the department desk sends a one-line update to the agent: "serial 4 issued." The agent immediately notifies the patient: "আপনি ৪ নম্বরে আছেন। আনুমানিক অপেক্ষা ৩৫ মিনিট। আপনাকে ডাকার ৫ মিনিট আগে জানানো হবে।" The patient can wait in the cafeteria, rest in their car, or stay with their companion instead of holding a plastic chair. When it is their turn: "আপনার পালা — এখন রুম ৩-এ আসুন।"

The agent removes no friction from the actual process. It removes the friction of not knowing.

Typical interaction: Patient's son messages the agent the evening before: "মা আগামীকাল রেডিওথেরাপিতে আছেন।" Agent: "সকাল ৫:৩০-এ বিলিং কাউন্টারে যান, রসিদ রেডিওলজি ডেস্কে জমা দিন। সিরিয়াল পেলে আমাকে জানান — তারপর থেকে আপডেট পাবেন।"

**Who Benefits**
Private hospital management is the buyer — patient satisfaction scores determine accreditation ratings and justify premium pricing. Long waits are the single most cited complaint in hospital satisfaction surveys. This agent does not reduce actual throughput or require any workflow change. It reduces perceived waiting misery at near-zero operational cost.

Bangladesh's premium private hospitals (Square, Evercare, United, Popular, Ibn Sina chain) are the first market. At BDT 30,000–80,000/month per hospital, 30 clients = BDT 1–2.4M/month. Applicable to any high-volume outpatient department in any country — the workflow friction is global.

**Why Now**
(1) No technology change is required at the hospital — the agent works with a single WhatsApp message from the desk clerk per patient per step; no integration, no new system. (2) JCI and NABH accreditation criteria explicitly include patient wait time management and communication. (3) Competition among premium hospitals is intensifying — patient experience is a differentiator they are actively spending on.

**Feasibility & Scope**
Pre-arrival guide delivery (templated per department type) → day-of queue position tracking via desk clerk messages → patient notification at each stage transition → arrival alert when turn is near.

POC: single department (oncology or radiology), one hospital, 2 weeks. No hospital system integration required in MVP — the agent operates entirely through WhatsApp between the desk clerk and the patient. EMR or queue management system integration is v2. Biggest unknown: desk clerk adoption of the one-message update habit. Solved by: keeping the update to a single standardised reply ("serial 4") that requires no typing beyond a number.

**Tag:** Quick Build

---

## Idea 47

**Title**
HajjReady — Hajj & Umrah Preparation Agent

**The Problem**
Bangladesh sends 100,000+ pilgrims to Saudi Arabia for Hajj annually and a larger number for Umrah throughout the year. The preparation process is one of the most document-intensive and deadline-sensitive personal undertakings a Bangladeshi family will ever manage: medical fitness certificate from a designated hospital, meningitis and other required vaccinations with specific timing windows, passport validity requirements, visa application through the registered Hajj agency, bank account and BDT denomination requirements, specific baggage allowances, mahram documentation for women travelling without a close male relative, and the ihram and religious protocol preparation that begins before departure.

Each of these has its own deadline, its own office to visit, and its own format requirement. A missed vaccination window means a missed visa. A passport renewed too recently may be rejected. Most pilgrims piece this together from what their agency tells them, what relatives who went before remember, and what Facebook groups say. Agencies vary enormously in how well they communicate requirements. Every year, pilgrims are turned away at the airport or have visas rejected for preventable documentation errors. For a family that has saved for this trip for a decade, that failure is devastating.

**The Agent Idea**
A WhatsApp agent that a Hajj or Umrah agency distributes to every registered pilgrim. The pilgrim registers their travel date, passport details, and whether they are travelling Hajj or Umrah. The agent becomes their personal preparation calendar: it maps every required step to a deadline, sends reminders as each window opens ("মেনিনজাইটিস টিকার শেষ তারিখ আগামী ১৫ দিনে — এই হাসপাতালগুলো অনুমোদিত: ..."), walks through document checklists one item at a time, explains exactly what each requirement means in plain Bangla, and confirms readiness as each step is completed.

For women: it explains the mahram requirement, which family relationships qualify, and what documentation Saudi authorities require. For first-time pilgrims: it covers ihram rules, what is permitted and prohibited, and what to pack — not as religious instruction, but as practical preparation.

At 30, 14, and 7 days before departure, the agent sends a full checklist review: what is confirmed complete, what is still outstanding, and what can still be fixed. The pilgrim arrives at the airport with every document ready. The agency has fewer last-minute crises.

**Who Benefits**
Hajj agencies are the buyers — Bangladesh has 500+ licensed Hajj agencies. They distribute this agent to their enrolled pilgrims as a value-added service. An agency offering a personalised preparation assistant differentiates from competitors offering the same briefing pamphlet. A pilgrim who arrives prepared does not call the agency in a panic the night before departure. At BDT 500–1,500 per pilgrim per travel cycle, an agency sending 500 pilgrims per year = BDT 250,000–750,000 per agency per Hajj season. 100 agencies = BDT 25–75M/year (seasonal but recurring annually).

Secondary: Umrah travel operates year-round — same product, continuous revenue.

**Why Now**
(1) **Saudi Arabia's Vision 2030 Hajj digitisation push** is tightening documentation requirements and reducing tolerance for manual errors — the preparation bar is rising, not falling. (2) **Bangladesh's Hajj quota has expanded** — more pilgrims means more agencies, more variation in preparation quality, and more families who have never done this before. (3) **No Bangla-language Hajj preparation tool exists** — preparation content is scattered across agency pamphlets, YouTube videos, and Facebook groups, all of which are unverified and generic. The knowledge base (vaccination requirements, document specifications, airline baggage rules) is stable and publicly available.

**Feasibility & Scope**
Pilgrim registration (travel date, type — Hajj/Umrah) → preparation timeline generation → deadline reminder push per requirement → document checklist walkthrough → completion confirmation per item → pre-departure readiness summary.

Knowledge base: Ministry of Religious Affairs circulars, Saudi embassy visa requirements, WHO vaccination requirements for Saudi Arabia, airline baggage policies — all public, updated annually. POC covers Umrah preparation (year-round, simpler checklist than Hajj) for a single agency, 2 weeks. Hajj-specific workflow (more complex, seasonal) is the full v1. No government API required — all information is sourced from published circulars.

Biggest unknown: religious content sensitivity — the agent covers practical preparation only, not religious rulings or scholarly guidance. It explicitly refers pilgrims to their imam or agency scholar for fiqh questions. This keeps the agent out of religious authority territory entirely.

**Tag:** Quick Build

---

## Idea 48

**Title**
InspectionReady — Factory Labour Law Compliance Agent

**The Problem**
Bangladesh's Department of Inspection for Factories and Establishments (DIFE) has the authority to inspect any registered factory at any time. When they arrive, they check for a specific set of documentation: appointment letters for all workers, a leave register, a wages register showing payment records, a muster roll, a service book per worker, an accident register, a fire safety certificate, and several others. Most small and mid-sized factories — garment accessories units, printing presses, food processors, furniture makers — do not have these in order. Not because the owner doesn't care, but because they don't know exactly what is required, and no one told them what "ready" looks like until an inspector is standing at the door.

A DIFE violation notice leads to fines, closure orders, and — for export-oriented factories — the risk of buyer audit failure that can cancel a supply contract. The financial consequence of an inspection failure is orders of magnitude larger than the cost of maintaining the required records.

**The Agent Idea**
A WhatsApp agent that turns DIFE's inspection checklist into a live compliance dashboard the factory owner manages through their phone. The owner registers their factory type and worker count. The agent maps the exact compliance requirements for that factory category under the Bangladesh Labour Act 2006 and its 2018 amendments — which registers are mandatory, what format they must be in, what must be updated and when. It checks in monthly: "এই মাসে মজুরি রেজিস্টার আপডেট হয়েছে?" Owner confirms or flags an issue. For items with renewal deadlines — fire safety certificate, boiler certificate, factory licence — it sends reminders 30 and 7 days in advance.

When an inspection is announced (or when the owner suspects one is coming), they can trigger a readiness check: the agent runs through every checklist item, flags what is missing or out of date, and tells them exactly what to do to close each gap. The owner arrives at the inspection with their documentation folder in order.

The agent does not interact with DIFE. It does not file anything on behalf of the factory. It simply ensures the owner is never surprised.

**Who Benefits**
Factory owners and HR managers at small and mid-sized manufacturing units — the 80,000+ registered factories in Bangladesh outside the large RMG sector (accessories, pharmaceuticals, food processing, printing, furniture, plastics). BGMEA and BKMEA member factories are already under buyer audit pressure — DIFE compliance is a subset of what they already need. The wider SME manufacturing sector has no compliance tooling at all.

Industry associations (BFMEA, BPF, BTMA) are B2B distribution channels — they have member factories who all face the same inspection risk. At BDT 500–1,500/month per factory, 10,000 factories = BDT 5–15M/month. Labour law compliance SaaS has extremely low churn — the problem recurs every inspection cycle and the switching cost (re-entering all the factory's compliance state) is high.

**Why Now**
(1) **DIFE enforcement has intensified** — post-Rana Plaza, international pressure has made the government visibly increase inspection frequency and penalty strictness. (2) **Bangladesh Labour Act 2018 amendments** added new compliance requirements that many factory owners are unaware of — there is fresh uncertainty in the market. (3) **No affordable compliance tool exists for this tier** — large RMG factories use expensive audit consulting firms; the 80,000 factories below that tier use nothing. The gap is fully open.

**Feasibility & Scope**
Factory registration (type, worker count) → compliance requirement mapping per factory category under BLA 2006/2018 → monthly check-in per live register → renewal deadline calendar → on-demand inspection readiness check → gap report with remediation steps.

Needs: WhatsApp Business API, LLM API, BLA compliance knowledge base (manually curated from published act and DIFE guidelines — public documents). No DIFE API required. POC: garment accessories factory, 50–200 workers, 10 compliance items, 2 weeks. Full coverage of all factory categories and all BLA requirements is the production version.

Biggest unknown: legal accuracy of compliance guidance — addressed by legal review of the knowledge base by a BD labour lawyer before launch, and a clear disclaimer that the agent is a preparation tool, not legal advice. Update cadence: BLA amendments are infrequent (2006, 2013, 2018) — knowledge base refresh is triggered by legislative change, not ongoing.

**Tag:** Quick Build
