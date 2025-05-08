# Variable Transformation (Variance-Stabilizing Transformation)

In this section, variable transformation is used for **variance stabilization**.  
In OLS, **homoscedasticity** is required for hypothesis testing of regression coefficients, and we can address heteroscedasticity through appropriate transformations.

For example, consider the case where Y<sub>i</sub> ~ Poisson(M<sub>i</sub>).

![KakaoTalk_20250507_223226342](https://github.com/user-attachments/assets/7d821ca9-98af-4b49-9327-643c9009afc7)

A key property of the Poisson distribution is that E(X)=Var(X)=M that is, the mean and variance are equal.

Therefore, in an OLS model, as the predicted value Ŷ<sub>i</sub> increases (i.e., as the expected value increases), the variance also increases, leading to **heteroscedasticity**.  
In such cases, applying the **square root transformation** to Y<sub>i</sub> can stabilize the variance.

---

# Delta Method

The **Delta Method** refers to a technique that uses **Taylor expansion** to approximate the variance of a transformed variable.  
For a Poisson-distributed variable Y<sub>i</sub>, we can expand &radic; using Taylor series and express its variance.

![KakaoTalk_20250507_223226342_01](https://github.com/user-attachments/assets/24bfa2a4-7657-48db-9e4a-de14e2112e05)

Now, if we compute the variance, we can observe that applying the square root transformation makes the variance converge to a constant value—  
in other words, the transformation satisfies the assumption of homoscedasticity.

![KakaoTalk_20250507_223226342_02](https://github.com/user-attachments/assets/d895bba5-9885-4e63-8e88-da3d55d89243)
