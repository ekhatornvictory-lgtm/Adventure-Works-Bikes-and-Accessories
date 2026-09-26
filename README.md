# Adventure-Works-Bikes-and-Accessories
An end-to-end Power BI dashboard built for Adventure Works, a bike/accessories retailer, covering executive KPIs, product-level performance simulation, and customer segmentation. The report spans Jan 2020 – Jun 2022 and combines revenue trending, category performance, a "what-if" price/profit simulator, and customer lifetime value analysis.

📊 4 interactive pages · 🔎 25.2K orders analyzed · 👥 17.4K unique customers · 💰 $24.9M in tracked revenue

📁 Table of Contents
1. Overview
2. Dashboard Pages
3. Key Insights
4. Tools & Techniques
5. Screenshots
6. Recommendations

* How is the business performing overall, and where is growth coming from?
Which products are profitable, on-target, and returned too often — and what happens if we test a pricing change?
Who are our customers, and is our revenue-per-customer trend healthy?

The model uses a rolling date filter, drill-through navigation from the executive summary into product and customer detail, and a live price-adjustment slider that recalculates profit in real time.

* Dashboard page and Page	Purpose
1. Exec Dashboard	|| Company-wide KPIs, revenue trend, category mix, top 10 products, month-over-month deltas
2. Product Detail	|| Drill-through view per product with actual-vs-target gauges and a price-adjustment simulator
3. Customer Detail	|| Customer segmentation by income/occupation, top 100 customers, revenue-per-customer trend
4. Map || Supporting geographic

Key Insights
1. Growth is real, but decelerating

Revenue grew from roughly $0.4M/month in early 2020 to $1.83M in the latest month (+3.31% MoM), well above the long-run trendline. However, order volume actually fell slightly month-over-month (-0.88%, 2,146 vs. 2,165), meaning recent revenue growth is coming more from spend-per-order than from new order volume — worth watching if it continues.

2. Category mix is tire/accessory-heavy

Orders skew heavily toward Accessories (17.0K) and Bikes (13.9K), with Clothing trailing at 7.0K. Consistent with this, "Tires and Tubes" is the single most-ordered product type company-wide — high-frequency, lower-ticket consumables are doing the volume, while bikes likely carry the margin.

3. One product is a clear return-rate outlier

Across the top 10 products, return rates cluster tightly between 1.55%–1.95%, except for the Sport-100 Helmet, Red, which sits at 3.33% — nearly double the next-highest product despite generating the highest revenue of the group ($73,444). This is the single biggest quality/fit-and-finish flag in the top-seller list and pairs with the finding that "Shorts" is the most-returned product type overall — sizing-sensitive apparel appears to be Vickson's systemic returns problem.

4. The pricing simulator shows real profit upside — but supply is the constraint

For the "Water Bottle – 30 oz." (Vickson's #1 product by orders), a +20% price adjustment was modeled. The simulation shows adjusted profit consistently outperforming actual profit across the full 12-month window (Jul 2021–Jun 2022) with no visible drop-off in order volume, suggesting the product is currently under-priced relative to demand. That said, the product is also missing target on all three core metrics: orders (404 vs. 438 target), revenue ($4,067 vs. $4,292), and profit ($2,546 vs. $2,687) — a ~5–8% shortfall across the board, so the near-term priority is closing the target gap, with the price increase as a lever to help close the revenue/profit gap specifically.

5. Revenue per customer is in a sustained decline — the most important trend on the report

Unique customers have grown to 17.4K, but Revenue per Customer has fallen from ~$3K+ (2020) to under $1K (2022), a clear and consistent downward trendline with two visible step-downs (mid-2020 and mid-2021). This is diluting the value of Vickson's overall customer base and is arguably a bigger long-term risk than any single product issue — it suggests either (a) heavy discounting/promotional acquisition, (b) a mix shift toward lower-value customer segments, or (c) natural cart-size decline as the customer base matures. This deserves a dedicated cohort/RFM analysis.

6. Customer value is concentrated, not segmented by tier

The Top 100 customers generated $615,329 in revenue (avg. ~$6,153/customer, vs. the $1,431 company average) — a small group driving outsized value. Order counts across the top 100 are modest (mostly 4–7 orders each), meaning this is a high-average-order-value group, not a high-frequency group. By income band, "Average" and "Low" income customers together account for the large majority of orders (10,266 + 11,600 vs. 2,827 "High"), and by occupation, Professional customers lead order volume (7,925), with the report flagging Ruben Suarez as the top revenue driver among Skilled Manual customers in 2022 ($4,683) — a useful example of value existing outside the "expected" high-income segment.

Tools & Techniques
* Power BI Desktop — data modeling, DAX measures, report design
* DAX — MoM % change measures, target-vs-actual gauges, dynamic price-adjustment simulation (parameter-driven "what-if" measure)
* Drill-through & bookmarks — Exec Dashboard → Product Detail / Customer Detail
* What-if parameter — live price elasticity slider on the Product Detail page
* Time intelligence — rolling trend lines with linear forecast overlays

[▶️ Watch my Power BI Dashboard Demo](videos/videopj.mp4)

<p align="Left">
  <img src="https://github.com/ekhatornvictory-lgtm/Adventure-Works-Bikes-and-Accessories/blob/67dbf2499146d86bd7f6a5c41a073f76dc10fb6f/Screenshot%202026-09-26%20125350.png" width="180" alt="Victory Ekhator">
</p> <p align="left">
  <img src="Screenshot 2026-09-26 130013.png" width="180" alt="Victory Ekhator">
</p>
</p> <p align="left">
  <img src="Screenshot 2026-09-26 130106.png" width="180" alt="Victory Ekhator">
</p>

## Recommendations
* Investigate the Sport-100 Helmet (Red) and the "Shorts" category for sizing, fit, or quality-control issues driving above-average returns.
* Run a controlled price test on the Water Bottle – 30 oz. given the simulator shows profit upside with no apparent volume penalty at +20%.
* Prioritize a revenue-per-customer root-cause analysis (cohort/RFM) — this multi-year decline is the biggest structural risk visible in the data.
* Build a lightweight loyalty or upsell motion targeting the "Average" and "Low" income segments, since they already drive the bulk of order volume but at lower value per order than the "High" segment.
