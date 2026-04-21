# DSI Ideathon 2026 — Ideas (v15)

Three new ideas. Different sectors from v14. All enterprise-sellable.

---

## Idea 43

**Title**
DischargeGuide — Hospital Patient Discharge & Medication Adherence Agent

**The Problem**
A patient is discharged from Square Hospital after a cardiac procedure. They receive a printed discharge summary, a list of 7 medications, and instructions to follow up in 2 weeks. They go home, feel better after 3 days, stop taking the medication. Two weeks later they are readmitted — same condition, preventable.

This is not an edge case. Medication non-adherence after hospital discharge is one of the leading causes of preventable readmission globally and Bangladesh is no exception. Private hospitals lose patients to non-adherence they never know about. They also have no channel to the patient after discharge unless the patient chooses to call. The discharge paper sits on a shelf. No reminder arrives. No one follows up.

Private hospitals in Bangladesh — Square, Evercare, United, Ibn Sina, Popular — are increasingly competing on patient outcome metrics. Readmission rates and patient satisfaction scores affect their accreditation and their ability to charge premium prices. They have a direct financial incentive to keep discharged patients on their recovery plan.

**The Agent Idea**
A WhatsApp agent that the hospital's discharge desk activates for every patient at the point of discharge. The agent receives the discharge summary — uploaded by the ward clerk — extracts the medication schedule, follow-up appointment date, and any warning signs to watch for. It sends the patient a Bangla-language medication reminder at the prescribed times: "এখন আপনার Aspirin 75mg খাওয়ার সময়।" It sends a 48-hour check-in: "ছাড়া পাওয়ার পর কেমন আছেন? কোনো সমস্যা হচ্ছে?" If the patient reports a warning symptom, it escalates immediately — sends an alert to the ward's duty nurse and tells the patient which number to call. It reminds them about the follow-up appointment 48 hours and 2 hours before.

When the patient arrives for their follow-up, the doctor sees a message log: did this patient confirm taking medications? did they report any symptoms? The clinical record is enriched automatically.

Typical interaction: Day 3 post-discharge. Agent: "আজকের সকালের ওষুধ খেয়েছেন? — হ্যাঁ / না।" Patient replies "না।" Agent: "ঠিক আছে, এখনই খেয়ে নিন। আপনার পরের ডোজ সন্ধ্যা ৭টায়।" No escalation needed. Patient stays on track.

**Who Benefits**
Private hospitals and clinic chains are the buyers — they pay because readmission reduction has a direct financial value and patient satisfaction scores affect accreditation. Bangladesh has 5,000+ private hospitals and clinics; the premium tier (Square, Evercare, United, Popular, Ibn Sina) is where the budget and the motivation align. At BDT 2,000–5,000/month per ward or BDT 50–150 per discharged patient, a single 300-bed hospital generating 600 discharges/month = BDT 30,000–90,000/month.

Pharmaceutical companies are a secondary buyer — adherence data across a hospital's discharge population is market intelligence they will pay for (anonymised, aggregated).

**Why Now**
(1) **JCI and NABH accreditation pressure** — Bangladesh's premium hospitals are pursuing international accreditation; post-discharge follow-up protocols are an assessed criterion. This agent is an accreditation line item. (2) **LLM structured extraction from discharge summaries** — reliable enough to parse a Bangla/English discharge document and produce a medication schedule. (3) **WhatsApp penetration** — patients discharged from premium private hospitals are urban, smartphone-owning, WhatsApp-using. No behaviour change required.

**Feasibility & Scope**
Discharge summary upload → LLM extraction of medication schedule, follow-up date, warning signs → reminder schedule generation → daily medication check-in push → symptom flag routing → follow-up appointment reminder.

POC: single ward (cardiology or general medicine), 50 patients over 4 weeks. Needs: WhatsApp Business API, LLM API, per-hospital patient database (name, number, discharge date). No EMR integration required in MVP — agent works from uploaded discharge summary PDF. EMR integration (Epic, OpenMRS, local systems) is v2.

Biggest unknown: patient WhatsApp responsiveness after discharge. Addressed by: (1) consent and number collection at discharge desk as part of standard checkout, (2) family member number as backup recipient, (3) SMS fallback. Readmission rate comparison (agent users vs. non-users) is the outcome metric that sells the next hospital.

**Tag:** Quick Build

---

## Idea 44

**Title**
SolarWatch — Solar Home System Fault Reporting & Maintenance Agent

**The Problem**
Bangladesh has over 6 million solar home systems (SHS) installed across rural households — the largest off-grid solar deployment in the world, built over two decades through IDCOL and its 57+ partner organisations. When a panel degrades, a battery fails, or a charge controller malfunctions, the household is left in the dark. They have no idea what failed or why. The installation company that sold them the system may no longer service the area. The nearest IDCOL partner office may be 30 km away. Most households wait weeks or simply abandon the system.

IDCOL has warranty obligations and quality standards but no real-time visibility into the field failure rate across 6 million systems. They find out about failures through field surveys that happen annually at best. Systematic product defects — a batch of faulty batteries, a controller model with a known failure mode — go undetected for months while hundreds of households sit in darkness.

**The Agent Idea**
A WhatsApp agent deployed by IDCOL and its partner organisations for SHS owners. When a system fails, the household messages the agent: "আমার সোলার কাজ করছে না।" The agent asks 4–5 structured diagnostic questions — does the indicator light come on? is it a cloudy day or was it sunny? which part stopped working — light, fan, charging? — and narrows the fault to one of three categories: panel fault, battery fault, or controller/wiring fault. It sends the household a simple first-response guide (check the connections, clean the panel). If the fault requires a technician, it identifies the nearest IDCOL partner service point, sends the household their contact number, and generates a pre-filled service request the household can forward.

On the back end, every fault report is logged with location, system age, fault type, and installation partner. IDCOL gets a real-time failure heatmap. When a cluster of battery failures appears in one district in one month, they know immediately — and they know which partner installed those systems.

Typical interaction: Household: "রাতে বাতি জ্বলছে না।" Agent: "চার্জার কি ঠিকঠাক লাগানো আছে? সবুজ বাতি জ্বলছে?" Household: "না।" Agent: "এটা চার্জ কন্ট্রোলারের সমস্যা হতে পারে। আপনার কাছের সার্ভিস সেন্টার: গ্রামীণ শক্তি, ফরিদপুর — 01XXXXXXXXX।"

**Who Benefits**
IDCOL is the primary buyer — they manage quality standards and warranty obligations for the entire SHS program and currently have no field failure visibility. Every fault log is data they need. At BDT 20–50/system/year on a 6 million system base: BDT 120–300M/year potential. Partner organisations (Grameen Shakti, BRAC, RDF and 54 others) pay per active system in their portfolio to distribute the agent to their customers — it reduces their field support cost by triaging faults remotely before dispatching technicians.

Solar panel and battery manufacturers are a secondary buyer — anonymised, aggregated fault data by product batch is product quality intelligence they will pay for.

**Why Now**
(1) **6 million systems already deployed** — the problem is not future-state, it is happening now across the existing installed base. (2) **WhatsApp penetration in rural BD is now sufficient** — the households that had solar installed in 2015–2020 are the same households whose family members have smartphones now. (3) **IDCOL's warranty liability** — IDCOL partner organisations have 3-year warranty obligations on components; systematic tracking of warranty claims reduces dispute and improves recovery from manufacturers.

**Feasibility & Scope**
Symptom intake via WhatsApp → structured diagnostic Q&A (fixed decision tree, 4–5 questions) → fault category classification → first-response guide delivery → service partner routing → fault log append with location and system metadata.

POC: single IDCOL partner organisation, one district, 500 active SHS households, 2 weeks to build. Decision tree is fixed — no heavy LLM inference required per interaction. Needs: WhatsApp Business API, LLM API (light), IDCOL partner and service point directory (manually compiled for POC). No IoT integration required — fault reporting is user-initiated, not sensor-triggered. IoT-triggered fault detection is v2.

Biggest unknown: rural household WhatsApp adoption vs. basic phone users. Addressed by: SMS fallback (same decision tree, SMS delivery), and IDCOL partner field agent as secondary intake point (field agent messages the agent on behalf of the household). Aggregate failure analytics dashboard for IDCOL is a 1-week addition on top of the log.

**Tag:** Quick Build

---

## Idea 45

**Title**
FlockGuard — Poultry & Livestock Disease Advisory Agent

**The Problem**
Bangladesh's poultry sector produces 1.5 billion broiler birds and 12 billion eggs annually, generated almost entirely by small and medium commercial farmers — operations of 500 to 20,000 birds per shed. When disease hits a flock, the farmer has hours to hours, not days, to identify and respond correctly. A wrong treatment, or no treatment, can kill 30–60% of a flock in 72 hours. The financial loss on a 5,000-bird flock can be BDT 200,000–400,000 in one outbreak.

The farmer's current option: call the feed company representative, who is often not a veterinarian and who has a financial incentive to recommend their company's products. Or call the upazila livestock officer, who may not answer or may be 20 km away. The average small poultry farmer in Bangladesh has no access to timely, unbiased veterinary guidance.

Disease outbreaks also spread. Avian influenza, Newcastle disease, and Gumboro move between sheds and between farms through shared equipment, workers, and wild birds. When outbreak data goes untracked, the cluster is invisible until it has already spread across a district. BLRI (Bangladesh Livestock Research Institute) and DLS (Department of Livestock Services) have no real-time field disease surveillance. They find out from newspaper reports.

**The Agent Idea**
A WhatsApp agent for poultry and dairy farmers. When a farmer notices abnormal bird behaviour — reduced feed intake, respiratory distress, sudden deaths — they message the agent with a description or a short video clip. The agent asks structured questions: age of flock, vaccination history, mortality rate, specific symptoms (sneezing, nervous signs, greenish droppings). It narrows the differential diagnosis to 2–3 most likely conditions and gives a triage response: what to do in the next 6 hours to limit mortality while waiting for a vet, which vaccines or treatments apply, what biosecurity steps to take immediately to prevent spread to adjacent sheds.

For confirmed or suspected reportable diseases (Avian Influenza H5N1, FMD in cattle), it automatically notifies the nearest DLS upazila veterinary officer with a pre-filled report.

Outbreak data is logged per location. When 3+ farms within 20km report similar symptoms in the same week, the agent alerts DLS district office and enrolled farmers in the area: "আপনার এলাকায় নিউক্যাসেল রোগের সংক্রমণ বাড়ছে — টিকার মাত্রা নিশ্চিত করুন।"

**Who Benefits**
Poultry and livestock input companies are the buyers — ACI Animal Health, CP Bangladesh, Kazi Farms, Renata Animal Health each have field representative networks and distribute advisory services to farmers as a retention tool. A branded advisory agent ("CP FarmAdvisor") reaching 50,000+ enrolled farmers is a distribution and loyalty platform they will pay for. Revenue: BDT 500–2,000/month per company or per-farmer per year.

DLS and BLRI pay for the outbreak surveillance layer — it turns a private advisory tool into a public health infrastructure. Development banks (FAO, World Bank livestock programs) fund exactly this kind of disease surveillance + response capacity building.

Secondary: dairy farmers managing mastitis, FMD, and reproductive health in cattle — same advisory model, different knowledge base, same enterprise buyer channel.

**Why Now**
(1) **LLM multi-turn reasoning** is now reliable enough to conduct a structured differential diagnosis for the 10–15 most common poultry diseases in BD — the knowledge base (BLRI guidelines, DLS protocols) is publicly available and well-documented. (2) **WhatsApp video intake** — a 15-second clip of affected birds gives more diagnostic information than a text description; multimodal LLM can extract observable signs from video. (3) **Avian influenza risk** — H5N1 surveillance gaps are a documented public health concern; DLS and FAO both have procurement budget for surveillance infrastructure. A private advisory agent with a public surveillance layer is fundable from two sources simultaneously.

**Feasibility & Scope**
Symptom intake (text + optional video) → structured diagnostic Q&A → differential diagnosis from BLRI knowledge base → triage response → reportable disease auto-notification to DLS → outbreak cluster detection → area alert push.

POC: broiler disease advisory covering 5 most common conditions (Newcastle, Gumboro, Coccidiosis, Salmonella, Marek's), single district, 2 weeks. Needs: WhatsApp Business API, multimodal LLM API, BLRI disease protocol knowledge base (manually curated), DLS upazila officer contact directory. No government API required in MVP.

Biggest unknown: diagnostic accuracy for uncommon or co-occurring disease presentations. Addressed by: (1) agent always recommends a licensed veterinarian for confirmation before treatment, (2) farmer outcome reporting ("birds recovered / mortality continued") builds a feedback loop improving accuracy over time. Dairy cattle advisory is v2 — same architecture, different knowledge base.

**Tag:** Quick Build
