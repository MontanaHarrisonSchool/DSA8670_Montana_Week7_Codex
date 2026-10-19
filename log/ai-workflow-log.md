# AI Workflow Log

Entries below were reconstructed from this project conversation on 2026-10-18. The original local files did not retain exact per-message times, so the entries preserve chronological order and state that limitation instead of inventing timestamps. Prompt wording is archived in `prompts/session-history.md`.

## Entry 01 — 2026-10-18 — time not retained — Review requirements and propose workflow

**Prompt:** Review the assignment document, inspect the project, and propose a rubric-aligned wireframe before choosing architecture.

**Codex produced:** Extracted the requirements and proposed a workflow that includes a defined question, iterative prompt/code review, notebook analysis, outputs, workflow log, reflection, and final rubric check.

**Accepted:** The assignment should be done in Jupyter and reviewed before final submission.

**Modified:** The user clarified that a separate `/data` directory was unnecessary.

**Rejected:** None.

**Rationale:** Establish scope and grading requirements before analysis.

## Entry 02 — 2026-10-18 — time not retained — Create folders and explore data

**Prompt:** Create required folders and subfolders, inspect data shape/trends, and start a VS Code notebook in reasonably sized steps.

**Codex produced:** `analysis/notebooks/ames_housing_exploration.ipynb`, output folders, and an exploratory question about neighborhood sale prices and living area. Initial inspection found 2,930 rows, 82 columns, and 28 neighborhoods.

**Accepted:** The user proceeded with the Ames data and Jupyter approach.

**Modified:** The dataset was kept in the project root as `AmesHousing-1.csv`; no `/data` folder was created. The first question remained provisional until the user directed Codex to choose one.

**Rejected:** None.

**Rationale:** Begin with data profiling and exploratory trends before fitting the final analysis.

## Entry 03 — 2026-10-18 — time not retained — Install notebook dependencies

**Prompt:** Add a package-install block, install missing packages, then comment the install lines.

**Codex produced:** An initial `.venv` based on Codex’s bundled Python and a commented package-install command.

**Accepted:** The request to centralize dependencies in a project environment.

**Modified:** This setup was later replaced after the environment was unavailable in VS Code. The initial interpreter choice was unsuitable for the user’s workflow.

**Rejected:** The initial environment setup as a working VS Code kernel; the user reported that it was not selectable.

**Rationale:** The kernel needs to use the user’s installed Python, not an internal bundled runtime.

## Entry 04 — 2026-10-18 — time not retained — Diagnose package/kernel mismatch

**Prompt:** Ask whether the installation worked and whether VS Code needed to be reopened.

**Codex produced:** Suggested selecting the project `.venv` interpreter and explained that a VS Code restart is usually unnecessary.

**Accepted:** The general distinction between installed packages and the notebook’s selected kernel.

**Modified:** The troubleshooting approach changed after the user said the `.venv` was unavailable. The UI could not be inspected through the available app inventory.

**Rejected:** The initial suggestion as a sufficient fix; it did not resolve kernel discovery.

**Rationale:** A concrete interpreter rebuild and kernel registration were needed.

## Entry 05 — 2026-10-18 — time not retained — Inspect unavailable kernel

**Prompt:** Try again to view the open VS Code kernel picker before the user fixes it manually.

**Codex produced:** Attempted computer-use inspection; no VS Code app/window was exposed. Filesystem checks showed the local `.venv` had been created from the Codex runtime and was ignored by Git.

**Accepted:** The user then specified the exact Python installation and requested a clean rebuild.

**Modified:** Diagnosis shifted from “select the existing environment” to “recreate the environment using the explicitly specified Python.”

**Rejected:** None.

**Rationale:** The existing environment’s base interpreter was the likely source of kernel discovery trouble.

## Entry 06 — 2026-10-18 — time not retained — Rebuild from installed Python 3.12

**Prompt:** Remove `.venv`, recreate it using `C:\Users\Montana\AppData\Local\Programs\Python\Python312\python.exe`, install pandas/matplotlib/ipykernel, register `Ames Week 7`, verify, and avoid project edits or commits.

**Codex produced:** A fresh Python 3.12.4 environment, installed packages, and a user Jupyter kernelspec named `Ames Week 7`. Imports and kernel registration were verified.

**Accepted:** The user later confirmed the notebook was functioning properly after the remaining dependency issue was addressed.

**Modified:** None to project files during this rebuild; `.venv` remained Git-ignored. No commit was made.

**Rejected:** Use of the Codex bundled Python.

**Rationale:** Bind the environment to the Python installation selected by the user and expose it as a notebook kernel.

## Entry 07 — 2026-10-18 — time not retained — Fix pandas Styler AttributeError

**Prompt:** Investigate the traceback stating that `DataFrame.style` requires Jinja2.

**Codex produced:** Identified missing optional dependency Jinja2, installed Jinja2 3.1.6 into the project `.venv`, added it to the commented recovery install command, and verified a styled DataFrame renders.

**Accepted:** The user confirmed the notebook was now functioning properly.

**Modified:** The dependency block was extended to include `jinja2`.

**Rejected:** None.

**Rationale:** Pandas uses Jinja2 to render styled DataFrames; this was a dependency issue rather than an error in the aggregation.

## Entry 08 — 2026-10-18 — time not retained — Identify the next workflow step

**Prompt:** Ask what comes next on the wireframe.

**Codex produced:** Recommended settling the final analytical question and then conducting the analysis while recording prompts and decisions.

**Accepted:** The user directed Codex to choose the question and proceed without requesting confirmation.

**Modified:** None.

**Rejected:** None.

**Rationale:** A specific question should drive the analysis and final deliverables.

## Entry 09 — 2026-10-18 — time not retained — Choose and run the analysis

**Prompt:** Select the best question and run the analysis without pausing for confirmation.

**Codex produced:** An OLS neighborhood fixed-effects model with a shared living-area slope; a 28-neighborhood table; a paired comparison chart; plain-language findings; and saved CSV/PNG artifacts. All nine notebook code cells executed successfully.

**Accepted:** The user proceeded to README preparation without requesting analytical changes; findings are available for review.

**Modified:** The exploratory notebook was extended with model details, fit metrics, common-size comparisons, and limitations. The chart excludes neighborhoods with fewer than 20 sales; the complete table retains them.

**Rejected:** None.

**Rationale:** The method addresses the assignment’s neighborhood/square-footage example and stays interpretable. The estimates are descriptive and GrnHill’s estimate (two sales) is flagged as unstable.

## Entry 10 — 2026-10-18 — time not retained — Prepare README and audit rubric

**Prompt:** Write the README and pay special attention to accuracy and assignment completeness.

**Codex produced:** `README.md` with the question, session date, one-paragraph findings summary, notebook instructions, and artifact links; a rubric audit found that prompt progression and the reflection still needed work.

**Accepted:** The user said the README looked good.

**Modified:** None requested.

**Rejected:** None.

**Rationale:** The README meets the explicit content requirements while the audit keeps remaining rubric gaps visible.

## Entry 11 — 2026-10-18 — current prompt — Capture prompts and prepare reflection scaffold

**Prompt:** Finish remaining tasks; prepare reflection notes on shortcomings, especially the Python bundle confusion and how it was fixed, leaving the personal reflection for the user.

**Codex produced:** A chronological prompt history, expanded per-prompt workflow entries, and a fact-based reflection scaffold for the user to personalize.

**Accepted:** The user reserved personal reactions and final reflection wording for themselves.

**Modified:** None.

**Rejected:** None.

**Rationale:** Preserve the real workflow evidence and leave subjective claims in the user’s voice.

