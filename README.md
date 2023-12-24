# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
## Step1:
import sys and numpy.Accept the size of the matrix(n) as user input. Create a matrix size(n,n+1)filled with zeros.

## Step2:
Create an array x if size n filled with zeros.Use nested loops to input the matrix element from the user.

## Step3:
Perform Gaussion elimination on the augmented matrix.Check the divide by zero error during the elimination process.

## Step4:
Perform back substitution to find the value of unknowns(x).

## Step5:
Print the result in the format "X%d = %0.2f" for each variable.

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: P.Sasinthar
RegisterNumber:23012532 
'''
import sys
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix [i][j]==0.0:
        sys.exit("Divide by zero error")
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
*/
```

## Output:

![Alt text](<Screenshot 2023-12-24 195347.png>)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

