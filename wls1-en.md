# Weighted Least Squares (WLS)
---
One of the methods to address heteroscedasticity, along with the variable transformation techniques discussed earlier, is the 'Weighted Least Squares (WLS)' method. 
Although it ultimately achieves the same effect as the 'variance stabilization using X term' in variable transformation, this method is interpreted from the perspective of assigning weights.

First, when comparing weighted least squares with ordinary least squares (OLS), it looks like the following:

![KakaoTalk_20250509_221636154](https://github.com/user-attachments/assets/0e95cc8e-bdf3-4292-887e-451b2a71b700)

Both aim to find coefficients that minimize the Mean Squared Error (MSE), but WLS assigns weights to each instance.
The weights are the inverse of the variance. Intuitively, this means:

## If the variance is large, its influence is reduced (small weight), and if the variance is small, its influence is increased (large weight).

Rewriting this:

## ∑ W<sub>i</sub> e<sub>i</sub><sup>2</sup>

Here, the squared error (e<sub>i</sub><sup>2</sup>) represents how far the actual y<sub>i</sub> value is from the predicted value E(y<sub>i</sub>|x<sub>i</sub>).
Thus, we can see that this is a discussion about the variance of the errors.
Since the weight (W<sub>i</sub>) is determined based on the relationship with the variance,
it seems dimensionally appropriate and natural to assign the weight (W<sub>i</sub>) to the variance (squared error).

---
## ■ How to determine the weights?

In fact, this is a very tricky issue. It would be convenient if existing theory or intuition had already revealed the form of the error variance (Remind: our goal is to create homoscedasticity, and homoscedasticity concerns the variance of the errors),
but in most cases, such relationships are not known. (We are simply given data that shows heteroscedasticity.)

Therefore, to assign weights, it is necessary first to express the variance of the errors.

In this post, we assume that the error variance Var(&epsilon;<sub>i</sub>) is already known from prior knowledge (in the example below, K<sup>2</sup>X<sub>i2</sub>), so we can first get familiar with how WLS works.

![KakaoTalk_20250509_223651555](https://github.com/user-attachments/assets/e3925f3e-6f3a-4cdf-8774-f489930825b5)
