# 📦 Supply Chain & Logistics Analytics
## Inventory & Delivery Optimisation — DataCo Smart Supply Chain

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python) ![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikit-learn) ![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualisation-11557c) ![Seaborn](https://img.shields.io/badge/Seaborn-Statistical_Plots-4C72B0)

---

> *In today's hyper-competitive global marketplace, supply chain efficiency is no longer a back-office concern — it is a strategic differentiator. This project delivers a comprehensive end-to-end analysis of a multinational supply chain operation, surfacing the root causes of late deliveries, identifying the customer segments that drive the most value, and building a predictive model that enables proactive logistics intervention before a shipment becomes a problem.*

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Analysis Sections](#-analysis-sections)
- [Key Findings](#-key-findings)
- [Customer Segments](#-customer-segments)
- [Recommendations](#-recommendations)
- [Tools & Libraries](#-tools--libraries)
- [How to Run](#-how-to-run)

---

## 🎯 Overview

Supply chain disruption costs global businesses trillions annually — yet most organisations lack the analytical infrastructure to diagnose *why* deliveries fail, *which* customers are most affected, and *what* operational levers will generate the greatest return on improvement investment. This project addresses all three questions using a real-world multinational supply chain dataset spanning five global markets, 11 product departments, and over 180,000 order transactions from January 2015 to September 2017.

The analysis is structured to mirror the way a **senior supply chain analyst or operations business partner** would approach the problem — beginning with a broad diagnostic of the operational landscape, drilling into the specific drivers of late delivery, quantifying the financial consequences of logistics failures, segmenting the customer base by profitability and behaviour, and culminating in a machine learning model that scores individual orders for late delivery risk at the point of placement.

The output is not just a collection of charts — it is an **operational intelligence brief** that equips logistics leaders, category managers, and customer success teams with the evidence they need to make faster, smarter decisions.

---

## 📊 Dataset

| Attribute | Details |
|-----------|---------|
| **Source** | [DataCo Smart Supply Chain for Big Data Analysis — Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis) |
| **Records** | 180,519 order transactions |
| **Features** | 53 columns |
| **Date Range** | January 2015 – September 2017 |
| **Markets** | Africa · Europe · LATAM · Pacific Asia · USCA |
| **Departments** | Apparel · Book Shop · Fan Shop · Fitness · Footwear · Golf · Health & Beauty · Outdoors · Pet Shop · Technology · Discs Shop |
| **Shipping Modes** | First Class · Same Day · Second Class · Standard Class |
| **Order Regions** | 23 global regions |
| **Late Delivery Rate** | 54.8% — a critical operational challenge requiring immediate intervention |

---

## 🗂️ Project Structure

```
supply-chain-analytics/
│
├── supply_chain_analytics.ipynb       # Fully executed analysis notebook
├── DataCoSupplyChainDataset.csv       # Primary transaction dataset
│
├── charts/
│   ├── eda_overview.png               # Exploratory analysis dashboard
│   ├── late_delivery.png              # Late delivery drivers deep-dive
│   ├── profitability.png              # Revenue & margin intelligence
│   ├── customer_segments.png          # Customer segmentation dashboard
│   ├── model_kpis.png                 # Prediction model & KPI evaluation
│   └── inventory_ops.png              # Inventory & operational insights
│
└── README.md
```

---

## 🔍 Analysis Sections

### 1️⃣ Exploratory Data Analysis
A panoramic view of the supply chain landscape — delivery status distribution revealing the scale of the late delivery crisis, order volume share across all five global markets, monthly order trend analysis tracking volume patterns over 33 months, revenue performance ranked by department, shipping mode usage breakdown, and order profit distribution exposing the extent of margin compression across the business portfolio.

### 2️⃣ Late Delivery Deep-Dive
A forensic examination of the 54.8% late delivery rate — deconstructed by shipping mode (uncovering a counterintuitive premium mode underperformance), market geography (identifying LATAM and Pacific Asia as highest-risk zones), customer segment, regional hotspots across 23 global regions, a shipping delay distribution showing the full spread of early versus late arrivals, and a temporal trend analysis determining whether the problem is structural or episodic in nature.

### 3️⃣ Profitability & Revenue Analysis
Market-level total profit performance, department profit margin ranking (including identification of loss-making units), top-10 product categories by revenue, a discount rate versus profit ratio scatter analysis quantifying the margin destruction caused by excessive discounting, revenue trend lines across all five markets over time, and a combined profit/late-rate comparison by shipping mode to expose the hidden operational cost of delivery failures.

### 4️⃣ Customer Segmentation
K-Means clustering applied to customer behavioural and financial features — order frequency, total sales contribution, total profit generated, discount utilisation rate, and experienced late delivery rate — producing four distinct, actionable customer profiles that inform differentiated service level agreements, commercial policies, and account management strategies.

### 5️⃣ Late Delivery Prediction Model
Three machine learning classifiers — Logistic Regression, Random Forest, and Gradient Boosting — trained on order-level features including market, shipping mode, customer segment, department, region, scheduled shipping days, quantity, discount rate, and profit ratio. The model predicts late delivery risk at the point of order placement, enabling proactive logistics intervention, carrier rerouting, and early customer communication before a delay materialises.

### 6️⃣ Model Evaluation & Supply Chain KPIs
ROC curves across all three models, confusion matrix analysis for the best-performing model, feature importance rankings identifying the strongest predictors of late delivery, on-time delivery rate benchmarking by shipping mode against a 60% operational target, a market × shipping mode profit heatmap revealing the most and least efficient combinations, and a financial impact comparison quantifying the profit differential between late and on-time orders.

### 7️⃣ Inventory & Operational Insights
Average order quantity analysis by top product category to inform stock positioning decisions, benefit-per-order ranking by department to guide inventory prioritisation, payment type influence on delivery performance, a scheduled versus actual shipping days matrix exposing systemic scheduling misalignment, and a regional revenue ranking identifying the top 10 markets by total sales to guide investment allocation.

---

## 💡 Key Findings

### 🚨 The Late Delivery Crisis
> **54.8% of all orders arrive late.** This is not a marginal performance gap — it is a structural operational failure that is almost certainly driving customer churn, brand damage, and lost lifetime value at scale. Immediate diagnostic and remediation action is warranted.

### 📉 Premium Shipping Modes Underperform
First Class and Same Day shipping modes demonstrate *worse* on-time performance than Standard Class — a counterintuitive finding that points directly to a capacity or routing mismatch in premium logistics channels. Customers who are paying a premium for speed are, on average, receiving a worse experience than those on standard delivery. This represents both a service failure and a pricing integrity risk.

### 💸 Discounting is the Single Biggest Margin Erosion Driver
The correlation between discount rate and profit ratio is strongly negative (r = -0.85). Every additional percentage point of discount applied at the order level translates directly into bottom-line margin destruction. Without a structured discount governance framework — including approval thresholds and commercial rationale requirements — the pricing strategy is effectively uncontrolled.

### 🌎 Geographic Risk Concentration
LATAM and Pacific Asia combine above-average late delivery rates with significant order volumes, making them the highest-priority markets for logistics partnership review, carrier performance management, and operational investment. Europe and USCA represent the strongest profit-per-order markets and should be protected with enhanced SLA commitments.

### 💰 Late Deliveries Have a Measurable Financial Footprint
Orders that arrive late generate lower average profit than on-time orders — consistent with the hypothesis that delayed deliveries trigger customer complaints, partial refunds, discount concessions, and return processing costs that collectively compress the margin on affected transactions.

---

## 👥 Customer Segments

| Segment | Profile | Strategic Response |
|---------|---------|-------------------|
| 🏆 **Premium High-Value** | High order frequency · High total profit · Low discount dependency | Protect with SLA guarantees · Assign dedicated account management · Early access to new product lines |
| 📈 **Regular Steady** | Consistent volume · Healthy margins · Moderate engagement | Upsell complementary bundles · Reward with loyalty programme access · Encourage cross-category purchasing |
| 🏷️ **Budget Discount-Seekers** | High volume · Low margin due to discount dependency | Apply minimum order thresholds · Review discount eligibility criteria · Shift focus to value-add rather than price |
| ⚠️ **At-Risk Low-Margin** | Low order frequency · Minimal or negative profit contribution | Conduct full profitability audit · Reduce fulfilment priority · Introduce minimum spend policy |

---

## 📌 Recommendations

1. **🔧 Audit First Class and Same Day routing** — on-time performance below Standard Class is a routing or capacity issue requiring immediate carrier-level investigation
2. **📋 Implement a discount governance framework** — orders with a discount rate above 0.20 should require manager approval, given the demonstrated r = -0.85 correlation with profit ratio
3. **📦 Prioritise inventory for Western Europe and Central America** — these regions generate the highest revenue and currently experience above-average late delivery rates
4. **🤖 Deploy the late delivery prediction model at order placement** — flagging high-risk orders (predicted probability > 0.65) enables proactive rerouting before dispatch, reducing the late delivery rate without changes to the underlying logistics network
5. **📊 Establish a monthly supply chain performance dashboard** — tracking on-time delivery rate, average profit per order, discount rate by segment, and regional revenue concentration as standing board-level KPIs

---

## 🛠️ Tools & Libraries

| Library | Application |
|---------|------------|
| **Pandas** | Data ingestion, cleaning, transformation, and feature engineering across 180K+ records |
| **NumPy** | Numerical operations, delay calculations, and correlation analysis |
| **Matplotlib** | Time series plots, bar charts, scatter plots, and multi-panel dashboards |
| **Seaborn** | Heatmaps, distribution plots, and statistical visualisations |
| **Scikit-learn** | K-Means clustering · Logistic Regression · Random Forest · Gradient Boosting · StandardScaler · ROC/AUC evaluation |

---

## ▶️ How to Run

1. Clone the repository and navigate to the project folder
2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
3. Place `DataCoSupplyChainDataset.csv` in the same directory as the notebook
4. Open and run the notebook:
```bash
jupyter notebook supply_chain_analytics.ipynb
```

> ✅ All cells are pre-executed with embedded outputs. You can review the complete analysis without re-running a single cell.

---

*Part of a 12-project data analytics portfolio spanning HR analytics, financial forecasting, NLP, e-commerce, public health, and supply chain intelligence.*
