# Basic Idea of Principal Components

# ■ What Are Principal Components For?

The purpose of principal components is to express the information in vectors X1 and X2 as a single vector, as shown below.  
It is similar to combining math and English scores into a comprehensive new vector called "academic ability."

![KakaoTalk_20250523_150302289](https://github.com/user-attachments/assets/1ad16f21-d0c1-45dc-881a-a41a21f45ee6)

# ■ What Kind of Vector Is Best?

When summarizing two vectors into one as above,  
the next question becomes how to draw the vector—called the principal component—onto a scatterplot.  
In other words, we need to determine which vector offers the best summary.

There are two possible situations, as shown below:

![KakaoTalk_20250523_152802396](https://github.com/user-attachments/assets/3d550b9c-ed88-4e90-9d75-5d66f91ead9e)

Intuitively, the vector in the right-hand plot seems to summarize X1 and X2 better.  
So we need to explore what exactly that intuition is based on.

![KakaoTalk_20250523_150302289_01](https://github.com/user-attachments/assets/2c66a720-2d34-48de-9545-96a6f1e1d994)

If we choose a vector **v** and project all the points in the scatterplot onto that vector,  
then the vector that **maximizes the variance** of those projections will best describe the data distribution.

# ■ The Vector with the Second Largest Variance

Interestingly, the vector with the **second largest variance**  
is the one that is **orthogonal to the vector with the largest variance**.

This is because most of the data distribution is already captured by the first vector.  
The remaining unexplained variance lies in the direction that the first vector cannot describe—its orthogonal direction.

![KakaoTalk_20250523_150302289_02](https://github.com/user-attachments/assets/e1472290-dc6d-416d-86ea-ca1563607de2)
