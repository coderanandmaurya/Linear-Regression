Here is a curated list of 30 challenging linear regression questions for a viva, covering simple, multiple, polynomial, and regularization concepts, along with equations where applicable:

---

### **Simple & Multiple Linear Regression**
1. **Assumptions**: State the key assumptions of simple linear regression.  
   *Answer*: Linearity, independence, homoscedasticity, normality of errors, and no multicollinearity (for multiple regression).

2. **OLS Derivation**: Derive the OLS estimator for the slope (β₁) in simple linear regression.  
   *Answer*: Minimize Σ(yᵢ - β₀ - β₁xᵢ)²; solve ∂/∂β₀ and ∂/∂β₁ to get:  
   β₁ = Σ(xᵢ - x̄)(yᵢ - ȳ) / Σ(xᵢ - x̄)².

3. **R-squared Interpretation**: How is R² calculated, and what does it measure?  
   *Answer*: R² = 1 - (RSS/TSS), where RSS = Σ(yᵢ - ŷᵢ)² and TSS = Σ(yᵢ - ȳ)². It represents the proportion of variance explained.

4. **R-squared in Multiple Regression**: Why does R² always increase when adding a predictor?  
   *Answer*: Adding variables reduces RSS, even if the predictor is irrelevant. Adjusted R² addresses this.

5. **Multicollinearity**: Explain its impact on coefficients.  
   *Answer*: Inflates standard errors, causing unstable coefficient estimates.

6. **VIF Calculation**: How is Variance Inflation Factor (VIF) computed? What VIF indicates severe multicollinearity?  
   *Answer*: VIF = 1 / (1 - Rⱼ²), where Rⱼ² is from regressing predictor j on others. VIF > 10 indicates severe issues.

---

### **Polynomial Regression**
7. **Linear Model Justification**: Why is polynomial regression a "linear" model?  
   *Answer*: Linear in coefficients (e.g., y = β₀ + β₁x + β₂x² + ε).

8. **Overfitting Risk**: How does increasing polynomial degree lead to overfitting?  
   *Answer*: Higher degrees fit noise, increasing variance and reducing generalization.

9. **Equation for Degree 2**: Write the equation for quadratic regression.  
   *Answer*: y = β₀ + β₁x + β₂x² + ε.

---

### **Regularization**
10. **Ridge vs. Lasso**: Write their cost functions and explain penalties.  
    *Answer*:  
    - Ridge: RSS + λΣβⱼ² (L2 penalty).  
    - Lasso: RSS + λΣ|βⱼ| (L1 penalty).  
    Lasso performs feature selection by shrinking coefficients to zero.

11. **Elastic Net**: Write its cost function.  
    *Answer*: RSS + λ[(1 - α)Σβⱼ² + αΣ|βⱼ|], where α balances L1/L2 penalties.

12. **Lambda (λ) Effect**: How does increasing λ in Ridge affect coefficients?  
    *Answer*: Coefficients shrink toward zero, reducing variance but increasing bias.

13. **Feature Scaling**: Why is scaling critical for regularized regression?  
    *Answer*: Penalties apply equally to all coefficients; unscaled features dominate the penalty term.

---

### **Model Evaluation & Diagnostics**
14. **Adjusted R²**: How does it differ from R²?  
    *Answer*: Adjusts for predictors: 1 - [(1 - R²)(n - 1)/(n - k - 1)], penalizing irrelevant predictors.

15. **F-test**: What does it test in regression?  
    *Answer*: Tests if at least one predictor has a non-zero coefficient: F = (Explained Variance)/(Unexplained Variance).

16. **MAE vs. RMSE**: Differentiate their sensitivity to outliers.  
    *Answer*: RMSE squares errors (penalizes large errors more), while MAE uses absolute values.

---

### **Advanced Concepts**
17. **Gauss-Markov Theorem**: State its conclusion.  
    *Answer*: Under assumptions, OLS estimators are BLUE (Best Linear Unbiased Estimators).

18. **Hat Matrix**: Define and interpret its diagonal elements.  
    *Answer*: H = X(XᵀX)⁻¹Xᵀ. Diagonal entries (leverages) measure influence of observations.

19. **Cook’s Distance**: What does it identify?  
    *Answer*: Measures influence of a data point on regression coefficients. Values > 1 suggest high influence.

20. **Interaction Terms**: Interpret β₃ in y = β₀ + β₁X₁ + β₂X₂ + β₃X₁X₂ + ε.  
    *Answer*: The effect of X₁ on y increases by β₃ for each unit increase in X₂ (and vice versa).

---

### **Optimization & Algorithms**
21. **Normal Equation**: Write the matrix form for OLS.  
    *Answer*: β = (XᵀX)⁻¹Xᵀy, where X is the design matrix.

22. **Gradient Descent Types**: Contrast batch and stochastic GD.  
    *Answer*: Batch uses all samples per update; stochastic uses one sample, speeding convergence on large data.

---

### **Troubleshooting**
23. **Heteroscedasticity**: How to detect and address it?  
    *Answer*: Use residual plots or Breusch-Pagan test; apply transformations or robust SEs.

24. **Omitted Variable Bias**: Define and explain its impact.  
    *Answer*: Excluding a relevant predictor correlated with included variables biases coefficients.

25. **Outliers**: How do they affect regression?  
    *Answer*: High-leverage points disproportionately influence slope estimates.

---

### **Practical Application**
26. **Categorical Variables**: How to include a 3-level categorical predictor?  
    *Answer*: Use dummy coding (e.g., two binary variables for three levels).

27. **Validation Set Purpose**: Why use it?  
    *Answer*: Tune hyperparameters (e.g., λ, polynomial degree) and prevent overfitting.

---

### **Equations Quick Reference**
28. **Cost Functions**:  
    - Ridge: $\text{RSS} + \lambda \sum_{j=1}^p \beta_j^2$  
    - Lasso: $\text{RSS} + \lambda \sum_{j=1}^p |\beta_j|$

29. **Interaction Model**: $y = \beta_0 + \beta_1X_1 + \beta_2X_2 + \beta_3X_1X_2 + \epsilon$

30. **Polynomial Model (Degree 3)**: $y = \beta_0 + \beta_1x + \beta_2x^2 + \beta_3x^3 + \epsilon$

---
