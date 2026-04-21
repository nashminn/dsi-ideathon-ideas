# DSI Ideathon 2026 — Alternative Ideas (v6)

Context: BD-specific. Issues addressed: healthcare access gap, electricity instability for small businesses, education-to-employment mismatch. Lightweight, Bangla-first, WhatsApp-based.

---

## Idea 16 — Rural Healthcare Triage & Referral Agent

**Tag:** Quick Build

**1. Problem being solved**
Rural and peri-urban Bangladeshis routinely make expensive, exhausting trips to overloaded district or divisional hospitals for conditions that could be managed locally — or, conversely, delay seeking care for serious conditions because they don't know how urgent it is. There are no qualified doctors in most union-level health centers. The gap isn't only physical distance — it's the inability to assess "do I need to go now, can I wait, or is there a local option?" Most families make this decision blindly or based on word of mouth.

**2. The AI agent concept**
A WhatsApp agent that conducts a structured symptom check in plain Bangla — asking about symptom type, duration, age of patient, and a few key red-flag questions — and outputs one of three responses: (1) go to a hospital now, here is the nearest emergency facility for your upazila; (2) visit your nearest community clinic or MBBS doctor, here is the address and hours; (3) this is likely manageable at home, here is what to do and what to watch for. It does not diagnose. It triages and routes. It also maintains a district-level directory of DGHS-registered facilities, community clinics, and telemedicine services so referrals are actionable, not generic.

**3. Beneficiary audience**
Families in rural and peri-urban Bangladesh — particularly mothers making healthcare decisions for children and elderly relatives. Also usable by community health workers (CHWs) and NGO field staff who currently make triage decisions without structured tools.

**4. Why now**
DGHS maintains a public directory of registered health facilities. Telemedicine services (Praava, Maya Apa, doctorola) already exist but aren't surfaced at the point of need. LLMs handle conversational Bangla symptom description well enough for structured triage logic. BRAC's community health worker network could distribute the agent through existing trust channels without requiring new infrastructure.

**5. Feasibility scope**
Symptom intake via conversational Bangla → rule-based + LLM-assisted triage logic → district-level facility directory lookup → response generation. Critically: the agent never claims to diagnose — it routes. This keeps it out of medical device regulatory territory. Quick Build with a responsible scope boundary. Upazila facility data is publicly available from DGHS.

---

## Idea 17 — Power Outage Pattern & Planning Agent

**Tag:** Quick Build

**1. Problem being solved**
Small businesses — tailors, printers, welders, cold storage operators, small food processors — in towns and secondary cities outside Dhaka face frequent, unpredictable power outages. These aren't random: outages in a given area follow patterns driven by load shedding schedules, infrastructure age, and peak demand times. But this pattern knowledge is informal, passed by word of mouth. Businesses can't plan production schedules, delivery commitments, or generator fuel purchases around information they don't have.

**2. The AI agent concept**
A WhatsApp agent where users register their area (upazila/ward) and business type. The agent crowdsources outage reports — users message "কারেন্ট গেছে" and "কারেন্ট এসেছে" — and builds a running outage log per area. Over 2–4 weeks it detects patterns (outages most likely Tuesday and Thursday 2–5pm in this zone) and starts sending morning planning nudges: "আজ বিকেলে লোডশেডিং হওয়ার সম্ভাবনা আছে — জরুরি কাজ সকালে সেরে নিন।" It also alerts users when BPDB or DPDC publishes a scheduled load shedding notice — currently this information exists but is poorly distributed.

**3. Beneficiary audience**
Small and micro business owners in secondary cities (Cumilla, Mymensingh, Bogura, Sylhet) and peri-urban areas who cannot afford UPS or generator backup for full operations but can rearrange their workday if they have advance notice. Also useful to households with medical equipment (oxygen concentrators, refrigerated medicine).

**4. Why now**
Outage duration has improved nationally but volatility outside major centers remains high. BPDB load shedding schedules are published but not pushed to the people who need them. Crowdsourced pattern detection with a 2-week training window is achievable with simple time-series logic — no heavy ML. The agent delivers high daily-life value with near-zero inference cost per interaction.

**5. Feasibility scope**
Area registration → outage event logging ("গেছে"/"এসেছে" message parsing) → per-area time-series pattern detection → morning planning nudge generation + BPDB notice scraping and re-distribution. Entirely text-based. Pattern logic is simple moving-average statistics, not ML. Quick Build — the data model is a timestamp log grouped by area.

---

## Idea 18 — Skills-to-Jobs Gap Agent

**Tag:** Quick Build

**1. Problem being solved**
Bangladesh produces hundreds of thousands of graduates annually who struggle to find relevant employment — not because jobs don't exist, but because of a deep mismatch between what universities teach and what employers actually need. Most students have no visibility into real market demand until after graduation. They choose subjects and build CVs based on what previous generations did, not on live signal from the job market. The mismatch compounds: graduates are unemployable in their field, employers can't find qualified candidates, and families have invested years and money into qualifications that don't convert.

**2. The AI agent concept**
A WhatsApp agent for students and recent graduates. The user states their subject (e.g., "আমি CSE পড়েছি, এখন চাকরি খুঁজছি") or their current skills. The agent — drawing from a weekly-updated digest of BD job postings scraped from Bdjobs, Chakri.com, and LinkedIn — tells them: what skills are most in demand right now in their field, which of those are likely missing from a typical university curriculum, and where to close those gaps (free Coursera/YouTube paths, affordable local training centers, govt SEIP programs). It doesn't give career counselling. It gives a specific, actionable skills delta based on live market data.

**3. Beneficiary audience**
Final-year university students and recent graduates across Bangladesh, particularly those from non-elite institutions outside Dhaka who have no career services office or professional network to tap. Also useful to parents who want to understand the market before their child chooses a subject.

**4. Why now**
BD job board data is publicly accessible and scrapeable. LLMs can extract skill demand signals from job description text and map them against a user's stated profile. Government SEIP (Skills for Employment Investment Programme) and a2i have catalogued affordable training options — this agent surfaces them at the moment of need rather than requiring the user to discover them independently. No comparable tool exists in Bangla for this specific population.

**5. Feasibility scope**
Weekly job board scrape → skill frequency analysis per domain → user profile intake via WhatsApp chat → gap identification → free/affordable resource matching → response in Bangla. The scraping and skill extraction pipeline is the most complex piece; the user-facing interaction is simple. Quick Build for a single domain (e.g., IT/CS jobs only) with expansion to other fields over time.
