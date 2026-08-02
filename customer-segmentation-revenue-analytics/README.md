# Customer Segmentation & Revenue Analytics

**Context:** MSc Business Analytics coursework, University of Bath
**Tools:** R, Tableau (interactive dashboard)

## Business Problem

An online retailer needed to understand which customers actually drive revenue, in order to prioritise retention and marketing spend rather than treating all customers equally.

## Data

500,000+ transactional retail records, analysed at the customer level across regions and time periods (monthly sales summary, regional/country breakdown, and per-customer transaction history).

## Method: RFM Segmentation

Applied **Recency, Frequency, Monetary (RFM)** analysis to score every customer on:
- **Recency** — how recently they last purchased
- **Frequency** — how often they purchase
- **Monetary** — how much they spend

Customers were grouped into **5 actionable segments** based on their combined RFM scores (e.g. high-value loyal customers, at-risk high-spenders, new customers, dormant customers, and low-value one-time buyers).

## Key Finding

The **top 20% of customers by RFM score were responsible for driving the majority of total revenue** — a concentration that justified building differentiated retention and marketing strategies rather than a one-size-fits-all approach.

## Deliverable

Built an interactive Tableau dashboard (linked workbook: sales trends by month, regional/country sales breakdown, and segmented customer view) enabling the commercial team to:
- Monitor segment performance and movement between segments over time
- Explore regional and monthly sales trends without needing to run new queries
- Self-serve on "who are our best customers right now" rather than waiting on ad-hoc analysis

## Business Impact

Provided a clear, data-backed basis for targeting marketing spend and retention efforts at the highest-value 20% of the customer base, and a reusable, self-service reporting tool for the team to track segment health going forward.
