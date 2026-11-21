# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

##Algorithm:
Step 1: Start the program.

Step 2: Import the NumPy library using import numpy as np.

Step 3: Get the coefficient matrix and constant matrix as input from the user.

Step 4: Use the np.linalg.solve() function to find the solution of the given system of linear equations.

Step 5: Display the solution of the matrix.

Step 6: Stop the program.
## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Abinaya P
RegisterNumber: 212225230003
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
n=int(input())
a=np.array([[float(input()) for j in range(n+1)]for i in range(n)])
for i in range(n):
    for j in range(i+1,n):
        r=a[j][i]/a[i][i]
        a[j]=a[j]-r*a[i]
x=np.zeros(n)
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=(a[i][n]-sum(a[i][j]*x[j] for j in range(i+1,n)))/a[i][i]
for i in range(n):
        print(f"X{i} = {x[i]:.2f}",end=" ")

```

## Output:
<img width="1210" height="882" alt="Screenshot 2026-11-21 105455" src="https://github.com/user-attachments/assets/16f2d23f-9b3a-4528-a951-dba32d7de7f3" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

