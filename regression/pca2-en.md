# Principal Components and Eigenvectors

# ■ Eigenvectors

Let’s revisit the definition of eigenvectors and eigenvalues.

![KakaoTalk_20250523_154101696](https://github.com/user-attachments/assets/377dcca7-c172-4d72-82df-a591084eb6f0)

In words:  
Any matrix **A** can be viewed as a kind of linear transformation that acts on the original space.  
In most cases (unless the transformation is a pure rotation), the transformation stretches the space in certain directions.

According to the definition of an eigenvector,  
when we apply a linear transformation **A** to an eigenvector **v**,  
the result is simply a scaled version of the same vector **v**—either stretched or compressed.

### In other words, **v** is a vector that already lies in the direction that **A** stretches the space.

# ■ Relationship to Principal Components

Principal components are closely related to eigenvectors.  
Since **v** is a vector that already points in the direction that matrix **A** stretches space,  
the “vector that maximizes variance” (as discussed in the previous post)  
must also be aligned with the direction of maximum stretching.

By definition, such a vector is an eigenvector.

Therefore, we arrive at the conclusion that principal components are, ultimately, the eigenvectors of the matrix.
