**Weekly Job Search: A Personal AI Job Assistant**

Our project is a reusable AI workflow that helps students find suitable jobs and prepare their applications. Each user provides their own background, preferences and existing documents. Once setup and the required connections are complete, the workflow is designed to run automatically each week and email up to five relevant opportunities with application checklists and prepared PDF drafts.

The user remains responsible for reviewing the documents and submitting applications.

**1. Personal setup**

The assistant guides each user through a setup interview. It extracts information from uploaded documents, asks for missing details and presents a profile for the user to check.

| **Information**              | **What the user supplies**                                            |
| ---------------------------- | --------------------------------------------------------------------- |
| Personal details             | Name and contact information for applications                         |
| Current CV                   | Preferably an editable Word document; PDF is also accepted            |
| Previous motivational letter | A template that provides the user’s wording, style and experience     |
| LinkedIn information         | Optional PDF export or pasted text to supplement the CV               |
| Academic transcript          | Original PDF, preserved unchanged                                     |
| Education                    | Degree, university, expected graduation and confirmed GPA             |
| Experience                   | Employers, roles, employment dates, responsibilities and achievements |
| Skills and languages         | Actual skills and language proficiency                                |
| Target roles                 | The types of jobs the user wants                                      |
| Career goals                 | What the user wants to learn and work towards                         |
| Location                     | Preferred cities, commuting limits and remote or hybrid preferences   |
| Employment type              | Student job, part-time, internship, graduate or full-time             |
| Working hours                | Preferred hours and any firm maximum                                  |
| Availability                 | Earliest start date and relevant study commitments                    |
| Company preferences          | Preferred employers, sectors, company sizes or startup stages         |
| Exclusions                   | Responsibilities or conditions the user wants to avoid                |
| Additional requirements      | Optional salary expectations and relevant work eligibility            |
| Application history          | Previous applications and preferences about repeated recommendations  |
| Delivery preferences         | Confirmed email address, language, weekday, time and timezone         |

The reusable instructions are separate from the individual profile. Another student can therefore use the same workflow with their own information.

Missing facts are not invented. For example, an intention to study for a master’s degree is not treated as confirmed enrolment.

**2. Automatic weekly search**

A scheduler starts the workflow at the user’s chosen weekly time. Our current configuration uses Friday morning around 08:00 Copenhagen time.

The workflow loads the confirmed profile, retrieves the source documents and checks relevant recommendation history and feedback. It then searches selected company career pages and job boards.

The weekly search focuses on jobs published during the preceding seven days. It searches broadly before selecting **up to five suitable recommendations**. Five is a maximum, not a target that must be filled.

For promising opportunities, it reads the individual advertisement and checks:

- Whether the job is still open.
- Its original publication date.
- Responsibilities and required qualifications.
- Location and remote or hybrid arrangements.
- Working hours and employment type.
- Language and student-status requirements.
- Start date and application deadline.
- Required application materials.
- The exact application route.

A recently updated advertisement is not automatically treated as newly published. Unknown dates and inaccessible sources are reported honestly. Opening a company’s homepage does not count as checking all its vacancies.

**3. How the workflow decides which jobs fit best**

The selection has two stages: eligibility checks followed by comparison.

First, it rejects jobs with confirmed conflicts with essential requirements. For example, a role requiring full-time work may be incompatible with a student seeking a maximum of 20 hours per week. Missing information remains an uncertainty rather than an assumed match.

The remaining candidates are compared using four criteria:

| **Criterion**                     | **Weight** | **What it measures**                                                         |
| --------------------------------- | ---------- | ---------------------------------------------------------------------------- |
| Responsibilities and career goals | 40%        | Whether the actual work matches the user’s interests and desired development |
| Relevant experience and skills    | 30%        | Whether the user has evidence supporting the employer’s requirements         |
| Practical compatibility           | 20%        | How well location, hours, flexibility and timing fit                         |
| Company and sector preferences    | 10%        | Whether the employer matches the user’s stated preferences                   |

Each criterion is rated from 0–4: no fit, weak fit, partial fit, good fit or strong direct fit. Ratings must be supported by information from the advertisement and the user’s profile.

The comparison score is:

**Score = 25 × (0.40 × career fit + 0.30 × experience fit + 0.20 × practical fit + 0.10 × company fit)**

For illustration, ratings of 4, 3, 4 and 3 produce a score of 90 out of 100.

This is a **decision rubric, not a statistically validated prediction**. A score of 90 does not mean a 90% chance of being hired. The weights are design choices, and the AI’s ratings involve judgment. Users can adjust the priorities to reflect their needs.

A high total cannot compensate for a mandatory qualification the user does not meet. Weak matches should not be recommended simply because they are the best candidates in a poor selection. Where fit is similar, an approaching verified deadline and then publication recency help determine the order.

Each recommendation explains its supporting evidence and main gaps in ordinary language.

**4. Application requirements and submission instructions**

For each selected job, the workflow produces a clear application checklist.

| **Item**            | **What it identifies**                                                          |
| ------------------- | ------------------------------------------------------------------------------- |
| CV                  | Whether a CV is requested and any specific instructions                         |
| Motivational letter | Whether a letter or short motivation statement is requested                     |
| Grades              | Whether an academic transcript is required                                      |
| Portfolio           | Whether work samples or project links are requested                             |
| Video               | Whether a Loom or other video is requested, including stated length and content |
| Screening questions | Questions the applicant must answer                                             |
| Language and format | Any stated language, document format or length requirements                     |
| Submission route    | Company portal, recruitment platform or explicitly stated application email     |
| Deadline            | The stated deadline, or “not stated”                                            |

Materials are labelled **required**, **optional** or **not stated**. A general contact email is not assumed to be an application address.

**5. Preparing documents with minimal changes**

The user’s original CV and motivational letter serve as master templates. Each application starts from those originals, preventing changes from accumulating across jobs.

The aim is to preserve the user’s wording, voice, structure and formatting while making necessary adjustments.

For the CV, the workflow:

- Preserves section order, chronology, layout and existing bullet wording wherever possible.
- Applies confirmed factual corrections.
- Makes small, relevant wording adjustments where justified.
- Avoids unnecessary rewriting, removing experience or redesigning the document.

For the motivational letter, it:

- Updates the company, role, addressee and date where appropriate.
- Adjusts employer-specific motivation and relevant examples.
- Preserves transferable sentences and paragraphs.
- Removes references that belong to another employer.
- Avoids generic praise, invented achievements and unnecessary new paragraphs.

The final text is compared with the original. Changes without a clear factual or application-related purpose should be reverted.

Employer requirements take precedence where a different language, format or length is explicitly requested. Any substantial adaptation or material formatting limitation should be disclosed.

**6. PDF packages and quality checks**

The workflow prepares CV and motivational-letter PDFs where requested. Filenames automatically identify the applicant, company, role and document type, for example:

-

```
Applicant_Company_Role_CV_DRAFT.pdf
```

1.

```
Applicant_Company_Role_Motivational_Letter_DRAFT.pdf
```

1.

```
Applicant_Transcript.pdf
```

Before delivery, it checks for incorrect company names, outdated facts, unsupported claims, leftover placeholders and layout problems.

The original transcript is included unchanged when required. If several applications need it, it can be attached once with clear instructions.

A requested video remains a user action. The assistant can help prepare a script but cannot claim that the user has recorded a video.

**7. The weekly email**

The email contains up to five suitable jobs, ranked by fit. Each entry includes:

- Job title, company and application link.
- A specific explanation of why it fits.
- Qualification gaps and unresolved questions.
- Location, hours, deadline and verified publication information.
- Required application materials.
- Clearly named PDF attachments where prepared.
- A short explanation of changes made to the source documents.
- Remaining actions, such as reviewing drafts or recording a video.

The email also states the search period and important coverage limitations. If no suitable jobs can be verified, it sends an honest report explaining that outcome.

Missing documents or failed attachments must be disclosed. The workflow should only report successful sending when the email tool confirms it.

**8. Feedback and future searches**

Users can mark recommendations as relevant, maybe, irrelevant or already applied, and explain why.

The workflow consults this feedback during later searches. Explicit preference changes can update the stored profile, and recommendation history helps prevent unwanted repetition.

This is updating stored instructions and preferences; it is not retraining the AI model. A user can also request that previously considered jobs remain eligible.

**9. Technical architecture**

| **Component**              | **Purpose**                                                                 |
| -------------------------- | --------------------------------------------------------------------------- |
| Reusable skill             | Defines setup, search, verification, ranking and document-preparation rules |
| Individual profile         | Stores confirmed background and preferences                                 |
| Document storage           | Makes the original CV, letter and transcript accessible to future runs      |
| Scheduler                  | Starts the workflow at the chosen time                                      |
| Search and retrieval tools | Find advertisements and retrieve their contents                             |
| AI processing              | Interprets requirements, assesses fit and makes targeted document edits     |
| Document tools             | Generate, export and inspect PDFs                                           |
| Email integration          | Delivers recommendations and attachments                                    |
| History                    | Records recommendations, feedback and delivery outcomes                     |

The skill supplies the procedure. The connected tools perform the search, document creation, scheduling and delivery. Each user needs their own confirmed profile, accessible source documents and authorized email setup.

**10. What AI enables us to build**

Before this project, we could search for jobs and prepare applications manually. Building a reusable system that performs personalized comparisons across differently structured advertisements would have required substantially more programming and language-processing expertise.

AI helps us connect these tasks into a workflow that other students can use. It interprets advertisements, relates their requirements to an individual’s experience and prepares targeted application drafts using existing documents.

Our project therefore examines whether AI enables our team to build and operate a useful personalized service beyond what we could previously implement ourselves.

**11. How we evaluate it**

We will evaluate the workflow using:

| **Measure**              | **How we assess it**                                                                 |
| ------------------------ | ------------------------------------------------------------------------------------ |
| Recommendation relevance | The proportion of recommendations the user considers relevant                        |
| Factual accuracy         | Whether extracted details match the original advertisements                          |
| Document quality         | Whether drafts preserve the original style and make only necessary, accurate changes |
| Time saved               | Total time spent, including review and corrections, compared with a manual process   |
| Technical reliability    | Whether a scheduled run completes searching, document preparation and email delivery |
| Adaptability             | Whether another student can use it successfully with their own profile               |

For example, four relevant recommendations out of five would give an observed relevance rate of 80% for that test. Multiple users and repeated runs are needed before drawing broader conclusions.

The current automation contains the five-job limit, ranking rubric, application-package instructions and minimal-edit rules. Earlier tests demonstrated email delivery and PDF attachments. The revised complete workflow still requires verification through a successful unattended run and review of its generated documents. The separate standalone skill has not yet been confirmed synchronized with all automation updates.
