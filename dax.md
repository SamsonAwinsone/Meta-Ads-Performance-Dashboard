1. Clicks
i. Total number of ad clicks.


Clicks = 
CALCULATE(
    COUNT(ad_events[event_id]),
    ad_events[event_type] = "Click"
)


ii. Purchases (Conversions)
Total successful transactions resulting from ad interactions.


iii. Purchases = 
CALCULATE(
    COUNT(ad_events[event_id]),
    ad_events[event_type] = "Purchase"
)

iv. Total Engagements
Sum of all active interactions (Clicks, Shares, and Comments).

Total Engagements = 
VAR ClicksCount = [Clicks]
VAR SharesCount = CALCULATE(COUNT(ad_events[event_id]), ad_events[event_type] = "Share")
VAR CommentsCount = CALCULATE(COUNT(ad_events[event_id]), ad_events[event_type] = "Comment")
RETURN
    ClicksCount + SharesCount + CommentsCount


2. Performance & Efficiency Ratios
Calculated metrics to measure the effectiveness of the campaigns.

i. Click-Through Rate (CTR)
Measures how often people who see the ad end up clicking it.


CTR % = 
DIVIDE([Clicks], [Impressions], 0)
Conversion Rate (CR)
Measures the percentage of clicks that resulted in a purchase.


ii. Conversion Rate % = 
DIVIDE([Purchases], [Clicks], 0)

iii. Engagement Rate (ER)
Measures overall interaction relative to reach.

Engagement Rate % = 
DIVIDE([Total Engagements], [Impressions], 0)


3. Dynamic Selection Logic
Used to allow the user to toggle between different metrics (Impressions, Clicks, Purchases) across all charts using a single slicer.

i. Selected Metric Value
This measure retrieves the value of the metric selected via the Field Parameter or a supporting slicer table.

Selected Metric = 
SWITCH(
    SELECTEDVALUE('Metric Selection'[Order]),
    0, [Impressions],
    1, [Clicks],
    2, [Purchases],
    3, [Total Engagements],
    [Impressions] -- Default fallback
)

4. Budget & ROI
i. Total Budget
Aggregated spend from the campaigns dimension table.

Total Budget = SUM(campaigns[total_budget])
Purchase Rate (Funnel Efficiency)
Percentage of impressions that converted into a purchase.


ii. Purchase Rate % = 
DIVIDE([Purchases], [Impressions], 0)
