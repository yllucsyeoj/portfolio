---
title: The £138,750 hidden inside a warehouse rent
description: A vehicle-routing and geodemographic study for Hines that put a number on the logistics cost buried in where a warehouse sits.
---

*A decision-science study for Hines, the global real estate investor, through London Data Unit. Published as a research paper (LDU-HINES 001, 2020). Built on public data: ONS Census, OpenStreetMap, OSRM, Ordnance Survey AddressBase.*

[&larr; Back to portfolio](../) · [Read the full 44-page paper (PDF)](../papers/hines001-logistics-location-analysis.pdf)

## The finding in one line

For a high-income customer base, picking the wrong London depot out of 23 cost more than **£1 per delivery**. Over 2,500 deliveries a week that is **£138,750 a year**, roughly the annual rent on 7,000 sq ft of industrial space in Acton, hidden inside a rent decision that looked like it was already settled.

## What this piece demonstrates

- **It reframed the question before touching the data.** Hines priced warehouses on floor area and broad location, as if every occupier valued a site equally. The real variable is not the building; it is the match between a depot's location and the geography of that occupier's customers. So the question is not "what is this warehouse worth" but "what is it worth to this occupier, given who they serve."
- **It put a defensible figure on an invisible cost.** The penalty for a bad depot choice never shows up on a rent roll. It shows up in delivery cost, and it is different for every occupier. Quantifying it meant simulating the actual deliveries, not estimating.
- **It separated signal from noise before trusting it.** The customer archetypes were screened with spatial autocorrelation (Local Moran's I / LISA) so that only factors with genuine geographic clustering fed the model, and factors like raw speed limits were deliberately left out as artefacts.

## The finding, with its edges

The cost of mis-selecting a depot is not uniform. For a non-specific, evenly-spread customer base the spread between the best and worst depot was small (£0.59 per delivery): location barely matters. For a sharply-defined high-income archetype it was widest (£1.11 per delivery): location matters enormously. That difference is itself the insight. It tells an investor which locations are safe bets for any tenant and which only suit a particular one, and it opens two commercial moves: pricing warehouse rent against the transport saving a location offers a specific occupier, and treating price-predictability as a location attribute in its own right for speculative investors and third-party logistics tenants.

## Method

A consistent spatial frame of 4,835 small areas (ONS LSOAs) across Greater London. Traffic-aware travel-time matrices built with the OSRM routing engine over a 12-hour delivery window. Twelve geodemographic customer archetypes, six derived by agglomerative hierarchical clustering over income, socio-economic class, age and sex, and six constructed heuristically as controls. A vehicle-routing solver on Google OR-Tools generating 1,932 simulated delivery routes from 23 real London depot locations. A vehicle-and-labour cost model converting routes into a cost-per-delivery for every archetype-and-depot pair. The study rejects its pre-registered null hypothesis: geodemographic archetype and logistics cost are related, and the relationship depends on how specific the customer base is.

## Honest limits

The archetypes are modelled test populations, not one real retailer's order book, so the figures show the size and shape of the effect rather than one company's exact bill. Costs are simulated from a routing and cost model, not measured from operations. The data is 2020 London. The value of the method is that it is repeatable and that it quantifies something the industry priced by feel.

---

*Built by Joey Scully. Product and Commercial Analytics consultant. Available for remote interim and contract work.*
