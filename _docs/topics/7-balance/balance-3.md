---
title: Distributions
permalink: /docs/balance-3/
---

## Weighted Distributions

A weighted distribution is one in which one result is more likely than others. A common example is 2d6 (7 is 6x more likely than 2 or 12). Another possibility is having a non-linear distribution of numbers on the sides of the die, for example: The attack die from Small World.

<centre>        
    <img src="{{ "/assets/img/balance/wtdie.png" | relative_url }}" alt="Weighted Die" class="img-responsive">
</centre>

## Randomizer Technologies in Paper Games

The most common randomizers in paper games are
* Dice
* Spinners
* Decks of Cards
Each have particular traits that make them attractive for different situations.  

### Dice
A single die has a linear probability distribution. The more dice you add together, the more the result is biased toward the average. Standard die sizes include: 4, 6, 8, 10, 12, and 20-sided. Commonly available packs of dice for gaming usually include 1d4, 2d6, 1d8, 2d10, 1d12, and 1d20. 

Two d10 are sometimes used as Percentile Dice. One die is used for the 1s place (marked with the numbers from 0–9), the other for the 10s place (marked with the multiples of 10 from 00–90). Rolled together, they give an even distribution of the numbers from 00 to 99 (where a roll of 0 and 00 is usually counted as 100%).

### Spinners
All spinners have a rotating element and a still element. In the image, the gray element is still, and the black rotates. Spinners are often used for children's games, young children can't roll dice with accuracy. Spinners are more difficult to swallow than dice.  
Spinners also provide some distinct advantages over dice  
* Spinners can have any number of slots (it's difficult to make a d7)
* Spinners can have any kind of weighted distribution without the limits of a die(image C below)

<centre>        
    <img src="{{ "/assets/img/balance/randomizer.png" | relative_url }}" alt="Spinners" class="img-responsive">
</centre>

### Cards
A standard deck of playing cards includes
* 13 ranks of 4 different suits ( Ranks: A-10, J, Q, & K )
* Suits are usually Clubs, Diamonds, Hearts, & Spades
* Sometimes two Jokers

<centre>        
    <img src="{{ "/assets/img/balance/cards.png" | relative_url }}" alt="Cards" class="img-responsive">
</centre>

When drawing a single card, you have these probabilities
* Chance of drawing a particular single card: 1/52 (0.0192 ≈ 2%)
* Chance of drawing a specific suit: 13/52 = 1/4 (0.25 = 25%)
* Chance of drawing a face card: 12/52 = 3/13 (0.2308 ≈ 23%) 
Custom Card Decks
* Very easy to make!
* Easily re-configurable!
When to shuffle?
* Shuffle the deck before each draw to have it act like a die roll
  * An equal chance of drawing any single card
* Shuffle the deck after it's exhausted to enforce theoretical probability
  * Each card will be seen once before any are seen a second time
  * However, this can allow card counting
* For a standard 52-card deck, according to mathematician and magician Persi Diaconis, seven good riffle shuffles should be sufficient to create a truly random distribution

### Bulls and Cows (Traditional Game)
The basis for Mastermind (1970 by Mordecai Meirowitz). Players take turns trying to guess their opponent's code. The code is a series of 4 digits (0-9). Each digit must be different from the others. For each guess, the guesser receives a number of bulls and cows.
* Bull: For each number that is in the correct place
* Cow: For each number that is in the code but in the wrong position

<centre>        
    <img src="{{ "/assets/img/balance/mastermind.png" | relative_url }}" alt="Mastermind" class="img-responsive">
</centre>

## Randomizer Technologies in Video Games

The use of randomness in games has to be considered carefully. What are you trying to achieve with the randomness? How will the inclusion of randomness affect the game?

### Generating Random Numbers

Most programming languages provide a random number generator (RNG). Below is an example in Python.

```python
import random

randFloat = random.random()
print (randFloat)

randIntRange = random.randint(5,10)
print(randIntRange)
```

Python's `random` library comes with a number of functions. See [https://www.w3schools.com/python/module_random.asp](https://www.w3schools.com/python/module_random.asp) for more details.  

#### More Random Randomness

Most random number generators are actually *pseudo-random number generators*. They do not generate a truly random number but instead use an algorithm to generate a number from a sequence. The random number generator in most programming languages will generate the same "random" numbers in the same order every time a program is run! The system uses a *seed* to determine where to start in the sequence and, unless given a new seed, will use the same seed every time the program start.

Ironically this doesn't seem to be true under replit.com but we can replicate it by deliberately using the same seed before generating a random number.

```python
random.seed(1)
randFloat = random.random()
print (randFloat)

random.seed(1)
randFloat = random.random()
print (randFloat)

random.seed(1)
randFloat = random.random()
print (randFloat)

random.seed(1)
randFloat = random.random()
print (randFloat)
```

produces

```console
0.13436424411240122
0.13436424411240122
0.13436424411240122
0.13436424411240122
```

We can get round this by *seeding* the RNG with a random number. Problem is how do we get a random seed? The usual solution is to use the computer's clock. Since the clock is constantly changing using it as the seed will generate different results every time. 

```python
random.seed(datetime.now())
```

### RNG Distribution

The numbers generated by an RNG are, by default, *uniformly distributed*. This means that the numbers will (given enough time) cover the full range of possible results and will be equally spread across those results. If you were to generate a random integer from 1 to 10 a million times you would get something close to 100,000 of each number 1, 2, 3, 4, 5, 6, 7, 8, 9, 10. It won't be exactly that but it should be close.  

Sometimes we don't want a flat, uniform distribution. Can we do that? Well yes, many RNGs have that capability built in. Python's `random` has a function called `normal` which will generate a a random number from a normal distribution - it will be more likely to be close to the mean value and increasingly unlikely to generate numbers further away.  

### Simulating Dice

If we wish to simulate dice we should simulate each individual dice rolled and add the results together rather than try to generate a random number within the range of possible values to ensure we get the same distribution as the dice would.  

For example rolling 3D6 (three six sided dice and adding them together) will result in a number between 3 and 18 (inclusively). However you are unlikely to roll a 3 or an 18 and much more likely to roll a 10 or 11 because 10 and 11 can be rolled in many more ways. You only get a 3 by rolling three 1s. You can get a 10 by rolling a 1,3,6 or a 1,4,5 or a 2,2,6 or a 2,3,5, etc. So a good replication of rolling three six sided dice and adding them together is to generate three random numbers from 1 to 6 and add them together.  

### Random Playing Cards

If we want to generate a random playing card we could generate a random number from 1 to 4 to determine the suit and a random number from 1 to 13 to determine the card (with 11, 12, 13 for Jack, Queen King).  

That approach is fine if we want to simulate players cutting the deck to pick a random card but if we are simulating cards being dealt to players it is useless. Why? Well every player could be dealt the same cards. It is unlikely but it is possible that each player gets five King of Clubs. Probably not the result we are looking for.

A better approach is to generate a list of cards, randomise the order and then remove cards from the list as they are dealt out. That way each card will only be dealt once.

### Simulating Spinners

If the spaces on a spinner are all the same size then simulating one is simply a matter of generating a number in the appropriate range. But what is the sizes on the spinner are different.  

The easiest solution is to generate a lookup table and use it with a random number to generate the result. I always use a percentage based table because I've played tabletop roleplaying games for many years and a d100 lookup table is how I think of these things.  

Imagine you have a spinner with five spaces. The two smallest (red and blue) are the same size. There are two that are twice as big as each of the smallest (green and yellow) and one that is twice as big again (purple). We could generate a lookup table as follows -  

|Random Number(0,100)|Result|
|---|---|
|1-10|Red|
|11-20|Blue|
|21-40|Green|
|41-60|Yellow|
|61-100|Purple|

Now we generate a number in the 1 to 100 range and look up the result in the left hand column, the right hand column tells us the spinner result.  
