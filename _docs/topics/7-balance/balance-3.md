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

