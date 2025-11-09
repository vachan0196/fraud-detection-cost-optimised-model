# Fraud Detection – Cost-Optimised Model  

**Business-aligned credit card fraud detection with cost-based thresholding (FN = 100× FP).**

## Summary  
Fraudulent card transactions pose significant financial and reputational risk. Conventional ML focuses on accuracy; this project prioritises *loss reduction*. We evaluated Logistic Regression, XGBoost and Random Forest, and selected operating threshold **0.025** for the final model to reduce expected cost by ≈ 90% vs default threshold.

## Approach  
- Balanced synthetic credit-card dataset (50% fraud) used for demonstration  
- Models tested: Logistic Regression, XGBoost, Random Forest  
- Cost function defined: `Loss = FN×100 + FP×1`  
- Threshold sweep performed → minimum cost at t = 0.025 (Random Forest)  
- Explainability via permutation importance & SHAP → Key drivers: V14, V12, V17, V10 (low ↑ risk) & V4 (high ↑ risk)  
- Leakage noted: `ID` feature excluded for production integrity

## Outcome  
- Selected Model: Random Forest  
- Operating Threshold: **0.025**  
- Key Business Result: Expected loss reduced by ≈ 90% vs default threshold  
- Recommendation: Deploy with human–review for borderline cases; retrain regularly

## Repo Structure  
