# MIST4610-Group-Project-2

## Team Name:
21479 Group 3

## Team Members:
1. Isabel Villaca [@icvillaca](https://github.com/icvillaca)
2. Carson Farris [@carsonf17](https://github.com/carsonf17)
3. Phoebe Prescott [@phoebeprescott](https://github.com/phoebeprescott)
4. Alexa Persad [@aepersad](https://github.com/aepersad)

## Overview of Data Set: 




## Question 1:
### How have overdose death rates changed over time across different drug types, and which drug type has driven recent increases?
**Importance:** This question is important because it takes a closer look at how overdose death rates have evolved in comparison to specific drug types. Drug use patterns shift over time due to social and behavioral factors. Socially, the rise in overdose death rates affects communities and this data helps identify which drugs populations are struggling with. There are also behavioral usage changes that have evolved during different time periods. This data set allows for a greater understanding and breaks down which drugs were used more frequently during a certain time period. Overall, analyzing and identifying which drug type is contributing to a rise in death rates can help healthcare providers design better intervention and prevention resources.
**Analysis and Results:**

## Question 2:
### Which demographic groups (by age, race, or sex) have the highest overdose death rates, and how have these patterns changed over time? 
**Importance:** This is an important topic because this question illustrates real lives lost, not just statistics. By understanding how the death rates differ by age, race, or sex, we can see where the problem is the most severe. Then using that data, targeted efforts can be made to prevent overdoses. This matters because according to the data, drug overdose death rates are steadily increasing, meaning that without action, overdoses will continue to be one of the leading causes of preventable deaths in the United States.

**Analysis and Results:**
![image alt](https://github.com/icvillaca/MIST4610-Group-Project-2/blob/bde6330fed3e0f1bab5f11f38605f1eec23e8113/question2MIST.png) 
Based on the Tableau visualizations, the data reveals certain trends in overdose mortality in the U.S. from 1999 to 2018. Sheet 1 addresses how overdose deaths have affected males and females throughout the years. We can see that males have consistently died at around double the rate of females, with that gap widening after 2013 to 12 male deaths per 100k compared to the 6 female deaths for 100k. This significant difference likely stems from the stigma and lack of male treatment programs. According to the sheet 2 table, we can see that middle-aged adults are affected most by drug overdose mortalities. Between the ages of 35 and 54, the death rates are the highest at 8 deaths per 100k. Sheet 3 visualizes the overdose death rates by race. From this visualization we can see that the Native Hawaiian or Other Pacific Islander demographic group shows the highest death rate peak at 18-20 per 100k. This is followed by American Indian or Alaska native at around 8 per 100k. Native Hawaiian/Pacific Islander and American Indian/Alaska Native communities face rates 2–4x higher than the national average. These groups are more susceptible to drug overdoses because of underrepresentation in mainstream treatment programs and other barriers including geographic isolation and underfunded health facilities. Across all these groups, we can see how the overdose death rates continuously increase throughout the years. There is also a significant spike around 2012-2013, which correlates with the opioid epidemic in the United States. Ultimately, the data illustrates that overdose mortality is not uniform, but varies depending on demographics like age, sex, and race. Visualizing these inequities is important to account for who is most at risk and why, so targeted interventions can be made to prevent drug overdoses.












## Appendix: Data Cleaning Manipulations

| # | Type | Original | Change |
|---|------|----------|--------|
| 1 | Rename | `PANEL` | Renamed to `Drug_Type` |
| 2 | Rename | `YEAR` | Renamed to `Year` |
| 3 | Rename | `AGE` | Renamed to `Age_Group` |
| 4 | Rename | `ESTIMATE` | Renamed to `Death_Rate_Per_100k` |
| 5 | Rename | `UNIT` | Renamed to `Rate_Type` |
| 6 | Rename | `FLAG` | Renamed to `Unreliable_Flag` |
| 7 | Recode | `UNIT` value | "Deaths per 100,000 resident population, age-adjusted" shortened to "Age-Adjusted" |
| 8 | Recode | `UNIT` value | "Deaths per 100,000 resident population, crude" shortened to "Crude" |
| 9 | Recode | `FLAG` value | Blank/null values recoded to "Reliable" |
| 10 | Recode | `FLAG` value | `*` values recoded to "Unreliable (*)" |
| 11 | Split | `STUB_LABEL` | Parsed into new `Sex` column |
| 12 | Split | `STUB_LABEL` | Parsed into new `Race` column |
| 13 | Split | `STUB_LABEL` | Parsed into new `Hispanic_Origin` column |
| 14 | Fill | `Sex` | Empty values filled with "All" |
| 15 | Fill | `Race` | Empty values filled with "All" |
| 16 | Fill | `Hispanic_Origin` | Empty values filled with "All" |
| 17 | Derive | `STUB_NAME` | New `Race_Classification` column created from existing values |
| 18 | Drop | `INDICATOR` | Removed — same value on every row |
| 19 | Drop | `PANEL_NUM` | Removed — redundant numeric sort key |
| 20 | Drop | `UNIT_NUM` | Removed — redundant numeric sort key |
| 21 | Drop | `STUB_NAME` | Removed — replaced by split columns |
| 22 | Drop | `STUB_NAME_NUM` | Removed — redundant numeric sort key |
| 23 | Drop | `STUB_LABEL` | Removed — replaced by split columns |
| 24 | Drop | `STUB_LABEL_NUM` | Removed — redundant numeric sort key |
| 25 | Drop | `YEAR_NUM` | Removed — redundant numeric sort key |
| 26 | Drop | `AGE_NUM` | Removed — redundant numeric sort key |

