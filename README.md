# Gaussian Elimination

### AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

### Algorithm
1. Import the numpy module to use the built-in functions for calculation
2. Prepare the lists from each linear equations and assign in np.array()
3. Using the np.linalg.solve(), we can find the solutions
4. End the program

### Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Dhanusya.K
RegisterNumber: 23006651
import numpy as np
import sys
n = int(input())
a = np.zeros((n,n+1))
x = np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j] = float(input())
for i in range(n):
    if a[i][i] == 0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio*a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    
    for j in range(i+1,n):
        x[i] = x[i]-a[i][j]*x[j]
        
    x[i] = x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end = ' ')
*/
```

### Output:
![Screenshot 2023-12-31 145914](https://github.com/Dhanu654/Gaussian/assets/148514965/0ad69090-556f-4fcc-87ee-429d35d230e8)
![Screenshot 2023-12-31 145941](https://github.com/Dhanu654/Gaussian/assets/148514965/8b6de245-f603-48a1-9222-35844505a3ba)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

