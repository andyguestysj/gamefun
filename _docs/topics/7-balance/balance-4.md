---
title: Permutations & Combinations
permalink: /docs/balance-4/
---

## Permutations
In maths, a permutation is a selection of elements where the order matters.
* The code in Bulls & Cows is a permutation without repetition
Permutations With Repeating Elements
* A bit easier to calculate than those without repetition
* To find the number of possible permutations, multiply the number of choices per slot by the number of slots
* For a selection of four digits (0-9)
* 10 x 10 x 10 x 10 = 10,000 possible permutation
Permutations Without Repeating Elements
* Subtract 1 from possible choices for each subsequent slot
* For Bulls & Cows
  * 10 x 9 x 8 x 7 = 5,040 possible permutations without repetition

## Combinations
In maths, a combinations is a selection of elements where order doesn't matter. 1234, 1423, 4231, and 2431 are all the same combination.
Example Combination
* How many possible combinations of three scoops of ice cream are there if there are 8 flavors?
  * For each scoop, there are 8 possible flavors
  * But, the order of the scoops don't matter, so 123 is the same as 213
* Written 8C3 in math (from 8 possibilities, choose 3)
* Formula: n is the number of possibilities, k the # of choices
  * nCk = n! / ( k! * (n-k)! )
  * 8C3 
    * = 8! / (3! * (8-3)! )
    * = 8*7*6*5*4*3*2*1 / ( 3*2*1 * ( 5*4*3*2*1) )	
    * = 8*7*6*5*4*3*2*1 / ( 3*2*1 * ( 5*4*3*2*1) )
    * = 8*7*6 / 3*2*1 
    * = 336 / 6 
    * = 56 combinations
  * Pascal's Triangle

<centre>        
    <img src="{{ "/assets/img/balance/PascalTriangle.jpg" | relative_url }}" alt="Pascal's Triangle" class="img-responsive">
</centre>

<centre>        
    <img src="{{ "/assets/img/balance/combs.png" | relative_url }}" alt="Pascal's Triangle Combinations" class="img-responsive">
</centre>


  





