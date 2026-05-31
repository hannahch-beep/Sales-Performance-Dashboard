# 🚴 AdventureWorks Bike Shop: Global Sales Performance Analysis

---

## 📑 Executive Summary
AdventureWorks, a global manufacturing company specializing in cycling equipment and accessories, transitioned its operations monitoring from unorganized, static data tracking to dynamic business intelligence. Faced with a fragmented folder of raw CSV files spanning transactions, returns, products, customers, and territories, this project engineered a production-grade, multi-page Power BI Desktop dashboard. 

The interactive analytical solution consolidates data across global regions (North America, Europe, Pacific), tracks high-level corporate KPIs, surfaces underlying product return vectors, and visualizes changing customer purchasing behaviors over time.

### **Core Impact Metrics**
* **Total Revenue:** \$24.9M 
* **Total Profit:** \$10.5M 
* **Order Volume:** 25.2K total processed orders globally 
* **Operational Health:** Maintained a stable global **Return Rate of 2.2%** 
* **Customer Base:** 17.4K unique customers acquired, averaging **\$1,431 in revenue per customer**

---

## ⚠️ Problem Statement & Business Challenges
Before this implementation, the AdventureWorks executive team lacked unified, data-driven visibility into global performance. Key organizational pain points included:

* **Data Fragmentation:** Transactional data, customer profiles, product metrics, and regional territory mappings were siloed across independent, unlinked CSV files. 
* **Blind Spots in Profitability:** Leadership lacked an interactive mechanism to simulate price adjustments or measure hypothetical impacts on profits across specific product lines.
* **Obscured Return Vectors:** High-return products drained margin without real-time tracking to alert product teams.
* **Declining Value Trajectory:** While top-line monthly revenue trended upward dynamically through 2021 and 2022, the *Revenue per Customer* metric was experiencing a steady, long-term structural decline.

---

## 🛠️ Methodology & Technical Skills
To convert raw inputs into actionable insights, an enterprise data modeling approach was implemented directly within **Power BI Desktop**:
[Raw CSVs] ➡️ [Power Query ETL] ➡️ [Star Schema Data Model] ➡️ [DAX Engine] ➡️ [Dashboard]

### **1. Data Extraction & Transformation (ETL)**
* Connected Power BI to a localized folder directory containing historical CSV datasets.
* Utilized **Power Query** to clean messy fields, handle missing values, format data types, and normalize attributes across transactions, returns, products, and geographies.

### **2. Relational Data Modeling**
* Designed a high-performance **Star Schema** data model.
* Established explicit relationships between Fact tables (Sales, Returns) and Dimension tables (Customers, Products, Territories, and a custom Calendar matrix) ensuring clean filter propagation.

### **3. Advanced DAX Calculations & Parameterization**
* Engineered time-intelligence metrics to compare Month-over-Month (MoM) revenue, orders, and returns (e.g., displaying current monthly revenue of \$1.83M, a +3.31% increase over the previous month).
* Implemented **What-If Parameters** allowing stakeholders to adjust prices dynamically via a slider scale (e.g., simulating a 10% price adjustment) to view immediate, forecasted impacts on total profit vs. adjusted profit.

### **4. Dashboard Design**
* **Page 1: Executive KPI Summary:** High-level metrics cards, macro revenue trends, order distributions by category, and a Top 10 Products grid.
* **Page 2: Regional Performance Map:** A spatial Bing Maps visualization filtered by Europe, North America, and Pacific territories to track geographic market density.
* **Page 3: Product Detail & Forecasting:** Deep dive analytical space tracking actual metrics vs. targets alongside the predictive price adjustment parameter.
* **Page 4: Customer Details:** Tracking cohort breakdowns by occupation and income level, paired with a detailed view of high-value customers.

---

## 💡 Key Results & Data Insights

### **Product Performance & Operational Risk**
* **Volume Drivers:** Accessories dominated overall order counts with 17.0K orders, followed by Bikes with 13.9K orders, and Clothing with 7.0K orders. 
* **Top Revenue Products:** The *Water Bottle - 30 oz.* secured the top spot with 3,983 orders (\$39,755 in revenue), while the *Fender Set Mountain* generated an impressive \$87,041 from fewer units (1,975 orders).
* **Return Vulnerabilities:** While the overall corporate return rate sits at 2.2%, **Shorts** were flagged as the *Most Returned Product Type* across the entire inventory, necessitating a quality or sizing review.

* ### **Customer Cohort Analysis**
* **Demographic Sweet Spots:** The largest consumer purchasing base belongs to the **Average Income Level** category with 11.6K orders and **Professional** occupations with 7.9K orders. 
* **The Revenue Divergence:** Although global revenue expanded strongly up to mid-2022, the **Revenue per Customer** steadily decreased from a high near \$4K in 2020 down toward lower thresholds in 2022.
* This signals that growth is currently being driven by rapid, high-volume customer acquisition rather than deep, expanding individual account value.

---

## 🚀 Strategic Recommendations

1. **Address the Clothing Quality Loop:** Investigate the supply chain, fabric specs, and customer reviews for the **Shorts** product type. Because clothing represents a massive chunk of sales (13.9K orders), curbing its high return behavior will immediately boost net margins.
2. **Reverse the Declining Revenue-per-Customer Trend:** Since individual customer spend is dipping over time, implement automated cross-selling bundles at checkout. For example, prompt purchasers of high-margin *Bikes* to instantly bundle top-selling *Water Bottles* or *Sport-100 Helmets*.
3. **Targeted Micro-Campaigns for Professionals:** Leverage the demographic finding that *Professionals* and *Skilled Manual* workers make up the vast majority of your active community. Direct digital marketing budgets toward these high-indexing occupational groups to optimize customer acquisition costs (CAC).
4. **Deploy Dynamic Pricing Safely:** Utilize the built-in DAX predictive pricing simulator on low-volume, high-revenue products (such as specialized touring lines) to execute targeted 10% price increases, optimizing profits without disturbing highly elastic accessory categories.
