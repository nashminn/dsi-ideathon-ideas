# DSI Ideathon 2026 — Ideas (v10)

---

## Idea 28 — Payroll & Attendance Agent for Small Factories and SMEs

**Tag:** Quick Build

**The Problem**
Small factories, workshops, and SMEs across Bangladesh — garment accessories units, printing presses, small food processors, construction firms — track worker attendance on paper registers and calculate monthly salaries manually: basic pay, overtime, late deductions, advance repayments. Errors cause disputes, underpayments cause turnover, and the whole process consumes the factory manager's last week of every month. There is no affordable digital payroll tool built for a factory owner who isn't tech-savvy and manages 20–200 workers.

**The Agent Idea**
A WhatsApp agent where a floor supervisor marks daily attendance by sending a simple message — "absent: Karim, Rahim / late: Saleha" — and the agent maintains a running attendance log per worker. At month end it calculates each worker's salary automatically: base rate × days present, overtime if logged, deductions for advances or absences, and generates a clean payslip per worker sent directly to their WhatsApp number. The factory owner gets a one-message payroll summary showing total payout, deductions, and advance balances. All in Bangla.

**Who Benefits**
Factory owners and operations managers at small and mid-sized manufacturing units — estimated 500,000+ registered SME employers in Bangladesh. Workers benefit from transparent, documented payslips that reduce dispute. Primary buyer is the owner or manager; willingness to pay is high because the alternative is hours of manual calculation and frequent errors that cost real money in disputes and turnover.

**Why Now**
Worker smartphone penetration is high enough that WhatsApp payslip delivery is practical. bKash and Nagad have made digital wage disbursement a realistic next step — this agent is the calculation layer that makes it possible. Labour law enforcement around documented wage payment is tightening. No product currently serves this tier of employer in Bangla with zero onboarding friction.

**Feasibility & Scope**
Worker roster setup (one-time WhatsApp conversation) → daily attendance intake → monthly salary calculation engine (configurable rates, overtime rules, deductions) → payslip generation → WhatsApp broadcast to workers. POC is a single-factory pilot with fixed pay structure in 2–3 weeks. Full version adds advance tracking, multiple pay grades, and export to bank disbursement format. Revenue: BDT 500–1,500/month per employer. At 20,000 employers: BDT 10–30M/month recurring.

---

## Idea 29 — Construction Site Daily Reporting & Material Audit Agent

**Tag:** Quick Build

**The Problem**
Real estate developers and building contractors in Bangladesh lose significant money to two silent problems: material pilferage (cement, rods, tiles disappearing from site) and lack of daily visibility into actual vs. planned progress. Developers funding multi-crore projects receive updates when the site supervisor feels like calling. There is no verifiable daily record of how many workers were on site, what materials were used, and what work was completed — so by the time a budget overrun or delay becomes visible, it's already too late to course-correct.

**The Agent Idea**
A WhatsApp agent used by the site supervisor at end of each working day. They send a structured update — workers present, materials received and used, work completed (e.g., "3rd floor slab pouring: 60% done"), and any issues. The agent parses this, appends it to a running project log, and sends the developer a clean daily summary. It cross-references material usage against progress (if 50 bags of cement were used but only 10% of the slab was poured, it flags the anomaly). Weekly it generates a progress-vs-plan summary. The developer gets ground truth without being on site.

**Who Benefits**
Real estate developers, building contractors, and project owners managing construction in BD — a market growing rapidly with urbanization. The buyer is the developer or project owner who has real money at stake and currently has no reliable information channel between them and the site. Banks financing construction projects are a secondary buyer — this agent produces audit-ready disbursement documentation.

**Why Now**
Dhaka's real estate sector is booming despite economic headwinds — construction activity is near-record. Material cost inflation makes pilferage more expensive than ever. Developers are increasingly funding multiple simultaneous projects and cannot be on every site. WhatsApp is already how supervisors communicate informally — this agent structures what they're already doing.

**Feasibility & Scope**
Daily report intake via WhatsApp (structured text prompt to supervisor) → field extraction → project log append → anomaly detection (material vs. progress ratio) → daily digest to developer → weekly summary generation. POC is a single active construction site, deployable in 2 weeks. Revenue model: BDT 2,000–5,000/month per active project site, or per-developer subscription covering all active sites. High-value market — a developer running 5 simultaneous projects pays BDT 10,000–25,000/month and saves multiples of that in material losses alone.

---

## Idea 30 — Legal Document Drafting Agent for Small Businesses

**Tag:** Quick Build

**The Problem**
Small businesses, freelancers, and entrepreneurs in Bangladesh routinely operate without basic legal documents — employment contracts, supplier agreements, service agreements, rent agreements, MoUs — because drafting one means hiring a lawyer at BDT 5,000–20,000 per document, which most small businesses won't pay for a one-page agreement. So they operate on handshake deals that turn into disputes. The legal risk isn't theoretical — it's a recurring financial loss when the dispute arrives with no documentation to stand on.

**The Agent Idea**
A WhatsApp agent that generates standard, BD-law-compliant legal documents through a guided question-and-answer flow in Bangla. The user says "আমার একটা চাকরির চুক্তি দরকার" and the agent asks 6–8 targeted questions: employee name, role, salary, notice period, probation duration, any specific clauses. Within minutes it produces a clean, formatted document as a PDF — ready to print and sign. Covers the 8–10 most common document types: employment contract, supplier agreement, service agreement, tenancy agreement, freelance contract, partnership deed, NDA, MoU. Per-document fee or monthly subscription for businesses that generate documents regularly.

**Who Benefits**
Small business owners, freelancers, startup founders, landlords, and traders — tens of millions of people who transact regularly but can't afford or won't pay lawyer rates for routine documents. Law firms and CA firms are a B2B channel: they white-label the agent for their own clients, saving their junior staff hours on boilerplate drafting. Legal tech is globally one of the highest-margin SaaS categories.

**Why Now**
LLMs are now reliable enough to generate structured legal documents from templates with variable substitution — the document doesn't require creative legal reasoning, just correct clause selection and field population. Bangladesh's growing freelance economy (BD is a top-5 global freelance market by volume) creates millions of people who need service contracts but have no access to affordable legal drafting. No Bangla-language legal document generator exists.

**Feasibility & Scope**
Document type selection → guided Q&A flow (fixed question set per document type) → template population via LLM → PDF generation → WhatsApp delivery. POC is 3 document types (employment contract, service agreement, tenancy agreement) in 2–3 weeks. Legal review of base templates by a BD lawyer is the critical non-technical dependency — done once per template, not per generation. Revenue: BDT 100–300 per document (transactional) or BDT 1,000–3,000/month subscription for frequent users. Law firm white-label accounts at BDT 10,000–30,000/month. Globally proven model (Rocket Lawyer, LegalZoom) with zero BD-specific competition.
