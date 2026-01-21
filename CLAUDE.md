# Unbound Fitness - Project Context

## Project Overview
**Goal:** Build a scalable virtual functional fitness coaching and programming business.
**Current Phase:** Side Hustle / Prototype / "Jim as Case Study"
**Primary Repository:** `workoutmania` (locally: `crossfit`)

## Team Structure
- **Chris (User):** Technical Lead, Operations, AI Integration
- **Jim:** Primary Athlete / Brand Ambassador ("Patient Zero" for programming)
- **Teaganne:** Head Coach (CF-L2) - provides programming oversight and ensures safety/standards

## Key Directories
- `01_Knowledge_Base/` - Foundational research (Methodology, Science, Programming)
- `02_Business/` - Admin, Planning, Legal
- `04_Clients/` - Client data. **Naming:** `[Name]/[Name]_[Cycle]_[Duration].md`
- `05_Programming/` - Workout templates and cycle design

## Branding & Legal (STRICT)

### Business Name
**Unbound Fitness** - NEVER use "CrossFit" in the business name.

### WOD Naming
Do NOT use trademarked names like "Fran", "Murph", or "Isabel".

Use functional names instead:
- "Thruster Sprint" not "Fran"
- "The Body Armor Challenge" not "Murph"
- "Snatch Speed Ladder" not "Isabel"

### Methodology Terms
Use these terms instead of "CrossFit":
- Functional Fitness
- HIFT (High-Intensity Functional Training)
- Metcon
- GPP (General Physical Preparedness)

See `02_Business/Legal/Intellectual_Property.md` for full guidelines.

## Programming Workflow
1. **Draft:** Create Markdown file in `04_Clients/[Client_Name]/`
2. **Review:** Coach or AI + Human review
3. **Format:** Use `npx md-to-pdf` with `branding.css` to generate PDFs
   - Style: Clean, sans-serif
   - Header: "**Unbound Fitness** • Peak Performance Programming"
4. **Deliver:** Send PDF to client

## Knowledge Management
- Store research/articles in `01_Knowledge_Base/`
- **Protocol:** "Fetch, Summarize, Structure"
- Do not dump raw text - always extract "Actionable Programming Principles"

### Knowledge File Template
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

## Current Focus
- Validating the model with Jim's training
- Jim's programming balances "Engine" (Endurance) with Strength
- Chris is exploring AI to scale programming

## Research Backlog
- Conjugate Method for HIFT (Westside Barbell application)
- Aerobic Capacity (Chris Hinshaw's pacing protocols)
- Energy Systems Training (ATP-CP vs Glycolytic vs Oxidative balance)
- Masters Athlete Considerations (Recovery curves for age 35+)
- Gymnastics Density (Building volume without joint overuse)
