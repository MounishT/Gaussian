# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Interchange and equation
2. Divide the equation by (or ).
3. Add times the equation to the equation 
 

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by:T MOUNISH 
RegisterNumber: 23002806
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
X=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
     if a[i][j]==0.0:
         sys.exit('Divide by zero detected')
     for j in range(i+1,n):
         ratio =a[j][i]/a[i][i]
         for k in range(n+1):
             a[j][k]=a[j][k]-ratio*a[i][k]
X[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i] = a[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-a[i][j]*X[j]
    X[i]=X[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,X[i]), end=' ')        
*/
```

## Output:
![Screenshot 2023-12-25 170227](https://github.com/MounishT/Gaussian/assets/138955798/d6cb62f4-5141-40fc-a7d2-5979c61cae37)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

