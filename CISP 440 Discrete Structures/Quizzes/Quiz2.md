## Q1 
What would be negations for the following two statements?
a. John is 6 feet tall and he weighs at least 200 pounds. 
b. The bus was late or Tom's watch was slow. Group of answer choices 
 
    a. John is not 6 feet tall or he weighs less than 200 pounds.
    b. Neither was the bus late nor was Tom's watch slow.


## Q2 
Write each of the two statements in symbolic form and determine whether they are logically equivalent. 
Include a truth table and a few words of explanation. 
a. If you paid full price, you didn't buy it at Crown Books. 
b. You didn't buy it at Crown Books or you paid full price.


    Let p represent “You paid full price” and q represent “You didn’t buy it at Crown Books.” Thus, “If you paid full price, you didn’t buy
    it at Crown Books” has the form p → q.  And “You didn’t buy it at Crown Books or you paid full price” has the form q ∨ p.
![](https://github.com/JeffreybVilla/ComputerScienceBSPATH/blob/main/CISP%20440%20Discrete%20Structures/images/2_2_pq_truth_2T1.png)


## Q3
Suppose that p and q are statements so that p → q is false. Find the truth values of each of the following:

   a.  ∼ p  →  q

   b.  p ∨ q

   c.  q → p

     a.  True

     b.  True

     c.  True


## Q4
p   ∨   q

∼ p

∴  q

What is the Rule of Inference?

    Elimination


## Q5
In the following a set of premises and a conclusion are given. Use the valid argument forms listed in Table 2.3.1 to deduce the conclusion from the premises, giving a reason for each step as in Example 2.3.8. Assume all variables are statement variables.

   a.  ∼ p ∨ q → r

   b.  s ∨ ∼ q

   c.   ∼ t

   d.  p → t

   e.  ∼ p  ∧  r → ∼ s

   f.  ∴  ∼ q
   
        (1)   p → t                                  by premise (d )

                    ∼ t                                        by premise (c)

               ∴  ∼ p                                       by modus tollens

           (2)   ∼ p                                       by (1) 

                ∴ ∼ p ∨ q                              by generalization   

           (3)  ∼ p ∨ q  →  r                    by premise (a)

                   ∼p ∨ q                                 by (2)

               ∴  r                                            by modus ponens 

           (4)   ~ p                                        by (1) 

                     r                                            by (3) 

                ∴  ∼p ∧ r                                by conjunction 

           (5)  ∼ p ∧ r → ∼ s                  by premise (e)  

                    ∼p ∧ r                                  by (4)

                   ∴ ∼s                                        by modus ponens 

           (6)  s  ∨  ∼ q                                  by premise (b) 

                   ∼s                                              by (5)    

                ∴ ∼q                                            by elimination


## Q6
De Morgan’s laws say (1) that the negation of an and statement is logically equivalent to the  ____________ statement in which each component is ______________, and (2) that the negation of an or statement is logically equivalent to the _________________ statement in which each component is _____________ .

  
    or;

    negated;

    and;

    negated
    
    
## Q7 
If statement forms P and Q are logically equivalent, then P ↔ Q is a tautology. Conversely, if P ↔ Q is a tautology, then P and Q are logically equivalent. Use ↔ to convert each of the logical equivalences for the falling statement a tautology. Then use a truth table to verify each tautology.

   p → ( q → r )  ≡  ( p ∧ q ) → r

    ANSWER:
![](https://github.com/JeffreybVilla/ComputerScienceBSPATH/blob/main/CISP%20440%20Discrete%20Structures/images/2_2_pqr_truth_T_2Eq3.png)


## Q8
Determine whether the following statement forms are logically equivalent:

p → ( q → r )   and   ( p → q ) → r

    ANSWER:
![](https://github.com/JeffreybVilla/ComputerScienceBSPATH/blob/main/CISP%20440%20Discrete%20Structures/images/2_2_pqr_truth_T_2Eq.png)


## Q9
   p  ∨  q

   p  →  r

   q  →  r

    ∴  r

What is the Rule of Inference?

    Proof by Division into Cases 


## Q10
Use symbols to write the logical form of the following argument. If the argument is valid, identify the rule of inference that guarantees its validity. Otherwise, state whether the converse or the inverse error is made.

   If I get a Christmas bonus, I’ll buy a stereo.

   If I sell my motorcycle, I’ll buy a stereo.

∴  If I get a Christmas bonus or I sell my motorcycle, then I’ll buy a stereo.

 
      p ⟶ r

      q ⟶ r

      p V q ⟶ r 

      valid, proof by division into cases


## Q11
Let p be the statement “DATAENDFLAG is off,” q the statement “ERROR equals 0,” and r the statement “SUM is less than 1,000.” Express the following sentences in symbolic notation.

   a.  DATAENDFLAG is off but ERROR is not equal to 0.

   b.  DATAENDFLAG is on and ERROR equals 0 but SUM is greater than or equal to 1,000.

   c.  Either DATAENDFLAG is on or it is the case that both ERROR equals 0 and SUM is less than 1,000.
   
    a.  p ∧  ~ q

    b.  ( ~ p ∧ q ) ∧ ~ r

    c.  ~ p ∨ ( q ∧ r )       
    
    
## Q12
The negation of  “ if p then q ” is ___________________.

    p ∧   ∼ q 
    
## Q13
Choose the best choice for the following?

Construct truth tables for the following statements.

   a.  p ∧ ∼ r  ↔  q ∨ r

   b.  ( p → r )  ↔  ( q → r )

    ANSWER: 
![](https://github.com/JeffreybVilla/ComputerScienceBSPATH/blob/main/CISP%20440%20Discrete%20Structures/images/2_2_pqr_truth_2T1.png)


## Q14
Given the following information about a computer program, find the mistake in the program. 

   a.   There is an undeclared variable or there is a syntax error in the first five lines.

   b.  If there is a syntax error in the first five lines, then there is a missing semicolon or a variable name is misspelled.

   c.  There is not a missing semicolon.

   d.  There is not a misspelled variable name.
   
     The program contains an undeclared variable. 

## Q15
An argument is called ___________ if, and only if, it is _________ and all its premises are ________. An argument that is not __________ is called ______________.

What would be the best choice to fill in blanks for the above question?

    sound;  valid;    true;   sound;  unsound 


## Q16
The following represents the common form of each argument using letters to stand for component sentences, and fill in the blanks so that the argument in part (b) has the same logical form as the argument in part (a).
a.  If n is divisible by 6, then n is divisible by 3.

If n is divisible by 3, then the sum of the digits of n is divisible by 3.

Therefore, if n is divisible by 6, then the sum of the dig- its of n is divisible by 3.

(Assume that n is a particular, fixed integer.)

b.  If this function is  __________ then this function is differentiable.

If this function is ______________ then this function is continuous.

Therefore, if this function is a polynomial, then this function   _____________________ .

    common form: If p then q.

    If q then r

    Therefore,  if p then r.

    b.  a polynomial;   differentiable;  is continuous 
    
## Q17
“If compound X is boiling, then its temperature must be at least 150◦ C.” Assuming that this statement is true, which of the following must also be true?

   a.   If the temperature of compound X is at least 150◦ C, then compound X is boiling.

   b.  If the temperature of compound X is less than 150◦ C, then compound X is not boiling.

   c.  Compound X will boil only if its temperature is at least 150◦ C.

   d.  If compound X is not boiling, then its temperature is less than 150◦ C.

   e.  A necessary condition for compound X to boil is that its temperature be at least 150◦ C.

   f.  A sufficient condition for compound X to boil is that its temperature be at least 150◦ C.
   
    b, c and e. 
    
## Q18
write each of the two statements in symbolic form and determine whether they are logically equivalent. Include a truth table and a few words of explanation.

   1.  If you paid full price, you didn’t buy it at Crown Books.

   2.  You didn’t buy it at Crown Books or you paid full price.
   
   
   
    Let p represent “You paid full price” and q represent “You didn’t buy it at Crown Books.” Thus, “If you paid full price, you didn’t buy it at Crown Books” has the form p → q.  And “You didn’t buy it at Crown Books or you paid full price” has the form q ∨ p.
![](https://github.com/JeffreybVilla/ComputerScienceBSPATH/blob/main/CISP%20440%20Discrete%20Structures/images/2_2_pq_truth_2T1 (1).png)

## Q19 same

## 20
   Use symbols to write the logical form of the following arguments. If the argument is valid, identify the rule of inference that guarantees its validity. Otherwise, state whether the converse or the inverse error is made.

   a.  If I go to the movies, I won’t finish my homework.

   If I don’t finish my homework, I won’t do well on the exam tomorrow.

   ∴ If I go to the movies, I won’t do well on the exam tomorrow.

   b.  If this number is larger than 2, then its square is larger than 4.

   This number is not larger than 2.

   ∴ The square of this number is not larger than 4.
    
    
      
    a.  p → q

    q → r

    ∴  p  →  r

    valid: transitivity



    b.   p → q

    ∼ p

    ∴ ∼  q

    invalid: inverse error
