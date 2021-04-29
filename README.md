# HOG
Stimulation of hog
<img width="1386" alt="Screen Shot 2021-04-29 at 4 45 40 PM" src="https://user-images.githubusercontent.com/60949882/116616226-72757700-a90a-11eb-8166-300b502d6a06.png">


The hog game consists of the following rules:

In Hog, two players alternate turns trying to be the first to end a turn with at least 100 total points. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes.

To spice up the game, we will play with some special rules:

# Pig Out. 
If any of the dice outcomes is a 1, the current player's score for the turn is 1.

- Example 1: The current player rolls 7 dice, 5 of which are 1's. They score 1 point for the turn.
- Example 2: The current player rolls 4 dice, all of which are 3's. Since Pig Out did not occur, they score 12 points for the turn.

# Free Bacon. 
A player who chooses to roll zero dice scores the one more than the last digit of the product of the digits in the opponent's score.

- Example 1: The opponent has 46 points, and the current player chooses to roll zero dice. 4 * 6 = 24; the last digit is a 4, so the current player gains 4 + 1 = 5 points.
- Example 2: The opponent has 28 points, and the current player chooses to roll zero dice. 2 * 8 = 16; the last digit is a 6, so the current player gains 6 + 1 = 7 points.
- Example 3: The opponent has 5 points, and the current player chooses to roll zero dice. 0 * 5 = 0; the last digit is a 0, so the current player gains 0 + 1 = 1 point.

# Swine Align. 
Swine Align. After points for the turn are added to the current player's score, if both players have a positive score and the Greatest Common Divisor (GCD) of the current player's score and the opponent's score is at least 10, take another turn.

Example 1: At the end of the first player's turn, the players have scores of 8 and 36. The GCD of the scores is 4, so the first player does not take another turn due to swine align.

Example 2: At the end of the first player's turn, the players have scores of 20 and 30. The GCD of the scores is 10, so the first player takes an extra turn.

Example 3: At the end of the first player's turn, the players have scores of 24 and 36. The GCD of the scores is 12, so the first player takes an extra turn. The first player rolls a 12 and the scores are now 36 and 36. The GCD of the scores is 36, so the first player takes yet another turn.

Example 4: At the end of the first player's turn, the players have scores of 15 and 0. Swine align only applies when both player scores are positive (not zero), so the first player does not take another turn due to swine align.

### Pig Pass. 
After points for the turn are added to the current player's score, if the current player's score is lower than the opponent's score and the difference between them is less than 3, the current player takes another turn.

# How to start the GUI:
```
python3 hog_gui.py
```
(source: cs61a fall 2020)
cs61a.org
