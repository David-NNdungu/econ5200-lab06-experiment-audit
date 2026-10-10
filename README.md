# Experiment Design Audit — Power, Selection & Weighting

## Objective
I checked how experiment design and non-random selection affect the results, then used power calculations and weighting to assess the problems.

## Methodology
- I audited an A/B test with 1,000 treatment users and 49,000 control users.
- I calculated the sample size needed to detect a 0.8 percentage-point lift with 80% power.
- I checked the power_check function against statsmodels and compared the original allocation with an even split.
- I compared healthcare costs for participants and non-participants in a simulated wellness program.
- I estimated participation probabilities from baseline health and applied inverse probability weights.
- I completed the optional polling example and checked Meng's identity and effective sample size.

## Key Findings
- The original A/B test had only 19.8% power. Its p-value was 0.2512, so the observed lift was not statistically significant at 5%.
- The calculation gave about 12,514 users per group for 80% power. I would round up to 12,515 for planning.
- Splitting the same 50,000 users evenly gave about 97.7% power.
- The naive wellness-program estimate was -$1,396, compared with the true effect of -$500. My IPW estimate was -$522.
- The biased poll had 389,090 responses but an effective sample size of about 140. It underestimated Candidate A's share by 4.22 percentage points.
- My CCES calculation gave an effective sample size of about 402, consistent with the chapter's figure of about 400.

## Files
- lab_ch06_diagnostic.ipynb: my calculations, answers, checks, and charts.
