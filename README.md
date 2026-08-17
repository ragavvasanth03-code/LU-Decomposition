# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

1. LU Decomposition (printing L and U)
Algorithm (4 steps):
Read the matrix A.
Perform LU decomposition of A to obtain P, L, and U.
Extract L (lower-triangular) and U (upper-triangular) matrices.
Display L and U.
2. Solving AX = B using LU Decomposition
Algorithm (4 steps):
Read matrices A and B and perform LU decomposition to get P, L, U.
Compute Pb by multiplying Pᵀ with B.
Solve the forward substitution Ly = Pb.
Solve the backward substitution Ux = y and print x.


## Program:
(i) To find the L and U matrix
```
Program to find the L and U matrix.
Developed by: Ragavan V
RegisterNumber: 212225240111

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
from scipy.linalg import lu
A=np.array(eval(input()))
P,L,U=lu(A)
print(L)
print(U)
```
(ii) To find the LU Decomposition of a matrix
```

Program to find the LU Decomposition of a matrix.
Developed by: Ragavan V
RegisterNumber: 212225240111

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

import numpy as np
from scipy.linalg import lu_factor,lu_solve
A=np.array(eval(input()))
b=np.array(eval(input()))
lu,piv=lu_factor(A)
X=lu_solve((lu,piv),b)
print(X)

```

## Output:
![lu decomposition]()

<img width="1289" height="859" alt="image" src="https://github.com/user-attachments/assets/3d942870-161e-4444-877a-bdfa482866ca" />

<img width="1281" height="809" alt="image" src="https://github.com/user-attachments/assets/59ead0e8-ccdd-4c27-a0be-107a6cd8a5a0" />



## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

