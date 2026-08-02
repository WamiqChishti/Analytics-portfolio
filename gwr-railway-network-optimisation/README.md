# GWR Railway Network Optimisation: A Decision Support System

**Context:** MN50750 Optimisation & Spreadsheet Modelling, University of Bath
**Tools:** Excel, VBA, Ford-Fulkerson max-flow algorithm

## Business Problem

Great Western Railway faces fluctuating passenger demand during peak events (festivals, sporting matches, holidays), requiring fast, data-backed decisions on train allocation across the network. Route managers need clear, actionable numbers on how many trains can move between any two stations without exceeding track capacity.

## Approach

Built a Decision Support System (DSS) in Excel/VBA modelling a reduced GWR network of **34 major stations and 88 directed rail segments**, each with a defined capacity. The system implements the **Ford-Fulkerson max-flow algorithm**, which:

1. Iteratively searches for a path from origin to destination with spare capacity on every segment.
2. Sends the maximum possible number of trains down that path, limited by the bottleneck (lowest-capacity) segment.
3. Updates residual capacities and repeats until no further path exists.
4. Sums all flows to produce a maximum flow — mathematically guaranteed to be the highest throughput the infrastructure can support.

## User Interface

Designed for non-technical route managers:
- **Input:** enter Origin and Destination station IDs on the "Stations" sheet.
- **Load Data / Run Algorithm** buttons trigger the calculation in the background.
- **Output:** the "Optimal Flows" sheet lists every rail segment used, the flow assigned, and its capacity.
- **Reset function** clears prior results instantly, so a new origin-destination pair can be tested without reloading the workbook.

## Trial Results

Five origin-destination pairs were tested across different regions of the network to validate robustness.

**Trial 1: The South Coast Route (Southampton Central → Brighton)**
- Total max flow: **20 trains/day**
- Insight: the Havant–Brighton segment is fully saturated — the binding constraint on the entire route. To increase service frequency to Brighton, GWR would need to invest in physical track capacity specifically on this final leg, not elsewhere on the route.

*(Full report covers 5 scenarios in total; see coursework write-up for complete trial results.)*

## Key Outcome

The tool improved modelled network throughput by approximately **15%** over a manual, non-optimised baseline, and — critically — pinpoints the exact segment causing a bottleneck rather than just the overall capacity number, turning a vague "we need more capacity" into a specific, fundable infrastructure recommendation.

## Limitations & Future Work

The current prototype's interface, while functional, is Excel-based and not suited to on-the-go use. Proposed enhancement: convert into a deployable mobile application for use by route managers in real time.
