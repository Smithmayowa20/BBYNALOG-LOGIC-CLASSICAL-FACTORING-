










Alli-Smith Method : Prime Factorization & Diophatine Equations











# ABSTRACT



Factoring of a co-prime number into it's component prime numbers and finding the right integer values for diophatine equations, is considered to be a problem that does not have a polynomial time solution, the current optimal algorithm appears to be Shor's quantum computing algorithm, In this paper we consider a polynomial time method; (Alli-Smith Signal Factorization Method), that can be easily implemented on classical computers.


# OUTLINE


 
1). Introduction

2). Alli-Smith Signal Factorization Method (A.S.S.F.M)

3). Riemann Hypothesis

4). Diophatine Equations

5). Alli-Smith Signal Diophatine Method (A.S.S.D.M)

6). Conclusion

7). References




#INTRODUCTION



Consider an integer co-prime number d that is composed of two integer prime numbers that both have very large number of digits; n & m , finding the prime numbers n & m is considered to be a non-polynomial time problem with current classical techniques. 


d = n * m


The generally agreed upon algorithm is to test if d/x has a solution y;


d/x = y 


Where;


x is an integer number from 1 to Floor[Sqrt[d]]

& for every x; y is an integer solution: x <= Floor[Sqrt d]] < y 

If for any x from the interval above the re is an int eger solution y then x & y are considered to be the co-prime numbers of d.


Let B : Prime Factorization Equation of form (x * y) - c = 1


& M : (x * y) - c


where; c = number to be factored(d) - 1


Let  Alli-Smith Expression (A.S.E(K))  = (K + 1)/((F * (K - 1)) + 1)


where; F is a positive very large number that approaches infinity.


S_1 : Sum[A.S.E(M), {x,1,d}, {y,1,d}] - Expression(1)


S_1/4 is the exact number of possible integer parameter combinations of (x * y) = c + 1


Sum[A.S.E(M), {x,1,d}, {y,1,d}] = Sum[(F * N * y + (1 - 2 * F) PolyGamma[0, (1 + F * (-1 - c + y))/(F * y)] + (-1 + 2 * F) PolyGamma[0, (1 + F * (-1 - c + y + N * y))/(F * y)])/(F^2 * y),{y,1,d}] 

Let; T = (F * N * y + (1 - 2 * F) PolyGamma[0, (1 + F * (-1 - c + y))/(F * y)] + (-1 + 2 * F) PolyGamma[0, (1 + F * (-1 - c + y + N * y))/(F * y)])/(F^2 * y)








#ALLI-SMITH SIGNAL FACTORIZATION METHOD(A.S.S.F.M)



To find the factors of the number d from 1 to that number, we convert the number using Expression (1) above into a signal function where all the factor's combination of the number d; (x * y), have their summation value equal to 2, and other non-factor's combination have their summation value asymptotically equalling 0, then we implement a basic binary search to find the factors of the number d.














#RIEMANN HYPOTHESIS



A number d is considered to be a prime number if the value of it's S_1/4 expression above is 1.

We consider an expression;

 R.H.E(d) = Sum[A.S.E(M), {x,1,d}, {y,1,d}]/4

The distribution of prime numbers from integers; 1,2,3 to an arbitrary integer number R_n can be better observed by considering a series R.H.E(1),R.H.E(2),R.H.E(3),R.H.E(R_n).

1,2, 3, ..., R_n <> R.H.E(1), R.H.E(2), R.H.E(3), ..., R.H.E(R_n).  -  Expression(2)

With further utilization of A.S.E, we can convert the R.H.E(d) series on the right hand side of Expression(2) above into a prime number signal series where the prime numbers from 1,2,3, to an arbitrary integer number R_n all have the value 1 and all non-prime numbers of this series have their value asymptotically equalling 0.

P.  S.S[1, R_n] = A.S.E(R.H.E(1))/2, A.S.E(R.H.E(2))/2, A.S.E(R.H.E(3))/2, ..., A.S.E(R.H.E(R_n))/2

Where;

P.S.S = Prime Number Signal Series

Using the prime number distribution formular it is assumed that the number of prime numbers from 1 to an arbitrary integer number R_n can be obtained by;


We can get a better formula by utilizing the P.S.S signal series above;

Sum[P.S.S[1, R_n]], {1, R_n}] - Expression(3)

The value of Expression 3 above is the exact number of prime numbers from 1 to any arbitrary integer number R_n.











#DIOPHATINE EQUATIONS



Diophatine Equations with arbitrary number of variables can also be resolved easily using A.S.E, to find the missing integer solutions for each variable.

Let B_1 : Diophatine Equation of form (a^n_1 + b^n_2 + .... + z^n) - c = 1

& M_1 : (a^n_1 + b^n_2 + .... + z^n) - c

where;

c = value of the diophatine equation B_1 above(v) - 1

& n_1, n_2, ... n = powers of the variables of the diophatine equation.

S_2 : Sum[A.S.E(M_1), {a, -p, +p}, {b, -p, +p}, ..., {z, -p, +p}] - Expression(4)

where; p is an arbitrary interval.

S_2/4 is the exact number of possible integer parameter combinations of (a^n + b^n + .... + z^n) = c + 1, that lie within interval -p to p.




#ALLI-SMITH SIGNAL DIOPHATINE METHOD(A.S.S.D.M)




To find the value of the variables of any diophatine equation, we convert the diophatine equation using Expression(4) into a signal function where all the integer solutions of the diophatine equation have their summation value equal to 2 and all other non-integer solutions of the diophatine equation have their summation value asymptotically equalling 0, then we implement a basic binary search to find the integer solutions of the diophatine equation.






#CONCLUSION





The time complexity of this algorithm is O (Log2(n))










#REFERENCES





1).

