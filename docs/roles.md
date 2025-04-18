# PoliForge Campaign Role Mapping

This document outlines the real-world roles found in political campaigns and maps them to their equivalents (or automation targets) within the PoliForge architecture.

The goal is to clearly define:
- Which campaign roles PoliForge supports
- Which functions are automated, augmented, or human-led
- How these map to individual services and interfaces

---

## 🧍 Candidate
**Traditional Role:** Public figure, decision-maker, messenger

| Function | PoliForge Service | Automation Level |
|----------|--------------------|------------------|
| Profile & Platform | `candidate-service` | Manual input |
| Calendar & Events | `candidate-service`, `campaign-service` | Semi-automated |
| Voice & Tone Definition | `candidate-service` | Manual input + AI-assisted tuning |
| Speech Generation | `candidate-service`, `media-manager` | AI-generated drafts with manual approval |
| Debate Prep | `candidate-service`, `voterbot` | Simulated Q&A, issue prediction |

---

## 🧑‍💼 Campaign Manager
**Traditional Role:** Oversees all operations, strategy, and communication

| Function | PoliForge Service | Automation Level |
|----------|--------------------|------------------|
| Strategic Planning | `campaign-service`, `intel-service` | AI-assisted, human-reviewed |
| Messaging Coordination | `campaign-service`, `media-manager` | AI-generated content pipeline |
| Fundraising Oversight | `campaign-service` | Manual + AI-optimized appeals |
| Volunteer Management | `volunteer-mobilizer` | Admin interface + automated reminders |
| Compliance Monitoring | `infrastructure` | Alerts, logs, form templates |

---

## 🧠 Data Analyst / Pollster
**Traditional Role:** Provides insights on voters, sentiment, and trends

| Function | PoliForge Service | Automation Level |
|----------|--------------------|------------------|
| Demographic Analysis | `constituency-intel` | Fully automated |
| Sentiment Tracking | `constituency-intel` | RAG + ML summarization |
| Issue Heatmapping | `constituency-intel` | AI-generated, tunable granularity |
| Opposition Benchmarking | `counter-campaign` | Semi-automated, receipts required |

---

## 🛠️ Field Director / Volunteer Lead
**Traditional Role:** Manages ground game, canvassing, events

| Function | PoliForge Service | Automation Level |
|----------|--------------------|------------------|
| Event Planning | `campaign-service`, `volunteer-mobilizer` | Calendar-aware scheduling |
| Volunteer Coordination | `volunteer-mobilizer` | Contact trees, email/SMS blasts |
| Contact Scripts | `media-manager`, `campaign-service` | Auto-generated per voter segment |
| Yard Sign Tracking (manual) | _External integration_ | TBD |

---

## 🎨 Comms & Design Team
**Traditional Role:** Designs social media, flyers, websites, press kits

| Function | PoliForge Service | Automation Level |
|----------|--------------------|------------------|
| Graphic Generation | `media-manager` | AI + templates, editable by humans |
| Press Releases | `campaign-service` | Auto-drafted, editable |
| Social Scheduling | `campaign-service` | Smart queueing + A/B content testing |
| Brand Consistency | `candidate-service`, `media-manager` | Voice lock + asset reuse |

---

## 🛡️ Opposition Research
**Traditional Role:** Identifies weaknesses in opponents' records

| Function | PoliForge Service | Automation Level |
|----------|--------------------|------------------|
| Vote Tracking | `counter-campaign` | Fully automated |
| Quote Aggregation | `counter-campaign` | Fully automated, receipts generated |
| Narrative Building | `counter-campaign`, `media-manager` | Drafted by AI, approval required |
| Risk Analysis | `infrastructure` | Flagging based on tone/slander detection |

---

## 🗳️ Voter Outreach (Public Interface)
**Traditional Role:** Answers voter questions, builds trust

| Function | PoliForge Service | Automation Level |
|----------|--------------------|------------------|
| Voter Q&A | `voterbot` | LLM-powered with audit trails |
| Policy Clarifications | `voterbot`, `campaign-service` | Retrieved from platform/records |
| Feedback Intake | `constituency-intel` | Logged and classified |
| FAQ Generation | `voterbot`, `media-manager` | AI-generated from campaign data |

---

## 👥 Roles Not Yet Supported (Future Modules)

- Legal Counsel / FEC Liaison (manual for now)
- Coalition Builder (possible plugin)
- SMS/Phonebanking backend (integration-ready)
- PAC Interfacing Tools (intentionally omitted for ethical reasons)

---

This role map will evolve as PoliForge grows and contributor needs become clearer. All suggestions for expanding or refining roles are welcome in the GitHub Issues section.

