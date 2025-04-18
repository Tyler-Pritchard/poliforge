# PoliForge Data Sources

This document lists and evaluates potential external data sources that PoliForge may integrate with. These sources power constituent analysis, issue tracking, opposition research, and AI-assisted messaging through Retrieval-Augmented Generation (RAG) pipelines.

---

## 🧠 Constituency Intelligence Sources

| Source | Type | Purpose | Access Level | Notes |
|--------|------|---------|---------------|-------|
| [OpenStates API](https://v3.openstates.org/) | API | State legislation, roll calls, bill sponsors | ✅ Public API (key required) | High-quality for state-level races |
| [U.S. Census API](https://www.census.gov/data/developers/data-sets.html) | API | Demographics, economic data by district | ✅ Public API | Requires normalization by region/district |
| [Ballotopedia](https://ballotpedia.org/) | Scrape / API | District maps, election histories, candidates | ⚠️ No public API | Needs scraping strategy / fallback plans |
| Local news aggregators (e.g., Patch, NPR local) | Scrape / RSS | Sentiment, issues, narrative detection | ⚠️ Requires scraping | Evaluate feasibility + licensing |
| [ProPublica Congress API](https://projects.propublica.org/api-docs/congress-api/) | API | Federal votes, bills, statements | ✅ Public API | For federal races or opponent validation |

---

## 🛡️ Opposition Research Sources

| Source | Type | Purpose | Access Level | Notes |
|--------|------|---------|---------------|-------|
| [FEC API](https://api.open.fec.gov/developers/) | API | Donations, PACs, filings | ✅ Public API | Supports federal races only |
| [FollowTheMoney.org](https://www.followthemoney.org/tools/) | API | Campaign finance by state | ✅ Public API (key required) | Ideal for statehouse, governor, AG races |
| Opponent social media (X, Facebook, IG) | Scrape/API | Position mining, quote collection | ⚠️ Limited APIs | Needs custom pipelines + screenshot tooling |
| YouTube / Public debates | Scrape / ML | Video transcript + stance analysis | ⚠️ Manual ingestion or YouTube API | Requires Whisper / LLM summarization for insight |

---

## 🗳️ Voter Education & Civic Tools

| Source | Type | Purpose | Access Level | Notes |
|--------|------|---------|---------------|-------|
| [CanIVote.org](https://www.nass.org/Can-I-Vote) | Directory | State-specific registration & deadlines | ✅ Public | Link-based only, not API |
| [Vote.org](https://www.vote.org/) | Site / Scrape | Voter registration tools | ⚠️ Proprietary / restricted | Evaluate ethical use / link only |
| [Local election boards](varies) | Site / Email | Local deadlines, rules, ballots | ⚠️ Fragmented | May require manual entry or partnerships |

---

## 📝 Message Calibration & Tone Alignment

| Source | Type | Purpose | Access Level | Notes |
|--------|------|---------|---------------|-------|
| Internal candidate data | Manual input | Candidate beliefs, tone, off-limit topics | ✅ Fully controlled | Used to calibrate all AI outputs |
| Public sentiment (Reddit, Twitter, FB) | Scrape / API | Community-level opinion trends | ⚠️ Rate-limited, potential TOS issues | Ethical filtering required |

---

## 📌 Next Steps

- Create internal wrappers for key APIs (OpenStates, Census, FEC)
- Define rate limits, fallbacks, and caching strategies
- Build modular RAG pipelines for `constituency-intel` and `counter-campaign`
- Log all AI-generated claims with source metadata ("receipts engine")
- Explore optional plugin layer for local reporters, civic orgs, and data partnerships

---

_For new source suggestions or API integration proposals, open a GitHub Issue in the main repository._

