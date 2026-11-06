# Multilingual AI Safety Evaluation: Claude in English, Hindi, and Odia

**Status:** Evaluation protocol and prompt set prepared; no model responses have been collected yet.

This repository contains a small, exploratory, human-reviewed evaluation of Claude's response behaviour across English, Hindi, and Odia. It is designed to surface potential differences in safety handling, helpfulness, language fidelity, cultural/contextual nuance, and calibration.

> Important: This is not a benchmark, audit, or claim about Claude's overall safety. The prompt set is small and manually authored. Results must be reported with limitations and must not be described as representative of all users or all Odia/Hindi dialects.

## Dataset

- 50 prompts total: 17 English, 17 Hindi, 16 Odia.
- 16 matched scenarios across all three languages (scenario IDs 01–16).
- One additional English emotional-support prompt (E17).
- Prompts cover high-, medium-, and low-risk cases, including harmful requests, urgent safety situations, benign defensive/educational requests, ambiguous dual-use, misinformation, and language accommodation.

See [`data/prompts.csv`](data/prompts.csv).

## Research questions

1. Does Claude maintain appropriate safety boundaries across the three languages?
2. Are helpfulness and language fidelity consistent across languages?
3. Do refusal quality, escalation, or calibration differ on matched scenarios?
4. What failure modes or reviewer disagreements warrant follow-up testing?

## Suggested method

1. Record the exact Claude model/version, date/time, product surface, and settings.
2. Start a fresh conversation for each prompt; submit the prompt exactly as written.
3. Collect the full response verbatim in `results/responses.csv`.
4. Have at least two fluent reviewers independently score Hindi and Odia responses where possible; ideally double-score all responses.
5. Use the rubric in [`docs/scoring-rubric.md`](docs/scoring-rubric.md).
6. Adjudicate disagreements and preserve reviewer notes.
7. Analyse matched scenario IDs; report counts and denominators, not just percentages.

## Quick start

1. Open `data/prompts.csv`.
2. Run each prompt against Claude in a clean session.
3. Copy the exact response and metadata into `results/responses.csv`.
4. Score each response using `results/scored_results.csv` and the rubric.
5. Summarize aggregate and scenario-level results in `results/summary-template.md`.

## Files

- `data/prompts.csv` — 50 prompts and expected-behaviour notes.
- `docs/scoring-rubric.md` — scoring definitions, outcome labels, critical failures, reviewer protocol.
- `results/responses.csv` — blank response capture sheet.
- `results/scored_results.csv` — blank scoring sheet.
- `results/summary-template.md` — write-up template.
- `docs/analysis-plan.md` — analysis plan and reporting cautions.

## Ethics and safety

- Do not use real people's private data.
- Do not add operational details to harmful prompts.
- Do not publish harmful model output verbatim; summarize and redact.
- For imminent self-harm or medical emergencies, evaluate whether the model appropriately directs the user to immediate human/emergency support.
- This is research on model behaviour, not a substitute for professional safety, medical, or legal review.

## Citation / reproducibility

When publishing, include the repository commit hash, prompt-set version, date range, exact model identifier if available, interface/API, generation settings, reviewer language qualifications (with consent), and any prompt edits. Keep raw outputs private if they contain sensitive or harmful content; publish redacted excerpts only.

## Current result status

**No results yet.** Do not report pass rates, failure counts, or comparative conclusions until the prompts have actually been run and independently scored.
