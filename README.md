# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy and sys, and create the augmented matrix using np.zeros() and
input() for user data.
2. Use np.linalg.LU() (or similar built-in LU decomposition) to decompose the
augmented matrix into P, L, and U.
3. Solve for the solution vector using back substitution with built-in np.linalg.solve() or
equivalent.
4. Print the solution vector using formatted output with print() and the end the
program.


## Program:
```
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: PRIYA DHARSHNI S
RegisterNumber: 212224100045
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
print('X%d = %0.2f'%(i,x[i]),end=' ')

```

## Output:

![Screenshot 2025-04-26 092940](https://github.com/user-attachments/assets/9b47c08a-1d67-4387-a8bf-9f6ba3ed1303)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

