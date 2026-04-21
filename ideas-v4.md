# DSI Ideathon 2026 — Alternative Ideas (v4)

Context: Bangladesh market. Agents must be lightweight (WhatsApp/SMS-first, text-only, low bandwidth). Users are non-technical. Problems are local and high-frequency.

---

## Idea 10 — RMG Factory Compliance Tracking Agent

**Tag:** Quick Build

**1. Problem being solved**
Bangladesh is the world's 2nd largest garment exporter. Factories supplying H&M, Zara, and similar buyers must maintain dozens of compliance certifications — fire safety audits, labor standard inspections, environmental reports — each with separate deadlines and documentation requirements. Factory managers track these manually in spreadsheets or not at all. A missed renewal loses the export license or triggers a buyer suspension, costing millions in cancelled orders.

**2. The AI agent concept**
A WhatsApp-based agent that stores a factory's compliance calendar (certification names, renewal deadlines, responsible persons). It sends plain-language reminders in Bangla and English as deadlines approach, asks the manager to confirm renewal status via a simple reply, and — when a renewal is due — walks them through the required document checklist step by step over chat. No app to install, no dashboard to learn. Works on any phone with WhatsApp.

**3. Beneficiary audience**
Compliance officers and factory managers at small and mid-sized RMG factories across Dhaka, Narayanganj, and Chittagong. Most of these factories cannot afford a dedicated compliance software suite — they rely on a single person with a notebook.

**4. Why now**
International buyers are tightening compliance requirements post-Rana Plaza. BGMEA and BKMEA are pushing digital compliance adoption. WhatsApp penetration in factory management is near-universal. A lightweight reminder-plus-checklist agent requires no infrastructure beyond a WhatsApp Business API integration and a simple calendar backend.

**5. Feasibility scope**
Compliance calendar stored as structured data per factory → scheduled reminder triggers → WhatsApp Business API for message delivery → LLM for natural language checklist guidance in Bangla/English. Entirely text-based. No computer vision, no heavy inference. A Quick Build requiring only a WhatsApp API account and basic backend scheduling.

---

## Idea 11 — Small Shop Stock & Reorder Agent

**Tag:** Quick Build

**1. Problem being solved**
Bangladesh has millions of small retail shops — grocery stores, pharmacies, stationary shops — that manage inventory entirely from memory or handwritten ledgers. Owners routinely run out of fast-moving items or overstock slow ones because they have no system to track patterns. They also don't know when to reorder or how much, leading to lost sales or wasted capital tied up in dead stock.

**2. The AI agent concept**
A WhatsApp agent the shopkeeper interacts with entirely through simple text messages in Bangla — "sold 6 soaps", "received 2 dozen eggs" — and the agent maintains a running stock count. When an item falls below a threshold (learned from the shopkeeper's own sales velocity), it sends a reorder nudge: "আপনার সাবান শেষ হতে চলেছে — কাল আনার কথা মাথায় রাখুন।" At the end of the week it sends a simple summary of top-selling items. No app, no account creation beyond a WhatsApp number, no typing in English.

**3. Beneficiary audience**
Small shop owners across urban and semi-urban Bangladesh — a population of several million — the majority of whom own a smartphone but have never used a business management app. Also applicable to small pharmacies tracking medicine stock.

**4. Why now**
WhatsApp is the primary communication tool for this demographic. LLMs now handle noisy, informal Bangla text well enough for intent extraction. The barrier isn't technology — it's interface. A conversational, voice-of-the-user agent in Bangla eliminates the interface barrier entirely. No comparable product exists for this market segment at this price point (free or near-free).

**5. Feasibility scope**
WhatsApp Business API → Bangla NLU for stock event parsing (sold / received / check) → lightweight per-shop inventory store → threshold-based reorder logic → weekly summary generation. No heavy ML inference needed — the LLM handles only short text classification and reply generation. Extremely resource-efficient and scalable per-user cost is negligible.

---

## Idea 12 — Government Service Navigation Agent

**Tag:** Quick Build

**1. Problem being solved**
Ordinary citizens in Bangladesh lose days navigating government services — NID corrections, birth certificates, land records, passport applications, trade licenses — because the requirements, office locations, form names, and processing steps are scattered, poorly documented, and change without notice. Most people rely on brokers (দালাল) who charge fees to navigate the system on their behalf. This adds cost, creates corruption vectors, and leaves citizens dependent on intermediaries for services they are entitled to directly.

**2. The AI agent concept**
A WhatsApp agent that answers plain-language questions about government services in Bangla: "পাসপোর্ট নবায়ন করতে কী কী লাগবে?" or "জন্ম নিবন্ধন সনদ হারিয়ে গেলে কী করতে হবে?" The agent responds with step-by-step instructions, required documents, relevant office addresses, current fee amounts, and estimated processing times — sourced from a curated, regularly updated knowledge base of official government procedures. It also tells users which steps can be done online via government portals and provides direct links.

**3. Beneficiary audience**
General public across Bangladesh, particularly first-time applicants, rural citizens visiting divisional offices, and small business owners applying for trade or import licenses. The agent is especially valuable for people who cannot afford a broker and lack connections to navigate bureaucracy informally.

**4. Why now**
Bangladesh's a2i (Access to Information) programme has digitized significant portions of government services, but discoverability and guidance remain poor. LLMs handle Bangla conversational queries well. The knowledge base (government service requirements) is stable enough to maintain with monthly updates. No existing service combines conversational Bangla guidance with up-to-date procedural accuracy at zero cost to the user.

**5. Feasibility scope**
Curated knowledge base of government service procedures (document requirements, steps, fees, offices) → RAG-based retrieval → Bangla response generation via LLM → WhatsApp delivery. The bottleneck is knowledge base curation and keeping it current — not the agent itself. This is a content problem more than a technology problem, making it highly feasible to launch with a scoped set of high-demand services (passport, NID, birth certificate, trade license) and expand.
