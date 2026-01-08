# How the Covariance Matrix Represents X

In principal component regression, it may seem puzzling that the data matrix **X** is replaced by the principal components of its **correlation matrix** (or covariance matrix).

"Since the explanatory variables we use in regression analysis are **X**,  
why is it valid to replace **X** with the principal components of its correlation (or covariance) matrix?"

## This is clarified once we recognize that the correlation (or covariance) matrix encapsulates the distribution of the **X** data.

A matrix performs a linear transformation on space.  
Since the correlation and covariance matrices are also matrices, we can infer that they perform certain linear transformations.

In the figure below, the points on the **left plane** are random values generated from a Gaussian distribution.  
Being random, they exhibit no directionality or pattern.  
On the **right plane**, those same random values have been multiplied by the covariance matrix of **X**.  
The space is transformed by the covariance matrix, and now the data—which were previously directionless—appear to have a distinct directional structure.

![KakaoTalk_20250526_235452699](https://github.com/user-attachments/assets/bab5fbce-1c05-4705-a920-2ffcfef495ff)

This actually resembles the scatter plot of the original **X** data.  
The individual data points may not lie in exactly the same positions (since the covariance-matrix-transformed data are still randomly generated),  
but they show **the same distribution** as **X**.  
That’s because the covariance matrix of **X** captures and describes the characteristics of **X** itself.

Therefore, representing **X** via its covariance matrix is in fact  
a meaningful and appropriate substitution,  
since it effectively reflects the tendencies—or distributional structure—of the original **X** data.
