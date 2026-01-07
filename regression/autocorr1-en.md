# The Problem of Correlated Error Terms

Autocorrelation refers to the situation where observations are related to each other according to the natural order in which they are obtained.  
## cov(ε<sub>i</sub>, ε<sub>j</sub>), i ≠ j  
This violates the regression model assumption that error terms (ε) are independent of each other.

Therefore, the concept of autocorrelation is relevant primarily in **time series data**.  
In cross-sectional data, the order of observations is essentially arbitrary (since the data itself is unordered by nature).

# ■ Addressing the Causes of Autocorrelation

- Autocorrelation can occur when important **time-related variables** are omitted from the model.  
In other words, it may indicate the absence of explanatory variables that could capture the observed patterns in the data.  
If such variables are added to the model, the autocorrelation may naturally disappear.

- On the other hand, if the data inherently possess autocorrelation, it can be addressed through **data transformation**.  
In this case, we introduce the **Cochrane–Orcutt** method, which transforms the data to remove autocorrelation and allows for OLS estimation.
