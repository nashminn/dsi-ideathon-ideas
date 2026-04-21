# DSI Ideathon 2026 — Alternative Ideas (v5)

Context: Bangladesh-specific. Root-cause oriented. Lightweight (WhatsApp/SMS). Non-technical users. Problems: corruption in govt offices, traffic law non-compliance, violence against women and children.

---

## Idea 13 — Government Application SLA Watchdog Agent

**Tag:** Quick Build

**1. Problem being solved**
Corruption in government offices thrives on information asymmetry — citizens don't know what stage their application is at, what the official processing time should be, or who to escalate to when it's delayed. This ignorance is what makes "speed money" rational. Brokers and corrupt officers exploit the same gap. The problem isn't just slow processing — it's that citizens have no leverage to demand what they're legally owed.

**2. The AI agent concept**
A WhatsApp agent where a citizen registers their application (passport, NID correction, trade license, birth certificate) with a reference number and service type. The agent knows the official SLA for each service (e.g., passport renewal = 21 working days). It tracks elapsed time, sends the citizen a status check nudge on day 15, and — if the deadline passes with no resolution — gives them the exact escalation path: which officer to complain to, what form to submit, which helpline to call, and what their legal rights are under the Right to Information Act. It also lets them anonymously log the delay, building a crowd-sourced delay map by office and service type over time.

**3. Beneficiary audience**
Any Bangladeshi citizen interacting with government services — which is effectively everyone at some point. The delay-mapping layer is additionally valuable to journalists, civil society organizations, and the ACC (Anti-Corruption Commission) as evidence of systemic patterns.

**4. Why now**
The RTI Act and Citizens' Charter already legally define SLAs for government services — the information exists. What's missing is a citizen-facing tool that operationalizes these rights. Delay pattern data, if aggregated publicly, creates accountability pressure that informal systems cannot ignore. The agent requires no government cooperation to launch.

**5. Feasibility scope**
SLA knowledge base per service type → WhatsApp registration of application + start date → countdown logic → escalation script delivery on breach → anonymized delay logging per office. Entirely text-based. No government API access required — the agent works with public information and citizen self-reporting. Quick Build that could launch within weeks.

---

## Idea 14 — Traffic Violation Crowdsource & Pattern Agent

**Tag:** Quick Build

**1. Problem being solved**
Traffic law non-compliance in Bangladesh is near-total — wrong-way driving, no helmets, overloaded vehicles, footpath parking — not because penalties don't exist but because enforcement is sparse, inconsistent, and itself often subject to informal payments. Traffic police cannot be everywhere. But citizens are everywhere, and they have smartphones. The data exists; it's just uncollected.

**2. The AI agent concept**
A WhatsApp agent that lets citizens report a traffic violation in under 30 seconds — send a photo or short description with their location, the agent tags it (violation type, location, time), confirms receipt, and logs it. No account needed. Over time the agent builds a violation heatmap by area, time of day, and violation type. Weekly digests go to a public dashboard and — if a partnership exists — to BRTA or the relevant traffic division. The agent also sends school-zone and accident-blackspot alerts to subscribed community groups ("Mirpur Road 10 এলাকায় সকালে বিপজ্জনক যানজট ও ভুল পথে গাড়ি — সতর্ক থাকুন").

**3. Beneficiary audience**
General public as reporters. Parents of school-age children as subscribers to safety alerts. BRTA, traffic police, and city corporations as data consumers. Road safety NGOs (like Nirapad Sarak Chai) as advocacy partners.

**4. Why now**
Dhaka's traffic fatality rate is among the highest in the region. Post-2018 student road safety protests, public appetite for accountability on this issue is real and documented. WhatsApp groups already informally share traffic alerts — this agent formalizes and aggregates that behavior. Crowdsourced enforcement data has worked in other contexts (Waze hazard reporting, FixMyStreet) and the model is proven.

**5. Feasibility scope**
WhatsApp message intake (text + optional photo) → location tagging → violation classification via LLM → append to crowd-sourced database → periodic digest + alert generation. Photo processing (optional, for evidence logging) is the only compute-heavy step and can be deferred. MVP works entirely on text descriptions. Quick Build.

---

## Idea 15 — Violence Against Women & Children Safe Reporting Agent

**Tag:** Big Bet

**1. Problem being solved**
Violence against women and children in Bangladesh is severely underreported. Victims and witnesses face barriers that existing hotlines don't remove: fear of identity exposure, not knowing what options exist, social stigma preventing voice calls, and no knowledge of where the nearest shelter or legal aid office is. Cases go unreported, escalate, and repeat. The information gap — what can I do, who will help me, will I be safe if I report — is the first barrier to break.

**2. The AI agent concept**
A discreet WhatsApp agent (no identifying account name, generic icon) that a victim, witness, or family member can message at any time. It asks no identifying questions unless the user volunteers them. It provides: what types of cases qualify for legal action, the exact nearest shelter/safe house/legal aid office based on the user's district, how to file a case at the nearest police station (step by step, in plain Bangla), what the One-Stop Crisis Centre (OCC) is and how to reach it, and — for witnesses — how to report anonymously. For users in immediate danger, it surfaces the national helpline (109) and a pre-written message they can send to a trusted contact. Incident reports (anonymized, no personal data) are optionally logged and shared with partnered NGOs (BRAC, Ain o Salish Kendra) for advocacy and resource planning.

**3. Beneficiary audience**
Victims of domestic violence, sexual harassment, and child abuse; witnesses and family members who don't know how to help; NGO field workers who need a tool to share with community members. Relevant across urban and rural Bangladesh, though rural districts where access to physical services is hardest stand to benefit most.

**4. Why now**
Bangladesh's Digital Security Act and subsequent legal reforms have made digital reporting pathways more visible. The National Helpline 109 exists but is underused due to social barriers around voice calls. NGOs active in this space (ASK, BRAC, Manusher Jonno Foundation) are potential launch partners who already have ground-level trust. WhatsApp's end-to-end encryption provides the privacy layer the use case requires. This is a Big Bet due to the sensitivity of content moderation, safeguarding requirements, and the need for NGO partnerships — not due to technical complexity.

**5. Feasibility scope**
Knowledge base of legal rights, shelters, legal aid offices, and procedures by district → conversational Bangla guidance via LLM → WhatsApp E2E delivery → optional anonymized incident logging. No personal data stored. The agent itself is technically a Quick Build — the Big Bet classification reflects the partnership, content governance, and safeguarding work required to deploy it responsibly. Cannot be launched without NGO co-ownership.
