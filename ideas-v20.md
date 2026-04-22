# DSI Ideathon 2026 — Ideas (v20) — Undocumented Ideas from Session

Ideas pitched verbally during the session but not previously written to file. #64–#69.

---

## Idea 64

**Title**
RemitHome — Migrant Worker Family Finance Agent

**The Problem**
Bangladesh has 10+ million workers abroad remitting $20B+ annually. The worker has no visibility into how the money is being managed at home. The family — often a spouse handling finances independently for the first time — has no guidance. Both sides are anxious. The money arrives but nobody knows where it goes.

**The Agent Idea**
A WhatsApp agent the migrant sets up once. When a remittance arrives, both the worker and the family member are notified. The agent helps the family create a simple monthly budget — rent, school fees, food, savings — and tracks spend against it. The worker can check in from abroad: "এই মাসে কীভাবে খরচ হয়েছে?" and receives a summary. They can send instructions through the agent: "এই মাসে ৫০০০ টাকা সেভিংসে রাখো।" The agent tracks savings goals (house fund, children's education) and reports progress.

**Who Benefits**
Migrant workers and their families are the end users. The institutional buyer is the distribution layer: bKash, Nagad, and banks with NRB (Non-Resident Bangladeshi) products — they offer this as a value-added service to attract and retain remittance senders. bKash alone has 55M+ users. International: identical problem in Philippines (10M+ OFWs), India, Pakistan, Sri Lanka, Indonesia — every major migrant-sending country.

**Why Now**
WhatsApp penetration among both migrant workers (Gulf, Malaysia, Singapore) and their families in BD is near-universal. bKash/Nagad already have remittance receipt APIs. LLM reasoning over household finance is now practical at scale.

**Dishonesty Filter**
Remittance data comes from the mobile money provider — not self-reported. Family spending is self-reported but gaming it only hurts their own budget.

**Tag:** Big Bet

---

## Idea 65

**Title**
MamaGuide — Maternal and Infant Health Advisory Agent

**The Problem**
A mother in rural Bangladesh doesn't know if her baby's fever means go to the hospital or wait. Community health workers visit once a month. In between, she relies on relatives, Facebook groups, and guesswork. Every year, preventable infant and maternal deaths occur because no one was there to say "go now."

**The Agent Idea**
A WhatsApp agent that guides new mothers through pregnancy and their baby's first year. Sends vaccination reminders at the right dates, answers health questions in plain Bangla, and tells the mother clearly when a symptom needs urgent attention versus watchful waiting. Not medical advice — structured triage guidance based on WHO and DGDA protocols. When red flag symptoms appear (high fever in a newborn, difficulty breathing, signs of dehydration), the agent says go to hospital now and which facility to go to.

**Who Benefits**
Mothers and infants are the end users. Institutional buyers: MOHFW (Ministry of Health and Family Welfare), BRAC Health, CARE Bangladesh, Save the Children, UNICEF-funded programs — all of which run maternal health interventions and have budget for digital health tools. International: same product serves maternal health programs in Kenya, Nigeria, Nepal, Myanmar with minimal adaptation.

**Why Now**
Bangladesh's maternal and infant mortality rates have improved significantly but the last mile gap — between CHW visits — remains unaddressed by any digital tool in Bangla. USAID and FCDO actively fund digital health in this space.

**Dishonesty Filter**
Mothers report symptoms of their baby. No incentive to misreport — they're seeking help for their child.

**Tag:** Big Bet

---

## Idea 66

**Title**
ChronicCare — Chronic Disease Companion Agent

**The Problem**
Bangladesh has 13+ million diabetics and tens of millions more with hypertension and heart disease. Most see their doctor every 3–6 months. In between, nobody is watching. Blood sugar fluctuates, medications are missed, early signs of complications go unnoticed. When the patient finally sees the doctor, the visit is based on how they feel that day — not what actually happened over the past 90 days.

**The Agent Idea**
A WhatsApp agent that stays with the chronic disease patient between appointments. The patient logs readings (blood glucose, blood pressure) and symptoms via WhatsApp. The agent detects patterns — readings trending in the wrong direction, medication gaps, symptoms that warrant earlier attention — and flags them. When something needs a doctor's attention before the next scheduled visit, the agent says so and generates a referral-ready summary. At the scheduled appointment, the doctor receives a structured 90-day log instead of starting from zero.

The doctor gets better data. The patient gets caught before they deteriorate. Complications — which are expensive — are reduced.

**Who Benefits**
Hospitals and clinics pay because reduced emergency readmissions improve their outcomes metrics and reduce cost. Pharma companies (Novo Nordisk, AstraZeneca, Sanofi) pay because better adherence improves their drug performance data and patient outcomes. Insurance companies pay because fewer complications mean fewer large claims. Globally: 500M+ diabetics, 1B+ hypertensives. The market is one of the largest in healthcare.

**Why Now**
LLM-based health conversation is now good enough to conduct contextual patient check-ins reliably. Wearable and manual glucose/BP monitoring is mainstream even in BD. No Bangla-language chronic disease companion exists.

**Dishonesty Filter**
Patients self-report readings. Underreporting doesn't help them — it produces bad guidance. No institutional fraud possible.

**Tag:** Big Bet

---

## Idea 67

**Title**
TriageAI — Hospital Emergency Triage Agent

**The Problem**
In most Bangladeshi hospitals, triage is first-come-first-served. A patient with chest pain waits behind someone with a minor complaint. A child with a high fever sits in a queue behind adults with non-urgent issues. Systematic clinical triage — assessing severity before assigning queue position — exists in well-resourced hospitals globally but is almost absent in Bangladesh's private sector, where a senior clinician cannot stand at reception all day.

The result: preventable deterioration while waiting, misallocation of clinical attention, and occasional deaths in waiting rooms that could have been avoided.

**The Agent Idea**
An AI that conducts a rapid severity assessment when a patient arrives — via a tablet at reception or a WhatsApp pre-registration link sent when the appointment is booked. The agent asks targeted clinical questions (chief complaint, duration, associated symptoms, relevant history), flags red-flag responses, and assigns a triage priority score. The reception staff see a prioritised queue: critical, urgent, routine. The most critical patients are fast-tracked without requiring a doctor at the door.

For the hospital: real-time visibility into who is waiting and how sick they are. For the patient: knowing their position in a clinically ordered queue, not an arbitrary one.

**Who Benefits**
Hospital management and medical directors at private hospitals are the buyers — patient safety outcomes and reduced liability are the motivation. Every hospital with an emergency or outpatient department. International: clinical triage is a globally standard practice; automating it is universally applicable.

**Why Now**
LLM-powered symptom assessment is now reliable enough for triage screening (not diagnosis). Infermedica and similar tools exist internationally but no BD-local, Bangla-language implementation exists. Private hospital competition in BD is intensifying — patient experience and safety outcomes are differentiators.

**Dishonesty Filter**
Patients report their own symptoms. Exaggerating symptoms to get seen faster only results in getting seen — no financial or harmful gain.

**Tag:** Big Bet

---

## Idea 68

**Title**
SecondLook — AI Diagnostic Second Opinion Platform

**The Problem**
Every year, Bangladeshis spend their life savings travelling to India, Thailand, and Singapore for medical second opinions — because they don't trust the local diagnosis. Bangladesh loses $1B+ annually to outbound medical tourism, much of it driven by patients who simply want someone else to look at their reports before they proceed with surgery or major treatment.

The patients who travel are the ones who can afford to. The majority who can't afford it proceed on a diagnosis they're uncertain about, or delay treatment out of doubt.

**The Agent Idea**
A platform where a patient uploads their lab reports, imaging (X-rays, CT, MRI), clinical notes, and symptom history. An AI analyses the full clinical picture, generates a structured differential diagnosis with likelihood rankings, flags findings that might have been missed or warrant further investigation, and identifies any inconsistency between the reported diagnosis and the clinical evidence. The output is a structured second opinion report — not a diagnosis, but a clinical cross-check.

The platform also maintains a network of specialist doctors who review AI-flagged cases requiring human expertise, creating a hybrid AI + specialist second opinion model.

**Who Benefits**
Individual patients are end users. Institutional buyers: diagnostic chains (that want to offer second opinion as a premium service), telemedicine platforms, private hospitals that want to retain patients who would otherwise travel abroad. Health insurance companies that cover diagnostic workup have interest in second opinion reducing unnecessary procedures. International: medical second opinion is a multi-billion dollar global market — the AI layer makes it accessible at scale.

**Why Now**
Multimodal LLMs can now analyse medical images and clinical documents at a level that provides meaningful clinical cross-checking. No BD-local AI second opinion platform exists. Bangladesh's specialist density is extremely low — AI can close the gap between patient need and specialist availability.

**Dishonesty Filter**
Patient uploads their actual reports — no incentive to falsify documents they're seeking help with.

**Tag:** Big Bet

---

## Idea 69

**Title**
VerifyBD — AI-Powered Background Verification and Trust Score

**The Problem**
In Bangladesh, fake degrees, fabricated references, and falsified employment histories are widespread. Employers cannot reliably verify whether a candidate's credentials are real. Banks and NBFIs cannot verify whether a loan applicant's business or income claims are accurate. Every hiring decision and every credit decision carries hidden verification risk that currently goes unaddressed.

**The Agent Idea**
A triggered agent that, when a candidate or applicant is submitted, automatically cross-references available data sources: NID verification (Election Commission API), educational institution confirmation, CIB credit history, professional references via direct outreach, business registration (RJSC records). Aggregates signals into a structured trust report — verified facts, unverified claims, and red flags — delivered to the requesting employer or lender.

Not a pass/fail system. A structured evidence report that makes the human decision faster and better-informed.

**Who Benefits**
HR heads at large corporations, banks, NBFIs, staffing agencies, and background screening firms. International: employment background verification is a $5B+ global industry. In markets where digital identity infrastructure is stronger, the same product expands to more data sources.

**Why Now**
NID verification API exists in Bangladesh. RJSC business registry is digitised. LLM synthesis of multi-source verification signals into a coherent report is now practical. No local AI-powered background verification product exists.

**Dishonesty Filter**
The product is specifically designed to detect dishonesty — it is the solution, not the victim of the filter.

**Tag:** Quick Build (basic NID + CIB check) to Big Bet (full multi-source trust score)

---

*Pool total: 69 ideas*
