# CreditCard_PowerBI_Databricks

Overview
Credit card analytics dashboard built using transaction and cardholder data, providing insights into spending patterns, card usage, bank-wise performance, credit limits, and transaction trends. Interactive KPIs and visualizations enable analysis by card type, issuer, transaction date, and customer behavior for better decision-making.
---
Data Source
Property	Details
Platform	Power BI
Backend / Data Warehouse	Databricks
Scope	Multi-bank, multi-country credit card portfolio
Time Range	2007 – 2017 (approx.)
---
Dashboard Pages
Page 1 — Overview
High-level KPIs and distribution charts for the entire portfolio.
Key Metrics
Metric	Value
Active Cards	318K
Inactive Cards	182K
Sum of Transaction Amount	125 bn
Average Credit Limit	105.00K
Total Banks	16
Total Card Types	6
Visuals
Count of Credit Limit by Issuing Bank — Bar chart ranking all 16 banks. Diners Club, Discover, and JCB lead in credit limit count, while First National and PNC are at the lower end.
Sum of Transaction Amount by Merchant Category — Donut chart showing Travel dominates at 99.84% (125 bn), with all other categories (Shopping, Grocery, Pharmacy, Food) collectively accounting for just ~0.16%.
Count of Bank by Card Type — Donut chart showing relatively even distribution across 6 card types: DC, DS, AX, VI, MC, JC — each accounting for roughly 16–17% of total bank count.
Filters Available
Year
Bank
Card Type
---
Page 2 — Trends & Risk
Time-series analysis, risk scoring, and geographic breakdown.
Visuals
Sum of Transaction Amount by Year (2007–2017) — Area chart showing total transactions hovering between 11.3 bn and 11.5 bn per year. A notable peak is observed around 2014–2015, followed by a slight decline.
Risk Score by CardTypeCode — Line chart showing risk scores declining from DC (~269K) down through DS, VI, AX, MC to JC (~264.5K). DC cards carry the highest risk profile.
Risk Score by Issuing Bank and CardTypeCode — Treemap breaking down risk exposure by bank. Diners Club, Discover, and JCB are the largest blocks; Chase, American Express, Bank of America, Citibank, USAA, Capital One, U.S. Bancorp, Barclays, Wells Fargo, GE Capital, and First National are also represented.
Inactive Cards by Country — Curved line chart showing the United States has the highest inactive card count (~150K), followed by Japan with a steep drop-off, and the United Kingdom at the lower end (~near 0K). This suggests the portfolio is heavily US-centric.
Filters Available
Active / Inactive toggle
---
Card Types Reference
Code	Card Type
DC	Diners Club
DS	Discover
AX	American Express
VI	Visa
MC	Mastercard
JC	JCB
---
Key Insights
Travel dominates spending — Nearly all transaction volume (99.84%) is attributed to the Travel merchant category, which may indicate the dataset is travel-card focused or that the data needs further segmentation.
High inactivity rate — 182K out of 500K cards (36.4%) are inactive, representing a significant churned or dormant segment.
US-heavy inactive base — The United States accounts for the vast majority of inactive cards, suggesting a retention opportunity in the domestic market.
DC cards carry the highest risk — Diners Club cards score highest on the risk index across all card types.
Transaction volume peaked ~2014–2015 — Post-2015, transaction amounts show a modest downward trend worth monitoring.
Balanced card-type distribution — All six card types have near-equal representation (~16–17%), indicating a diversified portfolio with no single dominant card network.
---
How to Use the Dashboard
Connect Databricks — Ensure the Databricks workspace credentials and cluster endpoint are configured in Power BI's data source settings.
Refresh Data — Use the scheduled refresh or manual refresh to pull the latest data from Databricks.
Apply Filters — Use the Year, Bank, and Card Type slicers on Page 1 to drill into specific segments.
Toggle Active/Inactive — On Page 2, use the Active/Inactive arrow buttons to switch context for the geographic chart.
---
File Structure
```
CreditCard_Dashboard.pbix        # Main Power BI report file
├── Page 1: Overview             # KPIs, bank/category/card-type breakdowns
└── Page 2: Trends & Risk        # Time series, risk scores, country analysis
```
---

Last Updated	—
Data Refresh Frequency	—
