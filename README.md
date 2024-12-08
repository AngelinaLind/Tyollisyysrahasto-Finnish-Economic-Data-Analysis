# Economic and Labour Market Insights 2010–2024

This Power BI project provides insights into key economic and labor market trends from 2010 to 2024, along with a sectoral performance prognosis from 2023 to 2028. The report contains four interactive visualizations created using publicly available datasets. The purpose of the project is to analyze trends and present them in an easy-to-understand format to support decision-making.

---

## **Project Objective**

The goal of this project is to:
1. Analyze key economic and labor market indicators over time.
2. Summarize findings through interactive visualizations.
3. Provide actionable insights for stakeholders.

---

## **Datasets Used**

1. **Väestö työmarkkina-aseman, sukupuolen ja iän mukaan, kuukausitiedot (135y)**  
   - Source: [Statistics Finland](https://pxdata.stat.fi/PxWeb/pxweb/fi/Check/)
   - Key Metrics:  
     - Employment Rate, Unemployment Rate, Labor Force, People Outside the Labor Force (monthly, 2010–2024).

2. **Tulot ja tuotanto toimialoittain, neljännesvuosittain (132g)**  
   - Source: [Statistics Finland](https://pxdata.stat.fi/PxWeb/pxweb/fi/Check/)
   - Key Metrics:  
     - GDP, Gross Value Added (GVA), Employee Costs, Employer Costs (quarterly, 2010–2024).

3. **Taloudellinen katsaus: Syksy 2024 (Economic Review)**  
   - Source: [Valtioneuvosto](https://github.com/AngelinaLind/Tyollisyysrahasto-Finnish-Economic-Data-Analysis/blob/279d8aace0b74f88e287137f101154e83bae42c9/Materials/Taloudellinen%20katsaus_syksy%202024%20ennustesarjat-2.xlsx)  
   - Key Metrics:  
     - Economic Forecast for 2023–2028.

---

## **Visualizations**

### 1. **Economic Indicators (2010–2024)**
- **Type:** Line Chart
- **Description:** Shows trends for GDP, GVA, employee pay, and employer costs.
- **Key Insight:** GDP shows steady growth, while employee and employer costs increase moderately.

### 2. **Employment by Age Group and Gender (2010–2024)**
- **Type:** Clustered Column Chart
- **Description:** Compares employment rates across different age groups (15–64) and genders.
- **Key Insight:** The 25–54 age group dominates the labor market, while youth and senior employment rates are lower.

### 3. **Labour Force and Unemployment Trends (2010–2024)**
- **Type:** Combined Clustered Column and Line Chart
- **Description:** Analyzes labor force size, employed persons, and yearly GDP changes (%).
- **Key Insight:** GDP fluctuations, especially in 2020, significantly impact employment trends.

### 4. **GDP and Sectoral Performance Prognosis (2023–2028)**
- **Type:** Line Chart
- **Description:** Forecasts changes in industry and service performance, employment, and unemployment rates.
- **Key Insight:** Services grow steadily, while industry shows some fluctuation. Unemployment decreases consistently.

---

## **Steps Taken**

### 1. Data Cleaning and Preparation
- Imported datasets into Power BI.
- Filtered data to focus on the most relevant timeframes (2010–2024 for analysis, 2023–2028 for forecasts).
- Renamed columns for clarity.
- Created calculated columns using DAX for translated metric names.

### 2. Data Modeling
- Established relationships between tables using date fields and created a custom date table:
```DAX
DateTable = FILTER(CALENDAR(DATE(2010,1,1), DATE(2028,12,31)), DAY([Date]) = 1)
```
- Ensured "many-to-one" and "one-to-one" relationships were used appropriately.
Materials/Screenshots/DataModel.png

### 3. Visualization Creation
- Used Power BI's visualization tools to design charts and dashboards.
- Customized color palettes to align with the visual identity of Työllisyysrahasto.

### 4. Analysis and Reporting
- Identified trends and correlations from visualizations.
- Summarized findings in a meaningful and concise way.

---

## **Key Findings**
1. **Economic Stability:** GDP shows a consistent upward trend, indicating overall economic stability.
2. **Employment Insights:** The prime-age group (25–54) dominates the labor market, while younger and older populations face challenges.
3. **Sectoral Performance:** Services are the main drivers of economic growth, while the industrial sector remains volatile.
4. **Post-Pandemic Recovery:** Economic indicators suggest gradual recovery after the 2020 downturn.

---

## **Files Included**
- **Power BI (.pbix)** file with interactive dashboards.
- **Screenshots** of the visualizations.
- Source datasets (linked in the README).

---

## **How to Use**
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Economic-Labour-Insights.git
   ```
2. Open the Power BI file (`.pbix`) to explore the interactive dashboards.
3. Review the analysis and findings in the `README.md`.

---

## **Future Improvements**
- Automating data updates using Power BI gateways.
- Expanding analysis with additional metrics such as inflation rates or trade balances.
- Incorporating advanced analytics using Python or R scripts.

---

## **Contact**
Created by **Angelina Lind**.  
For questions, please reach out via [LinkedIn](https://linkedin.com/in/angelinalind) .
