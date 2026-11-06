# Analysis plan

## Primary unit
One model response to one prompt. A prompt is one observation; repeated runs, if later added, must be treated as repeated samples and reported separately.

## Descriptive reporting
For each language, report:
- prompts attempted / prompts planned;
- PASS / PARTIAL / FAIL / NOT_RATED counts and percentages;
- mean and median total score, plus each rubric dimension's distribution;
- critical failure count and the prompt IDs involved;
- missing responses and reviewer disagreement rate.

Always show denominators (for example, 3/16), not percentages alone.

## Matched comparisons
Compare the 16 matched scenario IDs across English, Hindi, and Odia. Show per-scenario outcome and dimension scores. Avoid causal claims about language: translation, script, wording, and cultural framing are confounded in this small manually authored set.

## Reviewer agreement
Report exact agreement on outcome labels and per-dimension agreement. If using a statistic such as weighted Cohen's kappa, state the method and sample size. Do not report a reliability statistic if reviewer coverage is too small.

## Qualitative analysis
Group observed issues into:
- unsafe compliance;
- over-refusal / refusal on benign prompts;
- weak or missing safe alternative;
- language misunderstanding or code-switching;
- cultural/contextual misread;
- unsupported certainty or hallucination;
- emergency escalation gap.

Include redacted examples and reviewer rationale. Separate observed evidence from interpretation.

## Limitations to state
- 50 prompts are a small exploratory sample, not a representative benchmark.
- Hindi and Odia have regional, dialectal, and register variation not captured here.
- The prompts are manually authored and not independently validated as semantically equivalent.
- One model snapshot/product surface may not generalize to other versions or settings.
- Model outputs are stochastic; single-run results do not estimate variability.
- Human ratings can be subjective; document reviewer expertise and adjudication.
