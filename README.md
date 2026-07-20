# EliteA Quiz CLI

EliteA is a beginner-friendly **terminal-based quiz game** built with **Node.js**.  
It lets you choose a quiz category, answer multiple-choice questions from the command line, and see your final score at the end.

The app is designed as a small, easy-to-understand project with a clean structure, making it a great example of how to build interactive CLI tools in JavaScript.

---

## Features

- **Interactive CLI experience** using Node.js
- **Category selection** before starting a quiz
- **Multiple quiz questions** loaded from JSON data
- **Scoring system** to track correct answers
- **Progress tracking** during the quiz
- **Replay support** so you can play again after finishing
- **Styled terminal output** using ANSI colors for a better user experience

---

## Project Structure

```txt
test-app/
├── index.js            # CLI entry point and game loop
├── package.json        # Node.js metadata and scripts
├── data/
│   └── questions.json  # Quiz categories and questions
└── src/
    ├── colors.js       # ANSI color helpers
    ├── input.js        # Readline-based input helpers
    └── quiz.js         # Quiz logic, scoring, and results
```

### Main files

- **`index.js`**  
  Starts the app, shows the banner, handles category selection, runs the quiz, and supports replay.

- **`src/quiz.js`**  
  Contains the `Quiz` class that manages the quiz flow, scoring, and answer tracking.

- **`src/input.js`**  
  Handles terminal prompts, menus, confirmations, and pauses using Node’s built-in `readline` module.

- **`src/colors.js`**  
  Provides small helper functions for colored and styled terminal text.

- **`data/questions.json`**  
  Stores the quiz content grouped by category.

---

## Getting Started

Follow these steps to run the quiz locally.

### 1) Install Node.js

Make sure you have **Node.js** installed on your computer.

- Recommended: Node.js 18 or newer
- You can check your version with:

```bash
node -v
npm -v
```

---

### 2) Open the project folder

Go into the `test-app` directory:

```bash
cd test-app
```

---

### 3) Install dependencies

Install the project dependencies with npm:

```bash
npm install
```

> If the project does not require external packages, this step will still prepare the local environment and create `node_modules` if needed.

---

### 4) Start the quiz

Run the app with:

```bash
npm start
```

This will launch the quiz in your terminal.

---

### 5) Play the game

Once the app starts:

1. Pick a quiz category
2. Answer each question from the terminal
3. See your score at the end
4. Choose whether you want to play again

---

## Available Scripts

From inside `test-app`, you can use:

```bash
npm start
npm test
```

- **`npm start`** — launches the quiz
- **`npm test`** — runs the project’s test script, if configured

---

## Quiz Data

Questions are stored in:

```txt
test-app/data/questions.json
```

The data is organized by category, such as:

- JavaScript Basics
- Node.js Fundamentals
- General Programming

Each category contains a list of questions and answers used by the quiz engine.

---

## How the App Works

At a high level, the application follows this flow:

1. Load quiz questions from the JSON file
2. Display a welcome banner
3. Ask the user to choose a category
4. Run through the selected quiz questions
5. Track correct answers and progress
6. Show the final result
7. Ask if the user wants to replay

---

## Troubleshooting

### `npm start` does not work
Make sure you are inside the `test-app` folder before running the command:

```bash
cd test-app
npm start
```

### Node.js command not found
Install Node.js from the official website and reopen your terminal afterward.

### Quiz does not load questions
Check that `data/questions.json` exists and that the JSON format is valid.

---

## License

No license information was provided in the repository summary.

---

## Contributing

If you want to extend this project, a few easy ideas are:

- add more question categories
- increase question difficulty
- add timers for each question
- save high scores
- improve the terminal UI

---

Enjoy the quiz and have fun learning with the CLI!
