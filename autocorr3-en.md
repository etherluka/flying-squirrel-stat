# Eliminating Autocorrelation through Transformation

## ■ Cochrane–Orcutt Method

If the results of the two previous tests (Runs test and Durbin–Watson test) indicate that autocorrelation exists in the model,  
then our regression model no longer satisfies the assumption that ε is i.i.d. and follows N(0, σ<sup>2</sup>).  
This means OLS is no longer valid, and a solution must be found.

One such solution is the Cochrane–Orcutt method, which eliminates autocorrelation through transformation.

Let’s begin with the **first-order autocorrelation equation**, as introduced in the previous post:

![KakaoTalk_20250512_201342271](https://github.com/user-attachments/assets/c830464c-eb69-4b6e-ab66-a60d963c5740)

Here, W<sub>t</sub> satisfies the i.i.d. assumption and follows N(0, σ<sup>2</sup>),  
so it perfectly aligns with the classical regression error assumptions — it's "white noise."

Given that we've identified a violation of the i.i.d. assumption through autocorrelation,  
W<sub>t</sub> becomes a very desirable target for us.

The reason W<sub>t</sub> is a viable target in practice is that we can express the first-order autocorrelation equation using our model.

First, we express ε<sub>t</sub> and ε<sub>t−1</sub> as follows:

![KakaoTalk_20250512_201342271_01](https://github.com/user-attachments/assets/c16b5ab1-556b-4e09-bfd9-a4bc885e9091)

Then, through the following transformation process,  
we construct a new regression model in which W<sub>t</sub> becomes the error term:

![KakaoTalk_20250512_201342271_02](https://github.com/user-attachments/assets/eb964ba9-ddf2-4989-a4ed-d5ee8d9ca5bb)

Since this model satisfies the assumptions about the error term, we can now apply OLS.  
Also, ρ can be estimated from the data we have.

Thus, after the transformation, we can recover the original estimates of β₀ and β₁.

# ■ Iterative Estimation Procedure of the Cochrane–Orcutt Method

1) Compute the OLS estimates from the original model.  
2) Based on the estimates, calculate the residuals and use them to estimate ρ.  
3) Fit the transformed model using y<sub>t</sub> − ρ̂ y<sub>t−1</sub> and x<sub>t</sub> − ρ̂ x<sub>t−1</sub> to obtain updated estimates of β̂₀ and β̂₁.  
4) Repeat the above steps until autocorrelation is no longer detected in the model.

# Summary

To summarize: our goal is to estimate β₀ and β₁,  
but since the error term does not satisfy the i.i.d. assumption,  
we cannot apply OLS to the original model:

y<sub>t</sub> = β₀ + β₁x<sub>t</sub> + ε<sub>t</sub>

However, we do not give up on estimating β₀ and β₁.  
Instead, we express the first-order autocorrelation equation using available information,  
and treat W<sub>t</sub> as the error term.

The transformed regression model, which uses W<sub>t</sub>, now satisfies the error assumptions and can be estimated using OLS.  
Once we obtain the OLS estimates, we can apply the inverse transformation to recover the original β₀ and β₁.

It’s like taking a detour in the method to ultimately reach our target.
