# Imposing Constraints & Exploring Linear Functions of β

# ■ Imposing Constraints

Suppose that based on theoretical reasoning, we assume that two highly correlated variables have **equal marginal effects** on the dependent variable.  
In that case, we can construct a regression model that imposes **restrictions** on the regression coefficients based on prior knowledge.

![KakaoTalk_20250528_213633580](https://github.com/user-attachments/assets/0d6a4f41-0690-4af5-b074-c5af728e0247)

By defining a new variable **X₄** in this way, **X₄** and **X₂** are no longer correlated.  
As a result, the multicollinearity issue is eliminated from the model.

# ■ Exploring Linear Functions of β

Now let's examine whether a clear linear relationship exists between two highly correlated variables.  
When a high correlation is observed, it is likely that a strong linear dependency exists between the two.

In the case of the **IMPORT** data, we can confirm a high correlation:

![KakaoTalk_20250528_213633580_01](https://github.com/user-attachments/assets/5bc6b6e6-dcae-470b-843d-1262850f6622)

Based on this, we can express one variable as a **linear function** of the other and incorporate that into the model.

![KakaoTalk_20250528_213633580_02](https://github.com/user-attachments/assets/501e0260-cc07-4a20-b8c6-0b677ca6181c)

By following this process, the variables in the model will no longer exhibit multicollinearity,  
thus resolving the collinearity issue effectively.
