# Autocorrelation and Omitted Predictors

Autocorrelation can occur when an important time-varying predictor is omitted from the regression model.  
In such cases, simply including the missing variable in the model can resolve the autocorrelation.

Therefore, techniques like variable transformation, as discussed earlier, are used under the assumption that no such omitted variable exists.  
They are more of a last-resort method. (Recall that these apply when “pure autocorrelation” is present.)

Since this post would be too light with just the theory, let’s use the dataset from the textbook and R  
to check whether adding the omitted predictor indeed solves the issue.

# ■ Verifying with R

We use the dataset called "Housing Starts" from Chapter 8.  
H is the number of housing starts, P is the population (in millions), and D is mortgage funds.

First, we fit a regression model using P to predict H, and inspect the residuals.

model <- lm(H ~ P, data = p219)  
residuals <- resid(model)

plot(residuals, type = "b", pch = 16,  
     xlab = "Observation", ylab = "Residual",  
     main = "Residuals by Observation Order")  
abline(h = 0, col = "red", lty = 2)

Image: https://github.com/user-attachments/assets/c92929a7-9d09-4959-a357-a8c6e8fa3bd6

As shown above, clear autocorrelation is visible.  
The p-value from the Durbin–Watson test is 6.645e-06, which strongly indicates autocorrelation.

Now let’s treat D as the omitted predictor and include it in the model:

model1 <- lm(H ~ P + D, data = p219)

Image: https://github.com/user-attachments/assets/1331754e-7975-44e2-a51b-ab69fa42c4aa

Now, autocorrelation seems to have disappeared.  
There’s one point in the middle that may look like an outlier,  
but the overall pattern appears fairly random.  
The Durbin–Watson statistic is now 0.2316, which is no longer statistically significant.

This confirms that autocorrelation can be resolved  
simply by including the missing predictor in the model.
