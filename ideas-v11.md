# DSI Ideathon 2026 — Ideas (v11)

Formatted to match the official submission form structure.

---

## Idea 31

**Title**
NoShow Killer — Clinic Appointment & Follow-up Agent

**The Problem**
Private clinics and diagnostic centers in Bangladesh book appointments entirely by phone. No reminders are sent. No-show rates run at 30–40% on any given day — a doctor sitting idle for 20 minutes per missed patient is direct revenue loss the clinic absorbs silently. On the other side, patients forget appointments, can't easily reschedule, and have no record of what the doctor told them to do next. This happens every single day across every private clinic in the country.

**The Agent Idea**
A WhatsApp agent that lives between the clinic receptionist and the patient. The receptionist books an appointment as normal — then forwards a standard message to the agent with patient name, number, doctor, date and time. The agent takes it from there: sends the patient a confirmation, a 24-hour reminder, and a 2-hour reminder. If the patient replies "cancel" or "reschedule," the agent notifies the receptionist and opens a new slot. After the visit, it sends a follow-up 3 days later: "How are you feeling? Do you need to book a follow-up?" — all in Bangla.

Typical interaction: Receptionist texts the agent "Karim Ahmed, 01711xxxxx, Dr. Nadia, Thursday 4pm." Agent confirms to receptionist, sends patient a booking confirmation, reminder chain, and post-visit follow-up automatically. Receptionist does nothing further.

**Who Benefits**
Clinic owners and practice managers pay — the ROI is immediate: one recovered no-show per day covers the monthly subscription. Bangladesh has an estimated 15,000–20,000 private clinics and diagnostic centers. At BDT 1,500/month per clinic, even 2,000 clinics = BDT 3M/month recurring. Patients benefit from reminders and follow-up without downloading anything.

**Why Now**
WhatsApp Business API makes broadcast reminders with reply handling practical and cheap. LLM intent detection handles "reschedule," "cancel," and "confirm" replies in noisy Bangla. The no-show problem is universal and well-understood — clinics know exactly what it costs them. No product currently targets this specific workflow for the BD private clinic market.

**Feasibility & Scope**
POC in 1–2 weeks: receptionist-facing intake message → patient reminder chain → cancel/reschedule reply handling → receptionist notification. No clinic software integration needed in MVP — the agent works as a standalone WhatsApp number. Biggest unknown: getting receptionists to consistently use the intake format. Solved with a simple template they paste and fill.

**Tag:** Quick Build

---

## Idea 32

**Title**
LoanReady — Bank Loan Application Preparation Agent

**The Problem**
Thousands of small business owners and individuals apply for bank loans in Bangladesh every month and get rejected — not because they don't qualify, but because their application is incomplete, their documents are wrong, or their financials are presented in a format the bank doesn't accept. Bank loan officers spend significant time returning incomplete applications. Applicants waste weeks resubmitting. The rejection often feels arbitrary because nobody told them exactly what was missing. Both sides lose time on a preventable problem.

**The Agent Idea**
A WhatsApp agent that walks a loan applicant through preparation before they set foot in a bank. The user states the bank name and loan type (SME loan, home loan, personal loan). The agent responds with the exact document checklist for that bank and loan type, then asks questions one at a time to assess readiness: trade license status, last 6 months bank statements, tax return, collateral type. Based on answers it tells the applicant what's missing, what format the bank requires it in, and what to fix before applying. It doesn't apply on their behalf — it makes sure they arrive ready.

Typical interaction: User sends "Islami Bank SME loan দরকার." Agent replies with document checklist, asks "আপনার ট্রেড লাইসেন্স কি আপ টু ডেট?" — works through each item, ends with a readiness summary: "আপনি ৭টার মধ্যে ৫টা ডকুমেন্ট রেডি। বাকি ২টা হলো..."

**Who Benefits**
Individual applicants save time and rejection cycles — millions of SME owners and individuals apply for loans annually in BD. Banks benefit from cleaner applications and lower processing cost per approved loan — making banks the more attractive enterprise buyer. A bank embedding this agent on their website or distributing it to branch visitors reduces their loan officer's administrative burden measurably. Sell to banks and NBFIs as a customer-facing pre-screening tool: BDT 50,000–200,000/month per institution.

**Why Now**
LLM reasoning over a structured knowledge base of bank-specific requirements is now reliable. Bangladesh Bank has been pushing financial inclusion — banks have regulatory incentive to approve more loans, not just reject them faster. The agent requires no bank API access in MVP — it runs entirely on a curated knowledge base of requirements that can be built and maintained manually.

**Feasibility & Scope**
Knowledge base of loan requirements per bank per product type → conversational checklist walkthrough → readiness assessment → gap summary. POC covers 3 banks × 2 loan types in 2 weeks. Biggest unknown: keeping the knowledge base current as banks update requirements. Solved with a quarterly review process and a bank partnership that provides official documentation.

**Tag:** Quick Build

---

## Idea 33

**Title**
FilterFirst — Job Application Screening Agent for HR Teams

**The Problem**
A mid-sized company posting a job on Bdjobs receives 300–800 applications within 48 hours. An HR officer manually opens each CV, skims for basic fit, and shortlists 20–30 for review — a process that takes 2–3 full working days per vacancy and is applied inconsistently depending on how tired the reviewer is. Good candidates in plain CVs get skipped. Weak candidates with formatted CVs get through. Every hire starts with this bottleneck, and companies hiring frequently — banks, telecom, FMCG, garment buying houses — repeat it dozens of times a year.

**The Agent Idea**
A web-based agent that lives inside the HR team's workflow. The HR manager pastes the job description and uploads the CV batch (or connects a Bdjobs/email intake). The agent screens every application against the job requirements, scores each candidate on fit (0–100) with a one-paragraph explanation, flags must-have criteria misses, and delivers a ranked shortlist in under 10 minutes. The HR officer reviews the shortlist, not the pile. For shortlisted candidates, the agent sends a WhatsApp screening message with 3 role-specific questions — answers come back, agent summarizes and appends to each candidate's profile.

Typical interaction: HR uploads 400 CVs and the job description at 9am. By 9:10 they have a ranked list of 25 candidates with fit scores and gap notes. They approve the top 15 for WhatsApp screening. By end of day, 12 have replied. Agent summarizes answers. HR books interviews from a curated, pre-screened list.

**Who Benefits**
HR managers and talent acquisition teams at companies hiring 20+ people per year. In Bangladesh: banks, telecom companies, FMCG firms, garment buying houses, large NGOs, and recruitment agencies placing candidates for clients. Recruitment agencies are a particularly strong buyer — they screen for multiple clients simultaneously and bill per placement. Market: ~5,000 companies in BD hiring at meaningful volume. At BDT 5,000–15,000/month per company: BDT 25–75M/month at 5,000 clients.

**Why Now**
LLMs can now reliably extract structured information from unstructured CVs and score against criteria — something rule-based ATS systems couldn't do accurately. Bdjobs application volumes have grown faster than HR team sizes. Bangladesh's growing corporate sector means more companies are hiring at scale without large HR departments. No BD-specific CV screening tool exists — the market is served by manual effort or expensive global ATS platforms that are over-engineered for local needs.

**Feasibility & Scope**
CV batch upload → LLM extraction + scoring against JD → ranked shortlist with fit explanations → WhatsApp screening question dispatch → answer summarization. POC is a single job posting end-to-end in 2 weeks. Integrating with Bdjobs API (if available) or email intake is the first production step. Biggest unknown: scoring consistency across very different CV formats common in BD — addressed by prompt engineering and a calibration step where HR validates the first 10 scores.

**Tag:** Quick Build
