# Weighted Least Squares (WLS) – Case 3

This time, we look at a case where the specific structure of heteroscedasticity is determined 'empirically' based on the sample.

The best approach is for the researcher to divide the data into several groups using their expert intuition,  
then calculate the variance within each group and use it as the weight.

One algebraic way to investigate violations of homoscedasticity is to fix certain x-values and repeatedly sample data for those values. The diagram makes this easy to understand.

![스크린샷 2025-05-10 145751](https://github.com/user-attachments/assets/77d5da55-67bf-407c-9afa-c89320fcdc1d)

The assumption of homoscedasticity means that the variance of the conditional distribution of y, given x, is the same for all x.

![스크린샷 2025-02-03 135432](https://github.com/user-attachments/assets/4911ff37-5703-4720-9edb-6adb4b281a30)

Therefore, the earlier mention of “repeatedly sampling y for fixed values of x”  
is equivalent to constructing the conditional distribution of y | x directly (refer to the idea in the image above).

If the researcher's grouping was well chosen,  
each x-value will show systematically different patterns of variance,  
and these variances can then be used as weights for each group.

---
Now, consider the following model:

![KakaoTalk_20250510_153652174](https://github.com/user-attachments/assets/1eee59d7-641e-4acf-8ffe-3e496acd5113)

The variance of the error term will appear as follows. This means that within each of the j groups, the data follow the same variance.  
(It does not vary with i, only with j.)
![KakaoTalk_20250510_153652174_01](https://github.com/user-attachments/assets/8b33d6c5-20e9-466f-a7c6-bf80c477a93c)

The variance for each group can be expressed as follows:
![KakaoTalk_20250510_153652174_02](https://github.com/user-attachments/assets/273833ee-707e-4ddd-9d4f-90d96d9b6332)

This group-wise variance can also be expressed using the total variance.  
By factoring out the common constant σ, we can express the variation between groups as C<sub>j</sub>:
![KakaoTalk_20250510_153652174_03](https://github.com/user-attachments/assets/77ddd6cb-60b9-46d1-b8e1-7c5563c53398)

In fact, this C<sub>j</sub> term reflects the variance difference between groups.  
So we can use C<sub>j</sub> to construct the weights.  
The equation in the image above can be rewritten in terms of C<sub>j</sub>, and each value can be obtained as follows:
![KakaoTalk_20250510_153652174_04](https://github.com/user-attachments/assets/beaa1be3-4d63-4be5-b3d6-cbf9502d48bd)

Finally, the weights are used as shown below:
![KakaoTalk_20250510_153652174_05](https://github.com/user-attachments/assets/bea67b02-13e2-4abc-b60a-50b0c6e0120f)
