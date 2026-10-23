# 🛒 Blinkit Sales Analysis (Python)

An exploratory data analysis of Blinkit's sales performance, customer ratings, and outlet distribution using **Python, Pandas, Matplotlib, and Seaborn** in a Jupyter Notebook.

---

## 📌 Business Requirement

Conduct a comprehensive analysis of Blinkit's sales performance, customer satisfaction, and inventory distribution to identify key insights and opportunities for optimization using KPIs and visualizations.

---

## 📂 Repository Structure

```
├── Blinkit_Analysis_in_Python.ipynb   # Main analysis notebook
├── Blinkit_Analysis.pptx              # Project brief: business requirements, KPIs & chart specs
├── blinkit_data.csv                   # Dataset (8,523 rows x 12 columns)
└── README.md
```

---

## 📊 Dataset Overview

The dataset contains **8,523 records** and **12 columns**:

| Column | Description |
|---|---|
| `Item Fat Content` | Fat category of the item (Low Fat / Regular) |
| `Item Identifier` | Unique product ID |
| `Item Type` | Product category (e.g., Snack Foods, Soft Drinks) |
| `Outlet Establishment Year` | Year the outlet was established |
| `Outlet Identifier` | Unique outlet ID |
| `Outlet Location Type` | Location tier of the outlet |
| `Outlet Size` | Size of the outlet |
| `Outlet Type` | Type of outlet |
| `Item Visibility` | Share of display area given to the item |
| `Item Weight` | Weight of the item |
| `Sales` | Revenue generated |
| `Rating` | Customer rating |

---

## 🧹 Data Cleaning

The `Item Fat Content` column had inconsistent labels (`Regular`, `Low Fat`, `low fat`, `LF`, `reg`). These were standardized to just two categories:

```python
df['Item Fat Content'] = df['Item Fat Content'].replace({
    'LF': 'Low Fat',
    'low fat': 'Low Fat',
    'reg': 'Regular'
})
```

---

## 📈 KPIs

| KPI | Description | Value |
|---|---|---|
| **Total Sales** | Overall revenue from all items sold | $1,201,681 |
| **Average Sales** | Average revenue per sale | $141 |
| **Number of Items** | Total count of items sold | 8,523 |
| **Average Rating** | Average customer rating | 4.0 |

---

## 📉 Visualizations

| # | Chart | Type | Objective |
|---|---|---|---|
| 1 | Sales by Fat Content | Pie / Donut | Analyze the impact of fat content on total sales |
| 2 | Total Sales by Item Type | Bar Chart | Identify top and bottom performing item categories |
| 3 | Outlet Tier by Item Fat Content | Grouped Bar Chart | Compare sales across outlet location tiers, split by fat content |
| 4 | Sales by Outlet Establishment Year | Line Chart | See how outlet age influences total sales |
| 5 | Sales by Outlet Size | Pie Chart | Analyze the relationship between outlet size and sales |
| 6 | Sales by Outlet Location Type | Horizontal Bar Chart | Assess the geographic distribution of sales |

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** – data manipulation
- **NumPy** – numerical operations
- **Matplotlib** – charts
- **Seaborn** – statistical visualization
- **Jupyter Notebook** – development environment

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Launch the notebook

```bash
jupyter notebook Blinkit_Analysis_in_Python.ipynb
```

> Make sure `blinkit_data.csv` is in the same folder as the notebook.

---

## 💡 Key Takeaways

- Standardizing categorical labels was essential for accurate fat-content analysis.
- Sales were analyzed across product categories, outlet sizes, location tiers, and establishment years.
- Outlets established around 2011 show a sharp dip in total sales compared with other years.

---

## 🔮 Future Improvements

- Build an interactive dashboard in Power BI or Streamlit
- Handle missing values in `Item Weight` and `Outlet Size`
- Add correlation analysis and predictive modeling for sales

