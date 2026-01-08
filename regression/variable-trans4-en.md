# Variable Transformation (Variance-Stabilizing Transformation)
---
# ■ Log Transformation

The log transformation is one of the most widely used variable transformations in regression analysis.  
This method uses log(Y) instead of Y as the response variable, and among its various effects, we will focus here on its impact on variance stabilization.

Let’s examine how the variance changes when log(Y) is applied.

![KakaoTalk_20250508_231626551](https://github.com/user-attachments/assets/a89c461b-ad19-40da-88d6-8e6b194e1212)

## As shown in the image, the variance is inversely proportional to the expected value \( M_i \).  
In the previously discussed sqrt transformation, the variance was constant, thereby satisfying the homoskedasticity assumption.  
However, in this case, it does not strictly meet the condition of homoskedasticity.

Still, the variance of log(Y) becomes significantly smaller than that of Y,  
and thus, to a certain extent, it can reproduce a condition where homoskedasticity is approximately satisfied.  
The following table illustrates how the magnitude of Var(Y) and Var(log(Y)) changes.

![KakaoTalk_20250508_231626551_01](https://github.com/user-attachments/assets/081b5f81-591c-41d5-8fcb-6c6a3befa68e)

While Var(Y) changes drastically, Var(log(Y))—due to its inverse relationship—decreases gradually but remains relatively stable in magnitude.  
Hence, we can consider that the assumption of homoskedasticity is approximately satisfied, at least in a weak sense.
