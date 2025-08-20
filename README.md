# Digital Marketing Campaign Data Analysis

## Project Overview
This project explores and analyzes a digital marketing campaign dataset containing 8,000 customer records and 20 features. The analysis covers customer segmentation, campaign performance evaluation, engagement metrics, and channel effectiveness. The goal is to uncover insights that can guide targeted marketing strategies, optimize campaign spend, and improve overall customer engagement.

**Dataset:** [Predict Conversion in Digital Marketing Dataset - Kaggle](https://www.kaggle.com/datasets/rabieelkharoua/predict-conversion-in-digital-marketing-dataset)  
**License:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

---

## 1. Dataset Overview
- **File Loaded:** `digital_marketing_campaign_dataset.csv`  
- **Shape:** 8,000 rows × 20 columns  
- **Data Types:**
  - Numeric: 15 columns (`int64`, `float64`)  
  - Categorical: 5 columns (`object`)  

## 2. Data Quality
- **Duplicates:** 0 duplicate rows  
- **Missing Values:** No null values detected  
- **Column Notes:** Revenue column not provided; ROAS cannot be calculated  

## 3. Descriptive Statistics
- **Age:** 18–69 (mean ≈ 43.6 years)  
- **Income:** 20,014–149,986 (mean ≈ 84,664, total = 677,313,574)  
- **Ad Spend:** 100.05–9,997.91 (mean ≈ 5,000.94, total = 40,007,558.64)  
- **Loyalty Points:** 0–4,999  
- **Campaign Metrics:**
  - CTR: 0.01–0.30  
  - Conversion Rate: 0.01–0.20  
  - Website Visits: 0–49  
  - Time on Site: 0.5–14.99 minutes  

## 4. Campaign Insights
- **Campaign Channels:** Social Media, Email, PPC, Referral, SEO  
- **Campaign Types:** Awareness, Conversion, Retention, etc.  
- **Customer Base:** 8,000 unique customers  

### Key Observations
- Dataset is clean: no duplicates, no missing values  
- Wide variation in AdSpend and Income indicates segmentation opportunities  
- CTR and Conversion Rates vary moderately, suggesting channel-specific performance differences  
- Balanced mix of marketing channels; Social Media, Email, and PPC are frequent  
- Wide demographic age range enables targeted strategies  

---

## 5. Customer Segmentation Analysis

### Transaction Patterns (by Previous Purchases)
| Segment | Purchases | Customers |
|---------|-----------|-----------|
| No Purchases | 0 | 838 |
| Occasional | 1–2 | 1,567 |
| Regular | 3–5 | 2,398 |
| Elite | 6+ | 3,197 |

**Observation:** Majority of customers are Regular or Elite, indicating strong repeat-buying behavior.

### Points Engagement & Loyalty (by Loyalty Points)
| Loyalty Tier | Points | Customers |
|--------------|--------|-----------|
| No Points | 0 | 4 |
| Low | 1–499 | 762 |
| Medium | 500–1999 | 2,440 |
| High | 2000–4999 | 4,794 |

**Observation:** Most customers are highly engaged in loyalty programs.

### Spending Patterns (by AgeGroup & IncomeGroup)
- Age and income segmentation helps tailor marketing campaigns  
- Female customers slightly outnumber males across age groups  

**Exported Segmented Dataset:** `customer_segments.csv`  
- Columns: `CustomerID`, `PurchaseFrequency`, `LoyaltyTier`, `AgeGroup`, `IncomeGroup`  

---

## 6. Campaign Metrics Evaluation

### Cost per Acquisition (CPA)
- **Definition:** AdSpend ÷ Conversions  
- **Observations:**
  - PPC Conversion campaigns have lowest CPA (~5,137 per conversion)  
  - Email and Social Media campaigns: CPA ~5,500–5,600  
- **Insight:** CPA varies by channel and campaign type, indicating efficiency differences  

### Cost per Social Share (CPRS)
- **Definition:** AdSpend ÷ SocialShares  
- **Observations:**
  - Social Media campaigns have lowest CPRS (~94–97 per share)  
  - SEO, Email, and PPC campaigns higher (~98–104)  
- **Insight:** Social Media campaigns are most cost-efficient for engagement  

**Visualization:** Bar charts for CPA and CPRS by CampaignChannel and CampaignType

---

## 7. Customer Engagement Analysis

### Website Engagement
- **Metrics:** WebsiteVisits, PagesPerVisit, TimeOnSite  
- Most users have 0–50 visits; Pages per Visit 1–10; Time on Site 0.5–15 minutes  

### Social Media Engagement
- **Metric:** SocialShares  
- Engagement is moderately uniform across campaigns  

### Email Engagement
- **Metrics:** EmailOpens, EmailClicks  
- Email Opens: 0–18, Email Clicks: 0–9  
- Not all opens convert to clicks, highlighting engagement gaps  

### Correlation Insights
- Conversion weak-to-moderately correlates with WebsiteVisits, PagesPerVisit, TimeOnSite, and EmailClicks  
- Loyalty Points show minor correlation with engagement metrics  
- SocialShares and EmailOpens have negligible correlation with conversion  

**Visualization:** Heatmap of engagement metrics vs. Conversion and Loyalty Points  

---

## 8. Channel Performance Comparison

### Average ClickThroughRate (CTR) by Channel
| Campaign Channel | Avg CTR |
|-----------------|---------|
| Email | 0.156 |
| PPC | 0.158 |
| Referral | 0.152 |
| SEO | 0.153 |
| Social Media | 0.156 |

### Average ConversionRate by Channel
| Campaign Channel | Avg Conversion Rate |
|-----------------|-------------------|
| Email | 0.105 |
| PPC | 0.104 |
| Referral | 0.103 |
| SEO | 0.104 |
| Social Media | 0.107 |

### Total Ad Spend by Channel (in millions)
| Campaign Channel | Total Ad Spend |
|-----------------|----------------|
| Email | 7.87 |
| PPC | 8.20 |
| Referral | 8.65 |
| SEO | 7.74 |
| Social Media | 7.54 |

**Insights:**
- PPC and Referral: slightly higher CTR but higher Ad Spend  
- Social Media: highest Conversion Rate despite lower spend  
- Metrics guide optimization of budget allocation and campaign strategy  

---

## 9. Visualizations Generated
- Customer Transaction Segments (bar chart)  
- Loyalty Points Engagement Tiers (bar chart)  
- Age Group Distribution (bar chart)  
- Income Group Distribution (bar chart)  
- Gender Composition by Age Group (stacked bar chart)  
- CPA and CPRS by CampaignChannel/Type (bar charts)  
- Website, Social Media, and Email Engagement Histograms  
- Correlation Heatmap: Engagement vs. Conversion/Loyalty Points  
