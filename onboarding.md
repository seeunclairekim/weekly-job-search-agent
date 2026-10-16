# Setup interview and stored profile

Present this short checklist; prefill supported answers and skip answered questions:

1. Upload a CV, paste your background, or upload a LinkedIn PDF. A profile link is optional; explain access limitations if encountered.
2. Confirm education, expected graduation, experience, skills, and languages extracted from it. Attach each claim to its source; let the user correct errors.
3. Which roles and industries interest you? What do you want to learn or move towards?
4. Where should the job be? Include commute radius and remote/hybrid preferences.
5. Student, part-time, internship, or graduate role? Weekly hours, earliest start, and study commitments?
6. What are your must-haves and exclusions? Optional salary expectations and work-authorization constraints only if relevant; do not infer nationality or eligibility.
7. Any preferred companies? Rank priorities such as responsibilities, learning, flexibility, salary, and industry. Separate deal-breakers from preferences.
8. Choose report language, delivery email, weekday/time, and timezone. Explain that scheduling and email need connected integrations.

Minimum viable profile: experience/education summary, target roles, location, and work type/hours. Unknown fields stay null. If no documents are available, use a short self-description and label it as such. Do not make the user answer irrelevant questions.

Use this structured representation in a durable task prompt or an explicitly authorized profile file:

```json
{
  "profile_version": 1,
  "updated_at": null,
  "name": null,
  "education": [],
  "experience": [],
  "skills": [],
  "languages": [],
  "target_roles": [],
  "industries": [],
  "location": {"cities": [], "commute_minutes": null, "remote": null},
  "work_types": [],
  "hours_per_week": {"min": null, "max": null},
  "earliest_start": null,
  "graduation": null,
  "must_haves": [],
  "exclusions": [],
  "preferred_companies": [],
  "priorities": [],
  "sources": [],
  "uncertain_or_dated_facts": [],
  "delivery": {"email": null, "language": null, "weekday": "Friday", "time": null, "timezone": null},
  "feedback": {"applied_job_ids": [], "explicit_preferences": []}
}
```

Store only necessary profile information, not a full CV in an email or task prompt. Never save another student's data into Albert's bundled personal reference. Each student's task must contain their own profile and recipient. In this personal installation Albert's source remains private; a public classroom distribution must omit it.

Example invocation: 'Use Weekly Job Search to set up my profile. I am a business student in Aarhus looking for a 10–15-hour student analyst role. Here is my CV.'
Example update: 'Exclude cold-calling roles and increase my maximum commute to 45 minutes.' Update confirmed preferences and the relevant scheduled task, then report the saved change.
