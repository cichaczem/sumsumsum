SumSumSum
======

Equipment
---------
- figures with multiplier x1
- figure with multiplier x2
- 1 board 6x6 fields
- 30 random game blocks

Game tiles
----------
Every tile should have random number between -4 and 5 which indicates amount of points this block gives to players.

Figures
-------
Player figure indicates that this player will gain all points from every game tile in row and column where the figure was placed.

Starting setup
--------------
There are no players' figures or game tiles on the board.
Each player has 3 figures (1 with multiplier x2 and 2 with multiplier x1) and 2 random game tiles.

Players turn
------------
Every player during his turn can:
1) place 1 figure on the board
or
2) draw one random game tile and place one of the three he will possess on the board
Once placed, figures and game tiles cannot be moved or removed.
Player's action is mandatory.

Counting score
--------------
After the whole board is filled with figures and blocks, players count their scores.
For each figure, player sums points from blocks in the same row and column where figure is placed. Sum is multiplied by multiplier of this figure.
Final score is the sum of all players figures points.

Winning
-------
Player with the highest score wins.

Example
-------
```     c1    c2    c3    c4    c5    c6
r1 | -4  |  2  |  5  | 1x1 | -3  | 2x1 |
r2 |  1  | 1x2 |  3  | -1  |  5  |  1  |
r3 | -1  |  5  | -2  | -3  |  0  |  0  |
r4 |  2  |  0  | 2x1 |  3  | -1  |  2  |
r5 | -3  |  1  | 2x2 |  4  |  2  | -4  |
r6 |  4  | -1  |  2  | 1x1 |  4  |  1  |
```

1x1 - players 1 figure, multiplier x1
1x2 - players 1 figure, multiplier x2

**Player1**
r1 x c4: ( ((-4) + 2 + 5 + (-3) ) + ((-1) + (-3) + 3 + 4 ) ) x 1 = 3
r2 x c2: ( (1 + 3 + (-1) + 5 + 1 ) + (2 + 5 + 0 + 1 + (-1)) ) x 2 = 32
r6 x c4: ( (4 + (-1) + 2 + 4 + 1) + ((-1) + (-3) + 3 + 4) ) x 1 = 13
score: 48

**Player2**
r1 x c6: ( ((-4) + 2 + 5 + (-3)) + (1 + 0 + 2 + (-4) + 1) ) x 1 = 0
r4 x c3: ( (2 + 0 + 3 + (-1) + 2) + (5 + 3 + (-2) + 2) ) x 1 = 14
r5 x c3: ( ((-3) + 1 + 4 + 2 + (-4)) + (5 + 3 + (-2) + 2) ) x 2 = 16
score: 30
