
---

# 📊 Amazon Consumer Behavior: An Experimental Big Data Study

## 🎯 Executive Summary

Does the first review on a product determine its destiny? This project investigates the **"First Impression Bias"** in e-commerce using the **Amazon Fine Food Reviews** dataset (~568k reviews). Unlike standard sentiment analysis, this study employs a rigorous **experimental design** to test whether early ratings statistically influence long-term sales velocity and product quality perception.

---

## 🛠️ Technical Stack & Data Engineering

To handle a dataset of over half a million records across 13 years (1999–2012), I utilized **distributed computing** to ensure scalability and performance.

* **Engine:** `PySpark` (Spark SQL & DataFrames) for high-performance distributed processing.
* **Environment:** Large-scale data ingestion and transformation of 74,000 unique products.
* **Feature Engineering:** * Time-series windowing to isolate the "First Rating" for every product.
* Aggregation of "Review Velocity" as a proxy for sales performance.
* Development of "Quality Stability" metrics using long-term rating means.



---

## 📈 Statistical Rigor (The "Science" in Data Science)

I moved beyond simple averages, applying robust statistical tests to ensure results weren't due to random noise.

### 1. Hypothesis Testing

| Hypothesis | Statistical Test | Business Rationale |
| --- | --- | --- |
| **H1: First Rating vs. Sales** | Mann-Whitney U | Non-normal distribution of sales data required a rank-based test. |
| **H2: Predictability of Quality** | Spearman’s Rank Correlation | Measuring the strength and direction of the relationship between early and late ratings. |
| **H3: The "Controversy Effect"** | Kruskal-Wallis Test | Testing if 3-star (polarizing) products generate more engagement than 5-star products. |

### 2. Key Findings

* **The Myth of First Impressions:**  for the correlation between first rating and sales volume. **Result:** The first rating is *not* a statistically significant predictor of long-term success.
* **The Controversy Effect:** 3-star products showed significantly higher engagement (review velocity) than 1 or 5-star products, supporting the behavioral theory that "middle-ground" or "controversial" products trigger more consumer discussion.

---

## 💼 Business & Strategic Insights

Translating data into actionable strategy:

* **Risk Mitigation:** Data proves that a single "bad" first review is not a death sentence for a product. Brands should focus on long-term quality rather than panicking over initial negative feedback.
* **Engagement Strategy:** The high velocity of 3-star products suggests that "mixed reviews" can actually keep a product relevant in recommendation algorithms by increasing activity.
* **Quality Signaling:** Early ratings are "weak signals." Real product quality reveals itself only after a critical mass of reviews is reached.

---

## 📁 Project Structure

* `Data.ipynb`: The heavy lifting—PySpark data cleaning, aggregation, and feature scaling.
* `Project Report.pdf`: A comprehensive 9-page breakdown of the experimental methodology, statistical proofs, and defense of the findings.
* `Visualizations`: Distributed plots showing the distribution of ratings and engagement metrics.

---

## 👤 Author

**Ahmed Salama**
*Data Scientist*

[LinkedIn](https://www.linkedin.com/in/ahmedsalamaa00/) | [GitHub](https://github.com/ahmedsalama00) | [Portfolio](https://ahmedsalama00.github.io/Ahmed)

---

> **Note:** This project was designed as a pilot study to demonstrate the application of experimental design and non-parametric statistics to large-scale observational data.
