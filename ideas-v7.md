# DSI Ideathon 2026 — Alternative Ideas (v7)

---

## Idea 19 — Dengue & Disease Outbreak Early Warning Agent

**Tag:** Quick Build

**1. Problem being solved**
Bangladesh loses thousands of lives to dengue every year — and the outbreaks are predictable by area and season, yet communities receive no localized early warning. IEDCR publishes national data but it doesn't reach the neighborhood level in time to change behavior. By the time a family learns their area has a surge, multiple members may already be infected. Prevention (removing stagnant water, using repellent, seeking early testing) is highly effective but only if people know the risk is active in their specific area right now.

**2. The AI agent concept**
A WhatsApp agent where users subscribe by area (ward/thana). They can report suspected dengue cases in their household or neighborhood ("আমাদের এলাকায় ৩ জন ডেঙ্গু হয়েছে"), and the agent aggregates these reports alongside IEDCR's published weekly bulletins. When reports in an area cross a threshold, it pushes a localized alert to all subscribers in that ward with: current risk level, specific prevention steps, nearest testing center, and when to go to hospital vs. manage at home. Off-season it sends a pre-monsoon preparation reminder each May.

**3. Beneficiary audience**
Urban and peri-urban households across Dhaka, Chittagong, and other dengue-endemic cities. City corporation ward councillors and community health workers as secondary users who can relay alerts through their own networks.

**4. Why now**
Dengue cases hit record highs in 2023. IEDCR data is public and structured enough to parse weekly. Aedes mosquito breeding season is consistent and predictable — making pre-monsoon alerts reliable. Community-level crowdsourcing closes the lag between IEDCR reporting and neighborhood-level awareness. Technically trivial; the value is entirely in distribution and localization.

**5. Feasibility scope**
IEDCR bulletin scraping (weekly PDF/HTML) + user case reports → per-ward case count aggregation → threshold trigger → alert push to ward subscribers. Pure text, no inference-heavy steps. Bangla message templates. Quick Build deployable before the next monsoon season.

---

## Idea 20 — Food Adulteration Reporting & Alert Agent

**Tag:** Quick Build

**1. Problem being solved**
Food adulteration in Bangladesh is pervasive and well-documented — formalin in fish, carbide in fruit, artificial color in sweets, expired products relabeled, fake cooking oil. It is a direct public health threat that disproportionately affects people who buy from local markets and street vendors. The Bangladesh Food Safety Authority (BFSA) conducts raids but is severely understaffed. Enforcement is reactive. The public has no channel to report suspicious products and no way to know which markets or vendors have had violations.

**2. The AI agent concept**
A WhatsApp agent where anyone can report a suspected adulteration incident — product type, market name, location, description of what was suspicious (smell, color, texture, illness after eating). The agent confirms the report, asks 2–3 structured follow-up questions, and logs it with location tagging. Reports from the same market cluster automatically. When a market or vendor accumulates multiple reports, the agent alerts subscribed BFSA officers and local consumer rights NGOs (like Consumers Association of Bangladesh). A public weekly digest summarizes flagged markets by district — no vendor names, just area-level signal — so buyers can make informed choices.

**3. Beneficiary audience**
General consumers, particularly women who manage household food purchasing. BFSA field officers who need prioritized enforcement leads. Consumer rights organizations and investigative journalists tracking food safety patterns.

**4. Why now**
BFSA was established in 2015 but enforcement capacity hasn't scaled. Mobile-based civic reporting has worked in analogous contexts. Public awareness of adulteration is high — people know it's a problem but have no outlet. An anonymous, frictionless reporting channel lowers the barrier to the near-zero level required for mass participation.

**5. Feasibility scope**
Structured incident intake via WhatsApp → location tagging → report clustering by market/area → threshold-based alert to BFSA contacts → weekly public digest generation. No image analysis required in MVP (text description is sufficient for intake). Quick Build. The challenge is distribution and establishing BFSA as a genuine downstream consumer of the data — without that partnership, reports go nowhere.

---

## Idea 21 — Waterlogging & Drain Blockage Civic Reporting Agent

**Tag:** Quick Build

**1. Problem being solved**
Dhaka and Chittagong flood after moderate rain not because of exceptional rainfall but because drains are blocked by garbage, construction debris, and encroachment — problems that build up slowly and visibly before every monsoon. City corporations (DSCC/DNCC) have maintenance mandates but no systematic way to receive, prioritize, or track citizen-reported blockages. Residents know which drains in their lane are clogged; the city doesn't. By the time flooding makes it to the news, the preventable window has passed.

**2. The AI agent concept**
A WhatsApp agent where citizens report a blocked drain or waterlogging point with a description and their location ("মোহাম্মদপুর বাসস্ট্যান্ডের পাশের নালা বন্ধ"). The agent logs it, tags it geographically, and issues a confirmation with a reference number. Reports cluster by location — when 3+ reports appear within 500m, the agent escalates to a mapped city corporation ward contact and generates a work order summary. Before the monsoon (April–May), it runs a "pre-monsoon drain check" campaign — actively nudging subscribers in flood-prone wards to check and report their local drains. Post-monsoon, it follows up on reported blockages to confirm resolution.

**3. Beneficiary audience**
Urban residents in flood-prone wards of Dhaka, Chittagong, and Sylhet. City corporation engineers and ward councillors as resolution owners. Urban planners and climate resilience researchers as secondary data consumers — a multi-year blockage dataset has significant analytical value.

**4. Why now**
DSCC and DNCC have digital complaint portals but they require account creation, are web-only, and have no follow-up mechanism — adoption is near zero. WhatsApp reaches the same population with zero friction. The 2024 flooding in Dhaka renewed public and political attention on drainage. A pre-monsoon campaign launched in April–May would be immediately timely and high-visibility.

**5. Feasibility scope**
Report intake (text + optional photo) → location tagging → clustering logic → ward contact alert → follow-up nudge after 7 days. Photo intake is optional and can be logged without processing. Clustering is simple proximity grouping, not ML. Quick Build — the city corporation partnership is the non-technical dependency, not the software.
