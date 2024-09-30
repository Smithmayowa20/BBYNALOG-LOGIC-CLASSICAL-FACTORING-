










Alli-Smith Method : Prime Factorization & Diophatine Equations











#ABSTRACT



Factoring of a co-prime number into it's component prime numbers and finding the right integer values for diophatine equations, is considered to be a problem that does not have a polynomial time solution, the current optimal algorithm appears to be Shor's quantum computing algorithm, In this paper we consider a polynomial time method; (Alli-Smith Method), that can be easily implemented on classical computers.




# OUTLINE


1). Introduction

2). Alli-Smith Signal Method (A.S.S.M)

3). Riemann Hypothesis

4). Diophatine Equations

5). Conclusion

6). References





#INTRODUCTION



Consider an integer co-prime number d that is composed of two integer prime numbers that both have very large number of digits; n & m , finding the prime numbers n & m is considered to be a non-polynomial time problem with current classical techniques. 


d = n * m


The generally agreed upon algorithm is to test if d/x has a solution y;


d/x = y 


Where;


x is an integer number from 1 to Ceil[Sqrt[d]]

& for every x, y is an integer solution; x < y < Ceil[Sqrt[d]]

If for any x from the interval above there is an integer solution y then x & y are considered to be the co-prime numbers of d.


Let B : Prime Factorization Equation of form (x * y) - c = 1


& M : (x * y) - c


where; c = number to be factored(d) - 1


Let  Alli-Smith Expression (A.S.E(K))  = (K + 1)/((F * (K - 1)) + 1)


where; F is a positive very large number that approaches infinity.


S_1 : Sum[A.S.E(M), {x,1,d}, {y,1,d}]


S_1/4 is exactly the number of possible combinations of (x * y) = c + 1


Sum[A.S.E(M), {x,1,d}, {y,1,d}] = Sum[(F N y + (1 - 2 F) PolyGamma[0, (1 + F (-1 - c + y))/(F y)] + (-1 + 2 F) PolyGamma[0, (1 + F (-1 - c + y + N y))/(F y)])/(F^2 y),{y,1,d}]





#ALLI-SMITH SIGNAL METHOD(A.S.S.M)



To find the factors of the number d from 1 to that number, we convert the number using A.S.E above into a signal function where all the factor's combination of the number d have their summation value equal to 2, and other non-factor's combination have their summation value asymptotically equalling 0, then we implement a basic binary search to find the factors of the number d.





#RIEMANN HYPOTHESIS



A number d is considered to be a prime number if the value of it's S_1/4 expression above is 1.

We consider an expression;

 R.H.E(d) = Sum[A.S.E(M), {x,1,d}, {y,1,d}]/4

The distribution of prime numbers from integers; 1,2,3 to an arbitrary integer number R_n can be better observed by considering a series R.H.E(1),R.H.E(2),R.H.E(3),R.H.E(R_n).

1,2, 3, ..., R_n <> R.H.E(1), R.H.E(2), R.H.E(3), ..., R.H.E(R_n).  -  Expression 1

With further utilization of A.S.E, we can convert the R.H.E(d) series on the right hand side of expression 1 above into a prime number signal series where the prime numbers from 1,2,3, to an arbitrary integer number R_n all have the value 1 and all non-prime numbers of this series have their value asymptotically equalling 0.

P.S.S[1, R_n] = A.S.E(R.H.E(1))/2, A.S.E(R.H.E(2))/2, A.S.E(R.H.E(3))/2, ..., A.S.E(R.H.E(R_n))/2

Where;

P.S.S = Prime Number Signal Series

Using the prime number distribution formular it is assumed that the number of prime numbers from 1 to an arbitrary integer number R_n can be obtained by;


We can get a better formula by utilizing the P.S.S signal series above;

Sum[P.S.S[1, R_n]], {1, R_n}] - Expression 2

The value of expression 2 above is the exact number of prime numbers from 1 to any arbitrary integer number R_n.





#DIOPHATINE EQUATIONS



Let B_1 : Diophatine Equation of form (a^n + b^n + .... + z^n) - c = 1


& M_1 : (a^n_1 + b^n_2 + .... + z^n) - c


where; c = value of the diophatine equation(v) - 1

S_2 : Sum[A.S.E(M_1), {a,-v,v}, {b,-v,v}, ..., {z,-v,v}]

S_2/4 is exactly the number of possible combinations of (a^n + b^n + .... + z^n) = c + 1





# CONCLUSION



The time complexity of this algorithm is O (Log2(n))





# REFERENCES



1).

