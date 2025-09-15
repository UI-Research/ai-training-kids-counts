# Copilot Agent Instructions — NEW EXAMPLE ISSUE

Goal
- Add a short, novel toy example (R + Python) that demonstrates an AI-assisted data workflow for Kids Count users. Keep it runnable without any API keys and completable in ~20 minutes.

High-level constraints
- Preserve voice and structure used in existing notebooks.
- Do not modify ai-exercise-session-plan.qmd (keep buggy example there). Put fixes and new example solutions into ai-exercise-session-plan-solutions.qmd and clearly label as "NEW EXAMPLE (reference) — SOLUTION".
- Keep changes minimal, well-documented, and reversible.

Primary deliverables
1. Toy CSV in toy-data/ (e.g., toy-data/child-poverty-county.csv) — public data, no API key required.
2. R notebook content: ai-exercise-new-example.qmd (or a new section appended to the main .qmd) — tidyverse-based, loads CSV, computes a simple county-level indicator, shows top-10 table, and saves one slide-ready plot PNG.
3. Python notebook: ai-exercise-new-example.ipynb (or Quarto .qmd with python) — same steps using pandas/geopandas/matplotlib so outputs match the R version.
4. A "human+AI workflow" block in both notebooks with step-by-step actions and two sets of prompts per step: (a) barebones copy-paste prompts and (b) slightly expanded prompts.
5. Risks & Uncertainty block in both notebooks listing data currency, MOE/sampling noise, and AI limitations with exact phrasing users should request from the AI (e.g., "report which columns you used and any assumptions").
6. Solutions: full working code and final prompts go into ai-exercise-session-plan-solutions.qmd under a labeled "NEW EXAMPLE (reference) — SOLUTION" section.

Step-by-step agent task list
1. Review ai-exercise-session-plan.qmd and ai-exercise-session-plan-solutions.qmd to ensure novelty vs existing examples.
2. Pick a small public dataset appropriate for state-level Kids Count work (county child poverty or similar). Add CSV to toy-data/.
3. Implement R and Python notebooks with functionally equivalent flows (load → compute → preview table → map/save PNG).
4. Add an explicit human+AI workflow (Setup, Ask AI to scaffold load/clean, Ask AI to compute indicator, Ask AI to plot, Iterate to refine). For each step supply:
   - Barebones prompt (one line, copy-paste ready).
   - Slightly expanded prompt (1–2 sentences).
5. Add short Risks & Uncertainty guidance and recommended verification checks (column names used, denominators, small-sample caveats).
6. Add acceptance metadata at top of the new example: estimated time (20 min), packages needed, and a one-line run command.
7. Add tests/quick-run notes: how to run R chunks in RStudio or run extracted script via knitr::purl(); how to run the Python notebook; confirm both run without internet/API keys.

Barebones example prompts (copy-paste)
- R: "Load toy-data/child-poverty-county.csv, compute county child poverty rate, show top 10 rows and save a PNG map as toy-data/child_poverty_county.png."
- Python: "Load toy-data/child-poverty-county.csv, compute county child poverty rate, show top 10 rows and save a PNG map as toy-data/child_poverty_county.png."
- Follow-ups: "Improve legend and caption for slides." and "List the columns you used and any assumptions."

Acceptance criteria (what to check)
- Both R and Python flows run locally with the included CSV and produce a PNG.
- Human+AI workflow section and copy-paste prompts are present in both notebooks.
- Risks & Uncertainty block included.
- Solutions notebook contains full working code, labeled "NEW EXAMPLE (reference) — SOLUTION".
- Exercise completes in ~20 minutes.

Notes for the human reviewer
- If you see potential overlap with existing examples, stop and summarize differences before implementing.
- Keep all new solution text clearly labeled and separate from the main exercise notebook.
- If data provenance or privacy concerns appear, flag them immediately.

Commit messages
- Use concise messages such as:
  - feat(example): add new R+Python toy example (child poverty)
  - docs: add human+AI workflow and prompts
  - fix: add toy CSV and ensure notebooks run offline
