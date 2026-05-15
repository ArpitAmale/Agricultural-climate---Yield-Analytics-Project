## 🌾 Agricultural Climate & Yield Analytics Dashboard
 AWS · Snowflake · Power BI · End-to-End Data Pipeline

## 📌 Project Overview
This end-to-end data analytics project analyzes agricultural climate conditions and crop yield patterns across Karnataka, India. It combines cloud data storage (AWS S3), cloud data warehousing (Snowflake), and interactive BI reporting (Power BI) to deliver actionable insights across rainfall, temperature, humidity, and crop yield dimensions.
The project covers ~20 years of agricultural data (2000–2020) across 12+ crop types, 3 cropping seasons (Rabi, Kharif, Zaid), and 12+ districts of Karnataka.

# 🏗️ System Architecture
Data Lake: Raw agricultural CSV files hosted on AWS S3.
Data Warehouse: Snowflake (used for staging, cleaning, and storage).
Connectivity: Established secure access between AWS and Snowflake using IAM Roles and Storage Integrations.
Analytics Layer: Power BI connected via Snowflake connector to build relational models and DAX-driven KPIs.
# Data Flow:
Raw agricultural datasets uploaded to AWS S3
Snowflake COPY INTO ingests data from S3 via external stage
Data transformed using SQL views in Snowflake
Power BI connects to Snowflake via native connector
DAX measures power all KPI calculations in the report

# 📊 Dashboard Pages
# Page 1 — 🌧️ RainFall Analysis
Visual <img width="1663" height="955" alt="Screenshot 2026-05-15 205004" src="https://github.com/user-attachments/assets/4d729949-7f1f-4e71-bd08-2480aded69b3" />

Key Insight
By Year
Peak rainfall ~3.2K mm around 2010–2012 and 2018–2020
By Season
Rabi leads (3,105 mm), Kharif (3,097), Zaid (3,070)
By Crops
Paddy highest (3.5K); Arecanut & Cardamum (~3.3K)
By Location
Bangalore highest (3.8K); Mysuru lowest (2.9K)




# Page 2 — 🌡️ Temperature Analysis
Visual <img width="1658" height="959" alt="Screenshot 2026-05-15 204949" src="https://github.com/user-attachments/assets/58b92e65-982d-4dba-a056-0d547322bb19" />

Key Insight
By Year
Ranges 41°F–73°F; 2010 & 2019 peak at 72–73°F
By Season
Kharif & Zaid tied at 72°F; Rabi cooler at 61°F
By Crops
Ginger hottest (79°F); Cardamum coolest (55°F)
By Location
Kasaragodu hottest (35°C); Davangere coolest (27°C)

# Page 3 — 💧 Humidity Analysis
Visual <img width="1658" height="956" alt="Screenshot 2026-05-15 204932" src="https://github.com/user-attachments/assets/77acb5a8-497e-44e0-87a1-c320465d11e5" />

Key Insight
By Year
Narrow band ~55.41–55.81%; very stable over 20 years
By Season
Rabi slightly higher (55.60%); Kharif lowest (55.55%)
By Crops
Cotton highest (55.95%); Groundnut lowest (55.35%)
By Location
Davangere & Raichur highest (~55.68%); Bangalore lowest (55.00%)

 📌 Humidity is remarkably consistent (~55–56%) across all dimensions, indicating stable regional climate conditions in Karnataka.


# Page 4 — 🌱 Yield Analysis
Visual <img width="1658" height="953" alt="Screenshot 2026-05-15 204915" src="https://github.com/user-attachments/assets/643cd74d-cce3-49b0-99aa-7dd70ecd44a6" />

Key Insight
By Year
2010 peak yield (28.7K); 2015 strong (27.8K); 2020 at 27.2K
By Season
Rabi dominates (24.9K); Zaid (22.0K); Kharif lowest (20.2K)
By Crops
Cotton far ahead (51K); Coconut (34K); Cashew lowest (3K)
By Location
Kodagu highest (28.7K); Davangere lowest (11.8K)

# Key Business Insights
Cotton is the highest-yielding crop at 51K — over 1.5x the next crop (Coconut at 34K)
Rabi season consistently outperforms Kharif and Zaid in both rainfall and yield
Kodagu and Mysuru are the top-performing districts for agricultural output
Bangalore receives the highest average rainfall (3.8K mm) despite being an urban center
Humidity across Karnataka is exceptionally stable (~55–56%) year-round — predictable for farmers
Temperature varies significantly by crop (Ginger 79°F vs Cardamum 55°F), suggesting crop-specific microclimates



# ⚙️ How to Replicate
Upload raw CSV files to your AWS S3 bucket
In Snowflake, create an external stage pointing to S3 and run COPY INTO to load data
Run transformation SQL to create clean views
Open Power BI Desktop → Get Data → Snowflake → connect using your credentials
Refresh and explore the 4-page dashboard

# 📈 Future Improvements
Add slicers for crop type, district, and year range for deeper interactivity
Build a KPI summary page with card visuals for quick executive view
Integrate real-time data via Snowflake Streams + AWS Lambda
Add predictive yield modeling using Python / Azure ML
#👤 Author
Arpit
Data Analyst | AWS · Snowflake · Power BI · SQL · Python
If you found this project useful, please ⭐ star the repository!
Query Language
SQL
Snowflake transformations
BI Language
DAX
Calculated measures & KPIs
