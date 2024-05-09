# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. At first, we have imported the necessary libraries we will use in our program.
2. Read Number of Unknowns: n
3. Read Augmented Matrix (A) of n by n+
4. Transform Augmented Matrix (A) to Upper Trainagular Matrix by Row Operations.
5. After that, we applied the Gaussian elimination method.
6. After that, we apply the back substitution method to obtain the desired output.
7. Display result.

## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: T. Gayathri
RegisterNumber: 212223100007

import numpy as np
n=int(input())
arr = np.zeros((n,n+1))
res = np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")
```

## Output:
![gaussian elimination]()
![Screenshot 2024-05-09 111640](https://github.com/gayumee/Gaussian/assets/149037327/8b4cd029-19e3-4e13-915e-8707b829eae6)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

