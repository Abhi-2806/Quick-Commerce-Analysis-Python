
# 🧾 Quick Commerce Analysis – Retail Inventory & Sales

_Cleaning, standardizing, and optimizing quick-commerce order data to support reliable downstream analytics and operational reporting using Python, Pandas, and NumPy._

---

## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>

This project cleans and preprocesses quick-commerce order and delivery records to prepare high-quality data for operational analytics and performance reporting. A complete data preparation pipeline was built using Python for data transformation, Pandas and NumPy for missing value imputation and type casting. Used Matplotlib, Seaborn & Plotly for visualization.

---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Effective inventory and sales management are critical in the retail sector. This project aims to:
- Vendor Management & Customer Experience
- Supply Chain & Inventory Management
- Finance & Fraud/Risk Management- Extreme high-value transactions distort revenue projections
- Identify underperforming brands needing pricing or promotional adjustments
- Future Expansion Probabilty

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- CSV files located in `/data/` folder (quick_commerce_data_raw.csv)


---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- Python (Pandas, NumPy, )
- Python (Visualization - Matplotlib, Seaborn, Plotly)
- GitHub

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
vendor-performance-analysis/
│
├── README.md
├── .gitignore
├── requirements.txt
├── Quick-commerce-Analysis-Report.pdf
│
├── notebooks/                  # Jupyter notebooks
│   ├── exploratory_data_analysis.ipynb
│   ├── Quick-Commerce-Analysis.ipynb
│
│
├── dashboard/                  # Jupyter notebooks
│   └── Q-Commerce.ipynb 
    └── images (images folder)

```

---
<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

- Removed Dataset with:
  - Null City value
  - Fillup empty records 

- Created summary statistics 
- Converted data types, handled outliers, round-off float values

---
<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

**Empty records Detected:**
- City column had empty records- irreplaceable hence removed (52,000 records)
- Null Item_count records- Replaced using Mode (33,228 records)
- Null Customer_Rating records- Replaced using Mean (44,575 records)
- Null Delivery_Partner_Rating records- Replaced using Mean (98,694 records)

**Outliers Identified:**
- Ignoring Unique Order_ID value
- Filtering Order_Value <= 2500

**Changed Data-type:**
-  int To String type
-  float to int type

---
<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

1. **Platform with highest Total_Revenue**: Swiggy Instamart  (INR-76407756)

2. **Platform with highest Average_Order_Value**: Swiggy Instamart  (INR-644.92)

3. **customer rating across platforms**: Blinkit (4/5)

4. **'Delivery time' affecting the 'delivery partner ratings'**: Inverse Relation

5. **Expansion based on performance**:
   - Blinkit: Amritsar, Chennai, Gurgaon, Kolkata, Pune
   - Zepto: Bengluru

6. **most popular Product Category on swiggy instamart, for the people of age between 30-40, in mumbai?**:
   - Highest: Dairy = 368
   - Lowest: Beverages = 299
7. **Impact of discount on total_revenue**: Discounts are reducing overall revenue rather than driving larger order sizes.

8. **Platform with best operational efficiency(Delivery Time vs Order Volume)**: Zepto (Efficiency Score- 0.564)

---
<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

- KPI Dashboard shows:
  - Total Orders
  - Total Revenue
  - Avg_Delivery_Time
  - Avg_Rating

![Quick-Commerce-Analysis-Dashboard]([KPI.png](https://github.com/Abhi-2806/Quick-Commerce-Analysis-Python/blob/e8298518fff7439fe299e0ecfdd8a403971f1071/images/KPI.png))

![Quick-Commerce-Analysis-Dashboard]([KPI_Dashboard.png](https://github.com/Abhi-2806/Quick-Commerce-Analysis-Python/blob/e8298518fff7439fe299e0ecfdd8a403971f1071/images/KPI_Dashboard.png))

---
<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone the repository:
```bash
git clone https://github.com/yourusername/vendor-performance-analysis.git
```
3. Load the CSVs and ingest into database:
```bash
python scripts/ingestion_db.py
```
4. Create vendor summary table:
```bash
python scripts/get_vendor_summary.py
```
5. Open and run notebooks:
   - `notebooks/exploratory_data_analysis.ipynb`
   - `notebooks/vendor_performance_analysis.ipynb`
6. Open Power BI Dashboard:
   - `dashboard/vendor_performance_dashboard.pbix`

---
<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- Revamp Discounting Strategy to Protect Margins & Boost AOV (Profit Margin & Revenue)
- Prioritize Hub Expansion in High-Performing Tier-1 & Tier-2 Clusters
- Curate Localized Inventory by Demographic Demand (Revenue & Growth)
- Standardize Delivery time Thresholds to Preserve Customer Ratings & experience
- Improve operational efficiency for underperforming platforms

---
<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Abhishek Pathak**  
Data Analyst  
📧 Email: wayoflife507@gmail.com  

🔗 Contact No.- 6307017308

🔗 [LinkedIn](https://www.linkedin.com/in/abhishekpathak2806/)  
