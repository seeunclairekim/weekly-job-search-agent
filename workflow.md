# Source access, execution, and delivery

## Architecture

The AI reads profile fields and runs SKILL.md as a reusable procedure. Web retrieval supplies evidence. The AI extracts job fields and compares duties against profile evidence. Automations supplies the Friday trigger. The connected email tool sends the digest; relevant sent digests preserve recommendation history. This is an orchestrated workflow, not a standalone server or a custom-trained model.

Profile persistence: include the minimum confirmed profile in the saved automation prompt. An authorized persistent profile file may supplement it; never depend on scratch paths. History persistence: search sent emails with the digest subject prefix for this recipient, read the matching messages, and recover canonical job links. Use all available relevant history or state the searched interval. Read feedback only in matching digest reply threads. Do not claim perfect duplicate suppression when history access is incomplete.

## Source retrieval

Start from current official careers links. Where pages load vacancies dynamically, use their publicly accessible ATS listing endpoint, RSS feed, or structured JobPosting data. Follow detail links and pagination. Verify the endpoint still belongs to the employer. A public listing feed is a retrieval method, not permission to bypass restricted systems.

Previously useful public endpoints (recheck on each run):
- Implement: https://api.smartrecruiters.com/v1/companies/implementconsultinggroup/postings?limit=100
- Deloitte Nordic: https://api.smartrecruiters.com/v1/companies/DeloitteNordic/postings?limit=100 (paginate offsets and filter Denmark)
- Intellishore: https://boards-api.greenhouse.io/v1/boards/intellishoredk/jobs (follow individual jobs; updated_at alone is not original publication)
- Fellowmind: https://career.fellowmind.dk/jobs.rss
- twoday: https://twodaydenmark.teamtailor.com/jobs.rss
- Copenhagen Optimization: https://copenhagenoptimization.teamtailor.com/jobs.rss
- The Hub: https://thehub.io/jobs?countryCode=DK&sorting=newJobs (featured listings can be old; read each job's publication evidence)

Fallback order: official listing, official ATS/feed, public job board with attributable employer listing, search lead requiring verification. When access remains blocked, retain its source and failure in the audit. Never infer that no vacancies exist.

## Normalized evidence

For each candidate retain job_id, employer, title, canonical_url, source_url, checked_at, publication_date, publication_evidence, first_seen, status, duties, mandatory_requirements, preferred_requirements, location, remote, hours, education, languages, deadline, start_date, required_documents, match_evidence, gaps, and ranking_reason. Missing is null, not false. For each source retain checked_at, status, pages_read, and failure_reason. Keep candidate and source records within the run result if no authorized persistent data store exists.

## Email contract

Subject: Weekly Job Search | YYYY-MM-DD
Opening: actual date window, profile summary, number of qualifying matches, coverage.
Per job: rank/title/company; direct apply link; date, location, hours, deadline; fit with evidence; gap; required documents; CV focus and optional cover-letter angle.
Closing: missing information; coverage limitations; 'Reply with relevant, maybe, irrelevant, or already applied, the job number, and a short reason. Feedback is read during the next search.'

Do not attach or transmit the full CV. Send up to five, never promise exactly five. If none qualify, explain whether this reflects completed checking or limited access. Email success requires a returned sent-message identifier. Before a retry check for the date-specific digest to the authorized recipient; an uncertain send result requires reconciliation, not immediate resend.

## Demonstration and validation

For a classroom demonstration use a synthetic profile and clearly labeled fictional advertisements when live sources are unavailable. Demonstrate at least one eligible match, a closed job, an old job with a recent update, a duplicate, and a missing application-document field. Show that requirements and optional advice remain separate. Do not send test fixtures through live email unless explicitly requested and clearly labeled.

For a real end-to-end demonstration verify sources, generate the digest, send only to the authorized user, and retain the returned message identifier. Scheduling success does not prove search quality or future delivery. Evaluate real usefulness with a second student: have them label the recommendations and record relevant recommendations divided by recommendations shown, time spent, factual errors, and document-requirement accuracy. Do not fabricate user-validation results.
