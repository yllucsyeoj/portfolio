---
title: Rebuilding a city as a map of its buildings
description: Joining property records, address registers, map data and an aggregate mobility panel into a building-level picture of who lives where, for a real estate investor.
---

*A decision-science engagement for an institutional real estate investor, through London Data Unit. Anonymised. Built on public data (HM Land Registry price-paid records, Ordnance Survey AddressBase, OpenStreetMap) and a licensed, aggregate mobility panel. No individual is identified anywhere in the method or its output.*

[&larr; Back to portfolio](../)

![Four unrelated datasets resolved to a common building-level unit.](../assets/fig/bp_assembly.png)
*Four datasets that share no common key, resolved to one unit: the individual building. Getting them to line up is most of the work.*

## The idea in one line

The investor wanted to understand the resident population around prime London residential assets: roughly who lives there, where they work, how far they travel. No register answers that at building level, so the picture is assembled from public property and map data and an aggregate mobility panel, resolved down to individual buildings, with no person ever named or singled out.

## What this piece demonstrates

- **Entity resolution is where the accuracy actually lives.** Property transaction records and the national address register describe the same buildings but share no common key, and both store addresses as free text: "23-33", "45A", "STAR & GARTER HOUSE", "CENTRE POINT TOWER 101-103". A parser pulls each string apart into structured components (building number, range, suffix, name) so the two sources can be joined. This unglamorous step determines whether everything downstream is attached to the right building.
- **A targeted filter finds the right stock.** Restricting to buildings with several separate high-value flat transactions isolates converted and subdivided houses, the specific asset type the investor cared about, straight from the transaction pattern.
- **The city is carved into buildings, not circles.** Instead of arbitrary catchment radii, a morphological tessellation divides the map into street-bounded cells around each building footprint, so every observation can be attributed to the building it genuinely belongs to.
- **Movement becomes an aggregate, never a profile of a person.** The mobility panel is reduced to stay points, then to an inferred home and workplace per device, then immediately aggregated to a building-level summary of commute distance and workplace geography. The unit of analysis is the building; a device is only ever a means to that aggregate.

## How it fits together

Public property records give high-value flat transactions; the address parser and a join to the national address register turn those into geocoded buildings. Map data supplies building footprints and the street network, from which a morphological tessellation produces one street-bounded cell per building. The licensed mobility panel is processed with stay-point detection, attributed to those cells, and reduced to inferred home and workplace per device. Everything is then aggregated to the building: a population profile of commute patterns and workplace zones, built from four sources that were never designed to be joined, and holding nothing about any individual.

![A messy address string resolved into structured, joinable fields.](../assets/fig/bp_entity.png)
*The parser that makes the join possible: free-text address strings resolved into the structured fields that let property records and the address register meet.*

## Honest limits

This describes the method, not the client's output or any building's residents. A mobility panel is a sample, skewed by who carries which apps, and inferred home and workplace are probabilistic rather than ground truth. The address resolution is imperfect, so the matched buildings are a subset of all of them. The mobility data is licensed and privacy-constrained; nothing individual is shown here or shareable. The value is the pipeline itself: assembling a building-resolution population picture from sources that share no key, while deliberately keeping the person out of the output.

---

*Built by Joey Scully. Product and Commercial Analytics consultant. Available for remote interim and contract work.*
