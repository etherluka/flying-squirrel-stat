# Detecting Autocorrelation

Typically, we begin by visually inspecting a graph to detect autocorrelation.  
At this stage, we observe whether the residuals exhibit a particular pattern according to their index.  
Such patterns usually indicate that residuals are clustered by region.

We now introduce two statistical tests that quantify this intuition.

---
# ■ Runs Test

A **run** refers to a sequence of consecutive residuals with the same sign.  
This may sound complicated in words, so let’s look at an example:

+++ -- ++ --- + -

In this example, there are 6 runs:  
'+++' is the first run, '--' is the second, '++' is the third, '---' is the fourth, '+' is the fifth, and '-' is the sixth.  
A run is simply a consecutive segment of residuals with the same sign.

If there are n₁ positive residuals and n₂ negative residuals,  
and both n₁ and n₂ are sufficiently large, and residuals are assumed to be random,  
then the expected value and variance of the number of runs are given by:

μ = 2·n₁·n₂ / (n₁ + n₂),  
σ<sup>2</sup> = 2·n₁·n₂·(2·n₁·n₂ − n₁ − n₂) / (n₁ + n₂)<sup>2</sup>(n₁ + n₂ − 1)

These are based on the assumption that the number of runs follows a normal distribution.  
So the actual number of runs (in the above case, 6) becomes the test statistic for a z-test.

By counting the number of runs, we can perform a z-test  
to determine whether the residuals are randomly distributed,  
or if they follow a specific pattern.

---
# ■ Durbin–Watson Test

Let’s begin by expressing autocorrelation as a formula:

ε<sub>t</sub> = ρ·ε<sub>t−1</sub> + w<sub>t</sub>

Here, ρ is the correlation coefficient between ε<sub>t−1</sub> and ε<sub>t</sub>,  
and it is assumed that |ρ| < 1.  
w<sub>t</sub> is white noise: it has mean 0 and constant variance, and follows a normal distribution.

Ultimately, the Durbin–Watson test is used to determine whether ρ = 0 (i.e., whether residuals are independent).  
(Recall: residuals are assumed to be independent in the regression model.)

Let’s first see how ρ is calculated.  
Since ε<sub>t−1</sub> does not exist when t = 1,  
both vectors begin at t = 2, and the correlation is based on n − 1 data points.  
![KakaoTalk_20250511_213403154](https://github.com/user-attachments/assets/0de1d179-2f22-4495-a275-b318a6fc4fd5)

Since the mean of e<sub>t</sub> is 0, the correlation coefficient formula is simplified as follows:  
![KakaoTalk_20250511_213403154_01](https://github.com/user-attachments/assets/9deb2272-57f8-4ab8-806e-a9485d97043d)

Now for the Durbin–Watson statistic:  
Unlike true errors ε<sub>t</sub>, the estimated residuals e<sub>t</sub> are distorted by the model.  
Hence, the statistic directly computes the differences between e<sub>t</sub> and e<sub>t−1</sub>.

Why the estimated residuals are distorted, and how this method corrects for that distortion,  
is a topic we will leave for a future post.  
![KakaoTalk_20250511_213403154_02](https://github.com/user-attachments/assets/cb067578-4a38-43a2-9415-e137dd935ea6)

Now consider the implication of the formula:  
Since the numerator is the sum of squared differences between e<sub>t</sub> and e<sub>t−1</sub>,  
a value close to 0 means the residuals are very similar to each other —  
in other words, the gap between adjacent residuals is almost zero.  
This implies a strong similarity and thus a high value of ρ.

On the other hand, a large numerator indicates large differences between adjacent residuals.  
Given that residuals have a mean of 0,  
this suggests they are scattered randomly above and below the horizontal axis.

It is known that the Durbin–Watson statistic d satisfies:

d = 2(1 − ρ),  
and d ranges between 0 and 4.
