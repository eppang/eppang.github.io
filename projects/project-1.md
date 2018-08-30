---
layout: project
type: project
image: images/micromouse.jpg
title: Hexadecimal Sudoku
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2015-07-01
labels:
  - Java
summary: Recursively solves a Hexadecimal Sudoku problem.
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>

This was a project for my ICS 211 class. It was one of the more challenging projects that I remember, since a lot of factors needed to be taken into consideration when writing the code for this project. In this assignment, a recursive method is implemented to find a solution to a given Sudoku problem.

A Sudoku is a 9x9 grid of integers, each with values 1..9. A Sudoku is valid when each of the 9 rows, each of the 9 columns, and each of the 9 3x3 boxes in the grid has exactly one each of the possible values 1..9, without any duplicates. A Sudoku problem is a Sudoku grid with some of the grid cells already filled. The solution fills the remaining cells to give a valid Sudoku.

A recursive strategy for finding a solution to a Sudoku problem is as follows:

- If all cells are filled, see if this Sudoku is valid. If it is, this means the solution has been found. If not, this Sudoku is not a solution.

- If at least one cell is not filled, see what values are legal in this cell:

- If no values are legal, then this Sudoku is not a solution.

- If one or more values are legal, place each legal values in the cell in turn, one at a time. For each, recursively attempt to find a solution that fills the remaining empty cells.

- If a solution is found for at least one legal value, set the Sudoku to reflect this solution, and return that a solution was found.

- If no solution is found for any legal value, reset this cell to the value it had when this method was called, and report that this Sudoku does not have a solution.

Every time the code recursively attempts to find a solution, it will fill cells in the Sudoku grid. If the attempt is not successful, returning, the code must restore the Sudoku grid to the values had before the call.

Here is some code that illustrates how we read values from the line sensors:

```js
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```



