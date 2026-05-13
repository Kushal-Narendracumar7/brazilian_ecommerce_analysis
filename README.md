# 🛒 E-Commerce Sales Analysis (2016–2018)

Exploratory Data Analysis on the [Olist Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) covering 100,000+ orders across 2016–2018. The project follows an end-to-end pipeline — from raw data preprocessing to statistical analysis and interactive visualizations.

---

## 📌 Key Findings

- **Delayed deliveries hurt ratings** — Orders delivered after the estimated date scored significantly lower on customer reviews. Confirmed statistically using the Mann-Whitney U test (p < 0.05).
- **Health & Beauty dominates revenue** — Consistently the top revenue-generating product category across all years.
- **São Paulo leads demand** — São Paulo was the top ordering city every year in the dataset.
- **Freight cost scales with price** — After log transformation, a clear positive correlation exists between product price and freight value.

---

## 📁 Project Structure

```
├── datasets/                        # Raw and preprocessed CSV files
├── preprocessing.ipynb              # Data cleaning, merging, feature engineering
├── analysis.ipynb                   # Statistical EDA and hypothesis testing
├── visualization.ipynb              # Interactive dashboards and business insights
└── README.md
```

---

## 🔄 Pipeline Overview

### 1. `preprocessing.ipynb`
- Merged 7 raw datasets: orders, order items, products, customers, sellers, reviews, geolocation
- Translated product category names from Portuguese to English
- Engineered key feature: `is_delayed` (actual delivery date > estimated delivery date)
- Exported clean dataset to `preprocessed_dataset.csv`

### 2. `analysis.ipynb`
- Correlation heatmap across all numeric features
- Scatter plots for price vs. freight value (raw + log-transformed)
- Boxplot and Mann-Whitney U test to validate delay impact on review scores
- Computed `delay_days` as a timedelta feature

### 3. `visualization.ipynb`
- Top 10 products by total revenue
- Year-wise sales trend (2016–2018)
- Top ordering city per year
- Best-selling product per year
- Most & least reviewed products (side-by-side comparison)
- Most delayed products and cities (treemap)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas | Data wrangling and merging |
| NumPy | Numerical operations and log transforms |
| Seaborn | Statistical plots |
| Plotly | Interactive dashboards |
| Scikit-learn | Label encoding |
| SciPy | Mann-Whitney U hypothesis test |

---

## 📊 Sample Visualizations
![Top Revenue Products](Brazilian_ecommerce\images\most_delayed_cities.png)
![Yearly Sales](Brazilian_ecommerce\images\yearly_sales.png)
![Most Delayed Cities](Brazilian_ecommerce\images\yearly_sales.)x



---

## 🚀 How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/Kushal-Narendracumar7/brazilian_ecommerce_analysis.git
   cd brazilian_ecommerce_analysis
   ```

2. Install dependencies
   ```bash
   pip install pandas numpy seaborn plotly scikit-learn scipy matplotlib
   ```

3. Run notebooks in order:
   - `preprocessing.ipynb` → generates `preprocessed_dataset.csv`
   - `analysis.ipynb`
   - `visualization.ipynb`

---

## 📂 Dataset

**Source:** [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) on Kaggle

Download and place all CSVs inside a `datasets/` folder before running.

---

## 👤 Author

**Your Name**
[LinkedIn](https://www.linkedin.com/in/kushal-narendracumar-08633a24a/) • [GitHub](https://github.com/Kushal-Narendracumar7)
