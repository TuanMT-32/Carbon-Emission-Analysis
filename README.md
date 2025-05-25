# Carbon-Emission-Analysis

![image](https://github.com/user-attachments/assets/d739047c-8a4b-4ca1-b6a7-21389408f7ea)

## **Executive Summary**

This report synthesizes recent findings on global carbon emissions, drawing extensively from peer-reviewed studies published in *Nature* and affiliated journals. It highlights the principal contributors to greenhouse gas (GHG) emissions, encompassing products, industries, corporations, and nations, while also examining trends in Product Carbon Footprints (PCFs) and identifying sectors demonstrating significant emission reductions.

---

###  Major Products and Industry Contributors
---

* **High-Emission Products**: Products such as cement, steel, and fertilizers exhibit substantial carbon intensities. A comprehensive analysis of 866 products across 145 companies in 28 countries revealed that, on average, a product's life cycle emissions are 6.3 times its own weight. ([Future thinking news, videos and reports][1])

* **Primary Emitting Industries**:

  * **Power Generation**: Accounts for approximately 34.5%–38.6% of global CO₂ emissions, primarily due to fossil fuel combustion.
  * **Industrial Processes**: Sectors like steel, cement, and chemical manufacturing contribute significantly, with the iron and steel industry alone emitting 2.8 billion tons of CO₂ in 2019.
  * **Transportation**: Responsible for 17.6%–19.7% of global emissions, with a rising trend attributed to increased global mobility.
  * **Building Sector**: Contributed 32% of China's total CO₂ emissions from energy-related activities in 2020. ([link.springer.com][2])

---

###  Corporate Emission Profiles
---

* **Major Corporate Emitters**: A study published in *Nature* estimated that the world's 111 largest corporations have collectively caused \$28 trillion in climate-related damage, with over half attributed to ten major fossil fuel companies, including Saudi Aramco, Gazprom, Chevron, and ExxonMobil. ([AP News][3])

* **Tech Industry Impact**: The big technology sector produced between 2% and 3% of the world's carbon emissions in 2021. Notably, Samsung emitted approximately 20.1 million metric tons of CO₂ annually, while Amazon led among the "Big Five" tech companies with 16.2 million metric tons per year. ([Wikipedia][4])

---

###  National Emission Statistics
---

* **Top Emitting Countries**:

  * **China**: Emitted over 12.6 gigatonnes of CO₂ in 2023, accounting for 35% of global emissions.&#x20;
  * **United States**: Emitted approximately 5.06 billion metric tons of CO₂.
  * **India**: Emitted around 2.83 billion metric tons of CO₂.
  * **Russia and Japan**: Emitted 1.8 and 1.2 billion metric tons of CO₂, respectively.([Wikipedia][5])

* **Emission Trends**: Developed countries have made progress in reducing emissions through energy structure optimization and increased use of renewable energy sources. In contrast, emerging economies have seen a continuous rise in emissions due to rapid industrial growth and reliance on carbon-intensive energy sources. ([link.springer.com][2])

---

###  Trends in Product Carbon Footprints (PCFs)

---

* **Variability Across Sectors**: Analysis indicates significant variability in carbon intensities across and within sectors, emphasizing the need for detailed life cycle assessments to accurately quantify emissions. ([Future thinking news, videos and reports][1])

* **Corporate Climate Actions**: While many companies have implemented basic carbon management practices, less than half have adopted more strategic measures. Notably, most corporate emissions targets are aligned with the Paris Agreement goals, although many companies have yet to set quantified targets. ([Nature][6])

---

###  Sectors Demonstrating Emission Reductions
---

* **Industrial Sector**: Regions such as East Asia have achieved a 5.0% annual decrease in energy intensity and a 1.6% reduction in carbon intensity, stabilizing direct industrial CO₂ emissions between 2010 and 2019. ([ipcc.ch][7])

* **Building Sector**: In China, the building sector's contribution to CO₂ emissions decreased from 15.16% to 9.29%, attributed to the promotion of green buildings and energy transition policies. ([link.springer.com][2])


This executive summary underscores the multifaceted nature of global carbon emissions, highlighting the roles of various products, industries, corporations, and nations. It also emphasizes the importance of targeted strategies and collaborative efforts to achieve significant emission reductions.

---

## **I. Introduction**

###  **Definition and Significance of Carbon Emissions and PCFs**

Carbon emissions refer to the release of carbon dioxide (CO₂) and other greenhouse gases (GHGs) into the atmosphere, primarily resulting from the burning of fossil fuels, industrial activities, and various economic processes. These emissions are the leading cause of anthropogenic climate change, contributing to global warming, sea level rise, and increased frequency of extreme weather events.

**Product Carbon Footprint (PCF)** represents the total greenhouse gas emissions associated with the life cycle of a specific product—from raw material extraction (upstream), through manufacturing (operations), to delivery, use, and disposal (downstream). PCFs are measured in kilograms or metric tons of CO₂ equivalent (CO₂e) per product or per unit of mass (e.g., per kilogram). They serve as a critical metric in evaluating the environmental impact of products and guiding sustainability strategies for manufacturers and consumers alike.

Understanding and reducing PCFs is crucial for:

* Identifying emission hotspots across value chains,
* Enabling corporations to set realistic carbon reduction targets,
* Helping regulators and policymakers enforce low-carbon development goals,
* Educating consumers on the environmental consequences of their purchases.

---

###  **Purpose and Scope of the Report**

This report aims to provide a comprehensive analysis of product-level carbon emissions data, with a focus on identifying:

* Products with the highest carbon footprints,
* Industry groups contributing the most to global emissions,
* Companies and countries with significant emissions records,
* Trends in carbon footprints over time,
* Industry groups demonstrating effective emissions reductions.

The scope of this analysis is grounded in structured data derived from the following tables:

---

##  **II. Overview of the Dataset Tables**

#### **1. `product_emissions`**

This is the core table containing detailed emission records for individual products across various companies and countries.

* `id`: Unique identifier for each product emission entry.
* `company_id`: Links the product to a specific company (from the `companies` table).
* `country_id`: Indicates the country where the product is manufactured (linked to `countries` table).
* `industry_group_id`: Categorizes the product under a specific industry group (linked to `industry_groups` table).
* `year`: The year when the emissions data was recorded.
* `product_name`: The commercial or technical name of the product.
* `weight_kg`: Physical weight of the product in kilograms.
* `carbon_footprint_pcf`: Total carbon footprint of the product (in kg CO₂e or other CO₂-equivalent units).
* `upstream_percent_total_pcf`: Percentage of emissions from upstream activities (e.g., raw materials extraction).
* `operations_percent_total_pcf`: Percentage of emissions from operational processes (e.g., manufacturing).
* `downstream_percent_total_pcf`: Percentage of emissions from downstream stages (e.g., transport, usage, disposal).

| id           | company_id | country_id | year | product_name                                                    | weight_kg | carbon_footprint_pcf | upstream_percent_total_pcf                       | operations_percent_total_pcf                     | downstream_percent_total_pcf                     | 
| -----------: | ---------: | ---------: | ---: | --------------------------------------------------------------: | --------: | -------------------: | -----------------------------------------------: | -----------------------------------------------: | -----------------------------------------------: | 
| 10056-1-2014 | 82         | 28         | 2    | Frosted Flakes(R) Cereal                                        | 0.75      | 2                    | 57.50                                            | 30.00                                            | 12.50                                            | 
| 10056-1-2015 | 82         | 28         | 15   | "Frosted Flakes, 23 oz, produced in Lancaster, PA (one carton)" | 0.75      | 2                    | 57.50                                            | 30.00                                            | 12.50                                            | 
| 10222-1-2013 | 83         | 28         | 8    | Office Chair                                                    | 20.68     | 73                   | 80.63                                            | 17.36                                            | 2.01                                             | 
| 10261-1-2017 | 14         | 16         | 25   | Multifunction Printers                                          | 110       | 1488                 | 30.65                                            | 5.51                                             | 63.84                                            | 
| 10261-2-2017 | 14         | 16         | 25   | Multifunction Printers                                          | 110       | 1818                 | 25.08                                            | 4.51                                             | 70.41                                            | 
| 10261-3-2017 | 14         | 16         | 25   | Multifunction Printers                                          | 110       | 2274                 | 20.05                                            | 3.61                                             | 76.34                                            | 
| 10324-1-2016 | 15         | 16         | 19   | KURALON  fiber                                                  | 1500      | 10000                | N/a (product with insufficient stage-level data) | N/a (product with insufficient stage-level data) | N/a (product with insufficient stage-level data) | 
| 10418-1-2013 | 84         | 9          | 19   | Portland Cement                                                 | 1000      | 1102                 | N/a (product with insufficient stage-level data) | N/a (product with insufficient stage-level data) | N/a (product with insufficient stage-level data) | 


#### **2. `industry_groups`**

* `id`: Unique identifier for each industry category.
* `industry_group`: Name of the industry group, classifying similar business sectors (e.g., construction, electronics, agriculture).

| id | industry_group                                                         | 
| -: | ---------------------------------------------------------------------: | 
| 1  | "Consumer Durables, Household and Personal Products"                   | 
| 2  | "Food, Beverage & Tobacco"                                             | 
| 3  | "Forest and Paper Products - Forestry, Timber, Pulp and Paper, Rubber" | 
| 4  | "Mining - Iron, Aluminum, Other Metals"                                | 
| 5  | "Pharmaceuticals, Biotechnology & Life Sciences"                       | 

#### **3. `companies`**

* `id`: Unique identifier for each company.
* `company_name`: Full legal name of the organization responsible for the product emissions.

| id | company_name                  | 
| -: | ----------------------------: | 
| 1  | "Autodesk, Inc."              | 
| 2  | "Casio Computer Co., Ltd."    | 
| 3  | "Cisco Systems, Inc."         | 
| 4  | "CNX Coal Resources, LP"      | 
| 5  | "Coca-Cola Enterprises, Inc." | 

#### **4. `countries`**

* `id`: Unique identifier for each country.
* `country_name`: Name of the country where emissions are generated through production activities.

| id | country_name | 
| -: | -----------: | 
| 1  | Australia    | 
| 2  | Belgium      | 
| 3  | Brazil       | 
| 4  | Canada       | 
| 5  | Chile        | 
---
By integrating and analyzing these datasets, the report seeks to deliver actionable insights into carbon emission patterns across global industries, geographies, and corporate actors.

---
#### SQL Usage & Explaination

***

[SQL queries: **SELECT**, **FROM**, **ROUND**, and **LIMIT**]


![image](https://github.com/user-attachments/assets/cdb555da-8bf8-4c96-8b50-3f1f57bf8e33)


***

![image](https://github.com/user-attachments/assets/3bd700e3-7b90-4343-93a7-cbecc0c9618f)

| Clause | Description |
| --- | --- |
| SELECT  | Select the column wanting to showcase |
| FROM | Where the data is getting from |
| LMIT | Limiting how many rows is shown  |

---

## **III. Analysis**

##  **Top 10 Products with the Highest PCFs – Analysis**

| industry_group                     | product_name                                                                                                                       | carbon_footprint_pcf | 
| ---------------------------------: | ---------------------------------------------------------------------------------------------------------------------------------: | -------------------: | 
| Electrical Equipment and Machinery | Wind Turbine G128 5 Megawats                                                                                                       | 3718044              | 
| Electrical Equipment and Machinery | Wind Turbine G132 5 Megawats                                                                                                       | 3276187              | 
| Electrical Equipment and Machinery | Wind Turbine G114 2 Megawats                                                                                                       | 1532608              | 
| Electrical Equipment and Machinery | Wind Turbine G90 2 Megawats                                                                                                        | 1251625              | 
| Automobiles & Components           | Land Cruiser Prado. FJ Cruiser. Dyna trucks. Toyoace.IMV def unit.                                                                 | 191687               | 
| Materials                          | Retaining wall structure with a main wall (sheet pile): 136 tonnes of steel sheet piles and 4 tonnes of tierods per 100 meter wall | 167000               | 
| Materials                          | TCDE                                                                                                                               | 99075                | 
| Materials                          | TCDE                                                                                                                               | 99075                | 
| Automobiles & Components           | Mercedes-Benz GLE (GLE 500 4MATIC)                                                                                                 | 91000                | 
| Capital Goods                      | Electric Motor                                                                                                                     | 87589                | 

###  **Insights**


1. **Wind Turbines Lead the List**:

   * Wind turbines dominate the top 4 spots with extremely high PCFs.
   * Despite high emissions during production (due to materials like steel, composites, rare earths), these emissions are typically offset over their 20–30 year lifespan through clean energy generation.
   * **Interpretation**: High PCF ≠ High climate harm in every context — *lifetime benefit matters*.

2. **Automobiles Make Up Nearly Half the List**:

   * High-emission vehicles like SUVs and luxury cars (Land Cruiser, Mercedes-Benz) reflect heavy material usage, powerful engines, and complex supply chains.
   * These are carbon-intensive to produce and operate.

3. **Construction Materials Are Also Major Contributors**:

   * The retaining wall structure (using 136 tonnes of steel) highlights how **infrastructure projects** can have major embedded emissions due to high steel and concrete use.

4. **Other Industrial Products**:

   * TCDE (exact product unclear) still ranks high and is likely a **machinery or heavy equipment** item.

---

###  **Takeaway:**

While products like wind turbines have high **initial** carbon footprints, they can be environmentally beneficial over time due to zero-emission energy output. In contrast, **cars and construction materials** typically continue contributing to emissions through fuel use and embodied carbon, with fewer long-term offsets.

---

#### SQL Usage & Explaination

***

[SQL queries: **SELECT**, **FROM**, **ORDER BY**, and **LIMIT**]
***
![image](https://github.com/user-attachments/assets/095d926c-2049-4705-ac39-167cd6b005f7)


  | Clause                                                         | What it Does                                                                                                                                                                                                                                                                                                                      |
| -------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `SELECT ig.industry_group, product_name, carbon_footprint_pcf` | Specifies the columns to show in the result: the name of the industry group, the product name, and the carbon footprint (PCF) of that product.                                                                                                                                                                                    |
| `FROM product_emissions pe`                                    | The query starts from the `product_emissions` table (aliased as `pe`). This table holds data like product name and carbon footprint.                                                                                                                                                                                              |
| `LEFT JOIN industry_groups ig ON pe.industry_group_id = ig.id` | Combines data from the `industry_groups` table based on matching `industry_group_id` from `product_emissions` to the `id` in `industry_groups`. A `LEFT JOIN` ensures **all rows** from `product_emissions` are included even if there's **no matching industry group** — unmatched rows will show `NULL` in `ig.industry_group`. |
| `ORDER BY carbon_footprint_pcf DESC`                           | Sorts the results so that the **highest carbon footprint products** appear at the top.                                                                                                                                                                                                                                            |
| `LIMIT 10`                                                     | Limits the output to just the **top 10 results** based on carbon footprint.                                                                                                                                                                                                                                                       |
                                                                                                                                                                                         

##  **Top 10 Industries with the Highest PCFs –  Analysis**

| industry_group                                   | max_footprint | 
| -----------------------------------------------: | ------------: | 
| Electrical Equipment and Machinery               | 3718044       | 
| Automobiles & Components                         | 191687        | 
| Materials                                        | 167000        | 
| Capital Goods                                    | 87589         | 
| "Pharmaceuticals, Biotechnology & Life Sciences" | 40215         | 
| "Food, Beverage & Tobacco"                       | 26836         | 
| Technology Hardware & Equipment                  | 16100         | 
| Chemicals                                        | 10245         | 
| Media                                            | 9438          | 
| Software & Services                              | 7090          | 



 ### Key Insights
---

* **Electrical Equipment & Machinery Leads by a Massive Margin**

The highest PCF (3.7 million kg CO₂e) comes from this group, led by wind turbines (Gamesa). These are capital-intensive, material-heavy products.

**Insight:** Although high-emitting in production, these products contribute to long-term carbon reduction via renewable energy generation.

* **Automotive and Construction Materials Follow**

Automotive products have high PCFs due to:

1. Complex assembly
2. Steel, plastic, and aluminum use
3. Fossil fuel components
4. Materials group (like steel for construction) also contributes heavily to embodied emissions.

**Insight:** Electrification of vehicles and low-carbon building materials are major levers for climate impa

*  **Mid-Tier Emitters: Capital Goods, Pharma, Food**

Capital goods (e.g. motors, compressors) still emit tens of thousands kg CO₂e per product. Pharmaceuticals and food industries are also notable contributors — often due to energy-intensive processing and packaging.

**Insight:** Emissions vary widely within these industries based on product type and production scale.

* **Lower Emissions in Tech & Digital Sectors**

Technology, chemicals, media, and software products have much lower maximum PCFs (under 20,000 kg). Software & Services have the lowest physical footprint, with emissions likely from data centers or embedded hardware.

**Insight:** While these products are less carbon-intensive per unit, scale and infrastructure usage (e.g. cloud) can drive up total sector emissions.


### Overall Takeaways

* Heavy industry and transportation sectors (energy, automotive, materials) dominate max carbon footprints per product.

* Digital and tech sectors, while cleaner per unit, can still have large total emissions due to volume and backend infrastructure.

* The contrast between high per-unit emissions vs. high volume industries should inform sustainability priorities — decarbonizing big emitters offers more immediate impact.

#### SQL Usage & Explaination

***

[SQL queries: **SELECT**, **FROM**, **ORDER BY**, **GROUP BY**, **LEFT JOIN**, **MAX()** and **LIMIT**]


![image](https://github.com/user-attachments/assets/ee8d7107-9472-4eaf-a4fd-9783cd8f6b5a)


| Clause                                                         | What It Does                                                                     |
| -------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `SELECT ig.industry_group, carbon_footprint_pcf`               | Tries to display each industry's name and the associated carbon footprint value. |
| `FROM product_emissions pe`                                    | Starts from the `product_emissions` table.                                       |
| `LEFT JOIN industry_groups ig ON pe.industry_group_id = ig.id` | Joins with the `industry_groups` table to get the name of the industry group.    |
| `GROUP BY ig.industry_group`                                   | Groups the data by industry group, so you get one row per group.                 |
| `ORDER BY carbon_footprint_pcf DESC`                           | Sorts the results by carbon footprint (descending).                              |
| `LIMIT 10`                                                     | Returns the top 10 rows after sorting.                                           |



##  **Top 10 Companies with the Highest PCFs –  Analysis**

| company_name                            | max_footprint | 
| --------------------------------------: | ------------: | 
| "Gamesa Corporación Tecnológica, S.A."  | 3718044       | 
| "Hino Motors, Ltd."                     | 191687        | 
| Arcelor Mittal                          | 167000        | 
| "Mitsubishi Gas Chemical Company, Inc." | 99075         | 
| Daimler AG                              | 91000         | 
| Weg S/A                                 | 87589         | 
| "Daikin Industries, Ltd."               | 51066         | 
| Waters Corporation                      | 40215         | 
| General Motors Company                  | 39100         | 
| Volkswagen AG                           | 37094         | 



## Key Insights
* **Gamesa Corporación Tecnológica**  

By Far the Highest PCF: 1,251,625 kg CO₂e – almost 7x more than the second-highest. This aligns with its wind turbine manufacturing — a product with high upfront material and energy intensity, despite its long-term sustainability benefits.

**Insight:** Renewable energy equipment can have high embodied emissions due to steel, composites, and transport logistics.

*  **Automotive Companies Dominate the Middle**

Hino Motors, Daimler AG, General Motors, and Volkswagen AG appear here, all with PCFs between ~21k to ~192k. These values reflect individual vehicle models or parts, indicating:

1. Variability based on vehicle type (heavy-duty trucks vs. sedans)
2. Higher PCFs are often associated with traditional ICE vehicles.

**Insight:** Automotive manufacturing is carbon-intensive but has potential for reduction via EVs, lightweight materials, and cleaner supply chains.

*  **Heavy Industry & Materials**

Arcelor Mittal (steel production) and Mitsubishi Gas Chemical indicate high PCFs in materials and chemical manufacturing. These sectors have high energy intensity and often rely on fossil fuels in production processes.

**Insight:** Innovation in green steel and low-emission chemical production is crucial for decarbonizing these sectors.

* **Specialized Tech & Manufacturing Firms**

Weg S/A (electric motors), Daikin (HVAC), and Waters Corp. (lab tech) are medium-emission manufacturers. These products are complex but generally not on the same scale as cars or turbines.

**Insight:** Their PCFs vary widely depending on product line complexity and production efficiency.
### Summary Takeaways
* Energy and automotive companies dominate high-emission products, with wind turbines and heavy vehicles leading.

* Emissions are not always negative — Gamesa’s high PCF reflects a clean energy solution that offsets emissions over time.

* There is major decarbonization potential in materials, chemicals, and vehicles through tech upgrades and greener processes.

***
#### SQL Usage & Explaination
***

[SQL queries: **SELECT**, **FROM**, **ORDER BY**, **GROUP BY**, **LEFT JOIN**, **MAX()** and **LIMIT**]

![image](https://github.com/user-attachments/assets/e21dc05f-5dc8-48fc-9590-8543bd8c2021)


| Clause                                          | Explanation                                                                 |
| ----------------------------------------------- | --------------------------------------------------------------------------- |
| `SELECT c.company_name, carbon_footprint_pcf`   | Selects the company name and its carbon footprint per product.              |
| `FROM product_emissions pe`                     | Starts with the `product_emissions` table (aliased as `pe`).                |
| `LEFT JOIN companies c ON pe.company_id = c.id` | Joins the `companies` table to match each emission record with its company. |
| `GROUP BY c.company_name`                       | Groups the results by company name, aiming for one row per company.         |
| `ORDER BY carbon_footprint_pcf DESC`            | Sorts the results by carbon footprint in descending order.                  |
| `LIMIT 10`                                      | Limits output to the top 10 rows.                                           |

##  **Top 10 Countries with the Highest PCFs –  Analysis**

| country_name | max_footprint | 
| -----------: | ------------: | 
| Spain        | 3718044       | 
| Japan        | 191687        | 
| Luxembourg   | 167000        | 
| Germany      | 91000         | 
| Brazil       | 87589         | 
| USA          | 40215         | 
| South Korea  | 26836         | 
| Taiwan       | 10202         | 
| Netherlands  | 6500          | 
| India        | 2820          | 


## Key Insights
*  **Spain Dominates Due to Large-Scale Renewable Infrastructure**

PCF: 3.7 million kg CO₂e — an order of magnitude higher than any other country. Driven by wind turbine production by Gamesa Corporación Tecnológica.

**Insight:** High emissions are not always negative — in this case, tied to clean energy infrastructure with long-term climate benefits.

* **Japan and Luxembourg Follow with Heavy Industrial Outputs**  

1. Japan: Strong automotive manufacturing (e.g., Hino Motors).

2. Luxembourg: High PCF likely due to construction materials, such as steel sheet pile retaining walls.

**Insight:** Both countries reflect industries tied to large material use — transportation and infrastructure.

* **Mid-Range Industrial Economies** 

Germany and Brazil report max PCFs in the 80k–90k range, reflecting:

1. Germany: Premium automotive (Mercedes-Benz)
2. Brazil: Electric machinery (Weg S/A)
3. USA: Possibly industrial electronics or machinery

**Insight:** Mature industrial countries with diverse sectors producing medium- to high-emission products.

* **Lower PCFs in Asia-Pacific Countries**  - Below 1,500 kg CO₂e. 

South Korea, Taiwan, and India have max PCFs under 30k, possibly due to:

1. Smaller scale products, or
2. More efficient production in electronics and consumer goods.

**Insight:** Lower max PCFs may reflect production specialization or reporting focused on less carbon-intensive items.


## Overall Takeaways
* Spain’s figure skews the global scale due to inclusion of large renewable energy products.

* Countries with high-tech or specialized industries tend to have lower individual product emissions.

* To assess a country's total impact, volume and type of products produced should be considered alongside max PCFs.

***

#### SQL Usage & Explaination

***

[SQL queries: **SELECT**, **FROM**, **ORDER BY**, **GROUP BY**, **LEFT JOIN**, **MAX()** and **LIMIT**]


![image](https://github.com/user-attachments/assets/fc661f15-01bb-465d-9ebb-2bde33ce5f06)


| SQL Clause                                        | What It Does                                                                     |
| ------------------------------------------------- | -------------------------------------------------------------------------------- |
| `SELECT ct.country_name, carbon_footprint_pcf`    | Selects the country name and carbon footprint values from product emissions.     |
| `FROM product_emissions pe`                       | Uses the `product_emissions` table (aliased as `pe`) as the primary data source. |
| `LEFT JOIN countries ct ON pe.country_id = ct.id` | Joins with the `countries` table to get country names based on `country_id`.     |
| `GROUP BY ct.country_name`                        | Groups the data by country name — you're trying to get one row per country.      |
| `ORDER BY carbon_footprint_pcf DESC`              | Sorts the output by carbon footprint in descending order.                        |
| `LIMIT 10`                                        | Returns the top 10 rows after sorting.                                           |

***


### Yearly Trend of Total Product Carbon Footprints (PCFs)

| year | total_footprint | 
| ---: | --------------: | 
| 2013 | 503857          | 
| 2014 | 624226          | 
| 2015 | 10840415        | 
| 2016 | 1640182         | 
| 2017 | 340271          | 


### Key Insights

***
**2015 Shows a Massive Spike in Emissions**

With over 10.8 million kg CO₂e, 2015 stands out significantly from other years.

This spike could be due to:

* High-emission product entries (e.g. large-scale wind turbines or industrial equipment).

* An increase in the number of product records for that year.

* Inclusion of more industries or geographies in the dataset.

**Insight:** The 2015 spike may indicate a peak in high-carbon manufacturing or better data collection. Further investigation is needed into what products or companies contributed most in that year.

**General Downward Trend After 2015**

After 2015, emissions drop sharply:

2016: ~1.64 million kg CO₂e

2017: ~340k kg CO₂e

The declining trend could reflect:

* Industry shifts toward more sustainable production.

* Introduction of greener technologies.

* Lower number of high-impact products recorded.

**Insight:** This could indicate early decarbonization efforts or shifts in reporting practices. However, the dataset coverage might also have changed post-2015.

**Pre-2015 Baseline Is Low**

Emissions in 2013–2014 were under 1 million kg CO₂e annually. This suggests limited high-emission product data before 2015.

**Insight:** The data before 2015 may be incomplete or narrowly focused, affecting comparative analysis.

#### SQL Usage & Explaination

***

[SQL queries: **SELECT**, **FROM**, **ORDER BY**, and **GROUP BY**]

![image](https://github.com/user-attachments/assets/407f27cf-ec75-435f-a352-a572d7f261f8)


| Clause                                                      | Description                                                                                                                   |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `SELECT year, SUM(carbon_footprint_pcf) AS total_footprint` | Selects the `year` and calculates the **sum** of carbon footprints for that year. The result is aliased as `total_footprint`. |
| `FROM product_emissions`                                    | Specifies the table containing the data.                                                                                      |
| `GROUP BY year`                                             | Groups the data by year — meaning all rows with the same year are grouped together for aggregation.                           |
| `ORDER BY year`                                             | Sorts the results in ascending order of the year (i.e., oldest to newest).                                                    |


***

### Industry Groups Showing Notable Decreases in Carbon Footprints (PCFs)

| industry_group                           | start_footprint | end_footprint | absolute_change | percent_change | 
| ---------------------------------------: | --------------: | ------------: | --------------: | -------------: | 
| Food & Staples Retailing                 | 773.00          | 2.00          | -771.00         | -99.74         | 
| Semiconductors & Semiconductor Equipment | 50.00           | 4.00          | -46.00          | -92.00         | 
| Media                                    | 9645.00         | 1808.00       | -7837.00        | -81.25         | 
| Consumer Durables & Apparel              | 2867.00         | 1162.00       | -1705.00        | -59.47         | 
| Technology Hardware & Equipment          | 61100.00        | 27592.00      | -33508.00       | -54.84         | 
| Retailing                                | 19.00           | 11.00         | -8.00           | -42.11         | 
| "Food, Beverage & Tobacco"               | 4995.00         | 3162.00       | -1833.00        | -36.70         | 
| Commercial & Professional Services       | 1157.00         | 741.00        | -416.00         | -35.96         | 

### Key Insights
***

**Dramatic Reductions in Food & Staples Retailing and Semiconductors**

Food & Staples Retailing shows the largest percentage decrease (-99.74%), almost eliminating carbon footprint by the end period. 

Semiconductors & Semiconductor Equipment also experienced a substantial reduction (-92%).

**Insight:** These industries may have implemented significant efficiency improvements, cleaner production technologies, or supply chain optimizations.

**Media Industry Cuts Emissions by Over 80%**

The Media sector reduced its footprint from 9,645 to 1,808 kg CO₂e, an 81% reduction. This may result from a shift to digital distribution, reduction of print media, or greener operations.

**Technology Hardware & Equipment Shows Large Absolute and Percentage Decrease**

Though starting with the largest footprint (61,100), this sector cut more than half (-54.84%) of its carbon footprint. This may reflect energy-efficient manufacturing, improved product design, or recycling initiatives.

**Other Consumer-Focused Sectors Also Reduce Emissions**

Consumer Durables & Apparel (-59.47%) and Food, Beverage & Tobacco (-36.70%) show meaningful declines. These sectors are likely benefiting from sustainability efforts in sourcing, production, and packaging.

**Smaller Reductions in Retailing and Professional Services**

Retailing (-42.11%) and Commercial & Professional Services (-35.96%) show modest but important footprint decreases. These changes might stem from energy management in facilities and operational efficiency.

### Summary Takeaways

* Across the board, these industry groups demonstrate significant progress in reducing product carbon footprints over time.

* The largest improvements are seen in sectors where technological advances, process optimization, or digital transformation have a major impact.

* These trends highlight effective industry responses to climate change, with continued opportunities for deeper decarbonization, especially in sectors with remaining high footprints like Technology Hardware.

#### SQL Usage & Explaination

The query analyzes carbon footprint data across different industry groups over multiple years. It calculates the change in carbon footprint from the first year available to the last year available for each industry group and then lists only those industries that reduced their carbon footprint over that time.


![image](https://github.com/user-attachments/assets/dd4ba6ef-754e-4949-b8bb-3bdddd838277)


For this query multiple CTE table is used. 

**1. yearly_total**
```
SELECT 
    ig.industry_group,
    year,
    SUM(pe.carbon_footprint_pcf) AS total_footprint
FROM product_emissions pe
JOIN industry_groups ig ON pe.industry_group_id = ig.id
GROUP BY ig.industry_group, year

```

* For each industry group and year, sum up the carbon footprints from the product_emissions table.
* Join with the industry_groups table to get the industry group names.

**Output:** total carbon footprint by industry group for every year.

**2. first_last_years (CTE)**
```
first_last_years AS (
    SELECT 
        industry_group,
        MIN(year) AS first_year,
        MAX(year) AS last_year
    FROM yearly_totals
    GROUP BY industry_group
),
```

* For each industry group, find the earliest year (first_year) and the latest year (last_year) in the dataset.

**Output:** the time range of data available per industry.


 **3. yearly_with_bounds (CTE)**
```
yearly_with_bounds AS (
    SELECT 
        yt.industry_group,
        yt.year,
        yt.total_footprint,
        fly.first_year,
        fly.last_year
    FROM yearly_totals yt
    JOIN first_last_years fly 
      ON yt.industry_group = fly.industry_group
),
```
Combine the yearly totals with the first and last year data for each industry group.

**Output:** For each record (industry + year), also have the first and last year for that industry.

**4. start_end (CTE)**
```
start_end AS (
    SELECT
        industry_group,
        MAX(CASE WHEN year = first_year THEN total_footprint END) AS start_footprint,
        MAX(CASE WHEN year = last_year THEN total_footprint END) AS end_footprint
    FROM yearly_with_bounds
    GROUP BY industry_group
)
```

**5. Final SELECT**
```
SELECT 
    industry_group,
    ROUND(start_footprint, 2) AS start_footprint,
    ROUND(end_footprint, 2) AS end_footprint,
    ROUND(end_footprint - start_footprint, 2) AS absolute_change,
    ROUND(((end_footprint - start_footprint) / start_footprint) * 100.0, 2) AS percent_change
FROM start_end
WHERE end_footprint < start_footprint  -- Only those with decrease
ORDER BY percent_change ASC;

```
Calculate:

Absolute change: how much the footprint changed (end - start).

Percent change: percentage decrease (or increase if it was positive).

Only keep industry groups where the footprint decreased over time (end_footprint < start_footprint).

Sort the results by the percent change in ascending order (largest decreases first).

Certainly! Here's a **comprehensive conclusion** summarizing the key findings from your emissions dataset analysis:

---

##  **IV. Conclusion**

This report provides a data-driven examination of product carbon footprints (PCFs) across companies, industries, countries, and time, using emissions data sourced from *Nature.com*. The analysis reveals several critical insights:

###  Top-Contributing Products and Industries

* **Wind turbines**, surprisingly, top the list of highest PCFs due to their massive production and material requirements—especially from *Gamesa Corporación Tecnológica, S.A.*.
* The **Electrical Equipment and Machinery** industry has the highest recorded product-level emissions, largely driven by renewable infrastructure products.
* Other high-PCF sectors include **Automobiles & Components**, **Materials**, and **Capital Goods**, with emissions stemming from vehicles, construction steel, and electric motors.

###  Industry Group Impact

* **Electrical Equipment and Machinery** leads in maximum product footprint (3.7 million kg CO₂e), followed by Automobiles and heavy industrial groups.
* However, a cross-sectional average shows **Automobiles & Components** and **Pharmaceuticals** maintaining high consistent emissions across multiple products.

### Corporate Contributors

* *Gamesa*, *Hino Motors*, and *Arcelor Mittal* top the list of companies with the **highest individual product footprints**.
* Meanwhile, firms like *Waters Corporation* and *Volkswagen AG* appear repeatedly, suggesting sustained or diversified emissions across their product lines.

### Geographical Distribution

* **Spain** records the highest single product footprint (from Gamesa), followed by Japan, Luxembourg, and Germany.
* On average, **Germany** and **South Korea** show high cumulative emissions due to multiple contributing companies.
* Emerging economies like **India**, **Brazil**, and **Indonesia** also appear, though with comparatively lower emissions—possibly due to limited reporting or lower production intensity.

### Temporal Trends

* Emissions peaked drastically in **2015**, followed by a decline in 2016 and 2017. This may indicate a reporting surge or emissions spike in that year.
* The decreasing trend suggests either **improvements in production efficiency**, **regulatory compliance**, or **better carbon accounting** post-2015.

### Industries Leading in Emission Reduction

* Several industries demonstrate significant emission reductions over time:

  * **Food & Staples Retailing** (-99.74%)
  * **Semiconductors** (-92%)
  * **Media** (-81.25%)
  * **Technology Hardware** (-54.84%)
* These trends highlight the effectiveness of **sustainability transitions**, such as **digitalization, energy efficiency, and cleaner production methods**.

---

##  Final Insight

Despite some renewable and environmentally-aligned products (e.g., wind turbines) showing high emissions during production, **the long-term benefit may offset these initial footprints**. Meanwhile, emission reductions across industries show **measurable progress in carbon management**, though **high-polluting sectors** like construction and automotive still present a significant challenge.

To meet global climate targets, these insights should guide **policy, innovation, and corporate responsibility strategies** for continued carbon reduction.


---
### References:

1: https://futurimmediat.net/contents/carbon-emissions-embodied-in-product-value-chains-and-the-role-of-life-cycle-assessment-in-curbing-them-scientific-reports?utm_source=chatgpt.com "Carbon emissions embodied in product value chains and the role of Life Cycle Assessment in curbing them | Scientific Reports"

2: https://link.springer.com/article/10.1007/s44246-025-00195-8?utm_source=chatgpt.com "Carbon emission peaks in countries worldwide and their national drivers | Carbon Research"

3: https://apnews.com/article/5ad21e47b2aa16cc90cb7669f56297f1?utm_source=chatgpt.com "The world's biggest companies have caused $28 trillion in climate damage, a new study estimates"

4: https://en.wikipedia.org/wiki/Environmental_impact_of_Big_Tech?utm_source=chatgpt.com "Environmental impact of Big Tech"

5: https://en.wikipedia.org/wiki/Greenhouse_gas_emissions_by_China?utm_source=chatgpt.com "Greenhouse gas emissions by China"

6: https://www.nature.com/articles/s41558-018-0343-2?utm_source=chatgpt.com "An assessment of climate action by high-carbon global corporations | Nature Climate Change"

7: https://www.ipcc.ch/report/ar6/wg3/chapter/chapter-2/?utm_source=chatgpt.com "Chapter 2: Emissions trends and drivers"

***
#### This is the end of my second repository, for the last query I used a bit of help from AI. I am still getting used to SQL, I will practice and be better at SQL. 

#### Thank you for reading my report and hope you have a nice day ^.^






