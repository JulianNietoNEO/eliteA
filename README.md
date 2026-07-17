# Quiz CLI

An interactive command-line quiz game built with Node.js. It lets users choose a category, answer multiple-choice questions, get instant feedback, and review incorrect answers at the end.

## Project Overview

Quiz CLI is a beginner-friendly terminal application designed to demonstrate core Node.js and JavaScript concepts, including:

- ES Modules (`import` / `export`)
- async/await
- built-in Node.js file and terminal APIs
- object-oriented programming with classes
- input validation and reusable helpers
- ANSI-colored terminal output

The app loads quiz data from a JSON file, runs a guided quiz flow, and shows a score summary when finished.

## Features

- Category-based quizzes
- Randomized question order
- Select how many questions to answer
- Colored terminal output
- Progress tracking
- Final score summary
- Review of missed questions
- Replay support

## File Structure

```text
test-app/
├─ index.js
├─ package.json
├─ data/
│  └─ questions.json
└─ src/
   ├─ colors.js
   ├─ input.js
   └─ quiz.js
```

### What each file does

- `index.js`  
  Main entry point. It loads quiz data, manages the game flow, and handles replay.

- `src/quiz.js`  
  Contains the `Quiz` class. This file manages question order, scoring, progress, and results.

- `src/input.js`  
  Provides reusable terminal input helpers for prompts, selections, confirmations, and pauses.

- `src/colors.js`  
  Small helper module for ANSI color styling in the terminal.

- `data/questions.json`  
  Stores quiz questions grouped by category.

## Requirements

- Node.js 18 or newer
- No external dependencies are required

## Setup Instructions

### 1. Clone the repository

```bash
git clone <repository-url>
cd eliteA/test-app
```

### 2. Install dependencies

```bash
npm install
```

> This project does not require third-party packages, but running `npm install` keeps the project ready if dependencies are added later.

### 3. Start the quiz

```bash
npm start
```

This runs:

```bash
node index.js
```

## Usage Examples

### Start the quiz

```bash
npm start
```

### Example flow

1. A welcome banner is shown
2. You choose a quiz category
3. You choose how many questions to answer
4. Each question is displayed with multiple-choice options
5. Your answer is checked immediately
6. A final score is shown
7. Incorrect answers are reviewed
8. You can choose to play again

### Example categories

- JavaScript Basics
- Node.js Fundamentals
- General Programming

## How It Works

### Quiz flow

- The application reads quiz data from `data/questions.json`
- The user selects a category
- The app builds a quiz from the chosen category
- Questions are shuffled before starting
- Each answer is validated against the correct option
- The final score is calculated and displayed
- Missed questions are shown with explanations

### Input handling

The `src/input.js` module simplifies terminal interaction by providing helpers such as:

- prompt input
- menu selection
- yes/no confirmation
- press-enter pause

### Scoring

The `Quiz` class tracks:

- current question index
- correct answers
- incorrect answers
- total score

## Quiz Data Format

Questions are stored in JSON and grouped by category.

Example question structure:

```json
{
  "question": "What keyword is used to declare a constant in JavaScript?",
  "options": ["var", "let", "const", "define"],
  "answer": 2,
  "explanation": "The `const` keyword declares a constant value that cannot be reassigned."
}
```

### Expected fields

- `question`: the text shown to the user
- `options`: array of possible answers
- `answer`: index of the correct option
- `explanation`: extra information shown after the quiz for wrong answers

## Scripts

From `package.json`:

- `npm start` — run the quiz application
- `npm test` — run the built-in Node.js test runner

## Development Notes

- The project uses `"type": "module"`
- The app is written with only built-in Node.js functionality
- Questions can be expanded by editing `data/questions.json`
- The code is structured to be easy to extend for beginners

## Possible Improvements

Ideas for future enhancements:

- add more quiz categories
- add difficulty levels
- store high scores
- add timer-based questions
- support text input answers
- load questions from an API
- add more tests

## Troubleshooting

### `node` command not found
Install Node.js 18+ and make sure it is available in your terminal.

### Quiz does not start
Check for syntax errors in `index.js` or invalid JSON in `data/questions.json`.

### Questions are not loading
Verify the JSON file path and make sure the file contains valid JSON.

## License

This project is licensed under the MIT License.
