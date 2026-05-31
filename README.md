# Digital-Game-Performance-Analysis-2025

<img width="975" height="515" alt="image" src="https://github.com/user-attachments/assets/d126704a-d25c-44b6-a2d9-bd500db0261c" />


**Introduction**

This analysis examines mobile gaming user behaviour specifically in-app purchase patterns, engagement levels, and demographic spending drivers to produce actionable insights for monetization strategy, user acquisition, and retention planning.

My motivation for this dataset came directly from my professional role in transaction monitoring, where identifying customer behaviour patterns and financial anomalies is a core daily responsibility.

This dataset offered a direct parallel: the same segmentation lens I apply to financial transactions, classifying users by spend velocity, identifying high-value versus dormant customers, and tracking conversion signals maps precisely onto “gaming analytics”. Analyzing gamer behaviour allowed me to apply those skills in a new domain while generating commercially meaningful insights.

**Data Story**

This report analyses the Digital Game Performance 2025 dataset, 3,024 mobile gaming users across 30+ countries to uncover patterns in in-app purchase (IAP) behaviour, engagement, and demographic spending profiles. Some of the notable findings include: the 30–39 age bracket leads all cohorts in IAP revenue (82,267), closely followed by 40–49 (82,116). Male users account for 67.4% of total revenue. Android outspends iOS at 157,722 vs. 129,488. India dominates by session count (2,424) and purchase volume (34,204). Battle Royale and MOBA genres drive the longest sessions. The Minnow segment represents 84.1% of users, with Whales (2.3%) generating outsized revenue. Eight strategic recommendations are proposed covering monetisation, retention, and geographic expansion.

<img width="720" height="315" alt="image" src="https://github.com/user-attachments/assets/7707b120-d59f-47df-a4e0-81e7a0d3af12" />

**Data Splitting & Preprocessing**


To get clean insights, I performed a rigorous “Data Tune Up”

• I replaced the “null” values in categorical fields (Gender, Game Genre, Device, Payment Method) with ‘nil’ thus preserving all 3,024 records for pivot analysis.

• I got the ‘Month’ column derived from Last Purchase Date for time-series analysis using this formula (=TEXT([@lastpurchasedate],”mmmm”))

• I scrubbed all duplicates within the dataset

• Age groups binned into six cohorts (0–9 through 50–59) for revenue segmentation.

**Pre-Analysis: Initial Trends & Hypotheses**

Before detailed pivot analysis, scanning the raw data revealed several immediate signals that shaped the analytical approach:

• Spending skew: Maximum In App Purchase of 4,964.45 vs. median of 11.98 extreme right-skew confirming classic long-tail distribution.

• Geographic concentration: India (242 users) is the single largest country to dominate both session and spending metrics.

• Age-revenue: Users aged 30–49 represent the two largest cohorts with independent payment access expected to lead revenue.

• Device split: 1,738 Android vs. 1,226 iOS, Android is expected to lead absolute revenue.

• Genre-engagement link: Competitive multiplayer genres (Battle Royale, MOBA) to produce longer sessions due to structured match formats.

• Payment diversity: Seven payment methods present, near-uniform distribution suggesting optimised checkout design.

All six hypotheses were confirmed in subsequent analysis.

**In-Analysis: Key Findings**


<img width="720" height="292" alt="image" src="https://github.com/user-attachments/assets/47e6ee52-2d60-44fd-b9f3-d8c5f4915541" />

<img width="682" height="493" alt="image" src="https://github.com/user-attachments/assets/d5b7d7c5-2d61-4881-8a1f-fdcf03dea6bc" />

**Post- Analysis**

<img width="395" height="598" alt="image" src="https://github.com/user-attachments/assets/6d3930fa-0ec2-496c-b3a7-b6d4a84380fe" />

**Top User Profiles**

<img width="655" height="150" alt="image" src="https://github.com/user-attachments/assets/1d07f2c8-b188-4293-94de-ad033e8d1d33" />

**Key Findings vs. Initial Hypotheses**


All six pre-analysis hypotheses were confirmed. The magnitude of India’s dominance leading in both session count and purchase volume simultaneously exceeded expectations. The convergence of all top user profiles on Whale classification and Indian market origin is a notable finding that signals both geographic concentration risk and an exceptionally loyal high-value user base in that market.

**Unexpected Outcomes**

August engagement collapse: Drop from 4,167 (July) to 1,697 sessions the dataset’s most anomalous finding. Likely partial-month data, but a genuine competitive or platform shock cannot be excluded.

• Payment method uniformity: Near-perfect equal distribution across 7 methods unusual and suggests deliberate checkout design or sampling coincidence.

• Narrow session length variance: Only 0.65 min spread across all genres (20.48–21.13 min) more homogeneous than typical multi-genre platforms.

**Data Visualization & Charts**


<img width="720" height="380" alt="image" src="https://github.com/user-attachments/assets/589b5eab-be87-42ec-a04b-a8b3d3aa3e17" />

To effectively communicate insights, I built a dashboard using Excel. The dashboard consolidates all key findings into five KPI cards and five interactive charts, with a Control Panel featuring slicers for In-App-Purchase Amount, Spending Segment, Game Genre, and Country.

<img width="647" height="224" alt="image" src="https://github.com/user-attachments/assets/28a2a927-9436-48f0-89ef-46374161a8d5" />

**Recommendation**

<img width="651" height="388" alt="image" src="https://github.com/user-attachments/assets/46cc0545-bcf8-49e6-a814-226c92dab274" />

**Conclusion**

This analysis confirmed six pre-analysis hypotheses and surfaced three unexpected findings. The platform’s revenue is concentrated in working-age adults (30–49), the Indian market, Android devices, and a tiny but critical Whale user segment. Battle Royale and MOBA genres drive the deepest engagement. The near-uniform payment distribution confirms effective checkout design. The August engagement collapse is the most urgent unresolved question.

To address these issues, I suggest tracking users from install stage through first purchase stage to churn to compute true lifetime value by segment, also measure causal impact of price-point and promotion changes on In App Purchase conversion rates, and finally investigate the August engagement decline to discover the root cause of the problem.

**References & Appendices**

• Software Used: Microsoft Excel

• Source: Kaggle
