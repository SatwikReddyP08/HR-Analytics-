# HR Analytics - Predicting Employee Attrition

## Objective
Predict employee attrition and identify key drivers using HR data, as part of Elevate Labs' Phase 2 internship project.

## Dataset
- **hr_data.csv**: HR dataset (1,470 rows, 35 columns), including:
  - `Attrition`: Target variable (Yes/No, ~16% Yes).
  - Key features: `MonthlyIncome` (1,009–19,999), `Department` (Sales, R&D, HR), `YearsAtCompany` (0–40), `OverTime` (Yes/No).
  - No missing values.
  - Dropped columns: `EmployeeCount`, `StandardHours`, `Over18`, `EmployeeNumber` (constant or irrelevant).

## Tools
- **Python**: Pandas, Scikit-learn, SHAP, Seaborn for EDA, modeling, and explainability.
- **Power BI**: Interactive dashboard with default visuals.
- **Google Colab**: Notebook execution.
- **GitHub**: Repository hosting.


## File Structure
- `hr_data.csv`: Raw dataset
- `attrition_analysis.ipynb`: Python notebook (EDA, preprocessing, model, SHAP)
- `attrition_dashboard.pbix`: Power BI dashboard file
- `attrition_dashboard.png`: Dashboard screenshot
- `attrition_report.pdf`: Final report
- `README.md`: This file

## How to Run
1. Clone this repository
2. 2. **Python Analysis**:
- Open `attrition_analysis.ipynb` in Google Colab.
- Upload `hr_data.csv`.
- Run all cells to reproduce EDA, model training, and SHAP analysis.
3. **Power BI Dashboard**:
- Open `attrition_dashboard.pbix` in Power BI Desktop.
- Interact with visuals and slicers to explore attrition trends.
4. **View Report**:
- Open `attrition_report.pdf` for a summary of findings.

## Insights
1. Only 16% of employees leave, indicating an imbalanced dataset that biases the model toward predicting No.
2. Employees who leave have lower salaries (median ~4,000 vs 7,000), highlighting salary as a key attrition driver.
3. Sales department has the highest attrition rate (~20%), suggesting a need for retention strategies like bonuses.
4. Employees with <5 years at the company (especially 0–3 years) are more likely to leave, indicating onboarding issues.
5. Overtime work is associated with higher attrition (~30% for OverTime=Yes), suggesting workload reductions could help.
6. The model accurately predicts employees who stay (e.g., 230/247 No) but struggles with leavers (e.g., 20/47 Yes) due to imbalance.
7. SHAP analysis confirms low `MonthlyIncome` and `OverTime`=Yes as top attrition drivers, guiding HR to focus on salary and workload.

## Learnings
- **EDA Skills**: Used Seaborn to visualize distributions and relationships (e.g., box plots, histograms).
- **Machine Learning**: Handled imbalanced data with Logistic Regression, evaluated with confusion matrix, and added a bonus prediction.
- **Explainability**: Applied SHAP to interpret model predictions, identifying actionable drivers.
- **Power BI**: Built an interactive dashboard with default visuals, adapting to personal account limitations (no marketplace access).

- **Challenges Overcome**:
- Encoded categorical variables (`get_dummies`) and scaled features for modeling.
- Managed imbalanced data by focusing on confusion matrix insights.
- Used default Power BI visuals (e.g., clustered bar chart instead of box plot) due to license constraints.

## Author
Satwik Reddy Pathapati  
[GitHub Profile](https://github.com/SatwikReddyP08)  
[LinkedIn Profile](http://www.linkedin.com/in/pathapati-satwik-reddy)  
Completed as part of Elevate Labs Internship, May 2025.

## Acknowledgments
- Elevate Labs for the project opportunity.
- Online resources (Kaggle, Stack Overflow) for learning SHAP and Power BI.
