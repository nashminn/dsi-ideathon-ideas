# DSI Ideathon 2026 — Ideas (v14) — Dreamy Tier

Three high-ambition ideas. All address systemic problems at national scale. All enterprise-sellable. All tagged Big Bet due to scope — but each has a Quick Build POC path.

---

## Idea 40

**Title**
FarmAdvisor — AI Agricultural Extension Agent

**The Problem**
Bangladesh has 15+ million smallholder farming households. The government's Department of Agricultural Extension employs roughly one extension officer per 1,000+ farmers. In practice, most farmers never see one. When a crop fails — pest attack, fungal disease, nutrient deficiency — the farmer makes a judgment call based on what a neighbor told them, what the local agrochemical shop recommended (which is always "buy more input"), or nothing at all. A wrong call costs a season's income. A season's income is a family's entire year.

This is not a niche failure. It is the default experience of agriculture in Bangladesh. Crop losses from preventable misdiagnosis and mistimed intervention add up to billions of taka annually across the country. No tool reaches the farmer at the moment the crop starts failing.

**The Agent Idea**
A WhatsApp agent that puts a qualified agronomist in every farmer's pocket. The farmer registers once: crop type, district, land size. When something goes wrong, they photograph the affected plant and send it. The agent identifies the disease or pest from the photo, explains what it is in plain Bangla, and tells the farmer exactly what to do — which treatment, what dosage, when to apply, what it costs at the local market. Before planting season it sends region-specific crop recommendations based on expected weather. During the growing season it sends timing alerts: "ধানে ব্লাস্ট রোগের ঝুঁকি আছে এই সপ্তাহে — ফাঙ্গিসাইড দিন।" It does not sell anything. It gives the same advice a good extension officer would give.

Typical interaction: Farmer photographs yellowing leaves. Agent responds: "এটা আয়রন ডেফিসিয়েন্সি — ফেরাস সালফেট স্প্রে করুন, ১ গ্রাম প্রতি লিটার পানিতে। ৭ দিনে উন্নতি না হলে আবার জানান।" Farmer acts. Crop survives.

**Who Benefits**
Bangladesh Krishi Bank (10M+ loan customers, all farmers) is the natural institutional buyer — distributing this agent to their borrower base is a customer retention and default reduction tool. Agri-input companies (BADC, ACI Agribusiness, Syngenta BD) pay to distribute as marketing — farmers who receive accurate advice buy inputs confidently. Development banks (ADB, World Bank GAFSP) fund agricultural advisory programs; this is that program at 1/10th the cost. Government DAE is the ideal co-builder — BARC knowledge base + DSI agent layer.

At BDT 200–500/farmer/year at institutional rate, even 1M enrolled farmers = BDT 200–500M/year. TAM is 15M farming households. Internationally: identical extension gap in every South and Southeast Asian agricultural economy.

**Why Now**
(1) **LLM vision** — plant disease identification from a smartphone photo is now reliable enough for field use; this was not true two years ago. (2) **BMET weather API** — Bangladesh Meteorological Department data is accessible and fine-grained enough for upazila-level crop timing advice. (3) **BARC knowledge base** — Bangladesh Agricultural Research Council has decades of publicly available crop advisory publications; this is the knowledge base waiting to be operationalized. No one has built the agent layer on top of it.

**Feasibility & Scope**
Farmer registration (crop, district) → photo intake → LLM vision diagnosis → treatment recommendation from BARC knowledge base → weather-timed alert push → follow-up loop.

POC: single crop (boro paddy), single district (Mymensingh), covers the 5 most common paddy diseases, 3 weeks. Needs: WhatsApp Business API, multimodal LLM API, BMET weather feed, BARC publication knowledge base (manually curated for POC, expanded with BARC partnership). No government API required in v1.

Biggest unknown: diagnostic accuracy for uncommon diseases on low-quality photos. Addressed by: (1) the agent always recommends a local extension officer visit if confidence is low, (2) confirmation step — farmer reports back outcome, building a feedback loop that improves accuracy over time. Yield impact measurement for development bank reporting is a built-in v2 feature.

**Tag:** Big Bet

---

## Idea 41

**Title**
ShiftPath — RMG Worker Reskilling Agent

**The Problem**
Bangladesh's 4 million+ ready-made garment workers — 80% of them women — built the country's largest export industry. Automation is dismantling the work they were hired to do. Cutting machines, automated sewing lines, and finishing robots are already deployed in factories supplying H&M and Zara. The workers most at risk are in the exact roles being automated first: fabric cutting, basic sewing operations, finishing and QC. Most are women in their 30s with a primary or secondary education, no formal certification, and no awareness of what adjacent employment they could qualify for.

When their line is automated or their factory closes, they have no fallback. They don't know which roles in nearby industries are hiring. They don't know which of their current skills transfer. They don't know which training programs exist, how to enroll, or whether the programs lead to actual jobs. The information gap is total. By the time they find out, the factory has closed.

This is a crisis arriving in slow motion. Bangladesh has no transition infrastructure for it.

**The Agent Idea**
A WhatsApp agent that builds a worker's transition path before they need it. A worker registers: current role, years of experience, education level, district. The agent tells them three things: (1) which adjacent roles are hiring in their district right now, pulled from live job board data; (2) which of their current skills transfer directly and which gaps need to close; (3) which government or NGO training programs near them close those gaps — with enrollment information, schedule, and cost. The agent sends a weekly job alert matching their evolving profile. As they complete training, they update the agent and their match quality improves.

Factories use a parallel interface: an HR manager registers their workforce profile and gets a transition report — which roles are at automation risk, what retraining pathway exists per role, estimated timeline. It becomes the factory's workforce transition plan.

Typical interaction: A cutting operator registers. Agent: "আপনার কাজের দক্ষতা দিয়ে কোয়ালিটি ইন্সপেক্টর বা মেশিন অপারেটর পদে যেতে পারেন। আশুলিয়ায় BMET-এর ট্রেনিং শুরু হচ্ছে আগামী মাসে — ফ্রি, ৬ সপ্তাহ। আবেদন লিংক: ..."

**Who Benefits**
BGMEA (Bangladesh Garment Manufacturers and Exporters Association) is the collective buyer — 4,000+ member factories, all of whom will face workforce transition pressure, all of whom need a defensible response to buyer questions about worker welfare during automation. A BGMEA-distributed tool reaches the entire industry without DSI selling to each factory individually.

BMET (Bureau of Manpower, Employment and Training) and the government SEIP program are natural co-funders — this agent is the distribution layer for training programs that currently go unfilled for lack of awareness. Development banks (ADB, IFC, World Bank) routinely fund automation transition programs; DSI builds the platform they fund.

This is also the idea that DSI, as Bangladesh's most prominent tech company, has a specific responsibility to build.

**Why Now**
(1) **Automation is arriving now** — not in 10 years, now. The factories that can afford H&M's compliance requirements are the factories automating first. (2) **LLM job-skill matching** — reliable enough to map a worker's role history against live job demand and identify transferable skills without human career counsellors. (3) **SEIP program inventory is public** — training programs exist but enrollment is low because nobody knows about them; this agent is the missing awareness layer. (4) **No transition infrastructure exists** — the window to build it before the wave hits is now.

**Feasibility & Scope**
Worker profile registration → skills gap mapping against live job demand (Bdjobs scrape) → SEIP/BMET training program matching → weekly job alert push → factory-facing workforce transition report.

POC: 50 workers in Ashulia transitioning out of cutting operations, single district, 3 weeks. Needs: WhatsApp Business API, LLM API, Bdjobs/Chakri scraper, SEIP training program database (publicly available). No government API required. Factory HR interface is a lightweight web form on top of the same backend.

Biggest unknown: worker smartphone and WhatsApp penetration in peri-urban areas. Addressed by: factory-floor onboarding (factory distributes the WhatsApp number at shift end), SMS fallback for non-WhatsApp users. Outcome tracking (did the worker get the job?) is a v2 feature but a powerful one for development bank reporting.

**Tag:** Big Bet

---

## Idea 42

**Title**
ZeroClaim — Parametric Microinsurance Trigger Agent

**The Problem**
Bangladesh is among the world's most climate-vulnerable countries. Floods destroy crops in the haors every few years. Cyclones batter coastal fishermen. Drought ruins boro paddy in the northwest. Crop and livelihood insurance products exist — SBC, some NGO microinsurance programs — but penetration is near zero. The reason is not that farmers don't want insurance. It is that the claims process is broken.

When a flood destroys a crop, the farmer is supposed to: file a claim within a deadline, document their losses (how, exactly?), wait weeks for a field assessor to visit, argue about the assessed amount, and maybe receive a partial payout months later. Most farmers have tried this once and never again. The product fails because the process fails. The result: millions of farming and fishing households absorb catastrophic climate losses with no protection, year after year.

**The Agent Idea**
Parametric insurance with no claim filing. The payout is triggered automatically by a weather event, not by a human assessment.

The farmer registers their plot: GPS location (dropped on a map in WhatsApp), crop type, insured peril (flood, drought, cyclone). The agent monitors two data sources continuously: BMET weather station data and CHIRPS satellite rainfall indices — both public, both updated daily. When conditions in the farmer's registered zone cross the trigger threshold — rainfall below 40mm in 30 days during the growing season, or wind speed above 65 km/h during cyclone season — the agent fires: it verifies the threshold breach, logs it with a timestamp, and initiates a bKash or Nagad disbursement to the farmer's registered number. The farmer receives a WhatsApp notification: "আপনার এলাকায় খরার শর্ত পূরণ হয়েছে — ৩,০০০ টাকা আপনার বিকাশে পাঠানো হয়েছে।" No form. No adjuster. No dispute. No delay.

The agent is the trigger infrastructure. Insurance companies and NGO microinsurance programs sit on top of it — they define the products, set the thresholds, manage the premium collection. DSI builds the monitoring and payout layer.

**Who Benefits**
Insurance companies (SBC, Green Delta, MetLife BD) that want to offer microinsurance products without the prohibitive loss adjustment cost of manual claims processing. NGO microinsurance programs (BRAC, Palli Karma-Sahayak Foundation, Swiss Re Foundation programs) that already have farmer relationships but can't scale because claims handling consumes their operational budget. Development banks (ADB, World Bank GAFSP, IFAD) that fund agricultural resilience programs — parametric index insurance is a preferred instrument and BD has essentially no functional implementation of it.

Farmers pay premiums of BDT 200–500/season for coverage of BDT 2,000–8,000 per event. At 500,000 enrolled farmers: BDT 100–250M/year in premium flow. DSI earns as infrastructure provider per policy issued and per trigger processed. The market is currently zero — any penetration is upside.

**Why Now**
(1) **CHIRPS satellite rainfall data** — publicly available, free, daily updated, 0.05° resolution — makes weather-index triggering technically feasible without expensive ground station networks. (2) **bKash/Nagad disbursement APIs** — instant mobile money transfer to 60M+ accounts means payout can be automated without bank infrastructure. (3) **Climate events are intensifying** — BD farmers are experiencing more frequent and more severe weather shocks; the product need is growing. (4) **ADB and World Bank are actively funding parametric insurance in South Asia** — a working BD implementation is fundable on day one.

**Feasibility & Scope**
Farmer GPS registration → insurance product selection and premium intake → BMET/CHIRPS daily monitoring → threshold breach detection → breach verification and logging → bKash/Nagad disbursement trigger → farmer WhatsApp notification.

POC: rainfall-deficit trigger for boro paddy, Sunamganj haor district, 100 enrolled farmers, 4 weeks to build. Needs: WhatsApp Business API, CHIRPS API (free), BMET data feed, bKash disbursement API. Regulatory dependency: IDRA approval for parametric product structure — this is the Big Bet constraint, not the technology. Structure as B2B infrastructure sold to a licensed insurer who holds the regulatory relationship.

Biggest unknown: IDRA parametric product approval timeline. Addressed by launching as a pilot under an existing NGO microinsurance license (BRAC or PKFSF already have these), generating impact data, then moving to commercial insurer partnerships. ADB or World Bank co-funding of the pilot removes the revenue risk on the first deployment.

**Tag:** Big Bet
