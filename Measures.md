# Key Measures Created for HR Dashboard

1. **Total Employees**
   - Formula: `COUNT(EmployeeID)`
   - Purpose: Calculates the total number of employees in the dataset.

2. **On-Service Employees**
   - Formula: `CALCULATE(COUNT(EmployeeID), Filter(Status = "Active"))`
   - Purpose: Tracks the total number of employees currently active in the organization.

3. **Gender Distribution**
   - Male Count: `CALCULATE(COUNT(EmployeeID), Filter(Gender = "Male"))`
   - Female Count: `CALCULATE(COUNT(EmployeeID), Filter(Gender = "Female"))`
   - Percentage Male: `DIVIDE([Male Count], [Total Employees], 0)`
   - Percentage Female: `DIVIDE([Female Count], [Total Employees], 0)`
   - Purpose: Provides insights into the gender breakdown of the workforce.

4. **Employees Due for Promotion**
   - Formula: `CALCULATE(COUNT(EmployeeID), Filter(PromotionStatus = "Due"))`
   - Purpose: Identifies the number of employees eligible for promotion.

5. **Retrenchment Forecast**
   - Formula: `CALCULATE(COUNT(EmployeeID), Filter(RetrenchmentProbability > 0.5))`
   - Purpose: Predicts the number of employees at high risk of retrenchment based on specified thresholds.

6. **Job Satisfaction Levels**
   - High Satisfaction: `CALCULATE(COUNT(EmployeeID), Filter(JobSatisfaction = "High"))`
   - Medium Satisfaction: `CALCULATE(COUNT(EmployeeID), Filter(JobSatisfaction = "Medium"))`
   - Low Satisfaction: `CALCULATE(COUNT(EmployeeID), Filter(JobSatisfaction = "Low"))`
   - Purpose: Analyzes workforce morale and highlights areas needing improvement.

7. **Performance Ratings**
   - High Performance: `CALCULATE(COUNT(EmployeeID), Filter(PerformanceRating = "High"))`
   - OK Performance: `CALCULATE(COUNT(EmployeeID), Filter(PerformanceRating = "OK"))`
   - Low Performance: `CALCULATE(COUNT(EmployeeID), Filter(PerformanceRating = "Low"))`
   - Purpose: Measures the distribution of employee performance ratings.

8. **Department-Level Insights**
   - Promotions by Department: `CALCULATE(COUNT(EmployeeID), Filter(PromotionStatus = "Due" && Department = SelectedDepartment))`
   - Retrenchment by Department: `CALCULATE(COUNT(EmployeeID), Filter(RetrenchmentProbability > 0.5 && Department = SelectedDepartment))`
   - Purpose: Provides department-specific breakdowns for actionable insights.

9. **Average Service Years**
   - Formula: `AVERAGE(ServiceYears)`
   - Purpose: Highlights the average tenure of employees in the organization.

10. **Distance to Workplace Analysis**
    - Very Close: `CALCULATE(COUNT(EmployeeID), Filter(DistanceStatus = "Very Close"))`
    - Close: `CALCULATE(COUNT(EmployeeID), Filter(DistanceStatus = "Close"))`
    - Very Far: `CALCULATE(COUNT(EmployeeID), Filter(DistanceStatus = "Very Far"))`
    - Purpose: Analyzes the commuting distances of employees for workforce planning.
