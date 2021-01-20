# Fermat's Last Theorem

### Fermat's Last Theorem states that no three positive integers a, b, and c can satisfy the equation a^n + b^n = c^n for any integer value of n greater than two.

- Write a psuedocode algorithm to empirically prove this theorem by exhaustively checking
for all combinations of integers less than or equal to n.

- Hint: One way to do this is to generate all permutations of 4 variables, n, a, b, c, (skipping n = 1 or 2) then evaluate the
expression for each permutation. 

- Let n go from 3 to some large value N.

- What is the TIME COMPLEXITY of your algorithm in BigO notation?



## CODE
	// C++ program to verify fermat's last theorem 
	// for a given range and n. 
	#include <bits/stdc++.h> 
	using namespace std; 

	void testSomeNumbers(int limit, int n) 
	{ 
	if (n < 3) 
		return; 

	for (int a=1; a<=limit; a++) 
		for (int b=a; b<=limit; b++) 
		{ 
			// Check if there exists a triplet 
			// such that a^n + b^n = c^n 
			int pow_sum = pow(a, n) + pow(b, n); 
			double c = pow(pow_sum, 1.0/n); 
			int c_pow = pow((int)c, n); 
			if (c_pow == pow_sum) 
			{ 
				cout << "Count example found"; 
				return; 
			} 
		} 

		cout << "No counter example within given"
				" range and data"; 
	} 

	// driver code 
	int main() 
	{ 
		testSomeNumbers(10, 3); 
		return 0; 
	} 


## Time Complexity
O(N^2)
