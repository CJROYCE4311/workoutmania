# GEMINI Project Context: Unbound Fitness

## Project Overview
**Goal:** Build a scalable virtual functional fitness coaching and programming business.
**Current Phase:** Side Hustle / Prototype / "Jim as Case Study".
**Primary Repository:** `workoutmania` (locally: `crossfit`)

## Team Structure
- **Chris (User):** Technical Lead, Operations, AI Integration.
    - *Role:* Automates workflows, builds the website/platform, explores AI programming models.
- **Jim:** Primary Athlete / Brand Ambassador.
    - *Role:* "Patient Zero" for programming. His results validate the methodology.
- **Teaganne:** Head Coach (CF-L2).
    - *Role:* Provides programming oversight, credibility, and ensures safety/standards.

## Key Directories
- `01_Knowledge_Base`: Foundational research (Methodology, Science, Programming).
- `02_Business`: Admin, Planning, Legal.
- `04_Clients`: Client data. **Naming Convention:** `[Name]/[Name]_[Cycle]_[Duration].md`
- `05_Programming`: Workout templates and cycle design.

## Operational Procedures

### 1. Programming Workflow
1.  **Drafting:** Create a Markdown file in `04_Clients/[Client_Name]/`.
2.  **Review:** Coach (Teaganne) or AI + Human review.
3.  **Formatting:** Use `npx md-to-pdf` with `branding.css` to generate client-ready PDFs.
    - *Style:* Clean, sans-serif.
    - *Header:* "**Unbound Fitness** • Peak Performance Programming".
4.  **Delivery:** Send PDF to client.

### 2. Knowledge Management
- Store research/articles in `01_Knowledge_Base`.
- **Protocol:** "Fetch, Summarize, Structure."
    - Do not dump raw text.
    - Always extract "Actionable Programming Principles."

### 3. Branding & Legal (Strict IP Protocol)
- **Business Name:** **Unbound Fitness** (NEVER use "CrossFit" in the business name).
- **WOD Naming:** Do **NOT** use trademarked names like "Fran", "Murph", or "Isabel".
    - *Use Functional Names:* "Thruster Sprint", "The Body Armor Challenge", "Snatch Speed Ladder".
- **Methodology Terms:** Use "Functional Fitness", "HIFT", "Metcon", or "GPP" instead of the "C-word" where possible.
- **Reference:** See `02_Business/Legal/Intellectual_Property.md` for full guidelines.

### 4. Knowledge Acquisition Protocol
*Use this protocol to populate `01_Knowledge_Base`.*

**User Trigger:** "Research [Topic]" or "Deep dive on [Topic]".
**Agent Actions:**
1.  **Search:** Use `google_web_search` or `web_fetch` to find reputable sources (journals, reputable blogs, methodology papers).
2.  **Synthesis:** Create a new file in `01_Knowledge_Base/[Category]/[Topic].md`.
3.  **Structure:** The file MUST follow this template:
    ```markdown
    # [Topic Title]
    **Source:** [URL/Author]
    **Tags:** [Periodization, Strength, Engine, etc.]

    ## Executive Summary
    [2-3 sentences explaining the core concept]

    ## Key Methodology
    - [Point 1]
    - [Point 2]

    ## Application to Our Programming
    - **How we use this for Jim:** [Specific use case]
    - **Integration:** [Where this fits in a weekly template]
    ```

## Current Context
- **Date:** 2026-01-20
- **Focus:** Validating the model with Jim's training.
- **Recent Activity:** Updated Legal Protocols, V2 Programming, and Rebranding to "Unbound Fitness".

## Long-Term Memory (Facts)
- Jim's programming needs to balance "Engine" (Endurance) with Strength.
- Teaganne has CF-L2 credentials.
- Chris is exploring AI to scale programming.

## Target Knowledge Domains (Backlog)
- **Conjugate Method for HIFT:** (Westside Barbell application).
- **Aerobic Capacity:** (Chris Hinshaw’s pacing protocols).
- **Energy Systems Training:** (ATP-CP vs Glycolytic vs Oxidative balance).
- **Masters Athlete Considerations:** (Recovery curves for age 35+).
- **Gymnastics Density:** (Building volume without joint overuse).