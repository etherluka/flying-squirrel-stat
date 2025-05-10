# Weighted Least Squares (WLS) – Case 2
---
This time, we examine the case where #heteroscedasticity can be theoretically assumed in advance due to the nature of the data collection method#.  
It may sound complex, but the example is intuitive.

<Case>  
Consider a situation where students are sampled from each of four schools.

Let n<sub>j</sub> (j = 1, 2, 3, 4) be the number of sampled students from a specific school:  
n<sub>1</sub>: 100 students  
n<sub>2</sub>: 80 students  
n<sub>3</sub>: 70 students  
n<sub>4</sub>: 10 students

Compared to School 4, which sampled only 10 students, the result from School 1, which surveyed 100 students, is more trustworthy.  
WLS reflects this trust by assigning more weight to the results from schools with larger sample sizes.

Now, suppose in our regression model, the response variable y<sub>i</sub> represents the "average tuition of School <sub>i</sub>."  
So for School 1, y<sub>1</sub> would be the average tuition of 100 students, ..., and y<sub>4</sub> would be the average tuition of 10 students.  
According to the distribution of the sample mean, we theoretically know that:

Var(y<sub>i</sub>) = σ<sup>2</sup> / n<sub>i</sub>

Thus, σᵢ<sup>2</sup> = σ<sup>2</sup> / n<sub>i</sub>

Now that we can express the variance, we can also determine the weight W<sub>i</sub>:

### W<sub>i</sub> = 1 / σᵢ<sup>2</sup> = n<sub>i</sub> / σ<sup>2</sup>

Here, σ<sup>2</sup> is a constant, so it does not affect the minimization of the function.  
Therefore,

### W<sub>i</sub> = n<sub>i</sub>

is used as the weight when fitting the model.


![KakaoTalk_20250510_144256205](https://github.com/user-attachments/assets/3d6ded0d-5aba-4702-929c-0d9f85792687)
