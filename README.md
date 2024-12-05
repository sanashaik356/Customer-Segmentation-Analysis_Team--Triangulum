# Customer-Segmentation-Analysis_Team--Triangulum

### Objectives
This dashboard aims to provide actionable insights into customer segmentation, enabling the identification of trends, sales performance, and key customer demographics. Monitor trends and KPIs to support strategic decision-making

### Data Preparation
Our internal sales database (API-accessible) provided detailed transaction records including customer IDs, products, sales regions (country and state), dates, and quantities. Power Query cleaned and transformed the raw data. This included handling missing regional data (imputed using regional averages and sales trends), ensuring data type consistency, and addressing outliers (via box plots and Z-score analysis). Calculated columns for year-over-year growth and customer risk scores were added

### Data Modeling
The data model consists of interconnected tables: DimTable, Orders, People, and Returns. These relationships enable seamless analysis of trends, performance, and customer behavior across dimensions.

Developed critical DAX measures for enhanced analysis: TotalSales = SUM(Orders[Sales]) Sales Growth % = DIVIDE([TotalSales] - [SPLY Sales],[SPLY Sales],0) * 100 Purchase Frequency = DIVIDE([Total Orders], [Years Active], 0)

### Visualization Design
Top Panel: Key Performance Indicators (KPIs) for Total Sales, YoY Growth, and Average Sales per Customer. Left Sidebar: Filters for Region, Time Period, and Product Categories to allow customized views. Slicers: Enable filtering by Region, Time, and Customer Segment for tailored insights. Drill-throughs: Allow users to deep dive into specific customer or product details.

### Insights and Value Addition
Regional Performance: Identified that Region X sales dropped by 10%, prompting targeted marketing efforts. Time-Based Insights: Uncovered a significant YoY sales growth of 20% in the Central region, enabling resource allocation adjustments. Integrate customer feedback data to align products with customer preferences. Incorporate external datasets, such as market trends, to benchmark performance against competitors.
