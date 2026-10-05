# India-s-Export-To-African-Countries

## 📌 Project Overview

This project focuses on analyzing **India's export trade to African countries** using Python and Exploratory Data Analysis (EDA).

The analysis explores export patterns across **countries, commodities, quantities, export values, subregions, and years** to identify important trends, market concentration, relationships, and potential business opportunities.

---

## 🎯 Objective

The main objectives of this project are to:

* Clean and preprocess a large export-trade dataset.
* Analyze India's export performance across African countries.
* Identify major export destination markets.
* Study the relationship between export quantity and export value.
* Analyze export trends over different years.
* Identify variations across countries, subregions, and commodities.
* Detect missing values, inconsistencies, and outliers.
* Generate meaningful business insights and recommendations.

---

## 📊 Dataset

The original dataset contains:

* **2,826,373 records**
* **15 original columns**
* Data covering the period **2015–2025**
* **61 country names**
* Countries from **Northern Africa and Sub-Saharan Africa**

### Original Columns

```text
id
date
country_name
alpha_3_code
country_code
region_name
region_code
subregion_name
subregion_code
hs_code
commodity
unit
value_qt
value_rs
value_dl
```

### Important Variables

| Column           | Description                 |
| ---------------- | --------------------------- |
| `date`           | Export transaction date     |
| `country_name`   | African destination country |
| `commodity`      | Exported commodity          |
| `unit`           | Measurement unit            |
| `value_qt`       | Export quantity             |
| `value_rs`       | Export value in INR         |
| `value_dl`       | Export value in USD         |
| `subregion_name` | African subregion           |

---

## 🧹 Data Preprocessing

The following preprocessing techniques were applied:

* Converted the date column into the appropriate datetime format.
* Renamed `alpha_3_code` to `iso_code`.
* Checked for duplicate records.
* Checked ID uniqueness.
* Handled missing values.
* Filled missing units using commodity-wise mode.
* Filled missing quantities using grouped and overall median values.
* Filled missing INR values using grouped median values.
* Standardized inconsistent measurement units.
* Cleaned and standardized categorical text values.
* Standardized country names.
* Investigated suspicious zero USD values.
* Reconstructed relevant USD values using year-wise exchange-rate relationships.
* Detected outliers using the **IQR method**.

Outliers were **flagged rather than automatically removed** to avoid losing potentially important trade transactions.

---

## ⚙️ Feature Engineering

New variables were created to support deeper analysis:

```text
year
month
month_name
exchange_rate
export_value_category
quantity_category
value_dl_outlier
```

These derived variables were used for analyzing yearly trends, export categories, transaction patterns, and outliers.

---

## 📈 Exploratory Data Analysis

The project includes several visual analyses, including:

* Export value distribution by country and region.
* Export quantity vs. export value.
* Quantity category vs. export value category.
* Export value composition by commodity and region.
* Correlation analysis.
* Top 10 African countries by export value.
* Export value category distribution.
* Subregion-wise yearly analysis.
* Export value share of leading countries.
* Top 5 countries by yearly export value.
* Pareto analysis of export value by country.
* Geographic visualization of export values.
* Year-over-Year export growth analysis.
* Top 5 countries vs. other markets.

---

## 🔍 Key Insights

### 1. Strong Market Concentration

India's export value is concentrated in a relatively small number of African destination markets.

### 2. Country-Level Differences

African countries show significant differences in their contribution to India's overall export value.

### 3. Variation Over Time

Export performance changes across different years, highlighting periods of growth and decline.

### 4. Quantity–Value Relationship

Export quantity shows a strong positive relationship with export value, although commodity type and measurement units also influence this relationship.

### 5. Geographical Variation

Export activity differs between **Northern Africa and Sub-Saharan Africa**, indicating that African markets should not be treated as a single homogeneous market.

### 6. Diverse Export Portfolio

India exports a wide range of commodities to African markets, creating opportunities for product-level analysis and expansion.

### 7. Significant Transaction Variations

Some transactions have considerably higher quantities or values than typical observations, making outlier analysis important.

### 8. Importance of Data Quality

Missing values, inconsistent units, and suspicious zero values demonstrate the importance of proper data preprocessing before analysis.

---

## 💡 Recommendations

* Strengthen relationships with high-value African markets.
* Identify emerging markets with increasing export potential.
* Diversify into underrepresented African markets.
* Focus on high-performing commodities.
* Investigate high-volume but relatively low-value transactions.
* Explore low-volume, high-value export opportunities.
* Monitor year-over-year export growth.
* Improve data-quality and validation processes.
* Continuously monitor unusual or extreme transactions.
* Develop an ongoing export intelligence dashboard for decision-making.

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Plotly**
* **Jupyter Notebook**
* **Exploratory Data Analysis**
* **Data Cleaning & Preprocessing**
* **Data Visualization**

---

## 📁 Project Structure

```text
India-Export-Trade-Africa/
│
├── DA_51_MainProject.ipynb
│
├── Cleaned_Dataset_Sample.csv
│
├── README.md
│
└── images/
    └── project_visualizations/
```

---

## 📦 Dataset Availability

The complete analysis was performed using the **full dataset containing 2,826,373 records**.

Due to memory/storage limitations when working with large datasets on GitHub, only a **100,000-row sample of the cleaned dataset and uncleaned dataset** is included in this repository.

The sample is provided to demonstrate the dataset structure and preprocessing results, while the analysis and findings were generated using the complete dataset.

---

## 📌 Conclusion

This project provides an analytical view of India's export trade to African countries using Python. The analysis identifies key markets, export trends, quantity-value relationships, commodity patterns, and areas for market diversification. It also demonstrates the importance of data preprocessing and quality management when working with large real-world datasets.

---

## 👩‍💻 Project By

**Aleena Mathew**

*Data Analytics Project – Python*
