---
name: weekly-job-search
description: Set up a personal student or junior job-search profile, find and compare fresh vacancies, explain application requirements, and configure weekly top-five email digests. Use for Weekly Job Search, onboarding, preference updates, job feedback, or explaining this assistant. Includes Albert Slooten's private preset.
---

# Weekly Job Search

## Select the profile and mode

Support setup, one-off search, weekly digest, preference updates, and project explanation. Follow current explicit instructions over defaults. Use the user's language; Albert's search reports default to Danish.

For Albert, read [his private profile and complete company list](references/albert-profile-and-companies.md) in full before a search. Preserve factual experience and the original company list. Never apply Albert's background to another student. For another student or a demonstration, use only their supplied profile or explicitly fictional data. Never include Albert's private reference in a shareable version without his explicit authorization.

For setup and tailoring, read [onboarding and profile fields](references/onboarding.md). Ask only for missing information, extract supported facts from uploaded documents, and show the resulting profile for correction. A LinkedIn URL does not establish access to its contents: ask for a PDF export or pasted text if unavailable. Do not claim to have read an absent CV. A CV and LinkedIn export are alternatives, not mandatory duplicate inputs.

For Albert, treat semester, employment status, exchange, return date, availability, and application pipeline as dated. Do not generalize the old Balance January 2027 start date to all roles. In unattended runs continue research and flag uncertain availability; do not invent current status.

## Search and verify

1. Establish local run time and date window. Default digest: the preceding seven days ending at run time; this covers weekends between Friday runs. If the user specifically requests the calendar week, use Monday 00:00 through run time. State the actual interval. An explicit date range overrides defaults.
2. Read available prior digest history and explicit feedback. For email delivery, search only relevant sent Weekly Job Search messages and their reply threads. Match the current user and recipient. Without an accessible baseline, say duplicate checking was limited; do not claim something was newly posted because it was first discovered today.
3. Search the user's selected companies and relevant job boards. For Albert's normal full search, check every company in his bundled list plus Copenhagen startups. Keep the audit separate from the short digest. Only use a smaller source set if the user requests it; never imply complete coverage when sources were skipped or blocked.
4. Read [source access and technical workflow](references/workflow.md) for public ATS feeds, evidence fields, and fallback methods. Prefer official individual listings. Follow pagination. Reading a careers homepage is not equivalent to reading its jobs. Respect authentication and access controls; inaccessible means unknown, not no vacancies.
5. Verify the individual job is open and extract duties, required/preferred qualifications, location, remote arrangement, hours, student eligibility, language, start date, deadline, application URL, and required documents. Mark absent fields 'not stated' (or 'ikke oplyst'). Link to evidence and record checked time.
6. Require reliable original publication evidence within the requested window for the fresh shortlist. Distinguish original publication, updates, reposts, and first-seen dates. Do not use a search-engine crawl date or updated_at as proof of new publication. Keep unknown-date leads separate, outside the top five.
7. Deduplicate by ATS job ID or canonical URL, then employer + title + location. Strip tracking parameters, not identity parameters. Exclude jobs already recommended or marked applied, unless the user requests updates. Label genuine changes separately.

## Compare and rank

Apply hard requirements first: location/remote compatibility, work type and hours, mandatory education/student status, language, start timing, and exclusions. Reject known contradictions. Treat missing material requirements as uncertainty rather than a pass. Keep full-time exceptions outside a student-only top five unless explicitly allowed.

For remaining candidates compare: responsibilities and career goals (40%), supported experience/skills (30%), practical compatibility (20%), and stated company/sector preferences (10%). These are an adjustable editorial rubric, not a probability of being hired. Use strong/plausible/uncertain labels in the digest rather than falsely precise percentages. Within similar fit, prioritize an approaching verified deadline, then newer publication.

For each recommendation connect at least one actual duty to a supported profile example, identify a meaningful gap or uncertainty, and explain the tradeoff against other shortlisted jobs. Do not infer technical skills from a business degree or invent achievements. For Albert use concrete founder support, HubSpot workflows, dashboards, investor updates, or market research where relevant; preserve 'department record' for Telia and never expose Legacy's revenue situation.

## Deliver and explain applications

Return up to five verified fresh relevant vacancies, ordered by fit. Fewer than five is a valid result; never fill with stale, closed, unsuitable, or fabricated jobs. Include:

- Role, employer, direct application link, original publication date, and verification date.
- Location/remote, hours, deadline, and material eligibility information.
- Why it fits this profile, the main gap, and why it ranks here.
- Application documents explicitly required by the advert, separately from optional advice. A suggested cover letter must not become an employer requirement.
- Two or three concrete application priorities: relevant CV experience, evidence to emphasize, and a role-specific cover-letter angle if useful. Never invent metrics.

End with a short coverage count and blocked/missing-source disclosure, plus separate uncertain leads if useful. Keep the full source audit in the run result, not in a long email. If none qualify, send an honest zero-match report. Say whether history was available.

For feedback accept 'relevant', 'maybe', 'irrelevant', or 'already applied', plus a reason. Record applied job identifiers to suppress repeats. A single irrelevant job does not imply exclusion of its entire industry; ask or use explicit reasons. Persist confirmed preference changes in the authorized profile/task configuration; do not claim model training or automatic learning. Never claim a change is durable unless a save succeeds.

## Schedule and email

Read [workflow](references/workflow.md) before configuring delivery. A skill supplies instructions; scheduling and email are separate integrations. On a request for recurring delivery, use Automations and verify required connector access with a harmless read first. Resolve the recipient from the user's explicit address or authenticated self profile. Do not silently use a profile contact address as the delivery address.

Use the user's timezone; Albert's is Europe/Copenhagen. For 'every Friday' without a clock time, use Friday morning with flexible scheduling and disclose the chosen window. Use exact scheduling only for an explicit clock time. Privately check existing tasks and update the matching one to avoid duplicates.

Make the task self-contained: include confirmed profile facts, exclusions, sources, date window, ranking and application guidance, recipient, language, history method, and failure behavior. Do not rely on temporary local files or this conversation being available to future runs. Include the skill when accessible, but carry essential instructions in the task itself. Save confirmed profile changes to the task as well as any authorized profile store.

Send only to the authorized user. Use a stable subject prefix 'Weekly Job Search | YYYY-MM-DD'. Check the exact-date sent digest before sending so retries do not duplicate delivery. Use sent digests as the minimal durable recommendation ledger; search relevant reply threads for explicit feedback. Do not assume incoming email replies trigger this skill immediately. Apply them on the next run, or when the user asks. Never send applications, contact employers, or forward CVs without separate authorization.

Distinguish schedule saved, run requested, search completed, and email sent. Confirm only what tool results prove. If email fails, return the report in the task result and clearly state delivery failure. If a source fails, report partial coverage. Do not misreport source failure as zero jobs.

## Demonstrate the project

Explain five components simply: structured user profile, online source retrieval, AI comparison, scheduled trigger, and email delivery/history. Show the setup questions, a clearly labeled example digest or a verified live digest, and actual test results. Distinguish implemented instructions and configured integrations from untested reliability. Never represent a fictional demonstration as a real vacancy search or send synthetic jobs as real recommendations.
