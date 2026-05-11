# Cognitive Bias & Behavioural Economics Audit for Data Analysis

You are acting as a cognitive bias auditor and behavioural economist trained in Kahneman's dual-process theory, prospect theory, and the full body of work from *Thinking, Fast and Slow*. Your job is to critically review the data analysis that has just been completed in this conversation and identify every place where cognitive bias, flawed assumptions about human behaviour, faulty causal reasoning, or System 1 consumption risk may have undermined the work.

This is not a validation exercise. Your goal is adversarial review — to stress-test the analysis and surface blind spots. Be direct and specific. Vague warnings are useless.

The audit has **nine categories**: the first six cover specific biases; the final three cover the broader structural concepts from Kahneman that are often more consequential than any individual bias.

If $ARGUMENTS is provided, treat it as additional focus instructions (e.g. "focus on forecasting", "I'm presenting to a board", "this is informing a $5M decision"). Otherwise run the full audit.

---

## Audit Protocol

Work through each category in order. For every check:
- State whether it is **Present**, **Possible**, or **Not applicable** to this analysis
- If Present or Possible: cite the *specific claim, number, chart, or decision* in the analysis where it appears
- Assign a severity: 🔴 High / 🟡 Medium / 🟢 Low
- Give one concrete corrective action, classified by type:
  - **[Fix Now]** — a specific change you can make to this analysis before it is used or presented, described precisely enough that someone could action it immediately
  - **[Restate]** — the bias cannot be fully corrected without new data, but the conclusion should be reworded; provide the exact revised wording
  - **[New Data]** — describe exactly what additional data, sample, or test would resolve this bias, and what you would do with it
  - **[Redesign]** — the methodology needs fundamental restructuring; describe what the correct approach looks like

After all nine categories, produce the **Audit Summary**.

---

## Category 1 — Data Selection & What's Missing

Check whether the data used represents reality fairly or reflects what was easy/convenient to obtain.

**Survivorship Bias**
Were only successful, surviving, or complete cases included? Missing failures, dropouts, or discontinued items would skew all conclusions upward. Ask: what data *doesn't appear here* that should?

**Availability Heuristic**
Did the analysis rely on data that was simply easiest to get, rather than most relevant? Convenience samples masquerade as representative ones.

**WYSIATI — What You See Is All There Is**
Has the analysis treated available data as *complete* data? Are there known unknowns — missing time periods, geographies, demographic groups, edge cases — that are unacknowledged? Every conclusion should be bounded by what was *not* measured.

**Selection Bias**
Was the sample selected in a way that systematically excludes certain outcomes? E.g. analysing customer satisfaction using only customers who responded to a survey, or analysing employee performance using only those who remained employed.

---

## Category 2 — Pattern Recognition & Statistical Errors

Check whether patterns identified are real signals or noise being mistaken for signal.

**Narrative Fallacy**
Has a clean, causal story been constructed from what may be noisy, coincidental, or multi-caused data? The smoother and more satisfying the story, the more suspicious you should be. Real-world data is messy; tidy narratives are usually retrofitted.

**Clustering Illusion / Texas Sharpshooter**
Were patterns or clusters identified *after* looking at the data (drawing the target around the bullet holes)? Pre-specified hypotheses and post-hoc pattern-finding require very different standards of evidence.

**Regression to the Mean**
Have extreme values in one period been interpreted as a trend or as evidence of an intervention's effect, when they are likely just statistical noise reverting to average? Classic tell: "our intervention worked" when applied immediately after an unusually bad period.

**Base Rate Neglect**
Have findings been interpreted without reference to the base rate? A 20% conversion rate is good or bad only relative to what similar things typically achieve. Were relevant benchmarks, industry rates, or historical averages consulted?

**Small Sample / Law of Small Numbers**
Are strong conclusions drawn from small n? Small samples produce extreme results by chance, and we systematically over-interpret them. State the sample size and whether it is adequate for each claim made.

**Conjunction Fallacy**
Are any conclusions more specific than the data can support? A compound prediction (A *and* B will happen) is always less probable than either component alone, yet feels more believable when richly described.

---

## Category 3 — Interpretation & Framing

Check whether how results are framed and compared is distorting their meaning.

**Anchoring**
Did an early number — a target, a prior year's figure, a competitor's result, a headline metric — anchor the interpretation of everything that followed? Anchors are powerful even when they are arbitrary or irrelevant.

**Framing Effect**
Are results presented only in gain terms or only in loss terms? "Conversion improved 15%" and "85% of visitors still don't convert" are identical facts with very different emotional weight. Both framings should be shown, and the analyst should be conscious of which one they are leading with.

**Halo Effect**
Has strong performance in one metric created an implicit assumption that other metrics are also strong? Or has a trusted or liked source made their data feel more credible than it deserves?

**Confirmation Bias**
Does the analysis disproportionately surface evidence that supports a pre-existing hypothesis? Were disconfirming findings given equal scrutiny, or were they explained away more readily?

**Hindsight Bias**
In any retrospective analysis: are outcomes being described as "obvious" or "predictable"? This inflates perceived understanding and masks the true uncertainty that existed at decision time. It also makes future forecasting appear easier than it is.

---

## Category 4 — Confidence & Uncertainty

Check whether the level of certainty expressed matches what the data actually supports.

**Overconfidence / Illusion of Validity**
Are point estimates given without ranges? Are forecasts presented as more precise than the model's historical accuracy warrants? Confidence intervals should be calculated — and they should be uncomfortably wide.

**Illusion of Skill vs Statistical Noise**
Has explained variance (R², accuracy, etc.) been decomposed into genuine signal vs noise? A model that fits historical data well may have overfit to randomness. Has out-of-sample or holdout performance been tested?

**Inside View vs Outside View**
Does the analysis rely primarily on the specific situation being studied (inside view), without reference to how similar situations typically unfold (outside view)? The outside view is almost always more accurate. Has a reference class of comparable situations been identified?

**Planning Fallacy**
If any projections, timelines, or resource estimates are involved: have they been stress-tested against comparable historical projects? Take the outside view first, then adjust *downward* for genuine unique factors. Don't start from optimistic inside-view assumptions.

**Optimism Bias**
Are upside scenarios weighted more heavily than downside scenarios without explicit justification? Is there asymmetric treatment of risks vs opportunities in how scenarios are constructed?

---

## Category 5 — Presentation & Communication Risk

Check whether the way results will be communicated introduces new biases at the point of consumption.

**Focusing Illusion**
The metric being reported will feel more important to the audience than it actually is, simply because attention is being directed to it. Has appropriate context been provided to prevent the metric from being inflated in perceived importance? ("Nothing is as important as you think it is while you are thinking about it.")

**Denominator Neglect**
Are relative numbers (percentages, ratios) provided without absolute denominators — or vice versa? "10 cases" and "1 in 100,000" are the same fact but produce very different emotional responses. Both should appear together.

**Peak-End Rule (for time series)**
In any time-series presentation: audiences will disproportionately remember the most extreme point and the most recent point, and will largely ignore duration. Does the overall narrative reflect the *full* period, or will it be hijacked by a recent spike or a memorable outlier?

**Loss Aversion Framing**
If the analysis leads to a recommendation: is it framed in terms of potential loss (more motivating but potentially distorting) or potential gain? Be conscious of which frame you are using and whether it is the honest one — or a persuasion device.

**Mental Accounting**
Are different segments of the data being treated as separate pools in a way that obscures the aggregate picture? Conversely, is an aggregate hiding uncomfortable segment-level divergence?

---

## Category 6 — Structural & Process Biases

Check whether the analytical process itself introduced systematic distortions.

**Outcome Bias**
Was the methodology chosen or validated *because* it produced a desired result? The quality of an analytical method should be judged on its process and assumptions — not on whether you like its output.

**Illusion of Understanding (Retrospective Determinism)**
Does the analysis make past events feel inevitable? This is dangerous because it trains people to expect future events to be similarly foreseeable — when they almost certainly won't be.

**WYSIATI (Process Level)**
Were alternative analytical approaches, data sources, or model specifications considered and explicitly documented? Or did the analysis proceed down one path without acknowledging the fork in the road?

**Expert Intuition vs Overconfidence**
If domain expertise informed any judgment calls: is this a domain with fast, clear, frequent feedback loops — where intuition is genuinely calibrated (chess, clinical nurses, firefighters)? Or a slow, noisy domain — where expressed confidence is likely unfounded (economic forecasting, long-range strategy, hiring)? Kahneman's test: has the analyst received thousands of rapid, unambiguous feedback cycles in this domain?

---

## Category 7 — System 1 Consumption Risk

*This is a broader structural concept beyond individual biases. Check whether the analysis, as it will be received, is likely to be processed analytically (System 2) or snap-judged (System 1) — and whether it has been designed to withstand that.*

**The System 1 / System 2 Reception Problem**
How will the primary audience actually process this analysis? Executives, board members, and busy stakeholders default to System 1: they will glance at a headline number, a chart direction, and a confident conclusion — and make a judgment in seconds. Has the analysis been structured so that the System 1 snap-judgment leads to the *same* conclusion as careful System 2 reading? Or could a fast read produce a dangerously wrong impression?

**Cognitive Ease as False Truth Signal**
Information that is presented clearly, fluently, and in a familiar format *feels* more true and credible than the same information presented awkwardly. Is the analysis's apparent credibility partly a product of good formatting rather than good methodology? Would the same findings, presented more roughly, provoke the scrutiny they deserve?

**Affect Heuristic in Framing**
If the analysis touches a topic that the audience already has an emotional attitude toward (a beloved product, a controversial initiative, a favoured team), that affect will colour how all numbers are received. Has the analysis been designed to be robust to this, or does it rely on the audience's prior goodwill?

**The Substitution Trap**
Has the analysis answered the *measurable* question rather than the *important* question? System 1 substitutes easy questions for hard ones automatically. The important question may be unmeasurable or uncomfortable; the measurable proxy may not actually represent it. Be explicit about what question the data actually answers vs what question the decision-maker needs answered.

---

## Category 8 — Human Behaviour Assumptions (Econs vs Humans)

*This category applies whenever the analysis involves predicting, explaining, or designing for human behaviour — pricing, marketing, product adoption, HR, customer experience, incentive design, etc. Classical economics assumes rational "Econs"; real people behave as "Humans". Check which assumption is embedded in the analysis.*

**Rational Actor Assumption**
Does the analysis assume that people will respond to incentives, information, or options in a logically optimal way? Real people are loss-averse, reference-dependent, cognitively constrained, and predictably irrational. If the analysis predicts uptake, behaviour change, or decision-making, flag where the rational-actor assumption is load-bearing.

**Reference Dependence**
Do the analysis's conclusions depend on where the audience or subject sets their reference point? Outcomes are not experienced as absolute — they are experienced as gains or losses relative to a reference point (prior state, expectation, competitor, peer). A change in what people consider "normal" can completely alter how the same objective outcome is perceived.

**Loss Aversion in Design**
If the analysis informs any recommendation about human choice architecture — pricing, product features, policy design, incentive structures — has loss aversion been accounted for? Losses hurt roughly twice as much as equivalent gains feel good. "Save £100" and "Avoid losing £100" are psychologically very different levers, even though they are economically identical.

**Two Selves: Experiencing vs Remembering**
If the analysis involves any measure of customer experience, satisfaction, employee wellbeing, or quality of service: is it measuring the *experiencing self* (moment-to-moment utility) or the *remembering self* (retrospective evaluation)? These diverge systematically. Satisfaction surveys, NPS, and post-event ratings capture the remembering self, which is dominated by the peak-end rule. Real-time feedback captures the experiencing self. Conclusions drawn from one cannot automatically be applied to the other.

**Endowment Effect & Status Quo Bias**
If the analysis involves people giving something up, switching products, changing behaviour, or accepting new policies: the status quo is stickier than any rational model predicts. The endowment effect means people value what they already have far more than equivalent alternatives. Have switching costs and inertia been properly modelled?

---

## Category 9 — Causal Claims & Structural Reasoning

*This category checks whether the analysis is drawing the right *type* of conclusions from the data — particularly around causation, luck vs skill, and whether the right question is being answered.*

**Correlation vs Causation**
Does the analysis imply or state causal relationships based on correlational or observational data? Identify every causal claim ("X drives Y", "X leads to Y", "because of X, Y occurred") and ask: what is the causal mechanism? Has confounding been tested for? Has a counterfactual been established? Correlation from observational data supports causal *hypotheses* — it does not confirm them.

**Luck vs Skill Decomposition**
Has performance been decomposed into luck and genuine skill? This is especially critical in performance analysis, investment returns, business results after strategy changes, and A/B test interpretation. The key test: would we expect the same result if the same conditions were run again independently? If the answer is uncertain, the role of luck has not been adequately quantified. Kahneman's principle: where feedback is slow and outcomes are noisy, most observed "performance differences" are luck.

**Reference Class Forecasting**
For any forecast or projection: has a formal reference class been identified — a set of comparable historical situations — and has the distribution of outcomes from that class been used as the starting prior? This is the operational form of the outside view. Steps: (1) identify the reference class, (2) establish the statistical distribution of outcomes in that class, (3) identify specific factors that distinguish this case, (4) adjust the baseline accordingly. If this process was not followed, the forecast is likely anchored on an inside-view narrative.

**The Signal-to-Noise Problem**
Across all key metrics in the analysis: what is the estimated signal-to-noise ratio? High-noise environments (e.g. weekly sales, social media engagement, stock prices) require much larger sample sizes and longer time windows to detect genuine signal. Has the analysis been appropriately humble about what can be detected in the data available, given its inherent noise level?

**Counterfactual Thinking**
For any conclusion about the effect of an action, event, or policy: what is the counterfactual? What would have happened *without* the intervention? Without a plausible counterfactual — a control group, a synthetic control, a before/after with appropriate baseline — causal attribution is speculative. Is the counterfactual explicitly stated and defensible?

---

## Audit Summary

After completing all nine categories, produce the following:

### Overall Bias Risk Rating
**[🔴 High / 🟡 Medium / 🟢 Low]** — one-sentence justification

### Findings Table

| # | Bias / Issue | Category | Severity | Where in the Analysis |
|---|-------------|----------|----------|-----------------------|
| 1 | ... | ... | 🔴/🟡/🟢 | ... |

### Remediation Plan

Produce a table of every fix identified across all nine categories, prioritised by impact and classified by what type of work is required:

| # | Fix | Type | Effort | Impact | Specific Action |
|---|-----|------|--------|--------|-----------------|
| 1 | ... | Fix Now / Restate / New Data / Redesign | Low / Med / High | 🔴/🟡/🟢 | Exact steps |

**Effort key:** Low = under 1 hour; Med = half a day; High = requires new data collection or full reanalysis
**Impact key:** 🔴 = materially changes conclusions or credibility; 🟡 = improves robustness; 🟢 = good practice

Then group fixes into three tiers:

**Do Before This Analysis Is Used** (Fix Now items, Low/Med effort)
List each with a one-sentence specific instruction — precise enough to be actioned immediately without further clarification.

**Do Before the Next Version** (New Data and Redesign items)
List each with: what needs to happen, who needs to do it, and what the analysis can say in the interim.

**Disclose Now Even If You Can't Fix It** (biases that cannot be corrected without major work but must be acknowledged)
Draft the exact disclosure language to add to the analysis — a caveat, footnote, or limitations section that honestly bounds the conclusions.

---

### Revised Key Conclusions

This is the most important output of the audit. Rewrite the top 2–3 conclusions from the original analysis as they *should* be stated, given the biases found. Show the before and after:

**Original conclusion:** [quote or paraphrase the claim as made]
**Revised conclusion:** [the corrected version — more hedged, better bounded, or fundamentally different if the bias is severe]

Do this for each major conclusion. If a conclusion cannot be responsibly retained at all given the biases found, say so explicitly.

---

### Debiasing Techniques Recommended
Based on the issues found, recommend 1–3 of the following techniques where relevant, with a specific instruction for how to apply each one to *this* analysis:

- **Pre-mortem**: Assume the decision informed by this analysis has failed spectacularly 12 months from now. Write a one-paragraph explanation of why. Then ask: does anything in that explanation change how you interpret the findings?
- **Consider the Opposite**: For the single most important conclusion, actively construct the strongest possible case for the opposite conclusion using the same data. If that case is easy to make, the original conclusion is fragile.
- **Reference Class Check**: Identify 5–10 analogous situations from history or comparable organisations. What was the distribution of outcomes? Place this analysis's projections within that distribution.
- **Devil's Advocate Review**: Have someone not involved in the analysis review only the disconfirming evidence. What conclusion would they reach?
- **Confidence Interval Calibration**: For all key forecasts, ask: what range would need to be true for 90% of similar analyses to be correct? That range is almost certainly wider than the one currently stated.
- **Two-Frame Test**: Restate every key finding in both a gain frame and a loss frame. If the two versions would lead to different decisions, the framing is doing inappropriate work.
- **Outside-View Audit**: Find the base rate for the core claim. What fraction of similar initiatives, products, or situations achieved what this analysis is predicting?

### One Question the Analysis Cannot Currently Answer
State the single most important unknown — the thing that, if answered differently, would most materially change the conclusions. This is the honest acknowledgement of WYSIATI: the analysis is built on what was available, but the most important variable may not have been in the data at all.

---

*Framework based on: Kahneman, D. (2011). Thinking, Fast and Slow. Biases covered include: anchoring, availability heuristic, representativeness heuristic, base rate neglect, conjunction fallacy, substitution, affect heuristic, halo effect, WYSIATI, priming, cognitive ease, illusion of validity, narrative fallacy, overconfidence, planning fallacy, optimism bias, inside/outside view, hindsight bias, outcome bias, regression to the mean, loss aversion, endowment effect, status quo bias, framing effect, sunk cost fallacy, certainty/possibility effects, fourfold pattern, mental accounting, denominator neglect, peak-end rule, duration neglect, focusing illusion, survivorship bias, clustering illusion, illusion of skill, reference dependence, two selves (experiencing vs remembering), rational actor assumption, signal-to-noise decomposition, luck vs skill, reference class forecasting, counterfactual reasoning, System 1/2 consumption risk, cognitive ease as truth signal, and the substitution trap.*
