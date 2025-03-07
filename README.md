# emerepo

Get App
received_1636033413710082.png
PNG 406.98KB
received_1359177488616766.png
PNG 257.82KB
provide the answer using a and b
To address the assignment, let's provide the algorithms and examples for both Strassen’s Matrix Multiplication and the Karatsuba algorithm.

a. Strassen’s Matrix Multiplication
Algorithm:

Divide: Split the matrices 
A
A and 
B
B into four submatrices each.

Conquer: Compute seven products 
P
1
P 
1
​
  to 
P
7
P 
7
​
  using these submatrices.

Combine: Use these products to compute the resulting matrix 
C
C.

Example:
Consider two 2x2 matrices:

A
=
(
1
2
3
4
)
,
B
=
(
5
6
7
8
)
A=( 
1
3
​
  
2
4
​
 ),B=( 
5
7
​
  
6
8
​
 )
Using Strassen’s method:

Compute the seven products:

P
1
=
(
1
+
4
)
(
5
+
8
)
=
5
×
13
=
65
P 
1
​
 =(1+4)(5+8)=5×13=65
P
2
=
(
3
+
4
)
×
5
=
7
×
5
=
35
P 
2
​
 =(3+4)×5=7×5=35
P
3
=
1
×
(
6
−
8
)
=
1
×
(
−
2
)
=
−
2
P 
3
​
 =1×(6−8)=1×(−2)=−2
P
4
=
4
×
(
7
−
5
)
=
4
×
2
=
8
P 
4
​
 =4×(7−5)=4×2=8
P
5
=
(
1
+
2
)
×
8
=
3
×
8
=
24
P 
5
​
 =(1+2)×8=3×8=24
P
6
=
(
3
−
1
)
×
(
5
+
6
)
=
2
×
11
=
22
P 
6
​
 =(3−1)×(5+6)=2×11=22
P
7
=
(
2
−
4
)
×
(
7
+
8
)
=
(
−
2
)
×
15
=
−
30
P 
7
​
 =(2−4)×(7+8)=(−2)×15=−30
Combine these to get the resulting matrix 
C
C:

C
=
(
P
1
+
P
4
−
P
5
+
P
7
P
3
+
P
5
P
2
+
P
4
P
1
−
P
2
+
P
3
+
P
6
)
=
(
19
22
43
50
)
C=( 
P 
1
​
 +P 
4
​
 −P 
5
​
 +P 
7
​
 
P 
2
​
 +P 
4
​
 
​
  
P 
3
​
 +P 
5
​
 
P 
1
​
 −P 
2
​
 +P 
3
​
 +P 
6
​
 
​
 )=( 
19
43
​
  
22
50
​
 )
b. Karatsuba Algorithm
Algorithm:

Split: Divide the numbers into high and low parts.

Recursive Multiplication: Multiply the parts recursively.

Combine: Use the results to compute the final product.

Example:
Multiply two 2-digit numbers 
x
=
12
x=12 and 
y
=
34
y=34.

Split:

x
=
10
×
1
+
2
,
y
=
10
×
3
+
4
x=10×1+2,y=10×3+4
Compute:

a
=
1
×
3
=
3
a=1×3=3
d
=
2
×
4
=
8
d=2×4=8
e
=
(
1
+
2
)
×
(
3
+
4
)
−
a
−
d
=
3
×
7
−
3
−
8
=
21
−
3
−
8
=
10
e=(1+2)×(3+4)−a−d=3×7−3−8=21−3−8=10
Combine:

x
×
y
=
1
0
2
×
a
+
10
×
e
+
d
=
100
×
3
+
10
×
10
+
8
=
300
+
100
+
8
=
408
x×y=10 
2
 ×a+10×e+d=
