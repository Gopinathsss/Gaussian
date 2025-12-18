# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Display the values of all unknowns X0, X1, ..., X(n-1).


2.  Input

. Read the number of unknowns n.

. Declare an augmented matrix a of size n × (n+1).

. Declare a solution vector x of size n.


3. Read the elements of the augmented matrix row by row.


4. For each pivot row i = 0 to n-1:

. Check if the pivot element a[i][i] is zero.

. If zero, terminate the program with a divide-by-zero error.


## Program:
```



import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for  i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0:
        sys.exit("Divide by zero detected!")
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
    print("X%d = %0.2f"%(i,x[i]),end=" ")





/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: GOPINATH S
RegisterNumber: 25012981
*/
```

## Output:
![gaussian elimination]()




<img width="1366" height="768" alt="Screenshot 2025-12-18 102851" src="https://github.com/user-attachments/assets/abbeb032-003a-419c-8ca1-2a7bae79472b" />





## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

