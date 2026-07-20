# Quiz CLI

Quiz CLI is a beginner-friendly Node.js terminal game where you answer multiple-choice questions, get instant feedback, and review your mistakes at the end.

It is a great small project for learning how to build command-line apps with:

- ES Modules (`import` / `export`)
- `async` / `await`
- Node.js built-in APIs
- object-oriented programming with classes
- reusable input helpers
- ANSI-colored terminal output

## Features

- Choose a quiz category
- Select how many questions to answer
- Questions are shuffled before each game
- Colorful terminal output
- Progress indicator while playing
- Instant correct/incorrect feedback
- Final score summary
- Review of incorrect answers with explanations
- Replay the quiz after finishing

## Project Structure

```text
eliteA/
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

### What each file does

- `test-app/index.js`  
  Main entry point for the app. It shows the banner, asks the user to choose a category and number of questions, runs the quiz, shows results, and handles replay.

- `test-app/src/quiz.js`  
  Contains the `Quiz` class. This class handles shuffling, scoring, progress display, question flow, and review of missed answers.

- `test-app/src/input.js`  
  Wraps Node’s `readline` module and provides helpers for prompts, menu selection, confirmations, and “press enter to continue” behavior.

- `test-app/src/colors.js`  
  Provides ANSI color helpers so the terminal output is easier to read.

- `test-app/data/questions.json`  
  Stores the quiz questions grouped by category.

- `test-app/package.json`  
  Defines the app name, scripts, module type, and Node.js version requirement.

## Requirements

- Node.js 18 or newer
- No external npm packages are required

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

This project currently uses only built-in Node.js features, but installing keeps the project ready for future additions.

### 3. Run the quiz

```bash
npm start
```

This runs:

```bash
node index.js
```

## How to Use

1. Start the app
2. Choose a category
3. Choose how many questions you want to answer
4. Enter the option number for each question
5. Read the explanation after each answer
6. View your final score
7. Decide whether to play again

## Quiz Data Format

Questions are stored in `test-app/data/questions.json` and follow this structure:

```json
{
  "question": "What keyword is used to declare a constant in JavaScript?",
  "options": ["var", "let", "const", "define"],
  "answer": 2,
  "explanation": "The `const` keyword declares a constant value that cannot be reassigned."
}
```

### Fields

- `question` — the question text
- `options` — the available answers
- `answer` — the index of the correct option
- `explanation` — shown after the quiz to help you learn from mistakes

## Available Categories

- JavaScript Basics
- Node.js Fundamentals
- General Programming

## Scripts

From `test-app/package.json`:

- `npm start` — runs the quiz application
- `npm test` — runs the Node.js test runner

## Beginner Tips

- Open `questions.json` to add or edit questions
- Read `src/quiz.js` to understand the quiz logic
- Read `src/input.js` to learn how terminal input is handled
- Read `src/colors.js` to see a simple ANSI color utility

## Troubleshooting

### `node` is not recognized
Install Node.js 18+ and make sure it is added to your PATH.

### The quiz will not start
Check `index.js` for syntax errors and make sure `questions.json` is valid JSON.

### Questions are missing
Confirm that the category exists in `data/questions.json` and that the file path is correct.

## License

This project is licensed under the MIT License.
