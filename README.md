<h1 align="center">
`Matrix Multiplication in O(n<sup>2</sup>log<sub>2</sub>(6))`
</h1>

|||  
| :---: | :---: |   
|`A11xB11 + A12xB21`|`A11xB12 + A12xB22`|  
|`A21xB11 + A22xB21`|`A21xB12 + A22xB22`|

`M1 = (A11+A21)x(B11-B12)`  
`M2 = (A12+A22)x(B21-B22)`  
`M3 = (A11+A21)x(B11+B12)`  
`M4 = (A12+A22)x(B21+B22)`  
`M5 = A11xB11`  
`M6 = A12xB21`

`S1 = (M1+M3)/2`  
`S2 = (M2+M4)/2`  
`S3 = (M3-M1)/2`  
`S4 = (M4-M2)/2`  
`S5 = (M1+M2+M3+M4)/2`  
`S6 = (M1-M2+M3-M4)/2`

`S1+S2 = C11+C21`  
`S3+S4 = C12+C22`  
`S5 = C11+C22`  
`S6 = C12+C21`  
`S7 = C1+C2+C3+C4`

`S8 = S5+S1+S2-S7=C11-C12`  
`S9 = S7-S5-S1-S2=C12-C11`  
`SA = S6+S3+S4-S7=C21-C22`  
`SB = S7-S6-S3-S4=C22-C21`

`C11 = M5+M6`  
`C12 = C11-S8`  
`C21 = S1+S2-C11`  
`C22 = S3+S4-C12`  
