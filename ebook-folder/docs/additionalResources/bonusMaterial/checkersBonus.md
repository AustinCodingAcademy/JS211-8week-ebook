# Checkers App

## Overview

Today students will apply their knowledge of Object Oriented Programming to build checkers.

The goal of Checkers is to remove all your opponent's pieces from the board. Your pieces can only move forward one tile diagonally (they always stay on the color of tile they started on.)

To capture an opponent's piece and remove it from the board, you need to "jump" over their piece with one of yours. Jumping is mandatory, which means you have to jump with one of your pieces if you are able to. Try to force your opponent to make a jump and put them in a bad position!

If one of your pieces gets to the opposite side of the board (your opponent's back row), it will turn into a King. Kings can move and jump diagonally in any direction (remember, your regular pieces can only move forward). Kings can even combine jumps forward and backward on the same turn!

You win by removing all of your opponent's pieces from the board, or if your opponent can't make a move.

In your terminal app you will create create a board with an array or arrays then place "markers" for your checkers" then with the input of the user take in coordinates from where the checker starts to where the user wants the checker to go. Then you will add in logic to see if the move is legal. Then you will figure out how to remove a checker if it's jumped.

[How to Play Checkers](https://www.coolmathgames.com/0-checkers)

## How

- [ ] [Clone the Checkers Repo](https://github.com/AustinCodingAcademy/JS211_Checkers)
- [ ] Create a new branch called "checkers"
- [ ] Use [this guide to Whiteboard](https://gist.github.com/kevincolten/e1aaa8eb144874c30fa9077702060a47) ->
- [ ] Code Plan ->
- [ ] Psuedo Code ->
- [ ] Place your code in the /05week/checkers.js file in your workbook.
- [ ] Get to Coding!!

### Build the Board Class

The `Board()` function will print the a graph representation of the board with or without checkers on it.

One approach could be to generate a `grid = []` variable of the appropriate size. Then loop through the list of checkers in the board, and fill in the appropriate symbols in the correct cells. Once the grid is filled out, then we can loop through the grid rows and cols to print out the grid.

A board with no checkers would look like this:

```console
  0 1 2 3 4 5 6 7
0
1
2
3
4
5
6
7
```

Let's create some checkers! In your `Board` constructor, create an attribute called Checkers and assign it to an empty list. This will be your repository of checker pieces.
The `Board` constructor should generate 12 white pieces and 12 black pieces at the following initial positions.

```console
  White positions:
  [0, 1], [0, 3], [0, 5], [0, 7],
  [1, 0], [1, 2], [1, 4], [1, 6],
  [2, 1], [2, 3], [2, 5], [2, 7]

  Black Positions:
  [5, 0], [5, 2], [5, 4], [5, 6],
  [6, 1], [6, 3], [6, 5], [6, 7],
  [7, 0], [7, 2], [7, 4], [7, 6]
```

After instantiating each checker add it to the list of checkers held by the board.

### Get the Game Started

Below is what the display for the game would look like when started

```console
  0 1 2 3 4 5 6 7
  0   ○   ○   ○   ○
  1 ○   ○   ○   ○  
  2   ○   ○   ○   ○
  3                
  4                
  5 ●   ●   ●   ●  
  6   ●   ●   ●   ●
  7 ●   ●   ●   ●  

  'move' or 'remove' checker?
  move
  Enter Pickup Row:
  5
  Enter Pickup Column:
  0
  Enter Placement Row:
  4
  Enter Placement Column:
  1

  0 1 2 3 4 5 6 7
  0   ○   ○   ○   ○
  1 ○   ○   ○   ○  
  2   ○   ○   ○   ○
  3                
  4   ●            
  5     ●   ●   ●  
  6   ●   ●   ●   ●
  7 ●   ●   ●   ●
```

Go play yourself some [Checkers](https://cardgames.io/checkers/).

## Push Yourself Further

- [ ] Handle making checkers into Kings
- [ ] This would be an awesome game to attach to a GUI!