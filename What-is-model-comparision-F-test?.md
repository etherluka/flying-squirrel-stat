# What is model comparison F-test?

[English version]  
---  
In regression analysis, model comparison refers to the process of evaluating whether a **full model** significantly outperforms a **reduced model**.

In this context, it is commonly stated that the reduced model must be **nested** within the full model.  
But why is that?

**Main Question:** Why must the reduced model be nested within the full model?  
=> "Because they are essentially the same model, just with restrictions."

---

# [How should we understand a reduced model?]

Let’s say there are three explanatory variables. Then the full model can be written as:

## Y = β₀ + β₁X₁ + β₂X₂ + β₃X₃ + ε

A reduced model is one where certain coefficients in the full model are replaced  
**not by least squares estimates, but by arbitrary values**.

In most cases, these “arbitrary values” are 0, so it appears as if the corresponding variables have been "removed".  
Therefore, if we assume β₂ = β₃ = 0, the reduced model becomes:

## Y = β₀ + β₁X₁ + 0X₂ + 0X₃ + ε  
## Y = β₀ + β₁X₁ + ε

---

# [Comparison of reduced and full models]

## Full Model (FM): Y = β₀ + β₁X₁ + β₂X₂ + β₃X₃ + ε  
## Reduced Model (RM): Y = β₀ + β₁X₁ + 0X₂ + 0X₃ + ε

Rewriting for clarity:

## FM: Y = β₀ + β₁X₁ + β₂X₂ + β₃X₃ + ε  
## RM: Y = β₀ + β₁X₁ + ε

### If the SSE (Sum of Squared Errors) of the two models is not significantly different,  
### we may consider them essentially the same.  
Then the least squares estimates of β₂ and β₃ can be interpreted as being 0.

---

# [What if the coefficients are not zero, but equal?]

## H₀: β₂ = β₃

If we want to test whether β₂ and β₃ have the same value,  
we can express the reduced model like this:

## RM1: Y = β₀ + β₁X₁ + β′X₂ + β′X₃ + ε  
## RM2: Y = β₀ + β₁X₁ + β′(X₂ + X₃) + ε

Using RM2, we can still apply the least squares method.

## FM: Y = β₀ + β₁X₁ + β₂X₂ + β₃X₃ + ε  
## RM: Y = β₀ + β₁X₁ + β′X₂ + β′X₃ + ε

### Therefore, if the F-test shows no significant difference in SSE between the models,  
the full and reduced models may be considered equivalent.  
This implies that the least squares estimates of β₂ and β₃ are actually β′.
