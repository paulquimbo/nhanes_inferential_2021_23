# NHANES Data Analysis Project

This project explores relationships between demographic, behavioral, and health variables using data from the National Health and Nutrition Examination Survey (NHANES). The analyses are conducted in **Google Colab**, with each step documented and explained following the structure used in class notebooks.

## Project Objective

To investigate associations and differences between key health and demographic variables using appropriate statistical methods. The project includes both guided questions and one creative analysis developed independently.

---

## Questions and Analysis

### **Question 1** 
**Is there an association between marital status and education level?**  
- **Variables**: `DMDMARTZ` (Marital Status), `DMDEDUC2` (Education Level)  
- **Recoding**:
  - DMDMARTZ: Cleaned to remove invalid codes (77, 99)
  - Education level: Bachelor's degree or higher vs Less than bachelor's
- **Test Used**: Chi-square test of independence  
- **Purpose**: To determine whether marital status is associated with educational attainment.

- **Analysis** : Married individuals were more likely to have a bachelor’s degree or higher compared to single or widowed/divorced/separated individuals. This suggests that marital status and education level are meaningfully related in your sample data.

---

### **Question 2**  
**Is there a difference in mean sedentary behavior time between married and non-married individuals?**  
- **Variables**: `DMDMARTZ` (Marital Status), `PAD680` (Sedentary Behavior Time)  
- **Recoding**:
  - DMDMARTZ: Cleaned to remove invalid codes (77, 99)
  - PAD680: Cleaned to remove invalid codes (7777, 9999)
- **Test Used**: ANOVA
- **Purpose**: To compare average sedentary time between marital groups.

- **Analysis** : The analysis found a statistically significant difference in average sedentary behavior time across marital status groups. Single individuals had the highest mean sedentary time (382.43 minutes), followed by widowed/divorced/separated (363.46 minutes), and married individuals had the lowest (353.29 minutes). The result suggests that marital status may be associated with differences in sedentary behavior.

---

### **Question 3**  
**How do age and marital status affect systolic blood pressure?**  
- **Variables**: `RIDAGEYR` (Age), `DMDMARTZ` (Marital Status), `BPXOSY3` (Systolic BP)  
- **Recoding**:
  - DMDMARTZ: Cleaned to remove invalid codes (77, 99)
  - **Test Used**: ANOVA  
- **Purpose**: To assess the interaction and individual effects of age and marital status on blood pressure.

- **Analysis** : There is a statistically significant difference in average systolic blood pressure (BPXOSY3) across marital status groups. Widowed/divorced/separated individuals had the highest mean (126.14 mmHg), followed by married (122.61 mmHg), while single individuals had the lowest (118.85 mmHg). The result suggests marital status may be associated with variations in blood pressure.

---

### **Question 4**  
**Is there a correlation between self-reported weight and minutes of sedentary behavior?**  
- **Variables**: `WHD020` (Weight), `PAD680` (Sedentary Behavior Time)  
- **Cleaning**:
  - PAD680: Cleaned to remove invalid codes (7777, 9999)
  - WHD020: Cleaned to remove invalid codes (7777, 9999)
- **Test Used**: Correlation  
- **Purpose**: To measure the strength and direction of the relationship between weight and sedentary time.

- **Analysis** : The correlation between sedentary behavior time and self-reported weight was 0.16, indicating a very weak positive relationship. This suggests that individuals who spend more time being sedentary tend to weigh slightly more, but the association is minimal and likely not practically significant.


---

### **Question 5 (Creative Analysis)**  
**Is there an association between marital status and frequency of depressive symptoms?**  
I chose this question because, as someone who is married, I was curious whether people of different marital statuses experience similar emotional challenges. It helped me connect personal experience with a broader mental health issue using data.

- **Variables**: `DMDMARTZ` (Marital Status), `DPQ020` (Depressive Symptoms Frequency)  
- **Recoding**:
  - DMDMARTZ: Cleaned to remove invalid codes (77, 99)
  - DPQ020: Cleaned to remove invalid codes (7, 9)
- **Test Used**: Chi-square test of independence  
- **Purpose**: To explore whether depressive symptom frequency varies across marital status groups.

- **Analysis** : The chi-square test shows a statistically significant association between marital status and depressive symptoms (χ² = 157.03, p < 0.0001). Married individuals were more likely to report “Not at all” or “Several days” of depressive symptoms, while single and widowed/divorced/separated individuals had higher counts in the “More than half the days” and “Nearly every day” categories. This suggests that marital status may be linked to how frequently people experience depressive symptoms.

---

## How to Run

1. Open the notebook in [Google Colab](https://colab.research.google.com).
2. Upload the required NHANES datasets (`DEMO_L.xpt`, `WHQ_L.xpt`, `DPQ_L.xpt`, etc.).
3. Follow the documented steps in each analysis cell.
4. Review outputs and visualizations for interpretation.

---

## Notes

- All variables are cleaned and recoded as needed before analysis.
- Used R to convert .xpt files to csv
- Statistical tests are chosen based on variable types and research questions.
- Visualizations (boxplots, count plots, scatterplots) are included to support interpretation.

---