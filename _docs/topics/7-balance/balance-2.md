---
title: Schell's Rules
permalink: /docs/balance-2/
---

## Schell's Ten Rules of Probability

In The Art of Game Design, Jesse Schell lists 10 rules of probability that all game designers should know.

### Schell's 10 Rules:
* Rule #1 - Fractions = Decimals = Percents
* Rule #2 - Probabilities range from 0 to 1
* Rule #3 - Probability is Sought Outcomes divided by Possible Outcomes
* Rule #4 - Enumeration can solve simple problems
* Rule #5 - When sought outcomes are mutually exclusive (OR), add their probabilities
* Rule #6 - When sought outcomes are not mutually exclusive (AND), multiply their probabilities
* Rule #7 - One minus "does" = "doesn't"
* Rule #8 - The sum of multiple dice is not a linear distribution
* Rule #9 - Theoretical vs. practical probability
* Rule #10 - Phone a friend


### Rule #1 - Fractions = Decimals = Percentages
All three are different ways to represent the same numbers.  
The chance of rolling a 1 on 1d20 (a 20-sided die) is  
* 1/20 as a Fraction
* 0.05 as a Decimal
*   5% as a Percent 
To convert between them:  
* Fraction to Decimal  - Type the fraction into a calculator
* Percent to Decimal   - Divide by 100 (e.g., 5% = 5/100 = 0.05)
* Decimal to Percent   - Multiply by 100 (e.g., (0.05 * 100)% = 5%)
* Anything to Fraction - Unfortunately, there's no easy way to do so

### Rule #2 - Probabilities range from 0 to 1
According to Rule #1 - 0 to 1, and 0/1 to 1/1, and 0% to 100% are the same.
There can never be less than a 0% chance.  
There can never me more than a 100% chance.  

### Rule #3 - Probability is Sought Outcomes divided by Possible Outcomes
Example: Wanting to roll a 6 on 1d6
* Sought outcomes: 1 (the roll of 6)
* Possible outcomes: 6 (the number of sides of the die)
* Probability: 1/6 (≈1.666666 or ≈17%)
Example: Wanting to draw a spade from a deck of cards
* Sought outcomes: 13 (the number of spades in the deck)
* Possible outcomes: 52 (total number of cards)
* Probability: 13/52 = 1/4 (0.25 or 25%)

### Rule #4 - Enumeration can solve simple problems
If you have a low number of possible outcomes, enumeration can work, for example see the 2d6 example above. However, 10d6 has 60,466,176 possible rolls! This can only be reasonably enumerated by a computer

### Rule #5 - When sought outcomes are mutually exclusive, add their probabilities
Example: Drawing either an Ace or a Face Card from a deck
* There are no cards that are both an Ace and a Face Card
* So these sought outcomes are mutually exclusive
* Sought outcomes:
  * 4	Aces
  * 12	Face Cards
 * Possible outcomes: 52 total cards in the deck
 * Probability: 4/52 + 12/52 = 16/52 = 4/13 (≈0.3077 or ≈31%)
Example: Rolling 1, 2, or 3 on 1d6
* Sought outcomes: 3 (1, 2, or 3)
* Possible outcomes: 6 (number of sides of the die)
* Probability: 3/6 = 1/2 (0.5 or 50%)
If you use OR to describe sought outcomes, you can add them together.

### Rule #6 - When sought outcomes are not mutually exclusive, multiply their probabilities
Example: Drawing a card that is a Face Card and a Spade
* These sought outcomes are NOT mutually exclusive
* Probability for each case:
  * 12/52 to draw a Face Card AND 13/52 to draw a Spade
* Total Probability:    
  *   12/52 x 13/52
  * = (12 x 13) / (52 x 52)
  * =  156 / 2704
  * =  3 / 52 (≈0.0577 or ≈6%)
Example: Rolling two sixes on 2d6
* Sought outcomes:    1 on Die A and 1 on Die B
* Possible outcomes:  6 on Die A and 6 on Die B
* Probability: 1/6 x 1/6 = 1/36 (≈0.0278 or ≈3%)
If you use AND to describe sought outcomes, you multiply them together.


#### Rule #7 - One minus "does" = "doesn't"
The chance of something happening is one minus the chance of it NOT happening. Sometimes it's easier to figure the chance of something not happening and reverse it.  
Example: The chance of rolling at least one 6 on 2d6
* Sought outcomes: 6_6 OR 6_x OR x_6 (x means a non-6)
* These are mutually exclusive (with an OR), so add
* Probability: ( 1/6 x 1/6 ) + ( 1/6 x 5/6 ) + ( 1/6 x 5/6 )
  *            = 1/36 + 5/36 + 5/36 
  *            = 11/36
Example: The chance of Die A rolling a non-six AND Die B rolling a non-six (the opposite of the previous example).
* These sought outcomes are NOT mutually exclusive, so multiply. 
* Probability: 5/6 x 5/6 = 25/36
* Therefore, the chance of rolling at least one 6 on 2d6 is
  * Probability: 1 - 25/36 = 11/36 (≈0.3055 or ≈30.6%)

### Rule #8 - The sum of multiple dice is not a linear distribution
With multiple dice, the probability of sums is a bell curve. The more dice, the more extreme the bell curve).

<centre>        
    <img src="{{ "/assets/img/balance/distrubutions.png" | relative_url }}" alt="Distributions" class="img-responsive">
</centre>

### Rule #9 - Theoretical vs. practical probability
Results of real rolls will differ from theoretical predictions. This happens for several reasons - 
* Many dice are not perfectly balanced
* Probability is only the likelihood that something will happen, not a guarantee
For 2d6, you can guarantee theoretical results by printing a deck of 36 cards (one 2, six 7s, two 11s, etc.). Only shuffle the deck once it's been completely exhausted. This is an option for Settlers of Catan and was implemented in Tetris.  
You can also write a computer program to roll dice randomly several million times – The Monte Carlo approach. The results will be similar to the theoretical bell curve but not exact. This could be used to experimentally determine which properties on a Monopoly board are most likely to be landed on.  

### Rule #10 - Phone a friend
Nearly all college computer science and math students take classes in probability (heh!). Try asking one of them if you're stuck on a probability problem. This is how the study of probability began, the Chevalier de Méré wanted to know why - he won when he bet someone he would roll one 6 on 4 rolls of 1d6 but lost when he bet someone he would roll one 12 on 24 rolls of 2d6.  

The Chevalier asked his friend Blaise Pascal for help, and Pascal began corresponding Pierre de Fermat about it.  
Probability of one 6 in 4 rolls of 1d6
       1 - ( 5/6 x 5/6 x 5/6 x 5/6 )
    =  1 - ( 625 / 1,296 )
    =  ( 1,296 - 625 ) / 1,296
    =  671 / 1,296  
    ( ≈ 0.5177 or ≈ 52% )
Probability of one 12 in 24 rolls of 2d6  
Probability of one 12 in a roll of 2d6: 1/36  
Probability of NOT rolling a 12 on a roll of 2d6: 35/36  
Probability of NOT rolling a 12 on 24 rolls of 2d6:
    ( 35/36 )<sup>24</sup> ≈ ( 0.97222 )<sup>24</sup> ≈ 0.5086 ≈ 50.8%
Probability of rolling one 12 on 24 rolls of 2d6:
    1 - ( 50.8% ) ≈ 49.2%


















