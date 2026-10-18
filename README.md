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
Recommendations: 1. Analyze acquisition sources to identify channels generating high session volumes but low conversion rates to Product View.2. Evaluate landing pages, website navigation, loading speed, and product catalog accessibility.<br>

2. Product View → Add to Cart — Significant Losses Among Interested Visitors
Of the 63,816 sessions that included product views, only 14,891 (23.3%) progressed to Add to Cart. A total of 48,925 sessions (76.7%) did not continue toward purchase.<br>
This stage is particularly important because users have already demonstrated interest in a product but have not taken the next intended action. Potential reasons include pricing, insufficient product information, stock availability issues, poor user experience, or a mismatch between product offerings and customer expectations.
Recommendations: 1. Identify product pages with high view volumes but low Add to Cart conversion rates. 2. Evaluate the visibility of the Add to Cart button, pricing information, product availability, and delivery conditions. 3. Test improvements to product pages and measure their impact on Add to Cart CVR and subsequent funnel stages.<br>
<br>
3. Checkout and Payment Stages — Conversion Losses and a Critical Anomaly<br>
Analysis of the final e-commerce funnel stages revealed that, out of 5,324 sessions that initiated checkout, only 2,529 (47.5%) completed the full sequence through Purchase.<br>
The highest relative drop-off within the checkout process occurs at the Add Payment Info → Purchase transition, with a drop-off rate of 33.1%, highlighting the need for further investigation into the final purchase stage.<br>
A significant anomaly was also identified during the week of January 25. The conversion rate from Add Payment Info to Purchase dropped sharply from 70.9% to 24.5% in just one week, while the conversion rate from Begin Checkout to Add Payment Info remained relatively stable at 75.6%.<br>
This discrepancy may indicate payment processing issues, technical errors, or inaccurate tracking of the purchase event.<br>
Recommendations: 1. Prioritize validating data completeness for the week of January 25, checking purchase event tracking accuracy, and investigating potential payment system errors. 2. Conduct additional segmentation analysis by device category and country to determine whether the anomaly affected all users or specific groups.<br>
<br>
Overall Business Priority<br>
The immediate priority is to identify the cause of the sharp decline in final-stage conversion and address any confirmed barriers preventing users from completing their purchases. At the same time, improving early-stage engagement and product-to-cart conversion represents a significant opportunity to strengthen overall funnel performance and increase potential revenue.<br>

## Task 2. Which transitions between funnel stages have the lowest conversion rates (Step CVR) and require the highest priority for optimization?
Analysis of E-commerce Funnel Performance over 11 weeks (November 16, 2020 – January 25, 2021) showed that the lowest conversion rates occur at the early stages of the funnel, where a significant proportion of sessions do not progress to the next action.<br>
Key problematic transitions:<br>
1. Session Start → Product View — 20.9%. Only one in five sessions reaches the product viewing stage. The lowest weekly conversion rate was recorded on December 28 — 15.1%, indicating the need to investigate traffic quality and landing page performance.<br>
2. Product View → Add to Cart — 23.3%. Fewer than a quarter of sessions involving product views progress to the cart. The lowest conversion rate was recorded on November 16 — 8.0%. In addition, after reaching 33.7% on November 30, the rate declined to 17.5% on January 25. This indicates the need to analyze product offerings, pricing, and the usability of product pages.<br>
3. Add to Cart → Begin Checkout — 35.8%. Only about one-third of sessions in which a product was added to the cart proceed to checkout. The lowest rate was recorded on January 4 — 24.5%. This may indicate barriers preventing users from starting the checkout process.<br>
4. A critical anomaly was also identified at the final stage, Add Payment Info → Purchase. Despite an overall conversion rate of 66.9%, the rate dropped sharply to 24.5% during the final week (January 25), compared with 70.9% in the previous week. This deviation requires further investigation, as it may be related to technical payment issues or inaccurate tracking of completed purchases.<br>
<br>
Recommendations
<br>
The following actions are recommended as priorities:<br>
Investigate the Payment → Purchase anomaly on January 25: Examine the accuracy of purchase event tracking, data completeness, and potential errors in the payment process.<br>
Improve the Session Start → Product View and Product View → Add to Cart transitions: Analyze traffic sources, landing pages, product pages, and differences across device categories.<br>
Investigate the reasons for drop-offs after Add to Cart: Review delivery conditions, cart usability, and the process of proceeding to checkout.

## My Task 3. How does purchase conversion performance (Purchase CVR) vary across different device categories?

Analysis Period: November 16, 2020 – January 25, 2021<br>
To evaluate the traffic distribution, the Traffic Share metric was calculated — the proportion of sessions from each device type relative to the total number of sessions during the analyzed period.<br>
Calculation Formula:<br>
Traffic Share (%) = (Device Sessions / Total Sessions) × 100%<br>
<br>
Analysis Results
<img width="1027" height="233" alt="image" src="https://github.com/user-attachments/assets/9fd89e15-2fc0-4084-b6fa-21c9135f5f55" />
Note: The calculations are approximate, as the number of sessions for Desktop and Mobile is displayed in rounded values in the Tableau charts.<br>
<br>
To evaluate performance, two metrics were compared: Sessions — the number of sessions by device type, and Purchase CVR — the percentage of sessions that resulted in a purchase.
<img width="1008" height="277" alt="image" src="https://github.com/user-attachments/assets/f2e1dcfa-3d24-42a0-b9f9-0ecdc96fb101" />
Desktop — Highest Traffic Volume.Desktop accounts for 58.04% of all sessions, generating 46% more sessions than Mobile. However, its Purchase CVR is 1.18%, compared to 1.25% for Mobile.This means that Desktop generates more traffic but has a slightly lower proportion of sessions that result in a purchase.
Mobile — Highest Conversion Efficiency. Despite generating less traffic, Mobile has the highest Purchase CVR at 1.25%, approximately 5.5% higher than Desktop in relative terms. Mobile's conversion advantage is relatively small, but it demonstrates that a higher number of sessions does not always translate into greater efficiency in converting sessions into purchases.<br>
Tablet — Lowest Traffic Volume and Unstable Conversion. Tablet accounts for only 2.22% of all sessions, with a Purchase CVR of approximately 1.10%.
<br>
Recommendations:
<br>
Investigate opportunities to improve Purchase CVR on Desktop. Since Desktop generates the highest traffic volume, even a small improvement in conversion could increase the number of purchases.

## Task 4. Which acquisition sources generate high traffic volumes but show low purchase conversion rates (Purchase CVR)?
1. Comparison of Acquisition Sources
 <img width="1025" height="327" alt="image" src="https://github.com/user-attachments/assets/970bb986-9965-4f71-81f2-bd6662943341" />
 The analysis showed that Google and Other have the greatest potential for conversion improvement.<br>
Google is the largest acquisition source, generating 117,430 sessions (35.85% of total traffic), but its Purchase CVR is approximately 1.00%.<br>
Other accounts for 89,147 sessions (27.21%), with a nearly identical conversion rate of 1.00%.<br>
Together, these two sources generate 63.06% of total traffic but have lower conversion rates than Direct (1.13%), Shop (1.86%), and Unknown (2.87%).<br>
Therefore, Google and Other offer the greatest potential to increase the number of purchases due to their combination of high session volumes and relatively low Purchase CVR.<br>
<br>
Recommendations
1. Google — Priority for Optimization. Break down traffic by channels, campaigns, and landing pages. Identify segments that generate high session volumes but have low conversion rates.<br>
2. Other — Investigate the Source Breakdown. Determine which channels and campaigns are included in this category. This will help identify specific underperforming segments.<br>
3. Shop — Investigate the Reasons for Higher Conversion. Analyze user behavior and the purchase journey to identify factors that may explain the Purchase CVR of 1.86%.<br>
4. Unknown — Verify Attribution. Despite having the highest Purchase CVR (2.87%), the unidentified origin of this traffic limits the ability to evaluate acquisition effectiveness.<br>

## Task 5. How do revenue and purchase conversion rates (Purchase CVR) change over the analyzed period?
November 16 – December 7 — Growth in Both Metrics. Revenue increased from $14,297 to $57,766 (+304%), while Purchase CVR rose from 0.88% to 1.91%. Revenue grew faster than the number of sessions, indicating improved traffic monetization efficiency.<br>
December 14 – January 4 — Decline and Divergence Between Traffic and Revenue. Revenue decreased from $46,149 to $9,196, while Purchase CVR fell from 1.60% to 0.52%. January 4 is particularly noteworthy: the number of sessions increased by 41.8% compared to the previous week, but revenue declined by 8.2%. Therefore, an increase in traffic did not guarantee higher sales.<br>
January 11 – January 25 — Short-Term Recovery Followed by a Sharp Decline. By January 18, revenue had increased to $24,947, while Purchase CVR reached 1.27%, with almost no increase in traffic. However, on January 25, revenue dropped to $4,936 (−80.2%), and the conversion rate fell to 0.37%. This was the main anomaly of the period and requires further investigation.<br>
<br>
Key Finding: The trends in Revenue and Purchase CVR demonstrate that financial performance depends not only on traffic volume but also on the ability to convert sessions into purchases. The periods of January 4 and January 18 provide the most valuable analytical insights, as changes in revenue occurred without a corresponding increase in the number of sessions.

## Business Insights — E-commerce Funnel Performance
Conclusion: The main business problem is not a lack of visitors, but the low effectiveness of converting them into customers. Google and Other generate 63% of traffic, yet their conversion rates are around 1%. The funnel reveals where potential revenue is lost: only 20.9% of sessions reach the product viewing stage, and just 23.3% of those sessions progress to the cart. This suggests a possible mismatch between the expectations of the acquired audience and the website's product offerings. Additionally, at the end of January, the conversion rate after entering payment information dropped from 70.9% to 24.5%, creating another potential barrier to revenue generation. As a result, the business attracts a significant volume of traffic but fails to consistently convert it into financial results.
<br>
Recommendation: The business should shift its focus from visitor volume to acquisition profitability and purchase completion. The first priority is to investigate the sharp decline in completed purchases at the end of January. If the cause is a payment issue or technical error, resolving it should take priority, as the company is losing customers who are already ready to buy. The next step is to review which audiences Google and Other attract and whether the products, prices, and delivery conditions meet their expectations. Rather than increasing traffic volume, resources should be directed toward segments that generate more revenue relative to their costs, while improving the conditions that prevent customers from completing purchases. The goal is to generate more completed and profitable orders from existing traffic, rather than simply increasing website visits.
<br>
Access to Tableau<br>
https://public.tableau.com/shared/FM7P4N9B5?:display_count=n&:origin=viz_share_link<br>
<br>
SQL Query in BigQuery<br>
<img width="793" height="446" alt="image" src="https://github.com/user-attachments/assets/7c15472a-412f-475b-bebe-590d14865635" />
<img width="690" height="606" alt="image" src="https://github.com/user-attachments/assets/a2ff4a99-d138-483a-83b1-d77651cf8127" />
<img width="793" height="327" alt="image" src="https://github.com/user-attachments/assets/4cffdf32-4500-4d5d-8471-a19f234fc894" />
  <img width="950" height="445" alt="image" src="https://github.com/user-attachments/assets/3694c3db-38c9-4070-afc3-4f9562f3135c" />
  <img width="797" height="742" alt="image" src="https://github.com/user-attachments/assets/a5050483-1524-4196-b239-4905b7b6c13c" />
  <img width="827" height="817" alt="image" src="https://github.com/user-attachments/assets/5b3da86d-4936-4f57-b014-f5477c8291f9" />
  <img width="805" height="722" alt="image" src="https://github.com/user-attachments/assets/7a8ddd6d-9e84-4bd6-ab99-f570089badf8" />
  <img width="768" height="832" alt="image" src="https://github.com/user-attachments/assets/817b89dd-3d2d-4c89-84cd-c48ea9639d5f" />
  <img width="805" height="422" alt="image" src="https://github.com/user-attachments/assets/b39bda33-305c-4fd3-9afb-c2e868aba03c" />
  <img width="890" height="582" alt="image" src="https://github.com/user-attachments/assets/84e94ade-79e9-4da6-b5f4-3d4b518710a6" />
  <img width="731" height="778" alt="image" src="https://github.com/user-attachments/assets/aadbda88-9f55-4114-9924-b1f98cb9ba8f" />
  <img width="760" height="746" alt="image" src="https://github.com/user-attachments/assets/eb4f05d6-9f62-472e-ad51-b3854f802ada" />
  <img width="737" height="597" alt="image" src="https://github.com/user-attachments/assets/0072c01e-2eff-4819-8742-fe9b0bcea2a7" />

