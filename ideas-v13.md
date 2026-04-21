# DSI Ideathon 2026 — Ideas (v13)

Formatted to match the official submission form. All five fields per idea.

---

## Idea 37

**Title**
SamityBook — Informal Savings Group Management Agent

**The Problem**
Bangladesh has hundreds of thousands of informal savings groups — called samity or DPS groups — where 10–30 members contribute a fixed amount weekly or monthly, and members take turns receiving the full pool (a rotating credit system, known globally as ROSCA). These groups collectively move billions of taka across the country entirely outside the formal financial system. Every one of them is managed on paper: a notebook kept by the group organiser, often a housewife or community leader. When the organiser loses track, makes an arithmetic error, or the notebook is lost, disputes break out — sometimes destroying relationships within the group. There is no digital tool built for this demographic.

**The Agent Idea**
A WhatsApp agent used by the samity organiser. Members are registered once with their name and contribution amount. Each week or month, the organiser logs contributions by messaging "Fatema — 500 taka" and the agent updates each member's ledger, confirms the entry, and tracks who has and hasn't paid. It tells the organiser who is overdue. At the end of each cycle it generates a simple summary: total collected, who received the payout this round, and the schedule for upcoming payouts. If a member disputes their record, the organiser can pull their full contribution history in seconds.

Typical interaction: Saturday morning, organiser collects contributions door to door. Texts the agent after each visit. By noon, the agent sends a summary: "এই সপ্তাহে ১৮ জন দিয়েছেন, ২ জন বাকি: করিম ভাই, সুমাইয়া।" No arithmetic, no notebook, no disputes.

**Who Benefits**
Samity organisers — predominantly women managing community savings groups — save hours of manual tracking and avoid disputes. The wider beneficiaries are the 10–30 members of each group who gain a transparent, verifiable record of their contributions.

Market: conservative estimate of 500,000+ active samities in Bangladesh. Even at BDT 100–200/month per group (priced for a demographic with limited disposable income), the TAM is BDT 50–100M/month. More realistic monetisation: partner with bKash or Nagad to make digital contribution logging a gateway to their mobile savings products — platform partnership revenue rather than direct subscription. This is also a financial inclusion data play: samity contribution history is an alternative credit signal for the unbanked.

**Why Now**
WhatsApp penetration among urban and peri-urban women in BD is high and growing. LLMs handle informal Bangla input reliably. The specific pain — organiser arithmetic errors and lost notebooks — is solved by a simple ledger agent with zero ML complexity. No fintech startup has targeted this demographic with a purpose-built tool; they're either too informal for banks or too small for NGO programs.

**Feasibility & Scope**
Member registration (one-time setup via WhatsApp chat) → contribution intake per member → ledger update → overdue alert → cycle summary generation. Pure text, no inference-heavy steps. POC for a single 15-member samity in under a week. Biggest unknown: organiser adoption — requires the tool to be simpler than writing in a notebook. Solved by keeping every interaction to a single message. Digital payment integration (bKash reference confirmation) is v2.

**Tag:** Quick Build

---

## Idea 38

**Title**
DealPulse — B2B Sales Pipeline Intelligence Agent

**The Problem**
B2B sales teams — at software companies, agencies, consultancies, and enterprise service firms — lose deals not because their product is wrong but because follow-up falls through. A promising lead goes quiet after a demo. A proposal sits unanswered for three weeks. A deal that was "90% closed" six months ago is still sitting in the pipeline marked active. Sales managers spend their weekly reviews manually digging through CRM records to identify which deals are stale, which need a nudge, and which are quietly dying. Meanwhile, the sales rep is managing 40 open deals and has no system telling them where to focus today.

**The Agent Idea**
An agent that lives inside the sales team's existing workflow — connected to their CRM (HubSpot, Pipedrive, or even a shared Google Sheet). It monitors deal activity: last contact date, days in current stage, proposal sent but not responded to, meetings booked but not followed up. Each morning it sends the sales rep a prioritised list of 3–5 actions: "Rafiq at MegaCorp hasn't replied to your proposal in 11 days — here's a draft follow-up email." "The ACI deal has been in Negotiation for 28 days — typical close time is 14. Flag for manager." It also alerts the manager when a deal's velocity drops below the team's historical baseline.

Typical interaction: Rep starts their day. Agent sends: "আজকের ৩টা প্রায়োরিটি: (1) TechnoVista — follow up on proposal (12 days silent) — draft ready, (2) GreenTex — demo booked but no agenda sent, (3) NovaCorp — contract stage 35 days, flag for review." Rep acts on each in under 20 minutes.

**Who Benefits**
Sales managers and B2B sales reps at technology companies, agencies, consultancies, and enterprise service firms. Directly applicable to DSI itself — a 300-person software company with a BD and international client pipeline. Also sellable to DSI's enterprise clients, most of whom have B2B sales teams with the same problem.

Market: any company with a B2B sales function and a CRM. In BD alone: hundreds of software firms, telecoms, FMCG distributors, pharmaceutical companies, and financial services firms with field sales teams. Globally: this is a multi-billion dollar category (Salesforce, HubSpot all have adjacent features) but the agent-native, WhatsApp-delivered version for mid-market BD companies is unaddressed.

**Why Now**
LLM tool use + CRM API access enables an agent that reads deal context, interprets staleness, and drafts a contextually appropriate follow-up — not just a generic nudge. Agentic frameworks (LangGraph, which DSI already uses) make the daily monitoring loop straightforward to build. The "AI sales assistant" category exists globally but hasn't been built as a WhatsApp-native, Bangla-capable agent for BD's mid-market. DSI's own sales pipeline is a ready-made pilot environment.

**Feasibility & Scope**
CRM read access (HubSpot/Pipedrive API or Google Sheets) → deal activity analysis → staleness scoring against historical baseline → prioritised action list generation → draft follow-up email per deal → daily WhatsApp delivery to rep. POC against a Google Sheet pipeline in 2 weeks. Biggest unknown: CRM integration variance — each company uses different tools. Solved by starting with a Google Sheet template as the universal MVP, then adding native CRM connectors.

**Tag:** Quick Build

---

## Idea 39

**Title**
AdmitPath — University Admission Guidance Agent

**The Problem**
Every year, hundreds of thousands of Bangladeshi students navigate one of the most stressful and confusing admission processes in the world. Public university admissions (Dhaka University, BUET, medical colleges) run on separate, decentralised schedules — different exam dates, different eligibility criteria, different subject combinations, different seat counts. Private university admissions layer on top with their own deadlines and scholarship criteria. Students and their families piece together this information from rumour, coaching centre noticeboards, and Facebook groups. Mistakes — missing a deadline, applying to a unit you're ineligible for, submitting the wrong document — cost a full year of a student's life.

**The Agent Idea**
A WhatsApp agent that a student registers with once: their HSC result (GPA, group — Science/Commerce/Humanities), preferred subjects, and target university type. The agent then becomes their personal admission calendar: it knows which universities they're eligible for, sends reminders for application deadlines and admit card download dates, explains unit-wise eligibility criteria in plain Bangla, and answers questions like "বিজ্ঞান বিভাগ থেকে ঢাকা বিশ্ববিদ্যালয়ের 'খ' ইউনিটে আবেদন করতে কি লাগবে?" It doesn't submit applications — it makes sure students know exactly what to do and when.

Typical interaction: Student registers in July after HSC results. Agent maps their profile to eligible universities and units. In August when DU 'Ka' unit application opens, agent sends: "ঢাকা বিশ্ববিদ্যালয় 'ক' ইউনিট আবেদন শুরু — শেষ তারিখ ১৫ আগস্ট। আপনার SSC ও HSC সনদের স্ক্যান কপি লাগবে। এখানে সরাসরি লিংক: ..."

**Who Benefits**
Students sitting for university admission — approximately 1.3 million HSC candidates annually in Bangladesh, virtually all of whom go through some version of this confusion. Parents who are navigating the process alongside their children are equally served.

Monetisation options: (1) Freemium — basic deadline reminders free, premium tier (BDT 150–300/year) for personalised eligibility analysis and document checklist. (2) B2B — sell to coaching centres (there are 50,000+ in BD) as a value-added service for their enrolled students, white-labelled under the coaching centre's brand. Coaching centres pay BDT 5,000–20,000/month to offer it to their student base. The coaching centre channel solves distribution immediately.

**Why Now**
LLM reasoning over a structured knowledge base of admission criteria is now reliable for this type of eligibility logic. The data (admission circulars, seat plans, eligibility rules) is publicly available and consistent enough to maintain annually. No existing product serves this need conversationally in Bangla — students currently use Facebook groups and coaching centre WhatsApp broadcasts, both of which are noisy and unstructured. The coaching centre distribution channel makes this immediately scalable without a consumer marketing budget.

**Feasibility & Scope**
Student profile registration → eligibility mapping against university/unit criteria database → deadline calendar per student → reminder push at configurable intervals → Q&A over eligibility knowledge base. POC covers 5 major public universities in 2 weeks. Knowledge base updated once per year after HSC results and admission circular publication. Biggest unknown: admission circular release timing varies year to year — agent needs a monitoring layer to detect when new circulars are published. Solved with a simple web scraper on university admission portals.

**Tag:** Quick Build
