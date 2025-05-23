# Principal Components as Linear Combinations

Now that we have a general idea of what principal components are,  
let’s look at how they are expressed in terms of X1 and X2.

Let’s denote the first principal component axis as C1.  
Intuitively, we can see that there are infinitely many vectors that lie along this axis  
(since we're referring to eigenvectors here).  
So we choose a **unit vector** lying on axis C1.  
Let’s say the coordinates of its tip are (u1, u2).

![KakaoTalk_20250524_003322666](https://github.com/user-attachments/assets/44880fef-2f12-4967-acc3-476e452d605d)

# ■ Projection onto C1

To jump to the conclusion: C1 can be written as u1X1 + u2X2.  
This becomes easier to understand when we view it from the perspective of individual data points, as in the figure.

Suppose we have a data point (x11, x12) lying in the space defined by X1 and X2.  
Projecting this vector onto the unit vector (u1, u2) results in:

u1x11 + u2x12

![KakaoTalk_20250524_003322666_01](https://github.com/user-attachments/assets/35f483bd-19b7-4ee7-9526-67f8d1479e0a)

To project vector **a** onto vector **b** means expressing vector **a** in the direction of **b**,  
and this is done by taking the dot product of **a** and the unit vector of **b**.

Since (u1, u2) is a unit vector with length 1,  
the projection essentially becomes the magnitude of (x11, x12) in the direction of (u1, u2).

Although we've just looked at a single data point,  
from the axis perspective, we can extend this idea:  
the principal component axis C1 is represented as a linear combination of the original axes X1 and X2:

C1 = u1X1 + u2X2
