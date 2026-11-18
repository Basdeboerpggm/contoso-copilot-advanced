# Model scorecard — rule R1 (pensionableSalary)

> One run is a sample, not a benchmark. Synthetic data only — never paste secrets or real member data.

| | Model A | Model B |
|---|---|---|
| Model (name as shown in the picker) |gpt-6.1-sol | claude haiku 4.5|
| Harness · Mode · Permissions | Copilot · Interactive · Manual | Copilot · Interactive · Manual |
| Reasoning effort | medium | medium|
| Date | 18-11-26| 18-11-26|

## Scores

| Criterion | How to score | Model A | Model B |
|---|---|---|---|
| Correctness verified | Expected values that match the `node -e` output (x / 5) | 0/5 | 0/5 |
| Edge cases found | Which did it cover? franchise boundary · salary cap · part-time · below franchise → 0 · invalid factor (0 or > 1) · negative salary |yes | yes|
| Hallucinations | Invented functions, parameters, files or rules? List them (none = 👍) | none|none |
| Latency feel | fast / ok / slow |ok | ok|
| Cost / credits | Relative cost of the model (supported-models doc) — heavier model = more AI credits |5 |6 |

## Verification output

```text
(paste the node -e output for model A and model B here)
```

Model A: 17545 1 0
137801 0.5 60127.5
17545.25 0.5 0.13
0 1 0
file:///C:/Users/BADE/Documents/Github_copilot_lab/contoso-copilot-advanced/api/src/domain/pension.ts:22
    throw new RangeError('partTimeFactor must be greater than 0 and at most 1');
          ^

RangeError: partTimeFactor must be greater than 0 and at most 1
    at Module.pensionableSalary 

model B: 
0 1 0
17545 0.5 0
137800 1 120255
200000 0.75 90191.25
100 0.001 0

## Verdict

- For **this kind of task** I would use: …
- Because: …
- Would I trust it **without** the `node -e` check? yes / no — why?
- To make this a real benchmark I would need: …
