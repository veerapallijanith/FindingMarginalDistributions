# Marginal distributions and correation coefficient  

# Aim : 

To find marginal distributions and correation coefficient of joint probability mass funcition of two dimensional random variables

![image](https://user-images.githubusercontent.com/104613195/168222062-bb7dec1f-f115-4669-8b4c-58283af8ccf3.png)

# Software required :  

Python

# Theory:

A marginal distribution is a distribution of values for one variable that ignores a more extensive set of related variables in a dataset.
The marginal mass function for X is found by summing over the appropriate column and the marginal mass function
for Y can be found be summing over the appropriate row.

Correlation coefficients are indicators of the strength of the linear relationship between two different variables. The coefficient of correlation is measure of degree of realtionship betwen two variavbles. A linear correlation coefficient that is greater than zero indicates a positive relationship. A value that is less than zero signifies a negative relationship. Finally, a value of zero indicates no relationship between the two variables x and y.  



# Procedure :
![image](https://user-images.githubusercontent.com/104613195/168220332-09383cb4-a7ac-4526-b547-fc522ca53227.png)



# Program

```python
import numpy as np 
import math
x=[0,1,2,3,4,5]
y=[0,1,2,3]
p=[[0,0.01,0.03,0.05,0.07,0.09],
[0.01,0.02,0.04,0.05,0.06,0.08],
[0.01,0.03,0.05,0.05,0.05,0.06],
[0.01,0.02,0.04,0.06,0.06,0.05]]
px=np.sum(p,axis=0)
py=np.sum(p,axis=1)
Ex=np.inner(x,px)
Ey=np.inner(y,py)
px
py
Ex
Ey
Ex2=np.inner(np.square(x),px)
Ex2
Ey2=np.inner(np.square(y),py)
Ey2
vx=Ex2-Ex**2
vx
vy=Ey2-Ey**2
vy
sx=math.sqrt(vx)
sy=math.sqrt(vy)
Exy=0
for i in range(4):
    for j in range(6):
        Exy=Exy+x[j]*y[i]*p[i][j]
Exy
Cov=Exy-Ex*Ey
Cov
r=Cov/(sx*sy)
r
print("The coefficient-correlation %0.4f"%r)
```


# Output : 
![image](https://github.com/Ganesh517/FindingMarginalDistributions/blob/main/m3.png)
# Results 

Hence, a program To find marginal distributions and correation coefficient of joint probability mass funcition of two dimensional random variables is executed.
