# Principal Component Regression 1

# ■ Logic of Principal Component Regression

The idea of using principal components to address multicollinearity among X variables is as follows:

![KakaoTalk_20250526_235452699_01](https://github.com/user-attachments/assets/9a926a3d-93ad-41e2-8aae-9598045216b7)

In short, due to high correlations among variables, we avoid using **X** directly in regression.  
Instead, we search for substitutes—principal components—that can replace **X** while ensuring **linear independence** among themselves by construction.  
Finally, we perform regression using these substitutes, which retain the full informational content of **X**,  
and interpret the results through their relationship back to the original **X**.

# ■ Properties of Principal Components

When we standardize **X** (denoted as **Xs**) and compute Xs'Xs,  
this results in a **correlation matrix** rather than a covariance matrix, due to standardization.  
The eigenvectors of this correlation matrix are exactly the substitutes we were looking for: the **principal components**.  
Each principal component can be expressed as a linear combination of the variables in **Xs**, as shown below:

![KakaoTalk_20250526_235452699_02](https://github.com/user-attachments/assets/beacb553-65c6-485e-b5fb-9d2af7606639)

## Mean of 0  
Since the Xs variables have been standardized, each of them has a mean of 0.  
As a result, any linear combination of them (such as principal component C<sub>j</sub>) will also have a mean of 0.

## Variance equals eigenvalue  
It may not be immediately intuitive that the variance of C<sub>j</sub> is equal to the corresponding **eigenvalue**,  
but recall from a previous post:  
> *The vector that maximizes the variance when data points are projected onto it is the eigenvector.*

Therefore, if we project all data points onto an eigenvector—  
and that vector maximizes the spread (i.e., variance) of the projected points—  
then the **extent of spread** corresponds to how much that eigenvector stretches.  
This is precisely the relationship between variance and eigenvalue.
