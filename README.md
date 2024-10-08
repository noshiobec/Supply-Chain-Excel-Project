# Supply-Chain-Excel-Project

## Project Overview

This analysis seeks to explore and identify the key vendors and material defects affecting the operational performance of XYZ Production Company, particularly focusing on the years 2018 and 2019. Recent observations indicate a decline in customer satisfaction due to a low supply of original raw materials, leading to decreased patronage and threatening the business's survival. The objective is to highlight areas where improvement is needed to minimize downtime, defects, and overall cost implications.

A comprehensive supply chain dataset will be analyzed, containing defect quantities, unit prices, and downtime caused by various vendors across existing plant locations. This dataset is organized into four key sheets as shown diagram below in the below: Supplier Quality, Material Type, Defect Type, and Defect. Through data cleaning, vendor performance metrics, and material analysis, actionable insights into vendor reliability and product quality will be provided. Additionally, the analysis will focus on identifying which products have the most significant impact on operations. Interactive reports with slicers and filters will facilitate dynamic data exploration, ultimately leading to recommendations for optimizing production and improving operational efficiency.

![First_table](https://github.com/user-attachments/assets/6fff64d0-6d49-40d1-9d96-69011822c03a) 
![Other tables](https://github.com/user-attachments/assets/53103136-815c-4ae0-9c9b-5189d9a6e73a)

## [View Full Report](https://1drv.ms/x/c/b110de158371509c/EQONTWL8NnJNh2IP53C4jmAB0Cl42yPXDQ5ZeN4KhLeJXg?e=SRSjiC&nav=MTVfezY0MkIwRDE5LTExRUYtNDlDOS05NTc2LTJGMTAxOENFOTZDMn0)  

---

## Data Cleaning 

 Data cleaning was conducted before the analysis to ensure the reliability and accuracy of the dataset, as unclean data can lead to incorrect conclusions and misleading insights. This essential process addressed 
 inconsistencies, errors, and missing data points, providing a reliable foundation for decision-making. The cleaning involved removing duplicates, handling missing data, standardizing formats, correcting inconsistencies, 
 and fixing structural errors. By thoroughly preparing the data, a solid foundation was established for effective analysis and informed decision-making. The cleaning process for this report is detailed below:
 
#### 1. Supplier Quantity Sheet

- **Data Types**:  
  Columns were checked to ensure each field was of the correct type, such as integers for quantities and dates formatted correctly.

- **Missing or Incomplete Data**:  
  No blanks were detected.

- **Duplicates**:  
  No duplicate rows were found.

- **Invalid Data**:  
  In the *Total Downtime Minutes* column, one row contained a dash ("-"). Since this row represented less than 0.001% of the dataset, it was removed to avoid any negative impact on the analysis.

- **Inconsistencies in Naming**:  
  Similar entries, "Wrong Specifications" and "Wrong Spec", were found. The shorter entry, "Wrong Spec", was removed, and "Wrong Specifications" was retained to maintain consistency. This change was applied to both the Supplier Quantity and Defect tables.

- **Outliers**:  
  Key columns such as Date, Total Defect Quantity, Total Downtime Minutes, Total Downtime (Hours), and Unit Price were examined for outliers. No extreme values were found that would distort the analysis.

- **Conversion of Minutes to Hours**:  
  The *Total Downtime Minutes* column was converted to hours using the formula `minutes/60` for easier interpretation and comparison.

#### 2. Material Type, Defect Type, and Defect Sheets

- **Data Types**:  
  Columns in all sheets were reviewed to ensure that they were in the correct format, such as string values for names and integers for IDs.

- **Data Lookup and Merging**:  
  The *Supplier Quantity* sheet was enriched by importing data from the other sheets.  
  - **VLOOKUP** was used to bring the Material Type data into the Supplier Quantity sheet.
  - **XLOOKUP** was employed to merge Defect Type and Defect Classification data into the Supplier Quantity sheet. This avoided the need to reorder columns and allowed flexibility in data merging.

- **Final Adjustments**:  
  After merging the necessary data, columns were renamed for clarity, ensuring the final dataset was ready for analysis.

## Vendor Analysis Report

The vendor analysis was conducted using an Excel pivot table to evaluate the performance of various suppliers and their impact on production downtime and defects. An interactive dashboard was developed with slicers to allow users to filter the data by vendor, material type, and defect type. The analysis provided insights into which vendors were affecting production the most, which had the highest defect rates, and the financial implications of these defects.

![report1](https://github.com/user-attachments/assets/d1254e4a-a3ec-4750-a265-15e46fc5a144)

---

### Key Vendor Analysis Insights

#### 1. Which vendor is affecting production the most?
Vendor Avamm was identified as the main contributor to production downtime, with significantly higher downtime hours compared to other vendors. This vendor caused over **1164.82 hours** of production downtime.

#### 2. Top and Bottom 10 Vendors with Highest Downtime
Through the dashboard, a ranking of vendors was created to show the **Top 10 vendors** with the most downtime, which collectively accounted for a significant portion of total downtime. Conversely, the **Bottom 10 vendors** had minimal downtime, indicating their reliability.

#### 3. Which vendor has the highest quantity of defective raw materials supplied?
Vendor Yombu was flagged for supplying the highest quantity of defective raw materials, delivering **15.14 million defective units**. This resulted in considerable production inefficiencies. When defective raw materials that had no impact on production were filtered out, Yombu still topped the chart.

#### 4. Which vendor has the highest cost implications?
Vendor Yombu also caused the highest financial impact due to defects and downtime. The cost associated with downtime from this vendor was disproportionately higher compared to other vendors, which was expected as it had the highest defective raw materials.

#### 5. Which vendor has more downtime, and which category is the item?
Vendor Avamm had the most downtime hours, with **Mechanicals** being the category most affected.

### Additional Insights from Vendor Analysis

- **Top Plant Location by Vendor Count:** This analysis highlights the plant locations with the highest number of vendors supplying defective raw materials. Riverside leads with 199 vendors, followed closely by Charles City with 198. Twin Rocks and Hingham each have 194 vendors, while Chesaning has 188 vendors.
  
- **Interactive Filtering with Slicers:** Slicers were incorporated into the report to allow dynamic filtering by defect types, categories, years, and months. This interactive feature enables users to drill down into specific data points, such as analyzing the impact of particular defects over time or by category. This adds an extra layer of analysis and flexibility, allowing for deeper insights into vendor performance trends.

## Material, Defect, and Defect Type Analysis

The second part of the analysis focused on identifying the materials, defect types, and specific defects that have the greatest impact on production. This dashboard answered key questions about the role of materials and defects in downtime and production inefficiencies.

![Material and defect report](https://github.com/user-attachments/assets/b909506b-2b87-4615-8157-512786e70308)

---

### Material Analysis

#### 1. What materials are having a huge impact on production?
The dashboard highlighted that **Raw Materials** and **Batteries** are causing the highest production downtime. Raw Materials accounted for 10,441 hours of downtime, while Batteries followed closely with 10,334 hours, making them the most impactful materials.

#### 2. What quantity of these materials is affecting production?
**Raw Materials** contributed 124.12 million defective units, followed by Crates with 119.79 million defective units. Labels (118.34M), Electrolytes (118.24M), and Batteries (117.55M) also significantly affected production with high defect quantities.

#### 3. What is the trend pattern of the materials being defected?
A trend analysis of defect quantities over time showed that defects in raw materials peaked during certain months, indicating possible issues with the supplier or manufacturing processes during those periods. The trend analysis shows a rise in defective materials from 2018 to 2019:
- In 2018, defect quantities peaked in March (141.32M) and November (128.78M), totaling 1.16B units.
- In 2019, defects surged, especially in October (224.44M), with a total of 1.43B units, marking a clear increase compared to 2018.

#### 4. Is there any particular category that consistently faces more defects than others?
Logistics and Mechanicals consistently face the most defects, with totals of 698,671,504 and 820,838,675 respectively. Goods & Services also show significant defects at 196,577,588, while Electrical has 92,681,909. In contrast, Packaging and Materials/Comp have fewer defects at 443,769,697 and 345,384,184. This indicates a pressing need for quality improvement efforts, especially in Logistics and Mechanicals.

### Defect Type Analysis

#### 1. What is the quantity distribution of defect types?
The defect type distribution showed that **No Impact** accounted for the highest number of defective units, followed by **Impact** and lastly **Rejected**. No Impact had about 872.70 million quantities, Impact about 870.6 million, and Rejected 854 million.

#### 2. What downtime hours are attributed to each defect type?
The downtime hours associated with each defect type are as follows:
- Rejected defects led to the highest downtime, with 73,092.82 hours.
- No Impact defects resulted in 71,984.15 hours of downtime.
- Impact defects contributed 70,732.95 hours of downtime.
Rejected defects are the most time-consuming to address, closely followed by No-impact defects.

### Defect Analysis

#### 1. Which defect has the highest quantity affecting production?
The defect with the highest quantity affecting production was **Wrong Specification**, with a total of 18,053,647 defective units. This defect poses a significant issue for the business, disrupting production more than any other defect type.

#### 2. What is the top defect trending that the business should focus on?
The trend analysis reveals that **Wrong Specification** is the top defect consistently affecting production across quarters. Notably, in Qtr4 2019, this defect reached its peak with 4,601,877 defective units. The business should focus on improving specifications and communication with vendors to reduce this issue.

### Additional Insights from the Material and Defect Analysis

- **Interactive Filtering with Slicers:** Slicers were incorporated into the report to allow dynamic filtering by defect types, categories, years, and months. This interactive feature enables users to drill down into specific data points, such as analyzing the impact of particular defects over time or by category. This adds an extra layer of analysis and flexibility, allowing for deeper insights into vendor performance trends.

## Recommendations

Based on the findings from the vendor, material, and defect analyses, the following recommendations are proposed to optimize production efficiency, reduce downtime, and enhance supplier performance:

### 1. **Enhance Vendor Engagement**
   - Prioritize performance review meetings with high-downtime vendors like **Vendor Avamm** and **Vendor Yombu**. Implement performance agreements that include penalties for excessive defects and downtime.
### 2. **Conduct Regular Vendor Audits**
   - Establish a routine audit process for underperforming vendors to evaluate their quality control processes, especially those supplying **Raw Materials** and **Crates**, which showed significant defect quantities.
### 3. **Implement Quality Control Improvements**
   - Strengthen quality assurance checks for high-impact materials, particularly **Raw Materials** and **Batteries**, at both receiving and production stages to reduce defects entering the production line.
### 4. **Review and Update Material Specifications**
   - Collaborate with suppliers to revise material specifications and introduce stricter quality thresholds, specifically for categories with high defect rates.
### 5. **Optimize Supply Chain Management**
   - Maintain buffer stock for critical materials like **Crates** and **Raw Materials** to mitigate production disruptions caused by defective supplies.
### 6. **Focus on Mechanical Defects**
   - Invest in advanced monitoring systems for mechanical components, enhancing internal maintenance practices to address the highest sources of downtime and defect quantities.
### 7. **Conduct Root Cause Analysis**
   - Engage suppliers and internal teams in root cause analyses for logistics and packaging defects, identifying necessary process improvements and equipment upgrades to minimize these issues.
### 8. **Introduce Performance-Based Contracts**
   - Create performance-based contracts for vendors, tying payment terms to defect rates and downtime metrics, ensuring accountability for consistent performance.
### 9. **Utilize Total Cost of Ownership (TCO) Analysis**
   - Conduct TCO analyses to assess the true impact of vendor performance on costs, using insights to renegotiate contracts for better financial outcomes.
### 10. **Establish Real-Time Monitoring Systems**
   - Develop real-time dashboards to track key performance metrics, such as defect quantities and vendor performance, allowing for immediate intervention and quarterly performance reviews with all vendors.

**Conclusion:**
By implementing these recommendations, the business can expect to see a reduction in production downtime, improved vendor performance, and lower defect rates. A stronger focus on quality control, vendor collaboration, and real-time monitoring will help create a more efficient and resilient supply chain.



