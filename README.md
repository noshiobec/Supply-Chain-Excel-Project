# Supply-Chain-Excel-Project

## Project Overview

This analysis seeks to explore and identify the key vendors and material defects affecting the operational performance of XYZ Production Company, particularly focusing on the years 2018 and 2019. Recent observations indicate a decline in customer satisfaction due to a low supply of original raw materials, leading to decreased patronage and threatening the business's survival. The objective is to highlight areas where improvement is needed to minimize downtime, defects, and overall cost implications.

A comprehensive supply chain dataset will be analyzed, containing defect quantities, unit prices, and downtime caused by various vendors across existing plant locations. This dataset is organized into four key sheets as shown diagram below in the below: Supplier Quality, Material Type, Defect Type, and Defect. Through data cleaning, vendor performance metrics, and material analysis, actionable insights into vendor reliability and product quality will be provided. Additionally, the analysis will focus on identifying which products have the most significant impact on operations. Interactive reports with slicers and filters will facilitate dynamic data exploration, ultimately leading to recommendations for optimizing production and improving operational efficiency.

![First_table](https://github.com/user-attachments/assets/6fff64d0-6d49-40d1-9d96-69011822c03a) 
![Other tables](https://github.com/user-attachments/assets/53103136-815c-4ae0-9c9b-5189d9a6e73a)

## [View Full Report](https://1drv.ms/x/c/b110de158371509c/EQONTWL8NnJNh2IP53C4jmAB0Cl42yPXDQ5ZeN4KhLeJXg?e=O3cB6f)  

---

## Data Cleaning Report

### Why Data Cleaning is Important?

Data cleaning is an essential part of the analysis process because unclean data can lead to incorrect conclusions and misleading insights. Cleaning the dataset ensures that all inconsistencies, errors, and missing data points are addressed, providing a reliable foundation for decision-making. Without cleaning, issues such as duplicate records, invalid entries, and structural errors could skew the analysis, leading to inaccurate visualizations and recommendations.

---

### Data Cleaning Process

This report outlines the data cleaning process undertaken to prepare the dataset for analysis. The dataset consists of four sheets: **Supplier Quantity**, **Material Type**, **Defect Type**, and **Defect**. Each sheet was systematically reviewed using a comprehensive checklist to ensure the data's accuracy and consistency.

#### Data Cleaning Checklist
- **Remove duplicates**
- **Handle missing data**
- **Standardize formats**
- **Correct inconsistencies**
- **Remove irrelevant data**
- **Fix structural errors**
- **Validate accuracy**
- **Address outliers**
- **Correct data types**
- **Document cleaning steps**

---

### Sheet-by-Sheet Cleaning

#### 1. Supplier Quantity

- **Vendor Name Issue**:  
  Two similar entries, "Abata" and "abatz", were flagged for potential duplication. Further investigation or contact with the data owner was needed to clarify if these refer to the same vendor.

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

---

## Vendor Analysis Report

The vendor analysis was conducted using Excel to evaluate the performance of various suppliers and their impact on production downtime and defects. An interactive dashboard was developed with slicers to allow users to filter the data by vendor, material type, and defect type. The analysis provided insights into which vendors were affecting production the most, which had the highest defect rates, and the financial implications of these defects.

![report1](https://github.com/user-attachments/assets/d1254e4a-a3ec-4750-a265-15e46fc5a144)  <!-- Insert first report pic here -->

---

### Key Vendor Analysis Insights

#### 1. **Which vendor is affecting production majorly?**
Vendor A was identified as the main contributor to production downtime, with significantly higher downtime hours compared to other vendors. This vendor caused over **10,441 hours** of production downtime, largely due to defects in raw materials.

#### 2. **Top and Bottom 10 Vendors with Highest Downtime**
Through the dashboard, a ranking of vendors was created to show the **Top 10 vendors** with the most downtime, which collectively accounted for a significant portion of total downtime. Conversely, the **Bottom 10 vendors** had minimal downtime, indicating their reliability.

#### 3. **Which vendor has the highest defective raw materials being supplied?**
Vendor C was flagged for supplying the highest quantity of defective raw materials, delivering **124.12 million defective units**. This resulted in considerable production inefficiencies.

#### 4. **Which vendor has the highest cost implications?**
Vendor B caused the highest financial impact due to defects and downtime. The cost associated with downtime from this vendor was disproportionately higher compared to other vendors, despite not having the longest downtime in hours.

#### 5. **Which vendor has more downtime, and which category is the item?**
Vendor A had the most downtime hours, with **Raw Materials** being the category most affected. Other categories such as **Crates** and **Labels** also contributed but to a lesser extent.

---

### Additional Insights from Vendor Analysis

- **Defect Trends Over Time:** A trend analysis revealed that certain vendors caused more downtime during specific months, suggesting operational or seasonal issues that need to be addressed.
  
- **Category Performance Comparison:** Vendors supplying packaging materials had fewer defects and downtime compared to those supplying raw materials, indicating stronger performance.

- **Impact by Defect Type:** Different defect types impacted vendors differently. For instance, Vendor D had frequent labeling issues, which, although minor, caused repeated production delays.

---

## Material, Defect, and Defect Type Analysis

The second part of the analysis focused on identifying the materials, defect types, and specific defects that have the greatest impact on production. This dashboard answered key questions about the role of materials and defects in downtime and production inefficiencies.


![Material and defect report](https://github.com/user-attachments/assets/b909506b-2b87-4615-8157-512786e70308)

---

### Material Analysis

#### 1. **What materials are having a huge impact on production?**
The dashboard highlighted that **Raw Materials** and **Crates** were the materials causing the highest production downtime, contributing significantly to the total downtime hours.

#### 2. **Of what quantity are these materials affecting production?**
**Raw Materials** contributed over **124.12 million defective units**, followed by **Crates** with **119.79 million defective units**, both heavily impacting production.

#### 3. **What is the trend pattern of the materials being defected?**
A trend analysis of defect quantities over time showed that defects in raw materials peaked during certain months, indicating possible issues with the supplier or manufacturing processes during those periods.

#### 4. **Is there any particular category that consistently faces more defects than others?**
The **Raw Materials** category consistently had higher defect rates across various vendors, making it a priority for quality control and vendor management interventions.

---

### Defect Type Analysis

#### 1. **What is the quantity distribution of defect types?**
The defect type distribution showed that **Mechanical defects** accounted for the highest number of defective units, followed by **Logistics and Packaging defects**. Mechanical defects alone contributed **820.8 million defective units**, significantly impacting production.

#### 2. **What downtime hours are attributed to each defect type?**
Mechanical defects also caused the most downtime, with over **10,441 hours** lost due to this defect type, making it the most critical area to address.

---

### Defect Analysis

#### 1. **Which defect has the highest quantity affecting production?**
**Mechanical defects** were identified as having the highest quantity of defective units, posing the greatest threat to production continuity.

#### 2. **What is the top defect trending that the business should focus on?**
The trend analysis showed that **Mechanical and Logistics defects** are the top trending issues, consistently recurring across various vendors and time periods. The business should prioritize resolving these defects through vendor engagement and improved quality control processes.

---

### Additional Insights from the Material and Defect Analysis

- **Impact of Electrical Components:** Although not the highest in terms of defective quantity, **Electrical components** caused significant downtime compared to their defect rate, suggesting they require closer attention in terms of quality assurance.
  
- **Consistent Defect Sources:** Certain vendors were flagged for consistently supplying defective goods across multiple categories, making them high-risk suppliers.

---
## Recommendations

Based on the findings from the vendor, material, and defect analyses, the following recommendations are proposed to optimize production efficiency, reduce downtime, and enhance supplier performance:

### 1. **Vendor Performance Improvement Strategies**
   - **Engage with High-Downtime Vendors:** Vendors such as Vendor A and Vendor C, which caused the most downtime and supplied the highest quantity of defective materials, should be prioritized for performance review meetings. Implement vendor performance agreements that include penalties for excessive defects or downtime.
   - **Vendor Quality Audits:** Conduct regular audits on underperforming vendors. This should focus on quality control processes at their facilities, particularly those related to **Raw Materials** and **Crates**, which had the highest defect quantities.
   - **Vendor Tiering:** Establish a tiered vendor management system, rewarding high-performing vendors with better contracts and penalizing those with consistently high downtime or defect rates.

### 2. **Material and Supply Chain Optimization**
   - **Improve Quality Control for Raw Materials:** Since raw materials have the largest impact on downtime and defect quantities, enhancing the quality checks at both the receiving and production stages can help reduce the incidence of defective materials entering the production line.
   - **Review Material Specifications:** Collaborate with vendors to review and possibly update material specifications, particularly for categories like **Raw Materials** and **Crates**. Consider introducing stricter quality thresholds to minimize defects.
   - **Implement Buffer Stock for High-Impact Materials:** For materials such as **Crates** and **Raw Materials**, where defects lead to significant downtime, consider maintaining a buffer stock to mitigate the effects of delays caused by defective supplies.

### 3. **Defect Management and Prevention**
   - **Focus on Mechanical Defects:** Mechanical defects contributed to the highest downtime hours and defect quantities. The business should focus on improving its internal maintenance and quality control systems. Invest in advanced monitoring systems that flag issues early, allowing preventive measures to be taken before major downtimes occur.
   - **Target Recurring Defect Types:** Logistics and packaging defects also emerged as significant contributors to production issues. Engaging both the suppliers and internal teams in root cause analysis for these defects will help identify process improvements and equipment upgrades needed to reduce their occurrence.

### 4. **Improve Vendor Contracting and Cost Management**
   - **Performance-Based Contracts:** Introduce performance-based contracts for vendors, where payment terms or contract renewals are tied to meeting defect rate and downtime targets. Vendors who continually underperform should face penalties or have their contracts reconsidered.
   - **Total Cost of Ownership (TCO) Analysis:** Conduct a thorough TCO analysis to assess the real impact of vendor performance, factoring in defect rates, downtime, and the financial implications of delays. Use this data to renegotiate vendor contracts to ensure cost efficiencies.
   
### 5. **Enhanced Data Monitoring and Reporting**
   - **Establish Real-Time Dashboards:** Implement real-time data tracking for critical metrics such as defect quantities, downtime, and vendor performance. The interactive dashboard built in this analysis should be expanded to track these metrics in real-time, allowing management to intervene immediately when issues arise.
   - **Regular Performance Reviews:** Schedule quarterly performance reviews with all vendors using the dashboard insights to track progress. This will ensure that both vendors and internal teams are aligned in reducing defects and downtime.

### 6. **Collaboration with Vendors on Process Improvements**
   - **Joint Improvement Initiatives:** Work closely with high-impact vendors to co-develop process improvements aimed at reducing defect rates. This could include joint investment in technology, training, or lean manufacturing initiatives that benefit both parties.
   - **Vendor Training Programs:** Offer training programs for vendors on the specific quality issues identified, such as mechanical defects and packaging problems. This will ensure that suppliers are equipped to meet the company’s stringent quality standards.

### 7. **Production Process Adjustments**
   - **Process Redesign for Defect-Prone Materials:** Review the production processes related to **Raw Materials**, **Crates**, and **Labels**. Evaluate whether certain stages can be automated or made more efficient to reduce the impact of defects on the overall production process.
   - **Preventative Maintenance Programs:** Given the significant downtime caused by mechanical defects, implementing a robust preventative maintenance program can help mitigate production disruptions. Regular machine inspections and maintenance scheduling should be prioritized.

---

**Conclusion:**
By implementing these recommendations, the business can expect to see a reduction in production downtime, improved vendor performance, and lower defect rates. A stronger focus on quality control, vendor collaboration, and real-time monitoring will help create a more efficient and resilient supply chain.



