---
title: Scoring every site in a country as a location
description: A multi-criteria model that ranks an entire national network of fuel-and-logistics sites against the things that actually make a location good.
---

*A decision-science engagement for a European fuel-and-logistics operator, through London Data Unit. Anonymised. Built on public data (port throughput, national traffic counts, census income and population, OpenStreetMap) and licensed truck-stop service data, with OSRM for travel-time catchments.*

[&larr; Back to portfolio](../)

**Objective:** rank a national network of fuel-and-logistics sites, with competitor and greenfield sites alongside, by how good each is purely as a location, across six countries.

![A drive-time catchment follows the roads, reaching places a straight-line circle misses.](../assets/fig/mcda_catchment.png)
*Market size, competition and labour are measured within a 30-minute drive of each site over the real road network, not a circle drawn around its coordinates. Illustrative.*

## The idea in one line

The operator wanted to know which sites in its network, and which competitor and greenfield sites, were the best **locations**, across six countries. Instead of judging by feel or by a single proxy like traffic, the model scores every site against roughly 38 criteria, each tied to a specific commercial reason and given an explicit direction, then combines them into one rankable location score that can be filtered to any region.

## What this piece demonstrates

- **It turns a vague question into measurable, signed criteria.** "Which sites are good?" becomes thirty-eight things you can actually compute, each carrying a commercial rationale and a direction: closer to a growing port is good, closer to housing is bad (planning friction, noise, HGV access), more unemployment in the catchment is good (labour and footfall for a staffed stop). Making the direction explicit is what stops a scoring model from quietly rewarding the wrong thing, which is the most common way these models fail: a criterion gets added because the data exists, nobody decides which way is better, and it drags the ranking somewhere no one intended.
- **It measures catchments, not points.** Market size, competition and labour are measured within a thirty-minute drive of each site using real road-network travel times, not straight-line distance, because a location's value is the market it can actually reach, not its coordinates. Two sites a kilometre apart can have very different catchments if one sits by a motorway junction and the other behind a river with one bridge, and only drive-time distance sees that.
- **It is honest about proxies.** There was no clean dataset for trunking routes, so the presence of named logistics operators at nearby hubs stands in for it. It is labelled a proxy in the model, not dressed up as a direct measure, so anyone reading the ranking knows exactly which inputs are solid and which are standing in for something harder to observe.
- **It states its engineering trade-offs.** One country-scale distance was computed with hex-grid jumps rather than full routing, because the precision that routing buys is not worth the compute at national scale. That is a deliberate, stated choice, not a hidden shortcut, and the writeup is explicit about where that approximation is used and where it is not.
- **It reframes competition as opportunity.** Competitor service and pricing data is mapped to find "service deserts": places with a provision or pricing gap. A defensive metric (where are my rivals) becomes a commercial one (where could we compete on price or fill a gap).

## How the scoring works

Each criterion is computed for every candidate site, normalised to a common scale, and signed as either "more is better" or "closer/less is better". Normalising matters because the raw inputs live on wildly different scales, a port handles millions of containers while unemployment is a percentage, and without a common scale the biggest numbers would silently dominate the score. The ten families cover: proximity to ports and the container and roll-on/roll-off throughput there, including multi-year growth; logistics-hub proximity and size; motorway-junction access and whether junctions intersect; heavy-goods traffic in the area by time of day, by vehicle class, and how evenly or unevenly it is spread across the day; income, population and unemployment within the drive-time catchment; proximity to the operator's own fuel terminals by fuel type; competitor truck-stop provision and service pricing; and local residential density at several radii. The signed, normalised criteria are combined into a single composite score, which ranks every site nationally and can be filtered to a region.

The reason for keeping thirty-eight separate criteria rather than a handful of summary indices is that a good location is good for several independent reasons, and those reasons do not always agree. A site can sit on heavy HGV traffic yet far from any port, or near cheap labour yet hemmed in by housing. Collapsing that into one number too early hides the tension; keeping the criteria separate until the final combine means every trade-off stays visible and arguable.

## Honest limits

This describes the model and the approach, not the client's ranked output or its criteria weights, which belong to the client. A multi-criteria score is only as defensible as its weights, and weighting is a judgment: the design keeps every criterion transparent and separately inspectable precisely so that weight choices can be argued and tested rather than buried in a single black-box number. Several criteria are proxies, and the model is explicit about which. Some inputs are licensed and cannot be shared. The value here is the discipline of the design: a commercial question made fully computable, at continental scale, without pretending the judgment calls away.

**Methods and tools:** multi-criteria decision analysis, signed-and-normalised scoring, 30-minute OSRM drive-time catchments, H3 hex-grid approximation, proxy design, Python.

---

*Built by Joey Scully. Product and Commercial Analytics consultant. Available for remote interim and contract work.*
