##Suggested reading in raw code ##
<br>
Warshall's Algorithm
<br>
Let the given set A have a elements and R be a relation defined on A. Let M_{R} be n*n martrix
<br>
of the relation R. 
<br>
Step 1: Denote the matrix M_{R} by W_{0}( W for Warshall).
<br>
Step 2: Now, consider a blank square matrix of order n and denote it by w_{1} . Transfer all 1's
from W_{0} to W_{1}
<br>
Step 3: Observe the first column of w_{0} and the first row of w_{0} and find the positions of 1 in the first column and first row
If 1 appears in P1, P2,....positions of the first column and 1 appears in Q1,Q2,... positions of the first row, then put 1 in the position 
Pi,Qi of the above blank matrix (if 1 is not already there) 
Put 0 in all other positions of the above matrix and get the completed matrix W_{1} 
<br>
Step 4: Write a blank matrix of order r again and denote it by W_{2} Transfer all 1's from the matrix W_{1} to W_{2} 
Now, observe the second column of w_{1} and second row of w_{1}. If 1 appears in P1, P2,.... positions of the second column and in Q1,Q2,... positions of the second row, put 1 in the positions Pi,Qi  of the above matrix W_{2}
<br>
Step 5: Repeat the procedure till you get W_{n} in which no change is possible. Note that to fill up the matrix W_{k}, we consider the kth column and kth row of the matrix W_{k-1}.
<br>
The procedure will be clearer after you read the solution of the following example
NOTE :- The matrix  whose elements are either 1 or 0 is called a Boolean Matrix
let A ={1,2,3,4} and  R = {(1,1),(1,2),(1,4),(2,4),(3,1),(3,2),(4,2),(4,3),(4,4)}
Find transitive closure of R by using Warshall's Algorithm.
Step 1
Wo =  
 1 1 0 1
 0 0 0 1
 1 1 0 0
 0 1 1 1
Step 2
Column 1-->Pi = 1, 3,
Row 1-->Qi = 1, 2, 4,
So,we put one in (1,1)(1,2)(1,4)(3,1)(3,2)(3,4) positions,if 
there is no one already
W 1 =
 1 1 0 1
 0 0 0 1
 1 1 0 1
 0 1 1 1
Step 3
Column 2-->Pi = 1, 3, 4,
Row 2-->Qi = 4,
So,we put one in (1,4)(3,4)(4,4) positions,if there is no one already
W 2 =
 1 1 0 1
 0 0 0 1
 1 1 0 1
 0 1 1 1
Step 4
Column 3-->Pi = 4,
Row 3-->Qi = 1, 2, 4,
So,we put one in (4,1)(4,2)(4,4) positions,if there is no one already
W 3 = 
 1 1 0 1
 0 0 0 1
 1 1 0 1
 1 1 1 1
Step 5
Column 4-->Pi = 1, 2, 3, 4,
Row 4-->Qi = 1, 2, 3, 4,
So,we put one in (1,1)(1,2)(1,3)(1,4)(2,1)(2,2)(2,3)(2,4)(3,1)(3,2)(3,3)(3,4)(4,1)(4,2)(4,3)(4,4) positions,if there is no one already
W 4 =
 1 1 1 1
 1 1 1 1
 1 1 1 1
 1 1 1 1
