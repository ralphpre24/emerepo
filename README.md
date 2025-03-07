# emerepo

(
1Get App
received_1359177488616766.png
PNG 257.82KB
solve using a and b
To solve the assignment using Strassen’s Matrix Multiplication and the Karatsuba algorithm, let's break down each algorithm and provide an example for both.

a. Strassen’s Matrix Multiplication
Algorithm:
Strassen’s algorithm is used for matrix multiplication and is more efficient than the standard method for large matrices. It reduces the complexity from 
O
(
n
3
)
O(n 
3
 ) to approximately 
O
(
n
2.81
)
O(n 
2.81
 ).

Divide: Split the matrices into smaller submatrices.

Conquer: Perform recursive multiplications on these submatrices.

Combine: Combine the results to form the final product matrix.

Example:
Consider two 2x2 matrices 
A
A and 
B
B:

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
Divide: Split each matrix into four submatrices.

Conquer: Compute the seven products:

P
1
=
(
A
11
+
A
22
)
×
(
B
11
+
B
22
)
P1=(A11+A22)×(B11+B22)

P
2
=
(
A
21
+
A
22
)
×
B
11
P2=(A21+A22)×B11

P
3
=
A
11
×
(
B
12
−
B
22
)
P3=A11×(B12−B22)

P
4
=
A
22
×
(
B
21
−
B
11
)
P4=A22×(B21−B11)

P
5
=
(
A
11
+
A
12
)
×
B
22
P5=(A11+A12)×B22

P
6
=
(
A
21
−
A
11
)
×
(
B
11
+
B
12
)
P6=(A21−A11)×(B11+B12)

P
7
=
(
A
12
−
A
22
)
×
(
B
21
+
B
22
)
P7=(A12−A22)×(B21+B22)

Combine: Compute the final matrix 
C
C:

C
11
=
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
C11=P1+P4−P5+P7

C
12
=
P
3
+
P
5
C12=P3+P5

C
21
=
P
2
+
P
4
C21=P2+P4

C
22
=
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
C22=P1−P2+P3+P6

b. Karatsuba Algorithm
Algorithm:
The Karatsuba algorithm is a fast multiplication method that reduces the complexity of multiplying two numbers from 
O
(
n
2
)
O(n 
2
 ) to 
O
(
n
1.585
)
O(n 
1.585
 ).

Divide: Split the numbers into smaller parts.

Conquer: Perform recursive multiplications on these parts.

Combine: Combine the results to get the final product.

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

Divide: Split each number into two parts:

x
=
10
+
2
x=10+2

y
=
30
+
4
y=30+4

Conquer: Compute the products:

a
=
10
×
30
=
300
a=10×30=300

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
10
+
2
)
×
(
30
+
4
)
−
a
−
d
=
12
×
34
−
300
−
8
=
408
−
300
−
8
=
100
e=(10+2)×(30+4)−a−d=12×34−300−8=408−300−8=100

Combine: Compute the final product:

x
×
y
=
a
×
100
+
e
×
10
+
d
=
300
×
100
+
100
×
10
+
8
=
30000
+
1000
+
8
=
31008
x×y=a×100+e×10+d=300×100+100×10+8=30000+1000+8=31008
+
2
)
×=
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

 ×a+10×e+d=
