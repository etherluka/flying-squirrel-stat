# Limitations of the Durbin–Watson Statistic

Let us revisit the Durbin–Watson statistic discussed in a previous post.

Image: https://github.com/user-attachments/assets/7d43278b-aabb-415f-babb-5538bcb74c11

We can observe that the numerator of the Durbin–Watson statistic is essentially the sum of the squared differences between e<sub>t</sub> and e<sub>t−1</sub>.  
This confirms that the statistic is only capable of detecting **first-order autocorrelation**.

To illustrate the limitations of the Durbin–Watson statistic, we consider the "Ski Sales" dataset from Chapter 8.

We fit a regression model with **Sales** as the response and **PDI** (disposable income) as the predictor.  
The Durbin–Watson test is performed on this model.  
As shown below, the statistic suggests there is no first-order autocorrelation.

Image: https://github.com/user-attachments/assets/d18565fd-3690-4f4b-a1c0-142dcb8e4d04

However, if we group the residuals using a **second-order difference** — grouping summer-fall together and winter-spring together —  
we can clearly observe a pattern in the residuals.

Image: https://github.com/user-attachments/assets/affd2ab5-87a6-42d1-9c3f-492e5ed64c99

Even though there is an evident and unnatural pattern in the residuals,  
the Durbin–Watson statistic fails to detect it — precisely because the pattern appears only with **second-order differencing**.

Therefore, it is important to remember that the Durbin–Watson statistic is only valid  
for detecting **first-order autocorrelation** and does not account for higher-order structures.
