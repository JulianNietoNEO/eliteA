# Quiz CLI

Quiz CLI is an interactive Node.js terminal game that lets you test your knowledge with multiple-choice questions. You can choose a category, decide how many questions to answer, and get instant feedback with explanations at the end.

## Features

- Category-based quiz selection
- Randomized question order
- Choose how many questions to answer
- Colored terminal output
- Score tracking
- Progress updates while playing
- Review of incorrect answers
- Replay support
- Beginner-friendly command-line experience

## Project Structure

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

## Main Files

- `index.js` — Entry point for the CLI application. It loads the quiz data, displays the welcome screen, handles category selection, starts the quiz, and shows the final results.
- `src/quiz.js` — Contains the `Quiz` class, which manages the quiz flow, scoring, shuffling questions, tracking answers, and showing the final review.
- `src/input.js` — Wraps Node’s built-in `readline` module and provides helper functions for safe terminal input.
- `src/colors.js` — Adds ANSI color styling to make the terminal output easier to read and more engaging.
- `data/questions.json` — Stores all quiz questions grouped by category.
- `package.json` — Defines the project metadata, module type, and scripts.

## Requirements

- Node.js 18.0.0 or newer
- npm (comes with Node.js)

## Getting Started

1. Clone the repository

   ```bash
   git clone <repository-url>
   cd eliteA/test-app
   ```

2. Install dependencies

   ```bash
   npm install
   ```

   This project does not use external packages, but running `npm install` prepares the project and creates the lock file if needed.

3. Run the quiz

   ```bash
   npm start
   ```

This runs:

```bash
node index.js
```

## How to Use

When you start the app, you will:

- See a welcome banner
- Choose a quiz category
- Choose how many questions you want to answer
- Answer questions one by one in the terminal
- See whether each answer was correct
- Review your final score
- Read explanations for incorrect answers
- Choose whether to play again

## Quiz Data Format

Questions are stored in `data/questions.json` and organized by category.

Example question structure:

```json
{
  "question": "What keyword is used to declare a constant in JavaScript?",
  "options": ["var", "let", "const", "define"],
  "answer": 2,
  "explanation": "The 'const' keyword declares a block-scoped constant that cannot be reassigned."
}
```

## Field Descriptions

- `question` — the question text shown to the user
- `options` — possible answer choices
- `answer` — the index of the correct option
- `explanation` — extra learning information shown after answering

## Available Scripts

From `package.json`:

- `npm start` — runs the quiz app
- `npm test` — runs the Node.js test runner

## Development Notes

This project is a good example of:

- ES Modules
- async/await
- terminal input handling
- reusable helper functions
- object-oriented programming with classes
- working with JSON data in Node.js

## Troubleshooting

### The app does not start

Make sure you are using Node.js 18 or newer:

```bash
node -v
```

### The terminal looks broken after exiting

If input gets stuck, press `Ctrl + C` to stop the app and restart it.

### Questions are not loading

Check that `data/questions.json` exists and has valid JSON syntax.

## License

MIT
