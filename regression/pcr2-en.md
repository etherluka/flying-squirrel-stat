# Relationship Between the Principal Component Regression Equation and the Original Model

# The OLS Model That Encounters Problems

Principal component regression is designed to solve the issue of **multicollinearity** that arises when using OLS.  
Therefore, our discussion begins with the OLS estimation formula.

**Model 1** is a standard regression model fitted under the assumption of OLS.  
In this case, if the variables in **X** are highly correlated, applying OLS leads to **large variances** in the individual regression coefficients.  
When coefficient variances are high, the estimators become unstable,  
which means the regression results are not reliable.

**Model 2** is an OLS model where both **X** and **Y** have been standardized.  
Thus, it retains the **same information** as Model 1, but due to centering, it is fitted **without an intercept**.

![KakaoTalk_20250527_221241904](https://github.com/user-attachments/assets/4419237c-aec8-4110-9d83-95322ab0c590)

# Computing Principal Components

We compute the **eigenvectors of the correlation matrix** of the standardized **X** (denoted **Xs**),  
and construct the matrix **V** from those eigenvectors.

As discussed in previous posts, principal components are obtained by projecting **Xs** onto **V**.  
Since projection involves inner products, each principal component **C** can be expressed as a linear combination of **Xs**,  
according to the definition of the dot product.

We then define **Model 3** using the computed principal components.

![KakaoTalk_20250527_221241904_01](https://github.com/user-attachments/assets/05af902c-a4fa-4283-b4df-6737e4f624d5)

# Relationship Among the Models

![KakaoTalk_20250527_221241904_02](https://github.com/user-attachments/assets/543535b3-36f9-45cc-a1cb-946ea6d6bbb5)

Thus, we have constructed three models.  
It is intuitive that the first two models (Model 1 and Model 2) contain the same information.

Also, considering that the covariance (or correlation) matrix of **X** defines a linear transformation that describes the shape of the data,  
and that principal components express that matrix as a combination of **orthogonal vectors**,  
we can understand that **Model 3** retains the same informational content as Model 1 and Model 2.

# Transforming Between Models

Since all three models contain the same information,  
we can imagine that they are **freely convertible** into one another.

The principal components used in Model 3 are all linear functions of **Xs**,  
so if we express the **C** variables back in terms of **Xs**, we get the following:

![KakaoTalk_20250527_221241904_03](https://github.com/user-attachments/assets/0cb8210f-0cee-4a0b-a61f-1c9c8b64c04b)

By regrouping terms for each **Xs**, we can see that this structure is equivalent to **Model 2**.

Furthermore, since standardized regression coefficients can be converted back to the original scale using **Sx/Sy**,  
we can reconstruct **Model 1** from **Model 3** as well.

Thus, by constructing a principal component regression model,  
we make use of the fact that the principal components of a symmetric matrix (such as a covariance matrix) are orthogonal,  
and this allows us to escape the problem of multicollinearity.

By fitting a regression using these principal components via OLS,  
we can ultimately recover the relationship between **Y** and **X** that we originally sought.
