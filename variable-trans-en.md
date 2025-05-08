# Variable Transformation (Linearization)

Regression models assume that Y is expressed as a linear combination function of β.  
This corresponds to the "linearity" among the four regression assumptions we usually check (linearity, homoscedasticity, normality, independence).

# ■ When the model is a nonlinear function of X (re-expressible case)

However, in practice, we cannot verify with the data at hand whether Y is a linear function of β.  
Instead, we check whether Y maintains linearity with respect to X.  
(Since ŷ is expressed in the form Xβ̂, if Xβ̂ is a linear function with respect to X, it will also be a linear function with respect to β̂.)

Therefore, even if the relationship between X and Y is nonlinear (e.g., a quadratic relationship), we can simply replace X with X<sup>2</sup> and treat it as a new X (e.g., X<sub>2</sub>).

## Y = β₀ + β₁X₁<sup>2</sup> + ε  
## X₁<sup>2</sup> = X₂  
## Y = β₀ + β₁X₂ + ε

Thus, when the regression model is a nonlinear function of X, we can apply an appropriate transformation to create linearity and consider it as having introduced a new X variable, so it is not a significant problem.  
### This is because the linearity assumption of the regression model is about β, not X.  
The problem arises when the regression model is not a nonlinear function of X, but a nonlinear function of β (e.g., Y = β₀ + e<sup>β₁X₁</sup> + ε).

---

# ■ When the model is a nonlinear function of β

## T<sub>i</sub> = &alpha;β<sup>i</sup>

In such cases, a specific transformation must be applied to express the response variable T as a linear function of β.  
In the case above, we take the log to bring the exponent X down.

## log(T<sub>i</sub>) = log(&alpha;) + i log(β)  
## Y = log(T<sub>i</sub>), β₀ = log(&alpha;), β₁ = log(β), X = i  
## Y = β₀ + β₁X

Below are additional examples of linear transformations.

![Linear Transformation examples](https://github.com/user-attachments/assets/9ac5a557-d68b-44e7-b1bf-3b8533e8a608)
