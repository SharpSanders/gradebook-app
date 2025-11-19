# Gradebook App

A simple gradebook tool that takes a list of class scores and a single student's score, then calculates:

- the **class average**, and  
- the student's **letter grade** and **pass/fail** status.

Built to practice JavaScript control flow, loops, functions, and basic DOM work.

## Demo

The app shows a centered card with:

- A text input for **class scores** (comma-separated list).
- A number input for **your score**.
- A **Calculate Result** button.
- A result area that displays the class average and whether you passed or failed.

Example flow:

1. Enter:  
   - Class scores: `92, 88, 12, 77, 57, 100, 67, 38, 97, 89`  
   - Your score: `37`
2. Click **Calculate Result**.
3. The app calculates the class average and your letter grade, then shows a message like:

> `Class average: 71.7. Your grade: F. You failed the course.`

## Tech Stack

- **HTML** – markup for the form and result area.
- **CSS** – gradient background, card layout, and basic UI styling.
- **JavaScript** – grade calculations and DOM interaction.

## Features

- Parses a comma-separated list of scores into numbers.
- Calculates the **class average**.
- Converts a numeric score into a **letter grade**, with:
  - `A++` reserved for a perfect **100**.
  - `A` for 90–99.
  - `B` for 80–89.
  - `C` for 70–79.
  - `D` for 60–69.
  - `F` for anything below 60.
- Determines whether the student **passed** or **failed**.
- Handles basic validation:
  - Asks for class scores if the list is empty.
  - Asks for your score if it’s missing or invalid.

## How to Run the Project

1. **Clone the repository:**

   ```bash
   git clone https://github.com/SharpSanders/gradebook-app.git
   cd gradebook-app
Open the app:

Option A: Double-click index.html to open it in a browser.

Option B (recommended while developing): Use the Live Server extension in VS Code and open index.html via Live Server.

You should see a centered Gradebook card over a blue gradient background.

How to Use
In “Class scores (comma separated)”, enter the class results as a comma-separated list:

text
Copy code
92, 88, 12, 77, 57, 100, 67, 38, 97, 89
In “Your score”, enter your own score (for example, 37).

Click Calculate Result.

Read the message in the result area:

It shows the class average.

It reports your letter grade.

It tells you whether you passed or failed the course.

How It Works (JavaScript Overview)
All the core logic lives in the JavaScript file (gradebook.js / script.js depending on your filename):

getAverage(scores)

Loops through scores, sums them, and returns the average.

getGrade(score)

Returns "A++" for a score of 100.

Returns "A" for 90–99.

Returns "B" for 80–89.

Returns "C" for 70–79.

Returns "D" for 60–69.

Returns "F" for anything below 60.

hasPassingGrade(score)

Uses getGrade(score) and returns true if the grade is not "F".

studentMsg(totalScores, studentScore)

Computes the class average via getAverage(totalScores).

Gets the student's letter grade via getGrade(studentScore).

Returns a full message string:

"Class average: X. Your grade: Y. You passed the course."

or "Class average: X. Your grade: Y. You failed the course."

In index.html, the script:

Reads the class scores input, splits on commas, trims, and converts to numbers.

Filters out anything that isn’t a valid number.

Reads the student score and converts it to a number.

Calls studentMsg(totalScores, studentScore) and puts the returned message into the result <div>.

Project Structure
text
Copy code
gradebook-app/
├── index.html   # Markup for the gradebook form and result area
├── styles.css   # Gradient background, card styling, and basic layout
└── gradebook.js or script.js   # Grade and message logic, plus DOM interaction
What I Practiced
Using loops and arrays to compute averages.

Writing reusable helper functions for grade logic.

Implementing conditional logic for grading and pass/fail messages.

Working with the DOM to read inputs and display results.

Basic data validation and user feedback.

Future Improvements
More detailed validation and error messages for bad input.

Support for weighting assignments or categories (tests, quizzes, etc.).

Visual indicators for pass/fail (colors, icons).

Ability to save and load multiple classes or students.

Display class statistics like min, max, and median scores.

Author
Created by Trevyn Sanders.