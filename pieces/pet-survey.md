---
title: Who actually buys a pre-planned pet funeral
description: It is not the segment you would target. A survey of 267 pet owners, run with real statistical discipline, where age and gender predicted nothing and a behavioural chain predicted everything.
---

*A quantitative survey analysis for a Taiwan pet-care group weighing an integrated brand (medical, grooming, boarding, and end-of-life under one name): 267 respondents, 276 categorical relationships tested. Client anonymised; data held privately under confidentiality.*

[&larr; Back to portfolio](../)

**Objective:** find who to target for a pre-planned pet-funeral product, and test whether the obvious demographic segments are the right ones to aim at.

## The finding in one line

The obvious way to target a pre-planned pet funeral product is by demographics: age, gender, "urban professional women in their forties." In this data **age and gender predicted nothing**. The real buyer is found through a behavioural chain: owners with 10+ years of tenure are far more likely to have experienced pet loss, which is by far the strongest predictor of knowing the product exists, which leads to a planning mindset, which is what actually predicts intent to buy.

![Association strengths for behavioural predictors, with age and gender at zero.](../assets/fig/survey_effects.png)
*Cramér's V for each relationship after false-discovery correction. Behavioural signals clear the effect-size floor; age and gender do not register.*

## What this piece demonstrates

- **It refused the obvious segmentation and proved it was empty.** Segmenting by "35 to 45 year old women" feels right and is not evidence-based here. After correcting for multiple comparisons, gender produced zero significant links to any key outcome and age predicted none of them. The piece says so plainly instead of quietly dropping it, because a demographic targeting plan is expensive to run and the whole point of the survey was to find out whether it would work before the money was spent.
- **It used real statistical discipline, not eyeballed cross-tabs.** 276 categorical pairs were tested with Benjamini-Hochberg false-discovery correction and an effect-size floor, so the findings that survive are the ones worth acting on. This matters more than it sounds: test 276 relationships at the usual threshold and you expect around a dozen to look significant by chance alone, so without the correction a confident-sounding targeting rule could be built entirely on noise. 221 of the 276 pairs showed nothing, and that is reported as a result, not hidden.
- **It turned the surviving signal into a targeting rule.** Tenure predicts loss experience (the strongest effect in the study), loss experience predicts awareness, awareness predicts a planning mindset, and planning predicts purchase intent. That is a chain, not a coincidence, and it names a warm audience that already sits inside the customer base.

![The behavioural chain from ownership tenure through to purchase intent.](../assets/fig/survey_chain.png)
*The chain behind the targeting rule. Long tenure makes pet loss more likely; loss experience is the strongest single predictor of knowing the product exists; awareness leads to a planning mindset, which predicts intent. Cramér's V shown where measured; age and gender attach nowhere on it. Anonymised survey, 267 respondents.*

## Why demographics fail here

The reason the obvious segments come up empty is that buying a pre-planned pet funeral is not something a life stage predicts; it is something an experience predicts. A forty-year-old who has never lost a pet has no reason to have thought about it, while a long-tenured owner who has been through it once already carries the mindset the product needs. Age and gender are visible and easy to buy media against, which is exactly why they are tempting, but here they are standing in for the thing that actually matters, length of ownership and lived experience of loss, and they turn out to be poor stand-ins. The chain is less convenient to target than a demographic, because it lives in the group's own behavioural data rather than on an ad platform's dropdown menu, but it is the one that is real.

## The commercial levers it surfaced

- **Grooming is a brand channel, not just a service line.** Grooming frequency is the strongest behavioural predictor of brand awareness, so every salon visit is a brand touchpoint with dual return: retention and awareness. A regular grooming customer is already a warm audience for the wider brand, at no additional acquisition cost.
- **Two "separate" products are one conversion.** Interest in the integrated brand and intent to trial it move together so tightly that a single pitch converts both; running two campaigns wastes one, and the saving is real because the group was weighing exactly that two-track spend.
- **The price gap has to be met head-on.** Most respondents anchor an acceptable funeral cost well below the NT$16,000 contract. The large undecided middle does not close by leading with "affordable," which only confirms and hardens the low anchor. It closes with value framing and instalments, by changing what the price is being compared against rather than apologising for it.

## Method

A survey instrument covering service behaviour, brand awareness, price expectations, and five business outcomes. Categorical relationships were measured with Cramér's V, Likert relationships with an effect-size measure for rank data, every test class corrected for false discovery, and sparse categories collapsed so that a handful of responses could not masquerade as a pattern. Findings were kept only if they cleared both significance after correction and a minimum effect size, which is what separates a real signal from one of 276 coincidences, and the ones that did not clear the bar were recorded as genuine null results rather than left out.

## Honest limits

This is a convenience sample skewed toward the group's own audience, 76% female and concentrated in Taipei, so the levels (how many are interested) are not population estimates and should not be read as market sizing. The relationships (what predicts what) are the durable part, because a correlation between tenure and awareness does not depend on the sample matching the national population in the way a headline interest rate would. Outcomes are self-reported intent, which overstates eventual purchase. The value is a disciplined map of which signals to target on and, just as useful, which to stop wasting money on.

**Methods and tools:** survey analysis, Cramér's V association, Benjamini-Hochberg false-discovery correction, effect-size thresholding, Python.

---

*Built by Joey Scully. Product and Commercial Analytics consultant. Available for remote interim and contract work.*
