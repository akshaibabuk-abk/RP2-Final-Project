# RP2-Final-Project
Marketing Campaign Performance Dashboard

1. 📁 Dataset Understanding (Short Summary)

This project is based on a marketing campaign dataset containing information about campaigns, ads, user demographics, and ad interaction events. The goal is to analyse campaign reach, engagement, and performance.

Tables Overview :-

Campaigns – Contains campaign-level details such as Campaign ID, Name, Start/End Date, and Budget.

Ads – Includes information about each advertisement such as Ad Platform, Ad Type, Target Audience, Campaign ID.

Users – Provides demographic attributes of users such as Age, Gender, Country, Interests.

Ad Events – Tracks user interactions with ads (Impressions, Clicks, Likes, Shares), including Timestamp, User ID, Ad ID.


How the Data Connects :-

Each Campaign contains multiple Ads (Campaign ID → Ads).

Each Ad generates multiple Ad Events (Ad ID → Ad Events).

Each Event is performed by a User (User ID → Users).

Together, these tables form a star schema, enabling end-to-end performance analysis across campaigns, ads, audiences, and engagement behaviour.


2. 📈 Proposed KPIs (Performance Indicators)

The dashboard evaluates marketing effectiveness using the following KPIs:

Total Impressions

Total Clicks

Total Engagements (Likes + Shares)

Click-Through Rate (CTR %)

Engagement Rate

Reach (Unique Users)

No. of Campaigns

Total Spend / Budget

Total Ads

Impressions by Platform

Engagement by Ad Type

Engagement by Time of Day

Engagement by Age Group

Reach by Gender

These KPIs help analyze campaign visibility, user behavior, platform effectiveness, demographic patterns, and overall marketing performance.


3. 🛠 Technical Approach
🔹 Tools Used

Power BI – for data cleaning, data modelling, DAX calculations, and dashboard creation.

Power Query (inside Power BI) – for preprocessing and cleaning.

Power BI Data Model – for relationships and DAX measures.

🔹 Step 1: Data Cleaning (Power Query)

Renamed inconsistent column names for clarity.

Removed unnecessary columns where applicable.

Removed duplicate rows in key relationship columns (Campaign ID, Ad ID, User ID).

Ensured correct data types for dates, text fields, and numeric values.

🔹 Step 2: Data Modelling (Power BI Model View)

Built a star schema with:

Campaigns as Campaign dimension

Ads as Advertisement dimension

Users as Demographic dimension

Ad Events as Fact table

Established one-to-many relationships:

Campaigns → Ads

Ads → Ad Events

Users → Ad Events

This enabled cross-filtering across campaigns, ads, user demographics, and interactions.

🔹 Step 3: DAX Calculations (Power BI)

Created custom measures for core KPIs, including:

Total Impressions

Total Clicks

Total Engagements

CTR %

Reach (Distinct Users)

Spend

Engagement Rate

These measures support accurate and scalable analysis.

🔹 Step 4: Dashboard Visualization (Power BI Desktop)

Designed a 1-page performance dashboard for clear storytelling.

Created KPI cards for quick metrics overview.

Added bar, donut, pie, and line charts to analyze:

Top campaigns

Ad type performance

Platform contribution

Time-of-day engagement

Age group and gender segmentation

Used slicers for Campaign, Platform, Ad Type, and Country filtering.

Applied a custom color palette (cyan, magenta, orange) for a modern marketing theme.

🔹 Step 5: Insights & Interpretation

The dashboard reveals:

Campaigns generating the highest impressions

Ad types driving the most engagement

Performance comparison between Facebook and Instagram

Best engagement time segments

Most interactive age and gender groups

How reach and engagement vary across demographics

These insights help optimize future marketing strategies and improve targeting effectiveness.
