# Superconductivity Modeling Playground

This project explores different ways to predict and classify the critical temperature (`critical_temp`) of superconducting materials using the UCI Superconductivity Dataset.

No deep learning. No black boxes. Just pure ML pipelines — the interpretable kind.

---

## Models we tried (so far):

1. **Linear Regression**  
   Your classic baseline. Surprisingly decent.

2. **Logistic Regression**  
   Binary classification: high-Tc vs low-Tc.  
   Also tested on top of linear regression outputs.

3. **Linear Regression with PCA**  
   Dimensionality reduction to explain 95% variance.  
   Slight drop in performance — expected tradeoff.

4. **Linear + Logistic (Stacked)**  
   Took predictions from linear regression and used them to train a logistic classifier — because why not.

5. **Linear with PCA + Logistic**  
   Same idea, but PCA-ed first. Worked okay, not magic.

6. **Decision Tree Regressor**  
   Basic tree model with limited depth. Just to test the structure.

7. **Random Forest Regressor**  
   Ensemble of trees. Better generalization, better feature insights.

---

## What we evaluated:
- **Regression**: R², MAE, RMSE  
- **Classification**: Accuracy, F1, Confusion Matrices  
- **Visuals**: Actual vs predicted, residuals, classification confidence, feature importances

---

## Binary target:
All classification tasks are based on whether `critical_temp ≥ 75`.  
1 = High-Tc, 0 = Low-Tc. Threshold can be changed easily.

---

## Why this notebook exists:
To experiment, test assumptions, and see how far classic models can go without overcomplicating things. Also, it's just satisfying to stack and compare them.

Nothing fancy, just trying to learn them better.
