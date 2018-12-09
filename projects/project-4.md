---
layout: project
type: project
image: images/project-landing.jpg
title: Oahu Waste Organizer
permalink: projects/owo
# All dates must be YYYY-MM-DD format!
date: 2018-12-7
labels:
  - Javascript
  - HTML
  - CSS
  - MongoDB
  - React
  - Meteor
  - Semantic UI
summary: An app that turns inputted trash audit data into graphs.
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/input.png">
</div>

## About

The inspiration for this app originated from the 2018 HACC competition. The theme was sustainability, and our job was to create an app that made data input for trash audits easier. Currently, data was done with simple paper and pen; the recorded data was then copied into an excel spreadsheet and further formatted by hand for individual graphs. We created an app that had an easy-to-use input page that took the data and created graphs in real time of the data that was inputted. Additionally, we created an Events page to show past and upcoming trash audits.
The Oahu Waste Organizer was then taken and adapted to fit the criteria of our 314 Final Project. It was updated to use Semantic UI, React, and MongoDB, and was further improved upon by myself, Alton Lee, and Jake Weber.
To see the official Github page of our 314 project, it is available here.

## Role and Responsibilities

For the HACC competition, I was part of the data visualization team, and acted as team captain to establish group meetings and make sure that everyone was on the same page. I additionally helped create the About Page, Landing Page, and promotional video. For the ICS 314 project, which was basically a continuation of our work on the Oahu Waste Organizer, I worked in a team of 3 with Alton Lee and Jake Weber to further improve the app. I helped design/implement the appearance and functionality of the Landing Page and Input Page.

## What I learned

From this experience, I learned a lot about learning from mistakes and how important it is to really go back and trace through the code to find any errors. Tracing code was really helpful and essential to completing this project, and it's just a good habit overall, even when you think your code don't have any errors. This project was a good example of how many mistakes programmers will encounter in the coding process, and really taught the class that you have to think of all the possible outcomes in order to produce successful code that can handle all those outcomes.

### Sample Code
I will refrain from uploading my code to GitHub as a courtesy to my professors and to discourage cheating by those who have yet to complete ICS 211.
Here is a piece of the code from my project that initially checks if the sudoku is solved, and if not, searches for possible values for the next empty space:

```
public static boolean solveSudoku(int[][] sudoku, int row, int column) {
    // If sudoku is full and solved
    if (column == 16 || row == 16) {
      return true;
    }

    // If there's already a value in the cell, move on
    else if (sudoku[row][column] != -1) {
      if (column == 15) {
        return solveSudoku(sudoku, row + 1, 0);
      } else {
        return solveSudoku(sudoku, row, column + 1);
      }
    } else {
      ArrayList<Integer> possibleValues = legalValues(sudoku, row, column);
      if (possibleValues == null) {
        return false;
      } else {
        for (int i = 0; i < possibleValues.size(); i++) {
          sudoku[row][column] = possibleValues.get(i);
          boolean retVal = solveSudoku(sudoku, row, column);
          if (retVal == true) {
            return true;
          } else {
            sudoku[row][column] = -1;
          }
        }
        return false;
      }
    }

  }
```



