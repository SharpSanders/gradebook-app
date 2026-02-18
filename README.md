Gradebook App

A lightweight, responsive gradebook application built with HTML, CSS, and vanilla JavaScript.

The app accepts a list of class scores and an individual student’s score, then calculates:

The class average

The student’s letter grade

The student’s pass/fail status

Live Site:
https://sharpsanders.github.io/gradebook-app/

<img src="./img/Screenshot-gradebook-app.png" alt="Gradebook App Screenshot">
Overview

This project was built to reinforce JavaScript fundamentals including:

Control flow and conditionals

Array parsing and transformation

Loop-based calculations

Function composition

DOM interaction and state updates

It focuses on clean logic separation and user-friendly input handling.

Core Features

Parses comma-separated class scores into numeric values

Filters invalid inputs safely

Calculates the class average

Converts numeric scores into letter grades:

A++ for 100

A for 90–99

B for 80–89

C for 70–79

D for 60–69

F below 60

Determines pass/fail status

Displays a formatted result message

Basic validation for missing or invalid inputs

Example Usage

Input

Class scores:
92, 88, 12, 77, 57, 100, 67, 38, 97, 89

Your score:
37

Output

Class average: 71.7  
Your grade: F  
You failed the course.

Technical Highlights

Modular helper functions:

getAverage(scores)

getGrade(score)

hasPassingGrade(score)

studentMsg(scores, score)

Defensive input handling

Controlled numeric conversion

Clear separation between logic and DOM manipulation

Stateless calculations with predictable outputs

Tech Stack

HTML5 (semantic structure)

CSS3 (gradient layout + card UI)

JavaScript (ES6)

No frameworks or external libraries.

Project Structure
gradebook-app/
├── index.html
├── styles.css
└── script.js

Run Locally

Clone the repository:

git clone https://github.com/SharpSanders/gradebook-app.git
cd gradebook-app


Open index.html in your browser.

No build tools or dependencies required.

What This Project Demonstrates

Array parsing and transformation from user input

Conditional grading logic

Function-driven architecture

Clean DOM updates based on computed results

Foundational algorithmic thinking

Future Improvements

Weighted grade categories

Additional statistics (min, max, median)

Enhanced validation messaging

Visual pass/fail indicators

Persistent storage for multiple classes

Author

Trevyn Sanders
Better Endeavors LLC