# SuiteStay Singapore: Identifying the Premium Business Travel Gap

**Context:** Analytics in Practice coursework, University of Bath — market entry strategy consulting exercise
**Tools:** Python (Pandas), Tableau, empathy mapping / design thinking

## Business Problem

Consulting for a property management company considering a new accommodation service to compete with Airbnb. The brief: choose a city and target demographic, and determine whether a genuine market gap exists.

**Chosen segment:** High-income single business travellers in Singapore.

## Data

Inside Airbnb Singapore dataset — **3,693 listings**, 12 months of calendar availability, and **8,768 reviews** from premium entire-home listings (defined as entire homes priced ≥ SGD 150/night).

## Key Findings

- **91%** of entire-home listings sit at or above SGD 150/night, clustering in the SGD 200–300 band — no meaningful budget segment exists, validating a premium positioning.
- **47%** of premium listings impose minimum-stay rules that exclude a typical 3–5 night corporate trip (44% require 90+ nights). This gap is invisible in review data, since travellers turned away by minimum-stay rules never book and never leave a review — the dataset hides rejected demand rather than reflecting it.
- **79.9%** of premium supply is controlled by hosts with 10+ listings — a portfolio-driven structure that prioritises volume over guest experience, explaining recurring complaints about noise and cleanliness.
- Premium listings record just **14.2% estimated occupancy** against a **76% hotel benchmark** (Singapore Tourism Board, 2023) — this points to unmet demand, not oversupply.
- A cluster of 58 listings priced at **SGD 200–350 achieves 40%+ occupancy** — a proven high-performance pricing zone.
- Only **37.8%** of premium listings offer self check-in, and just **0.3%** offer 24-hour check-in — a critical gap for business travellers arriving on irregular schedules.
- Demand is business-led, not leisure-led: only a 0.6 percentage point gap between weekday and weekend occupancy (vs a typical 20–30 point leisure-market premium), with a clear spike to 61.6% occupancy in September around the F1 Grand Prix.

## Empathy Mapping

Target persona "Marcus Chen" — a regional sales director visiting Singapore 4–6 times a year for 3–5 nights — surfaced core pains (noise, inconsistent cleanliness, long minimum stays, host unavailability) and core needs (reliable WiFi, a proper desk, seamless late-night check-in, flexible cancellation).

## Proposed Service: SuiteStay Singapore

A professionally managed entire-home service in the CBD corridor (River Valley, Orchard, Downtown Core), priced at SGD 200–350/night, offering:
- 1–5 night flexible bookings
- Verified soundproofing and hotel-grade cleaning
- Dedicated workspace
- 24-hour smart-lock self check-in

Positioning: **not cheaper, but more usable** — removing every friction point currently blocking premium Airbnb supply from serving business demand.

## Limitations

Occupancy figures are proxy-based (from availability data) and review sentiment used keyword tagging rather than full NLP — findings are directionally strong but not precisely measured. Recommended follow-up: primary research on willingness to pay, and a full financial model incorporating regulatory and operational costs.
