# Variance of the OLS Estimator

The matrix (X<sup>T</sup>X)<sup>−1</sup>, which appears when deriving the OLS estimator,  
is subject to conditions for invertibility and is also present in the variance formula of the estimator.

If the columns of X are linearly dependent, the inverse matrix does not exist,  
and the OLS estimator cannot be computed.  
Even if they are not linearly dependent, having high correlations between predictors may still result in unstable estimates,  
making statistical inference less reliable due to multicollinearity.

In this topic, we will explore several statistics used to detect multicollinearity.  
But before that, to ensure smooth understanding in future posts,  
we first review the structure of the OLS estimator’s variance.

# ■ When X Includes an Intercept

In multiple regression, when dealing with the OLS estimator,  
it is standard to include the intercept in X and compute statistics on non-centered data.  
(Centering is closely related to whether the intercept is included.)

Let’s first look at the general variance derivation.

![KakaoTalk_20250517_234512382](https://github.com/user-attachments/assets/cde7421d-fde8-4f47-bf2e-9d050ed90090)

We then compute the portion previously denoted as "A" for convenience, and derive the final variance formula.

![KakaoTalk_20250517_234512382_01](https://github.com/user-attachments/assets/91147ea4-831a-4239-910b-6e5a416f7e56)

# ■ When X Does Not Include an Intercept

The issue of multicollinearity focuses on **strong correlations between predictors**.  
Thus, the intercept is not a major concern in this context,  
since it cannot have meaningful correlation with the other explanatory variables.

So this time, we compute the variance while excluding the intercept from the X matrix.  
The main difference here is that removing the intercept effectively centers the data.

We begin by constructing P<sub>j</sub> using the X<sub>j</sub> matrix without the intercept and a vector j containing the intercept.

![KakaoTalk_20250518_003139990](https://github.com/user-attachments/assets/7b4ae39f-2b8d-419b-900c-33ccad3d1bff)

We then compute the OLS estimator for the multiple regression model without the intercept.

![KakaoTalk_20250518_003139990_01](https://github.com/user-attachments/assets/e9b49323-605f-45d3-89f3-96250babc5c6)

Using this OLS estimate, we derive the variance.

![KakaoTalk_20250518_003139990_02](https://github.com/user-attachments/assets/009177a6-f6a0-4abc-8851-619d2cd0252d)

As you can see, aside from the centering,  
the variance structure is fundamentally the same as the one we derived earlier.

![KakaoTalk_20250518_003139990_03](https://github.com/user-attachments/assets/46a378b8-418a-4be7-b9ce-8fa16f1f0645)
