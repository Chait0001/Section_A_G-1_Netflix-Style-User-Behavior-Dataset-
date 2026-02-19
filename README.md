# Netflix-Style User Behavior Analysis (OTT Sector)

## Project Overview

This project analyzes a Netflix-style OTT user behavior dataset to uncover actionable insights related to user engagement, churn, and revenue optimization.

The goal was to transform raw behavioral data into a strategic growth roadmap by linking demographics, device usage, content preferences, and subscription plans to financial outcomes.

---

## Problem Statement

Streaming platforms collect massive amounts of data but struggle to identify:

- Why users stay
- Why users churn
- Why premium tiers fail to convert
- Which content truly drives retention

Key Issues Identified:
- 14.5% inactive (churn) rate
- Premium+ contributes only ~9% revenue
- High session abandonment (~50%)
- Price–value mismatch in top-tier plan

---

## Dataset Information

- **Source:** Kaggle – Netflix-Style User Behavior Dataset  
- **Raw Records:** 10,000  
- **Processed Records:** ~6,685 unique clean users  

### Data Layers

1. **Demographics**
   - Age
   - Gender
   - Location
   - Household Size

2. **Subscription Details**
   - Plan (Basic / Standard / Premium / Premium+)
   - Monthly Spend
   - Status (Active / Inactive)

3. **Engagement Metrics**
   - Watch Duration
   - Device Type
   - Genre
   - Content Type
   - Completion Rate

---

## Data Cleaning & Preparation

- Mode imputation for Gender
- Median imputation for Age & Household Size
- Removed duplicates
- Standardized text values
- Converted data types
- Boolean consistency validation
- Created new feature: `maturity_level` (Kids / Family / Teens / Adult)

---

## KPI Framework

| KPI | Formula | Business Purpose |
|------|----------|----------------|
| Average Watch Duration (AWD) | Total Watch Minutes / Total Sessions | Measures content stickiness |
| Completion Rate (CR) | Total Progress % / Total Sessions | Measures engagement quality |
| ARPU | Total Monthly Spend / Active Users | Monetization efficiency |
| Inactive Rate | Inactive Users / Total Users | Tracks churn |

---

## Key Insights

### Premium+ Tier Underperformance
- Generates only ~$12.8k revenue (~9%)
- Standard Plan generates ~$51.6k
- Clear price–value mismatch

### Desktop Dominance
- Desktop users drive highest watch time (~91k mins)
- Contradicts mobile-first assumption

### Genre Stickiness
High Engagement:
- Drama (~71.8 mins avg)
- Animation (~70.1 mins avg)

Low Engagement:
- Music
- Family

### Golden Cohort
Users aged **26–35**
- Highest retention (>85%)
- Highest Customer Lifetime Value

### Discovery Bottleneck
- “Stopped” sessions ≈ “Completed” sessions
- Indicates weak recommendation alignment

---

## Advanced Segmentation

### Golden Segment
- Age 26–35
- Desktop users
- Drama viewers
- Highest CLV & retention

### At-Risk Segment
- Under 18
- Mobile users
- High early drop-off

---

## Interactive Dashboard

Built using **Google Sheets (Pivot Tables + Slicers)**

### Dashboard Includes:
- KPI Scorecard
- Device vs Watch Time
- Genre Performance
- Subscription Plan Revenue Split
- Completion Rate Analysis
- Interactive Filters (Age, Device, Genre, Plan)

---

## Strategic Recommendations

1. **Restructure Premium+**
   - Add exclusive bundles (early access, premium-only content)
   - Potential 12–15% MRR increase

2. **Desktop Optimization**
   - Improve Web UX
   - Feature parity with mobile apps

3. **Content Budget Reallocation**
   - Increase Drama & Animation investment
   - Reduce low-retention genres

4. **Win-Back Campaign**
   - Target 14.5% inactive users
   - Automated re-engagement offers

5. **Fix Discovery Algorithm**
   - Introduce content match scores
   - Reduce abandonment rate

---

## Business Impact Estimation

- ~15% CAC reduction via better demographic targeting
- Diversified revenue by reviving Premium+
- Increased engagement via content reallocation
- Improved retention through algorithm optimization

---

## Limitations

- Synthetic dataset
- Missing values (10–15%)
- Outliers present
- No direct causal validation for churn reasons

---

## Future Scope

- Predictive churn modeling
- Pricing A/B testing
- Recommendation engine enhancement
- Granular session-level tracking

---

## Team

- Ishan Goyal – Research Lead  
- Naman – Data Lead  
- Yashi – Analysis & Dashboard Lead  
- Neelanshu Karn – PPT Lead  
- Puneet – Strategy Lead  
- **Chaitanya – Project Lead**

---

## Tools Used

- Google Sheets
- Pivot Tables
- Data Cleaning Techniques
- KPI Design Framework
- Financial Correlation Analysis

---

## Final Takeaway

This project demonstrates how behavioral analytics can uncover hidden revenue leaks, optimize pricing structures, and improve retention strategy in the OTT industry.
