# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

1. Import the numpy module to use the built-in functions for calculation
2. Prepare the lists from each linear equations and assign in np.array()
3.  Using the np.linalg.matrix_rank(), we can find given matrix
4. End the program

## Program:
```
'''
Register Number:212225230170
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range (n):
    if a[i][j]==0:
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
    print('X%d = %0.2f'%(i,x[i]),end=' ')
           
```

## Output:

![WhatsApp Image 2026-02-14 at 08 59 23](https://github.com/user-attachments/assets/54fdb3a5-7cfb-446f-9edf-6956e6cf8544)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

