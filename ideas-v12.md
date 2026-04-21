# DSI Ideathon 2026 — Ideas (v12)

Formatted to match the official submission form. Avoids collision with ODMS, IPEMIS, and OpenCRVS domains.

---

## Idea 34

**Title**
ClaimStart — Insurance First Notice of Loss Agent

**The Problem**
When a Bangladeshi policyholder needs to file an insurance claim — a vehicle accident, a fire at their shop, a hospitalisation — they typically have to visit the insurance office in person, fill out a paper form, and wait days for an adjuster to contact them. In the meantime, evidence degrades, receipts get lost, and the claimant has no idea what stage their claim is at. Insurance companies on the other side receive incomplete FNOL (First Notice of Loss) reports that require multiple follow-up calls before an adjuster can even be dispatched. The result: slow claims, frustrated policyholders, high processing cost per claim, and a sector with one of the lowest customer trust ratings in the country.

**The Agent Idea**
A WhatsApp agent that insurance companies embed as their claims intake channel. When a policyholder has an incident, they message the agent. It guides them through structured FNOL intake: policy number, incident type, date and location, brief description, and photo evidence upload. The agent validates the policy number, checks coverage, asks clarifying questions specific to the claim type (for a vehicle claim: is the vehicle driveable? any injuries?), and generates a complete, structured FNOL report delivered to the insurer's claims team within minutes. The policyholder gets a reference number and a status update link. Adjusters arrive with a complete dossier, not a blank form.

Typical interaction: Policyholder texts "আমার গাড়ি এক্সিডেন্ট হয়েছে।" Agent asks for policy number, incident details, location, photos. 8 minutes later the claims team has a structured report with photos attached and policy coverage confirmed. Adjuster is dispatched same day.

**Who Benefits**
Insurance companies pay — sold as a SaaS intake layer per claim processed or monthly subscription. BD has 80+ registered insurance companies with millions of active policies across life, health, motor, and fire. Faster FNOL reduces total claims cycle time, which directly reduces the insurer's loss adjustment expense. Internationally: this exact problem exists in every insurance market — the model scales to any country without rebuilding.

**Why Now**
WhatsApp multimodal input (photo + text) makes evidence collection at the point of incident practical for the first time. LLM-based structured extraction from conversational input is reliable enough to replace paper forms. IDRA (Insurance Development and Regulatory Authority) is pushing digitisation of the sector. No BD insurance company has a functional digital FNOL channel — the bar to be first is low.

**Feasibility & Scope**
Policy number validation → claim type routing → structured Q&A flow per claim type → photo intake → FNOL report generation → delivery to claims team via email/API. POC covers motor claims only (highest volume) in 2 weeks. Biggest unknown: policy database integration — solved in MVP by manual policy number lookup, replaced by API in later version. **Revenue: BDT 50–150 per claim processed or BDT 30,000–80,000/month per insurer.**

**Tag:** Quick Build

---

## Idea 35

**Title**
GreenPass — ESG & Sustainability Compliance Agent for BD Exporters

**The Problem**
International buyers — H&M, Walmart, IKEA, Marks & Spencer — are now contractually requiring their BD suppliers to submit annual ESG (Environmental, Social, Governance) and sustainability reports: energy consumption, water usage, waste management, worker welfare metrics, carbon footprint estimates. Most BD suppliers — garment factories, leather goods manufacturers, jute processors — have no system to collect this data. They hire expensive consultants each year to do it manually, or simply lose the buyer contract when they can't comply. This problem is accelerating: the EU's Corporate Sustainability Due Diligence Directive (CSDDD) comes into full effect by 2027 and will tighten requirements further.

**The Agent Idea**
A WhatsApp + lightweight web agent for factory compliance managers. The agent runs a monthly data collection routine: it asks structured questions about energy bills (photo of meter or bill), water consumption, waste disposal records, worker headcount and incident logs — all via WhatsApp in Bangla. It stores responses, calculates derived metrics (kWh per unit produced, water intensity, injury rate), and at year end generates a buyer-ready ESG report in the format required by common international audit frameworks (Higg Index, SEDEX, UNGC). The compliance manager answers questions on their phone; the report writes itself.

Typical interaction: First Monday of each month the agent sends "এই মাসের বিদ্যুৎ বিল ছবি তুলে পাঠান।" Manager sends a photo. Agent extracts the figure, logs it, and moves to the next data point. Year-end report is auto-generated from 12 months of collected data.

**Who Benefits**
Factory compliance officers and owners at BD's 4,500+ export-oriented garment factories, plus leather, jute, and pharmaceutical exporters. Buyers and international audit firms are indirect beneficiaries. High willingness to pay: losing a single international buyer relationship costs multiples of any annual subscription fee. **Revenue: BDT 5,000–20,000/month per factory. At 500 factories: BDT 2.5–10M/month.** Internationally scalable to Vietnam, Cambodia, Sri Lanka, and any export-manufacturing economy facing the same buyer pressure.

**Why Now**
EU CSDDD enforcement deadline is approaching. International buyer ESG requirements have shifted from voluntary to contractual in the last 2 years. Multimodal LLMs can extract figures from photos of utility bills and handwritten logs — removing the last barrier to mobile-first data collection for factory managers who don't use computers. No affordable ESG data collection tool exists for mid-sized BD factories.

**Feasibility & Scope**
Monthly data collection prompts → photo + text intake → metric extraction and logging → year-end report generation against standard framework templates. POC covers energy and water metrics for a single factory in 3 weeks. Biggest unknown: mapping collected metrics to specific buyer audit frameworks (Higg vs. SEDEX vs. custom buyer templates) — scoped in MVP to one framework, expanded on demand. **This is also immediately sellable to DSI's existing RMG sector contacts.**

**Tag:** Quick Build

---

## Idea 36

**Title**
StockSense — Warehouse & Distributor Inventory Agent

**The Problem**
Small and mid-sized importers, distributors, and wholesalers in Bangladesh manage warehouse inventory manually — handwritten stock registers, basic Excel files, or memory. They don't know in real time what's in stock, what's moving fast, what's sitting idle, or when to reorder from their supplier. The result: stockouts on fast movers that cost sales, dead stock that ties up capital, and reorder decisions made on gut feeling rather than data. For a distributor managing 200–500 SKUs across multiple product categories, this is a daily operational failure with a direct cost in lost sales and wasted capital.

**The Agent Idea**
A WhatsApp agent for warehouse managers and distributors. Stock movements are logged by messaging the agent: "received 500 units Rice Bran Oil 1L from Supplier A" or "dispatched 200 units to Meghna Traders." The agent maintains a live inventory ledger per SKU, calculates sales velocity from dispatch history, and sends reorder alerts when stock drops below a dynamically calculated threshold. Weekly it delivers a summary: top 10 fast movers, bottom 10 slow movers, items approaching zero stock. For distributors with multiple warehouse locations, it tracks each location separately and flags transfer opportunities when one location is overstocked and another is running low.

Typical interaction: Warehouse worker texts "dispatched 150 cartons Surf Excel 1kg to Agora." Agent confirms, updates ledger, checks stock level — if below threshold it flags "Surf Excel 1kg: ৮৫ cartons remaining — reorder point reached, usual lead time 3 days."

**Who Benefits**
Owners and operations managers at small and mid-sized distribution companies, importers, and wholesale traders — a market of tens of thousands of businesses across BD. FMCG distributors, construction material suppliers, pharmaceutical distributors (complements #26 with a broader scope), and electronics importers are all natural buyers. High willingness to pay: a single avoided stockout on a high-margin SKU covers months of subscription. **Revenue: BDT 1,000–4,000/month per business depending on SKU count. At 10,000 clients: BDT 10–40M/month.** Internationally: identical problem in every emerging market with fragmented distribution.

**Why Now**
WhatsApp penetration among warehouse and operations staff is universal. LLMs handle noisy, informal product name variations in Bangla well enough to match SKUs reliably — the core technical challenge that made previous rule-based chatbots fail at this. No affordable inventory tool exists for this tier of BD distributor; enterprise WMS solutions (SAP, Oracle) are priced for multinationals, not a 10-person distribution company.

**Feasibility & Scope**
SKU master setup (one-time) → movement intake via WhatsApp text → ledger update → velocity calculation → reorder alert logic → weekly summary generation. POC for a single distributor with 50 SKUs in 2 weeks. Biggest unknown: handling SKU name variations in user messages (e.g., "surf" vs "surf excel" vs "surf 1kg") — solved with fuzzy matching and a confirmation step. Multi-location tracking is a v2 feature.

**Tag:** Quick Build
