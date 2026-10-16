# Weekly Job Search: Autonomous AI Job Matching Agent

## Overview
Weekly Job Search is a reusable, prompt-engineered AI workflow designed to match university students with fresh, verified job and internship opportunities based on their individual background and constraints. 

Rather than relying on generic keyword searches or black-box algorithms, this agent executes a transparent two-stage decision process:
1. **Hard Requirements Filter:** Strictly eliminates vacancies that violate hard constraints (e.g., maximum weekly hours, location boundaries, language prerequisites, or excluded duties like cold sales).
2. **Decision Rubric (40/30/20/10):** Evaluates qualified roles across career goals (40%), verified skills/experience (30%), practical feasibility (20%), and industry preferences (10%).

## Project Architecture & Core Files
- `PROJECT_EXPLANATION.md`: Comprehensive system architecture, technical design, rubric definitions, and evaluation framework.
- `installed-skill/SKILL.md`: The central execution ruleset controlling agent behavior, verification bounds, and output formatting.
- `installed-skill/references/onboarding.md`: The conversational intake questionnaire and standardized profile schema used to onboard new students.
- `installed-skill/references/workflow.md`: Retrieval procedures for public ATS endpoints (SmartRecruiters, Greenhouse, Teamtailor), freshness verification, and deduplication logic.
- `AUTOMATION_SETTINGS.md`: Scheduled recurring execution parameters (Friday weekly delivery).
- `AUTOMATION_PROMPT.md`: Reference configuration for scheduled task execution and document generation.

## How to Run & Validate
1. **Interactive Setup:** An incoming student provides their CV text or answers the structured intake checklist defined in `onboarding.md`.
2. **Execution:** Load `SKILL.md`, `onboarding.md`, and `workflow.md` into an LLM execution environment (e.g., ChatGPT / Custom Agent).
3. **Delivery:** The workflow retrieves active vacancies, executes the hard-constraint filter, calculates rubric match scores, and generates a structured digest with concrete match rationales and document checklists.

## Academic & Course Context
Developed as part of the Economics/Political Economy of AI course. This project demonstrates AI-enabled capability creation—orchestrating unstructured web retrieval, deterministic constraint filtering, and transparent qualitative comparison without requiring a traditional backend infrastructure.
