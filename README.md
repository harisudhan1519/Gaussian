# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
step1 First we want to import numpy, then import sys, assume a variable.

step2 For gaussian elimination method, we want to make 2nd and 3rd column zero.

step3 For that we want to make a range according to our program output.

step4 Then print the program with correct form then the output will display.

## Program:
```
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0.0:
        sys.exit('divide by zero detected!')
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
![Screenshot 2024-12-16 183133](https://github.com/user-attachments/assets/1e7c8f6e-93e2-4c4f-b17e-370d1ee79e78)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

