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
