# Meta-Ads-Performance-Dashboard
An end-to-end Power BI solution designed to track and optimize advertising performance across Facebook and Instagram. This project transforms raw Meta ad event logs into actionable marketing intelligence, focusing on conversion funnel efficiency and audience targeting.


# Meta Ads Performance Analytics Dashboard

![Power BI](https://img.shields.io/badge/Data_Visualization-Power_BI-yellow)
![Data Modeling](https://img.shields.io/badge/Modeling-Star_Schema-blue)
![Marketing Analytics](https://img.shields.io/badge/Domain-Digital_Marketing-orange)

## Project Overview
This repository contains a comprehensive **Meta Ads Performance Dashboard** developed in Power BI. The project transforms raw advertising event logs into strategic marketing insights, helping businesses optimize budget allocation, target specific demographics, and improve the conversion funnel across Facebook and Instagram.

## Business Objective
The primary goal is to track and analyze the ROI of paid social campaigns. By monitoring high-level KPIs and granular audience behavior, the marketing team can:
* Identify the most effective platforms (Facebook vs. Instagram).
* Optimize budget distribution based on real-time performance.
* Bridge the gap between high engagement (Clicks/Likes) and actual sales (Purchases).

##  Key Performance Indicators (KPIs)
* **Impressions:** 216K (Total Reach)
* **CTR (Click-Through Rate):** 11.76% (High creative effectiveness)
* **Engagement Rate:** 13.56% (Strong audience resonance)
* **Conversion Rate:** 5.21% (Efficiency of clicks to purchases)
* **Purchase Rate:** 0.61% (Overall funnel efficiency from reach to sale)

##  Data Architecture
The project follows a **Star Schema** design to ensure optimal performance and scalability:
* **Fact Table:** `ad_events` (Impressions, Clicks, Shares, Comments, Purchases)
* **Dimension Tables:**
    * `ads`: Metadata on creative types (Video, Story, Carousel) and targeting.
    * `campaigns`: Budget allocation, start/end dates, and strategy.
    * `users`: Demographic data (Age, Gender, Location, Interests).

##  Key Insights & Recommendations
1. **The "Awareness-Conversion" Gap:** While ads have a very high CTR (11.76%), the purchase rate is low (0.61%). *Action: Optimize landing pages and retargeting ads to drive sales.*
2. **Top Performing Format:** **Video Ads** yield the highest CTR and Conversion Rates, followed closely by **Stories**.
3. **Audience Sweet Spot:** Females aged 18–30 show the highest engagement levels.
4. **Geography:** High potential in India and Brazil for volume; Germany and the UK for high-purchasing-power targeting.
5. **Peak Timing:** User activity peaks during late afternoon and evening (15:00–20:00).

##  Tech Stack
* **Power BI:** Visualization & Dashboarding.
* **Power Query:** Data Cleaning, Transformation (ETL), and derived column creation.
* **DAX:** Advanced measures for dynamic KPI calculations and period-over-period analysis.
[View Detailed DAX Measures Documentation](./dax.md)

##  How to Use
1. Clone the repository.
2. Open the `.pbix` file in Power BI Desktop.
3. Interact with the **Dynamic Parameters** to toggle metrics (Impressions, Clicks, etc.) across all charts.

---
*Developed by Samson Ayamga (Business Analyst)* *Inspired by Data Tutorials*

