# Olist E-commerce Data Analysis

Comprehensive data analysis of the Brazilian Olist marketplace, examining revenue performance, customer segmentation, repeat purchase behavior, payment preferences, and regional market dynamics to generate actionable business insights.

---

## Dataset

Uses the **[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)** (CC BY-NC-SA 4.0). Contains **100,000+ orders** from 2016–2018 across 27 Brazilian states, with detailed information on customers, payments, products, sellers, geolocation, and reviews. Made publicly available by **Olist** and curated by André Sionek, Thomas Da Costa, and Pedro Chaves.

---

## Objectives

- Track monthly revenue growth and identify seasonal inflection points
- Analyze customer payment method preferences and trends
- Segment customers using RFM analysis to understand lifetime value
- Measure repeat purchase cycles and identify the critical repurchase window
- Evaluate regional market concentration and uncover category specialization opportunities

---

## Key Insights

**Revenue & Growth**
- Monthly revenue grew **4×** from ~$271K (Feb 2017) to ~$1.17M (Nov 2017)
- **Black Friday 2017** created a new revenue baseline above $840K

**Payment Behavior**
- **Credit cards dominate** (71–77%), gradually replacing *boleto*
- Debit cards and vouchers: **<8% combined**

**Customer Segmentation (RFM)**
- **"At Risk"** : largest segment by count (19.3%)
- **"High Value At Risk"** : highest revenue contributor (17.5%) – critical retention priority
- **"Emerging Loyalists"** : largest growth-ready segment (18.9%)

**Repeat Purchase Behavior**
- **14–30 day window** is critical: 550 repeat purchases – more than any other period
- Repurchase probability drops sharply after 30 days
- No return within 45 days = high risk of churn

**Regional Market Analysis**
- **Southeast (SP, RJ, MG)** : ~70% of transaction volume
- **SP alone**: 46,448 purchases – 3× RJ
- **Specialization hotspots** (LQ ≥ 2.0):
  - **PA**: Highly specialized in **health_beauty**
  - **PE**: Highly specialized in **health_beauty**, **watches_gifts**, **telephony**
  - **CE**: Highly specialized in **watches_gifts**, **health_beauty**
- Volume leaders (SP, RJ, MG) show low specialization; mid-sized states **punch above weight in niches**

---

## Methodology

- **Scope**: Only **"delivered"** orders; incomplete months excluded
- **Revenue**: Sum of `payment_value`
- **RFM**: Recency (1–5), Frequency (1–5), Monetary (1–5) → 10 behavioral segments
- **Repeat Purchase**: Days between consecutive purchases (filtered 14–365 days)
- **Regional Analysis**:
  - Transaction volume, top categories by revenue
  - **Location Quotient (LQ)** : Bayesian-adjusted, filtered ≥1.25 and ≥100 transactions
- **Visualization**: Bar charts, pie charts, stacked bars, histograms

---

## Strategic Recommendations

**1. Retention First**
- **Rescue "High Value At Risk"** immediately – highest revenue, declining engagement
- **Activate new customers within 30 days** – golden repurchase window
- Re-engage at **45 days** before churn

**2. Payment Optimization**
- **Optimize credit card checkout** – dominant method, growing share
- **Maintain *boleto*** – essential for unbanked segment

**3. Regional Expansion**
- **Defend Southeast** (SP, RJ, MG) – revenue backbone
- **Invest in specialization hubs** (PA, PE, CE) – partner with local sellers, build category champions
- **Test emerging frontiers** (AP, AC, RR) – low volume, nascent specialization

**4. Category-Led Personalization**
- Align campaigns with regional preferences (e.g., **health_beauty in PA/PE**, **watches_gifts in CE/DF**)
- Use LQ insights for **seller recruitment and inventory planning**

---

## Tech Stack

**Python** · **Pandas** · **NumPy** · **Matplotlib** · **Jupyter Notebook**

---

## How to Run

**1. Clone the repository**
```
git clone https://github.com/yourusername/olist-ecommerce-analysis.git
cd olist-ecommerce-analysis
```
**2. Create the virtual environment and activate**
 - Linux and MacOs
```
python3 -m venv vir_env
source vir_env/bin/activate
```
 - Windowns (CMD)
```
python3 -m venv vir_env
.\vir_env\Scripts\activate.bat
```

**3. Install dependencies**
```
pip install -r requirements.txt
```

**4. Download dataset from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) into `archive/` folder**

**5. Launch Jupyter**
   ```bash
   jupyter notebook
   ```

---

## License & Credits

**Dataset**: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) – CC BY-NC-SA 4.0  
**Authors**: André Sionek, Thomas Da Costa, Pedro Chaves (Olist)  
**Analysis**: Independent project for educational purposes.

---
