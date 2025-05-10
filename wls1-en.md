# Weighted Least Squares (WLS)
---
Along with the variable transformation techniques discussed earlier, one method to address heteroscedasticity is the 'Weighted Least Squares (WLS)' method.  
Although it is essentially the same technique as 'variance stabilization using the X term' in variable transformation, this approach is interpreted from the perspective of #assigning weights#.

First, let's compare Weighted Least Squares with Ordinary Least Squares (OLS):

![KakaoTalk_20250509_221636154](https://github.com/user-attachments/assets/0e95cc8e-bdf3-4292-887e-451b2a71b700)

Both aim to find coefficients that minimize the Mean Squared Error (MSE), but WLS assigns weights to each instance.  
Weights are the inverse of the variance, and intuitively this means:

## If the variance is large, its influence is reduced (small weight); if the variance is small, its influence is increased (large weight).

This can be rewritten as:

## ∑ W<sub>i</sub> e<sub>i</sub><sup>2</sup>

Here, the squared error (e<sub>i</sub><sup>2</sup>) refers to how far the actual y<sub>i</sub> value deviates from the predicted value E(y<sub>i</sub>|x<sub>i</sub>).  
Thus, this discussion pertains to the variance of the errors.  
Since the weight (W<sub>i</sub>) is determined based on the relationship with the variance,  
applying the weight (W<sub>i</sub>) to the variance (squared error) is dimensionally appropriate and natural.

---
## ■ How should the weights be determined?

In fact, this is a very difficult question. It would be convenient if existing theories or intuition had already revealed a formula for the variance of the errors  
(Remind: the goal is to achieve homoscedasticity, which pertains to the variance of the errors),  
but in most cases, such a relationship is not known. (We simply have data that shows heteroscedasticity.)

Therefore, in order to assign weights, it is necessary to first express the variance of the errors.

We will discuss three situations in which the weights can be determined:
- When, due to the nature of the study, the residual variance is expected to increase as the size of the predictor variable increases (i.e., the error variance is known in advance through background knowledge)
- When the nature of the data collection method allows heteroscedasticity to be theoretically assumed in advance
- When there is no prior information, and clusters are identified based on residuals from OLS

In this post, we assume that the error variance Var(&epsilon;<sub>i</sub>) is already known based on background knowledge (in the example below, K<sup>2</sup>X<sub>i2</sub>),  
so that we can first become familiar with how WLS works.

![KakaoTalk_20250509_223651555](https://github.com/user-attachments/assets/e3925f3e-6f3a-4cdf-8774-f489930825b5)
