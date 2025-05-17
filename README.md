# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
## Step1 :
Read the number of variables n. Create an augmented matrix a of size 𝑛×(𝑛+1) to hold coefficients and constants.

## step 2:
Create a solution vector x of size n. 

## step 3:
For each pivot row, check if the pivot element is zero (exit if true). For all rows below the pivot, eliminate the variable using row operations.

## step 4 :
Start from the last equation and solve for one variable at a time, moving upwards.

## step 5 :Print each variable X0, X1, ..., Xn-1 with 2 decimal precision.


## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Dashvin S
RegisterNumber:212224100008

'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
           a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f '%(i,x[i]),end='') 
*/
```

## Output:
![image](https://github.com/user-attachments/assets/729a4761-3b05-4827-a98e-c477fc0d111f)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

