# DSI Ideathon 2026 — Submission Ideas

Max 3 ideas per person. All tagged per ideathon format. Scored against: Business Value (30%), Problem Clarity (25%), Originality (25%), Feasibility (20%).

---

## Idea 1 — Meeting-to-Action Agent

**Tag:** Quick Build

**1. Problem being solved**
Meetings produce verbal commitments that go untracked. Decisions and action items are buried in notes no one reviews, causing missed deadlines and repeated conversations. Knowledge workers spend ~30% of their week in meetings yet follow-through rates are low.

**2. The AI agent concept**
An agent that ingests a meeting recording or transcript (Zoom, Google Meet, Teams), extracts every action item, maps each to a named owner from the attendee list, infers a deadline from context, and pushes tasks directly to Jira/Trello/Asana — then sends a structured follow-up email to all attendees within minutes of the meeting ending.

**3. Beneficiary audience**
Project managers, team leads, and operations staff at any company running recurring standups, client calls, or planning sessions. Immediately useful to software firms, agencies, and consulting teams.

**4. Why now**
Transcription APIs (Whisper, AssemblyAI) and LLM function-calling are mature enough to do this reliably and cheaply. Remote/hybrid work has made meeting sprawl worse, and no mainstream PM tool has solved the transcript-to-task gap natively.

**5. Feasibility scope**
Transcript → structured JSON (owners, tasks, deadlines) via LLM → webhook push to PM tool of choice. A working prototype can be built in days. Productizing requires integrations and an auth layer but no novel research.

---

## Idea 2 — Regulatory Change Monitor Agent

**Tag:** Big Bet

**1. Problem being solved**
Businesses operating in regulated industries (fintech, health, food, software export) face a constant stream of regulatory updates — GDPR amendments, local data laws, labor code changes — that legal and compliance teams struggle to monitor manually. Missing an update can mean fines or halted operations.

**2. The AI agent concept**
An agent that continuously scrapes official regulatory sources and legal gazette feeds for a specified jurisdiction and industry, summarizes what changed, maps each change to internal policy documents, identifies gaps, and drafts a memo flagging what needs updating — routed to the responsible team via Slack or email. Runs on a weekly cadence or triggers on detected change.

**3. Beneficiary audience**
Compliance officers, legal teams, and CTOs at mid-to-large companies in fintech, healthcare, HR tech, and any SaaS serving regulated markets. Particularly valuable for companies operating across multiple countries.

**4. Why now**
Regulatory velocity is increasing globally (AI Act, DPDP, SEC cybersecurity rules). RAG over regulatory documents is now practical with vector databases + LLMs. No affordable automated solution exists for SMBs — they rely on expensive law firm retainers or manual monitoring.

**5. Feasibility scope**
RSS/scraper layer → chunked vectorstore of current regulations → LLM diff-and-map against company policy docs → report generation. Challenging to make exhaustive but a scoped version (e.g., one country + one domain) is buildable. Big Bet due to data sourcing complexity and need for accuracy guarantees.

---

## Idea 3 — Client Requirement Extraction Agent

**Tag:** Quick Build

**1. Problem being solved**
Software and service companies lose significant time translating vague client briefs — scattered across emails, call notes, and PDFs — into structured requirements, user stories, and effort estimates. This work is repetitive, error-prone, and often the root cause of scope creep.

**2. The AI agent concept**
An agent that accepts raw client communication (email threads, call transcripts, uploaded documents) and outputs: a structured requirement spec, prioritized user stories in a standard format (As a / I want / So that), a list of open questions to clarify with the client, and a rough complexity estimate per story. Output is pushed into a Confluence page or Google Doc, ready for review.

**3. Beneficiary audience**
Business analysts, solution architects, and project managers at software development firms, digital agencies, and IT consultancies. Directly reduces BA hours per project and improves consistency across proposals.

**4. Why now**
LLMs are strong at information extraction and structured output from unstructured text. The BA-to-developer handoff is a well-understood, universal pain point. Tooling (structured outputs, function calling) makes reliable spec generation achievable without fine-tuning.

**5. Feasibility scope**
Document ingestion → LLM extraction with a fixed output schema → template-filled Google Doc or Confluence page via API. Fully buildable with existing APIs. The main challenge is prompt engineering for edge cases, not infrastructure. A Quick Build with high immediate ROI.
