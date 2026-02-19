# Parallel Computing with R (futureverse) — Final Exam

This repository contains a **single-file** submission for the *Parallel Computing with R* final exam,
focused on the **futureverse** approach to parallelization.

## File
- `futureverse-exam.qmd` — exam statement + answers + R code.

## What it covers (high level)
- Core concepts of **futures** and how they enable parallel execution by switching `future::plan()`.
- Differences between **{future.apply}** and **{furrr}** (apply-family vs tidyverse mapping).
- Progress reporting in parallel workflows (via **{progressr}**).
- Implementation of two statistics on a data matrix:
  - **T1** using the Moore–Penrose pseudoinverse via eigen decomposition
  - **T2** using a shrinkage covariance estimator
- Performance benchmarking with **{microbenchmark}**.
- Parallel simulation over **B = 1000** replications using **{furrr}**:
  - `plan(multisession, workers = 4)`
  - `future_map()` to compute T1/T2 across replications
  - histogram visualization of the resulting distributions

## How to view / run
### Option A — Read on GitHub
GitHub will display the `.qmd` as text (including code blocks).

### Option B — Render to HTML (recommended)
If you have **Quarto** installed:
```bash
quarto render futureverse-exam.qmd
