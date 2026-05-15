## 🌾Agricultural Climate & Yield Analytics Dashboard
AWS S3 | Snowflake | Power BI | Data Engineering & Analysis
## 📌 Project Overview
This project provides a comprehensive analysis of agricultural patterns in Karnataka, India, spanning two decades (2000–2020). By integrating a full cloud data stack, I transformed raw datasets into an interactive 4-page intelligence suite that correlates Rainfall, Temperature, and Humidity with Crop Yields.
The goal was to identify which environmental conditions drive the highest productivity for 12+ different crop types across various districts.
## 🏗️ System Architecture
Data Lake: Raw agricultural CSV files hosted on AWS S3.

Data Warehouse: Snowflake (used for staging, cleaning, and storage).

Connectivity: Established secure access between AWS and Snowflake using IAM Roles and Storage Integrations.

Analytics Layer: Power BI connected via Snowflake connector to build relational models and DAX-driven KPIs.

## 📊 Dashboard Insights
# 1. 🌧️ Rainfall Analysis
Peak Years: Noted high precipitation cycles around 2010 and 2020 (Avg. 3.2K mm).

Regional Winner: Bangalore recorded the highest average rainfall (3.8K mm).

Seasonal Lead: Rabi season slightly edges out Kharif in total water volume.

# 2. 🌡️ Temperature Analysis
Outlier Management: Cleaned and filtered historical data to ensure a realistic range of 27°C – 35°C across locations.

Crop Specifics: Ginger thrives in higher temperature bands (avg. 79°F in dataset records), while Cardamum prefers cooler climates.

# 3. 💧 Humidity Analysis
Climate Stability: Identified a remarkably stable humidity band in Karnataka, hovering between 55% and 56% regardless of the year or season.

Top Districts: Davangere and Raichur maintain the highest moisture levels.

# 4. 🌱 Yield Analysis
Performance Leader: Cotton is the highest-yielding crop at 51K, followed by Coconut at 34K.

Top District: Kodagu leads in overall agricultural output efficiency.


## 🔑 Key Business Insights
Cotton is the highest-yielding crop at 51K — over 1.5x the next crop (Coconut at 34K)

Rabi season consistently outperforms Kharif and Zaid in both rainfall and yield

Kodagu and Mysuru are the top-performing districts for agricultural output

Bangalore receives the highest average rainfall (3.8K mm) despite being an urban center

Humidity across Karnataka is exceptionally stable (~55–56%) year-round — predictable for farmers

Temperature varies significantly by crop (Ginger 79°F vs Cardamum 55°F), suggesting crop-specific microclimates




## ⚙️ How to Replicate

Upload raw CSV files to your AWS S3 bucket

In Snowflake, create an external stage pointing to S3 and run COPY INTO to load data

Run transformation SQL to create clean views

Open Power BI Desktop → Get Data → Snowflake → connect using your credentials

Refresh and explore the 4-page dashboard

## 📈 Future Improvements
Add slicers for crop type, district, and year range for deeper interactivity

Build a KPI summary page with card visuals for quick executive view

Integrate real-time data via Snowflake Streams + AWS Lambda

Add predictive yield modeling using Python / Azure ML



## 👤 Author
Arpit Amale

Aspiring Data Analyst

LinkedIn: www.linkedin.com/in/ arpit-amale-89796a27b

GitHub: https://github.com/ArpitAmale Email: arpitamale100@gmail.com
