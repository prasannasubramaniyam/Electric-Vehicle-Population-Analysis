# Electric-Vehicle-Population-Analysis

Electric Vehicle Population Analysis: Regional Adoption and Trend Insights (2000–2026)

Introduction
The automotive industry is undergoing a significant shift toward sustainability, with electric vehicles (EVs) at the forefront of this transformation. This project analyzes electric vehicle registration data to evaluate adoption trends, regional preferences, and the growth of clean energy transportation. The dataset focuses on the population of EVs in the State of Washington, providing a detailed look at how different regions and manufacturers contribute to the green mobility landscape.
The dataset was sourced from the Government EV Registration Dataset (Electric Vehicle Population).
Project Objective
To analyze the distribution and population of electric vehicles across different regions.
To understand trends in EV usage and adoption over time.
To support decision-making for governments, researchers, and companies regarding clean energy and transportation infrastructure.
To evaluate the performance and market presence of various EV manufacturers.
To identify the impact of legislative districts and utilities on EV adoption.
Dataset Description
Dataset Name: Electric Vehicle Population Data.
Time Period: 2000 – 2026 (Updated as of 2026).
Total Records: 47,914 rows.
Total Columns: 16.
Geographic Coverage: State of Washington, USA.
Data Source: Government EV Registration Dataset.
The dataset includes technical details like VIN, Electric Range, and Vehicle Type, alongside geographic markers such as County, City, and Legislative District.

Tools & Technologies Used
Python: Primary language for data processing and analysis.
Pandas: Data manipulation and structure analysis.
NumPy: Numerical computations.
Matplotlib & Seaborn: Generation of statistical visualizations.
Google Colab: Cloud-based environment for execution and documentation.


STAGE 1: Data Preparation & Cleaning 
Dataset Structure Analysis
df.shape confirmed 47,914 rows and 16 columns.
df.info() revealed a mix of objects (categorical), int64, and float64 (numerical) types.
df.describe() showed the average Model Year is approximately 2022, indicating a very recent and rapidly growing dataset.


STAGE 2: Data Preparation & Cleaning 
Dataset Overview
The dataset consists of 47,914 rows and 16 columns.
Statistical summaries indicate an average electric range of approximately 39.9 miles, though this value varies significantly (Standard Deviation ~78.5) across different vehicle types.
Model years range from 2000 to 2026, showing the longevity and future projections of the data.
Missing Value Analysis
Initial checks identified missing values in key geographic and technical columns.
Findings: Columns such as 'County', 'City', and 'Electric Range' contained null values that required attention to maintain data integrity.
Data Cleaning & Imputation
Geographic Imputation: Missing values in the 'County' and 'City' columns were handled by imputing the mode (most frequent value) of each respective column.
Verification: Post-imputation checks confirmed that the null count for 'County' and 'City' was reduced to zero.
Data Transformation
The 'Electric Range' column was examined for statistical consistency, revealing that many vehicles (likely newer long-range BEVs or certain PHEVs) have specific range markers that define their CAFV eligibility.
Categorical features like 'Make' and 'Model' were prepared for grouping to identify market leaders.


 STAGE 3: EDA, Statistical Analysis & Visualizations 
1. Exploratory Data Analysis (EDA) & Market Leadership
The analysis identifies key drivers in the electric vehicle ecosystem by grouping data across three primary dimensions: Manufacturer (Make), Model Year, and Geography (County/City).
Market Leaders by Manufacturer: The analysis distinguishes between established players and emerging brands.
Top Manufacturer: Tesla emerges as a significant leader in registration volume.
High-Range Performance: Manufacturers like Tesla and Nissan (with the LEAF) often lead in vehicles that meet Clean Alternative Fuel Vehicle (CAFV) eligibility.
Adoption Growth (Model Year): Grouping by Model Year reveals that the majority of current registrations are for vehicles produced between 2021 and 2025, indicating a recent and rapid acceleration in adoption.
Geographic Hubs: Analysis by County and City identifies King County (specifically cities like Seattle and Kent) and Snohomish County (Bothell, Marysville) as primary hubs for EV density.
2. Statistical Profiling
Statistical checks were applied to numerical columns such as Model Year and Electric Range to understand the reliability and distribution of the data.
Central Tendency & Dispersion:
Electric Range: The mean range is approximately 39.9 miles. However, a high standard deviation (~78.5) and a median of 0.0 indicate a heavily skewed distribution where many newer models do not yet have their range specified or are short-range city vehicles.
Model Year: A mean of 2022 and a maximum of 2026 highlight that the dataset is heavily weighted toward modern, current-generation vehicles.
CAFV Eligibility: The analysis shows a significant portion of the population is "Clean Alternative Fuel Vehicle Eligible," though a distinct segment is categorized as "Not eligible due to low battery range," highlighting the diverse range of available technologies (BEV vs. PHEV).
3. Data Visualization Insights
The following visualizations were planned or executed to satisfy the project objectives:
Plot Type
Visualization Focus
Interpretation/Insight
Bar Plot
Manufacturer (Make) Distribution
Ranks manufacturers by volume. Tesla and Nissan are primary market movers in the state.
Histogram
Electric Range Distribution
Shows a multimodal distribution. Most vehicles cluster at lower ranges (PHEVs), with a secondary peak for long-range Battery Electric Vehicles (BEVs).
Box Plot
Range by Manufacturer
Highlights that while some manufacturers (like Tesla) have high median ranges, others have a narrow, specific range for city-focused models.
Count Plot
Model Year Trends
Visually proves the exponential growth of the EV population from 2020 to 2026.
Scatter Plot
Range vs. Model Year
Shows how battery technology has improved over time, with maximum ranges increasing in newer models.
Bar Plot
Distribution by County
Satisfies the objective of identifying geographic trends; confirms high adoption in urban/tech centers like King County.

  
STAGE 4: Documentation, Insights & Presentation 
Summary of Findings
Total Market Reach: The dataset tracks electric vehicle registrations across the State of Washington, encompassing 47,914 individual vehicle records with 16 detailed attributes. 
Massive Manufacturer Concentration: Tesla dominates the digital registration landscape, frequently appearing as the top manufacturer, followed by established players like Nissan and Jeep.
Consistent Growth Trend: EV adoption has shown a continuous upward climb, with the average model year being 2022 and the data extending through 2026 projections, indicating no signs of stagnation.
Range Anomalies: While many vehicles are listed with a 0.0-mile electric range (likely due to reporting lags for new models), high-performance outliers reach up to 337 miles, representing the top tier of battery technology.
Adoption Efficiency: A significant portion of the fleet is already categorized as "Clean Alternative Fuel Vehicle Eligible," though newer plug-in hybrids are sometimes flagged for low battery range.
Data Reliability: Near 100% reporting consistency was observed; initial missing values in geographic fields like 'County' and 'City' were successfully imputed, ensuring a complete dataset for analysis.

Key Insights
Market Monopoly: A handful of manufacturers (led by Tesla) control a vast majority of the active EV population, creating a significant competitive gap for smaller or newer brands.
The Rise of Modernity: The distribution is heavily skewed toward newer models (2021–2025), proving that the current period is the most transformative for EV adoption in the region.
Infrastructure Correlation: High registration volumes correlate strongly with specific utilities (e.g., Puget Sound Energy Inc and City of Seattle), suggesting that utility-supported infrastructure is a primary driver of adoption.
Untapped Potential: Many vehicles are currently registered in legislative districts with lower adoption rates, representing a massive opportunity for increasing state-wide clean energy coverage through targeted incentives.




Descriptive Analysis
Total Records: 47,914
Primary Geographic Focus: State of Washington (e.g., Yakima, King, Snohomish Counties)
Time Period: 2000 – 2026
Mean Electric Range: ~39.9 miles (skewed by many 0-range entries and PHEVs)
Max Electric Range: 337 miles
Primary Metrics: Model Year, Make, Electric Range, CAFV Eligibility, and Legislative District.


Diagnostic Analysis — Why Did It Happen?
Why Tesla Dominates: As a pioneer in the dedicated EV space with an aggressive supercharger network, Tesla's massive registration base is a direct result of its brand legacy and infrastructure maturity.
Why Volume Correlates with Geography: The presence of EVs in counties like King is tied to urban density and the availability of charging stations provided by local utilities.
Why Range is Independent of Year for some: Some 2023-2025 models show low ranges (e.g., 21–28 miles) because they are Plug-in Hybrid Electric Vehicles (PHEV) rather than full Battery Electric Vehicles (BEV), suggesting diverse consumer needs.


Predictive Analysis — What Will Happen?
2026 Forecast: Based on the growth observed from 2021–2025, registration volumes are predicted to reach new peaks in 2026 as more manufacturers transition their fleets to electric.
Range Maturation: We predict the "Mean Electric Range" will rise significantly as older, shorter-range models are phased out by newer long-range BEVs.
Infrastructure Expansion: Growth will likely shift toward more rural counties (like Yakima) as charging networks expand beyond the primary urban hubs.


Prescriptive Analysis — What Should Be Done?
Targeted Incentives: Legislative districts with high populations but low EV counts should implement "Green Rebates" to encourage initial adoption.
Infrastructure for PHEVs: Since many vehicles are flagged as "not eligible due to low battery range," urban charging infrastructure should be optimized for quick "top-up" charging for hybrid users.
Utility Support: Utilities like Pacificorp should be encouraged to mirror the success of Puget Sound Energy in fostering EV-friendly environments.


Recommendations / Decision Support
Prioritize Charging Density: Focus on increasing charging stations in high-density residential areas where users may not have private garages.
Automated Reporting: Implement scripts to automate parts of the range and eligibility analysis to provide real-time dashboards for policymakers.
Modernize Older Fleets: Create "Trade-in" programs focused on replacing pre-2016 EVs with modern long-range alternatives to improve overall fleet efficiency.


Final Project Conclusion
The transition to sustainable automotive transportation in Washington is a documented reality. This project confirms that the EV sector is experiencing sustained growth, driven by a massive influx of newer models and a strong presence from market leaders like Tesla and Nissan. While the market remains "top-heavy" in urban centers, the increasing diversity in vehicle types (BEV and PHEV) suggests a future where different consumer segments can find a suitable electric alternative. Ultimately, the future lies in expanding infrastructure to rural regions and ensuring that the next wave of registrations (2026 and beyond) is supported by a robust and accessible charging gr



