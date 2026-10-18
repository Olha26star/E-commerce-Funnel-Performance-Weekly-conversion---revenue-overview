# E-commerce-Funnel-Performance-Weekly-conversion---revenue-overview
## E-commerce Funnel Performance Weekly conversion and revenue overview

## Business Task 
At which stages does the e-commerce funnel lose the most sessions, and which segments should be prioritized for further investigation?<br>
## My Task
1. At which stage of the e-commerce funnel do the largest absolute session losses occur?
2. Which transitions between funnel stages have the lowest conversion rates (Step CVR) and require the highest priority for optimization?
3. How does purchase conversion performance (Purchase CVR) vary across different device categories?
4. Which acquisition sources generate high traffic volumes but show low purchase conversion rates (Purchase CVR)?
5. How do revenue and purchase conversion rates (Purchase CVR) change over the analyzed period?

## Tools & Technologies (SQL-BigQuery+Tableau)
## Task 1. At which stage of the e-commerce funnel do the largest absolute session losses occur?
For this analysis, identifying the transition with the highest drop-off in a single week is not sufficient. It is necessary to determine where the largest number of sessions is lost, whether this pattern persists across different periods, and whether it indicates a decline in funnel performance.<br>
1. Analysis Methodology<br>
Using Google BigQuery, I built a sequential six-stage e-commerce funnel:<br>
<img width="1167" height="30" alt="image" src="https://github.com/user-attachments/assets/a1126c18-ed76-4437-8bb7-d30b98d51182" />
For each stage transition, I used three key metrics:
<img width="1902" height="530" alt="image" src="https://github.com/user-attachments/assets/1b1a7d1c-a3e2-4942-9379-230bc007e2ad" />
<img width="1042" height="596" alt="image" src="https://github.com/user-attachments/assets/3f9a4ef6-b898-417f-9abc-a37092ada19f" />
<img width="1457" height="636" alt="image" src="https://github.com/user-attachments/assets/fdb07d35-3a73-4e3d-98ce-188adc4b8001" />
Period: November 16, 2020 – January 25, 2021 (11 weeks)
<img width="1026" height="270" alt="image" src="https://github.com/user-attachments/assets/f6f93874-ab4e-4737-95e5-bcf37ff0146d" />
<img width="1035" height="662" alt="image" src="https://github.com/user-attachments/assets/2289e26d-5249-4d0b-ab1a-1cda1db0de73" />

The largest session losses are concentrated in the first two stages of the funnel, before users even begin the checkout process.<br>
<br>
1. Session Start → Product View — Largest Absolute Session Loss
Of the 305,365 initial sessions, only 63,816 (20.9%) progressed to Product View. A total of 241,549 sessions (79.1%) did not reach the next stage.<br>
This indicates that a relatively small proportion of sessions progress from visiting the website to interacting with products. Potential reasons include irrelevant traffic, underperforming landing pages, difficult navigation, or technical issues. However, some visitors may not have intended to make a purchase.
Recommendations:<br>
1. Analyze acquisition sources to identify channels generating high session volumes but low conversion rates to Product View.<br>
2. Evaluate landing pages, website navigation, loading speed, and product catalog accessibility.<br>

2. Product View → Add to Cart — Significant Losses Among Interested Visitors
Of the 63,816 sessions that included product views, only 14,891 (23.3%) progressed to Add to Cart. A total of 48,925 sessions (76.7%) did not continue toward purchase.<br>
This stage is particularly important because users have already demonstrated interest in a product but have not taken the next intended action. Potential reasons include pricing, insufficient product information, stock availability issues, poor user experience, or a mismatch between product offerings and customer expectations.
Recommendations:<br>
1. Identify product pages with high view volumes but low Add to Cart conversion rates.
2. Evaluate the visibility of the Add to Cart button, pricing information, product availability, and delivery conditions.
3. Test improvements to product pages and measure their impact on Add to Cart CVR and subsequent funnel stages.<br>
<br>
3. Checkout and Payment Stages — Conversion Losses and a Critical Anomaly<br>
Analysis of the final e-commerce funnel stages revealed that, out of 5,324 sessions that initiated checkout, only 2,529 (47.5%) completed the full sequence through Purchase.<br>
The highest relative drop-off within the checkout process occurs at the Add Payment Info → Purchase transition, with a drop-off rate of 33.1%, highlighting the need for further investigation into the final purchase stage.<br>
A significant anomaly was also identified during the week of January 25. The conversion rate from Add Payment Info to Purchase dropped sharply from 70.9% to 24.5% in just one week, while the conversion rate from Begin Checkout to Add Payment Info remained relatively stable at 75.6%.<br>
This discrepancy may indicate payment processing issues, technical errors, or inaccurate tracking of the purchase event.<br>
Recommendations:<br>
1. Prioritize validating data completeness for the week of January 25, checking purchase event tracking accuracy, and investigating potential payment system errors.
2. Conduct additional segmentation analysis by device category and country to determine whether the anomaly affected all users or specific groups.<br>
<br>
Overall Business Priority<br>
The immediate priority is to identify the cause of the sharp decline in final-stage conversion and address any confirmed barriers preventing users from completing their purchases. At the same time, improving early-stage engagement and product-to-cart conversion represents a significant opportunity to strengthen overall funnel performance and increase potential revenue.<br>





