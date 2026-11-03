# COMP5320 Tutorial #2: Requirements Engineering with AI agents (SoopiFood)

Individual submission. All outputs are in [`tutorial/workspace/`](tutorial/workspace/).

## How it was done

- Each part ran the course prompt (`starter/prompts/01`–`12`) with an AI coding agent that reads and writes files, in order A → I; Parts A–E each build on the previous output.
- Every part followed the loop **Round 1 (agent) → Review → Round 2 with more context → Review**, asking each time *what did the agent not know?*
- Part F round 1 used only the backlog; round 2 added the stakeholder notes. Part H round 1 had only the user story; round 2 (same session) added the business rules R1–R3.
- Review findings are kept in each output file (A–E) and summarised in the table at the end of this page.

> Parts B and C need interview, observation and walkthrough notes. No real restaurant managers were available, so those notes were **simulated with an AI agent** playing the managers, as the tutorial allows. They are marked as simulated in the files.

| Part | Activity | Output in `tutorial/workspace/` |
|---|---|---|
| A | Interview guide, round 1 → neutral rewrite | `01_interview_guide.md`, `02_interview_guide_iterate.md` |
| B | Interview notes (I1–I8, O1–O2) → personas | `03a_interview_notes.md`, `03_personas.md` |
| C | User stories + walkthroughs (W1–W4) → FRs | `04a_user_stories_walkthroughs.md`, `04_functional_requirements.md` |
| D | Non-functional requirements | `05_non_functional_requirements.md` |
| E | Epics, features, stories | `06_epics_stories.md` |
| F | MoSCoW round 1 → round 2 with stakeholder notes | `moscow_round1.md`, `moscow.md` |
| G | Change requests | `scope_changes.md` |
| H | Gherkin writer → review → rewrite with business rules | `discount.feature`, `review.md`, `discount_v2.feature` |
| I | Definition of Done audit | `dod_audit.md` |

## What the agent did not know (review findings)

| Part | Finding |
|---|---|
| A | Round 1 used leading words ("juggle", "most frustrating") and assumed something must change; rewritten neutrally. |
| B | Every bullet is traced to a note; persona 3 rests on only two sources (I4, I6), so it is weaker evidence. |
| C | The agent did not know timeouts, durations or "late" thresholds: 7 values are `[TBC]` with stakeholder questions. UI requests (colours, font size) are left to the NFRs. |
| D | Without stakeholder numbers, almost every threshold (including the TLS version) is `[TBC]` with a question. |
| E | NFR-05, 06, 08, 11, 12 are cross-cutting and have no story; they belong in the DoD or enabler items. |
| F | Without the notes, promo codes were Should and reviews Could; the founder's and marketing's notes moved them up. Cash on delivery was an assumption, then confirmed. |
| G | The legal CR is non-negotiable (Must), paid for by demoting SF-09; the marketing CR is Won't. Must rises to 68%. |
| H | Without the rules, round 1 invented the minimum (50,000), discounted the delivery fee, ignored the cap and rejected codes on their last valid day. |
| I | The PR claims Done, but the CI log shows a failed scenario, a skipped type checker, no reviewer, float arithmetic and no staging deploy. |
