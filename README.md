# Grant Management System Deliverables

This repository contains the initial prototypes and high-level architecture for the New Grant Management System (as of October 1, 2025).

## Overview

We are developing a modular agentic ecosystem to streamline grant discovery, application drafting, reviewer tailoring, and submission tracking. The core components include:

- **Grant Opportunity Finder Agent**: Scans federal, state, and private grant sources, normalizes metadata, and ranks opportunities by relevance.
- **Grant Writer Agent**: Generates first-draft proposals based on templates and organizational profiles, with customizable sections such as executive summary, project description, budget, and impact statements.
- **Reviewer Insight Agent**: Profiles funders and reviewers to highlight key priorities and tailor proposals accordingly.
- **Submission Tracker Agent**: Monitors application status, deadlines, and generates reminders for internal reviews and final submissions.
- **Grant Management Dashboard**: A web-based interface (Next.js) that displays opportunities, drafts, reviewer insights, and submission timelines in a single unified view.

## Current Structure (Prototype)

We plan to organize the project into a clear frontend and backend:

- **frontend/** – a Next.js dashboard that fetches data from the backend and displays it. For example, `pages/index.js` shows a list of mock opportunities and submission statuses using simple API calls.
- **backend/** – Python-based agents and a Flask API. Key files include:
    - `api.py` – exposes endpoints like `/api/opportunities` and `/api/submissions`.
    - `agents/opportunity_finder.py` – defines `OpportunityFinderAgent` with mock data.
    - `agents/submission_tracker.py` – defines `SubmissionTrackerAgent` with mock submission data.
    - `requirements.txt` – lists dependencies (`flask`, `requests`, `pandas` etc.).

At this stage, these files contain prototypes and mock data for demonstration and testing. They will evolve into fully functional agents integrated with real data sources and persistent storage.

## Next Steps

- Flesh out the grant writer and reviewer insight agents with actual logic and data.
- Build the frontend dashboard components to display drafts, reviewer insights, and submission status.
- Integrate with real grant data sources (grants.gov, foundation directories) for the opportunity finder.
- Improve error handling, configuration, and deployment scripts.

---

This is the first commit to populate the repository with our development plan and prototype structure.
