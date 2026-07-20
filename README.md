# Quiz CLI

A beginner-friendly Node.js command-line quiz game that runs entirely in the terminal. Players can choose a category, answer multiple-choice questions, get instant feedback, and review missed answers at the end.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
- [How to Use](#how-to-use)
- [Quiz Data Format](#quiz-data-format)
- [Scripts](#scripts)
- [Development Notes](#development-notes)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Overview

Quiz CLI is designed as a small learning project for practicing core JavaScript and Node.js concepts such as:

- ES Modules (`import` / `export`)
- `async` / `await`
- Node.js built-in APIs like `readline` and file handling
- object-oriented programming with classes
- reusable helper functions
- ANSI-colored terminal output

The app reads questions from a JSON file, guides the player through the quiz, and shows a score summary when the game ends.

## Features

- Category-based quizzes
- Randomized question order
- Choose how many questions to answer
- Colorful terminal output
- Progress tracking during the quiz
- Final score summary
- Review of incorrect answers with explanations
- Replay support

## Project Structure

```text
eliteA/
├─ README.md
└─ test-app/
   ├─ index.js
   ├─ package.json
   ├─ data/
   │  └─ questions.json
   └─ src/
      ├─ colors.js
      ├─ input.js
      └─ quiz.js
```

### File guide

- `test-app/index.js`  
  Main entry point for the CLI app. It loads quiz data, shows the banner, handles category selection, starts the quiz loop, displays results, and asks the user if they want to play again.

- `test-app/src/quiz.js`  
  Contains the `Quiz` class, which manages shuffled questions, scoring, progress display, and final results.

- `test-app/src/input.js`  
  Wraps Node.js `readline` and provides helper functions for prompts, selections, confirmations, and pause behavior.

- `test-app/src/colors.js`  
  Provides ANSI color and style helpers for improving terminal readability.

- `test-app/data/questions.json`  
  Stores quiz questions grouped by category.

- `test-app/package.json`  
  Defines the app name, module type, scripts, and supported Node.js version.

> Note: The `__MACOSX` folder and `.DS_Store` files are macOS metadata artifacts and are not part of the application logic.

## Requirements

- Node.js 18 or newer
- No external npm dependencies are required

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd eliteA/test-app
```

### 2. Install dependencies

```bash
npm install
```

This project does not rely on third-party packages, but running `npm install` prepares the project for future updates and keeps the workflow familiar.

### 3. Run the quiz

```bash
npm start
```

This command runs:

```bash
node index.js
```

## How to Use

When the app starts, you will usually follow this flow:

1. Read the welcome banner
2. Pick a quiz category
3. Choose how many questions to answer
4. Answer each question from the multiple-choice list
5. Receive instant feedback after each answer
6. Review your final score
7. See explanations for any missed questions
8. Choose whether to replay

## Quiz Data Format

Questions are stored in `test-app/data/questions.json` and grouped by category.

Example structure:

```json
{
  "question": "What keyword is used to declare a constant in JavaScript?",
  "options": ["var", "let", "const", "define"],
  "answer": 2,
  "explanation": "The `const` keyword declares a constant value that cannot be reassigned."
}
```

### Field meanings

- `question` — text shown to the player
- `options` — array of possible answers
- `answer` — index of the correct option
- `explanation` — helpful note shown when reviewing answers

## Scripts

From `test-app/package.json`:

- `npm start` — launches the quiz application
- `npm test` — runs the built-in Node.js test runner

## Development Notes

- The project uses ES Modules (`"type": "module"`)
- The code is written using only built-in Node.js features
- Questions can be extended by editing `data/questions.json`
- The code structure is intentionally simple and beginner-friendly
- The `Quiz` class keeps game state organized and easier to maintain

## Troubleshooting

### `node` is not recognized
Make sure Node.js 18+ is installed and available in your terminal.

### The quiz does not start
Check for JavaScript syntax errors in `index.js` or invalid JSON in `data/questions.json`.

### Questions are missing or not loading
Verify that the file path is correct and that the JSON content is valid.

## License

This project is licensed under the MIT License.