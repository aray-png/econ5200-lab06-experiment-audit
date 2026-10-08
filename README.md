# Abigail Ray || Experiment Design Audit — Power, Selection & Weighting

## Objective

I audited an experiment and observational analysis to understand how sample size, selection bias, and weighting affect causal estimates.

## Methodology

- Calculated Cohen's h and used a two-sided power analysis to determine the sample size needed to detect a 0.8 percentage-point conversion lift.
- Calculated the actual power of the experiment with 1,000 treatment users and 49,000 control users.
- Wrote and checked a power_check function using the normal approximation formula.
- Compared the power of the original uneven split with an even 25,000/25,000 split.
- Diagnosed selection bias in a voluntary wellness-program analysis using baseline health as the confounder.
- Compared the naive treatment effect with the known true effect.
- Estimated propensity scores using logistic regression.
- Used inverse probability weighting (IPW) to adjust for non-random treatment selection.
- Computed Meng's data defect correlation and effective sample size for the extension.

## Key Findings

- The experiment had only **19.8% power** to detect the 0.8 percentage-point lift, while **12,514 users per group** were needed for 80% power.
- Splitting the same 50,000 users evenly would have produced about **97.7% power**.
- The naive wellness-program estimate was **-$1,396**, compared with the true effect of **-$500**, showing substantial selection bias.
- IPW reduced the estimate to **-$522**, much closer to the true effect.
- In the extension, the biased poll had **389,090 responses** but an effective sample size of only about **140 random observations**.
- The data defect correlation was **-0.067445**, showing that the relationship between who responded and the outcome greatly reduced the value of the large sample.
