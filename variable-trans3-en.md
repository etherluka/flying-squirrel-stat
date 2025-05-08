# Variable Transformation (Variance Stabilizing Transformation)
---
## ■ Creating a Relationship Between the Error Term and X<sub>i</sub>

If we try to express a heteroscedastic relationship under the assumption of homoscedasticity,

Var(εᵢ)= σ<sub>i</sub><sup>2</sup>
       = σ<sup>2</sup> h(x<sub>i</sub>)

we can express it as above.  
In this case, various forms can be used for h(x<sub>i</sub>),  
but we most often use the form x<sub>i</sub><sup>2</sup>, which is the cleanest to compute.  
(This is used when a '<'-shaped heteroscedasticity appears, where the variance increases as x<sub>i</sub> increases)

Through the image below, we establish the relationship between the error term and X<sub>i</sub> and examine how this is applied in the OLS model.

![KakaoTalk_20250508_222340657](https://github.com/user-attachments/assets/35d4c0c7-d96a-4352-91fc-f758b5cdd866)

One important note is,
## The regression coefficient interpretation that reveals the actual relationship between y and x must refer to the result of β₀'.
Since we applied the least squares method to a model where both sides were multiplied by 1/X<sub>i</sub>,  
the intercept term becomes the partial regression coefficient we originally intended to interpret.
