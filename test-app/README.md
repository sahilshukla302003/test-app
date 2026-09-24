# Quiz CLI

An interactive command-line quiz game for learning JavaScript, Node.js, and general programming concepts.

## Overview

Quiz CLI is a dependency-free Node.js terminal application. It loads quiz questions from a local JSON data file, lets the player choose a category and question count, randomizes the questions, provides immediate feedback and explanations, and displays a final score with a review of incorrect answers.

## Features

- Interactive terminal-based menus
- Three quiz categories:
  - JavaScript Basics
  - Node.js Fundamentals
  - General Programming
- Choose all available questions, three questions, or five questions
- Randomized question order using the Fisher–Yates algorithm
- Immediate correct/incorrect feedback
- Explanations for quiz answers
- Progress bar during each quiz
- Score percentage and performance message
- Review of incorrect answers after completion
- Option to play multiple quizzes in one session
- ANSI terminal colors with no external runtime dependencies

## Technology Stack

- **Runtime:** Node.js 18 or newer
- **Language:** JavaScript using ES modules
- **Input:** Node.js built-in `readline` module
- **File loading:** Node.js built-in `fs/promises` module
- **Data:** JSON
- **Dependencies:** None

## Prerequisites

- Node.js `>=18.0.0`
- A terminal that supports standard ANSI escape codes for colored output

## Installation

Clone the repository and enter the application directory:

```bash
git clone <repository-url>
cd <repository-directory>/test-app
```

This project has no third-party packages, so `npm install` is not required. You may run it if you want npm to validate the package metadata, but it will not install dependencies.

## Configuration

Quiz content is stored in `data/questions.json`. Each category contains a display name and a `questions` array. Each question includes:

- `question`: prompt text
- `options`: answer choices
- `answer`: zero-based index of the correct choice
- `explanation`: optional answer explanation

To add or edit questions, preserve this structure and ensure that `answer` points to an item in `options`.

## Running the Project

Start the quiz from the `test-app` directory:

```bash
npm start
```

You can also run the entry point directly:

```bash
node index.js
```

The application will prompt you to select a category, choose the number of questions, answer each question by entering its displayed number, and decide whether to play again.

## Usage Example

```text
Choose a category:
  1. JavaScript Basics
  2. Node.js Fundamentals
  3. General Programming

Your choice (enter number): 1
```

The exact question order and score depend on the selected category and randomized quiz order.

## Project Structure

```text
test-app/
├── data/
│   └── questions.json   # Categories, questions, answers, and explanations
├── src/
│   ├── colors.js        # ANSI color and formatting helpers
│   ├── input.js         # Readline interface and prompt helpers
│   └── quiz.js           # Quiz state, scoring, shuffling, and results
├── index.js              # Application entry point and main loop
├── package.json          # Project metadata and npm scripts
└── README.md             # Project documentation
```

## Testing

The package defines a test script using Node.js's built-in test runner:

```bash
npm test
```

No test files were present in the repository at the time this README was generated, so the command may report that no tests were found.

## Build

No build step is configured. The application runs directly from its JavaScript source using Node.js.

## Deployment

No deployment configuration, Dockerfile, or hosting instructions were found. The application is designed to run locally in a terminal.

## Contributing

1. Create a feature branch.
2. Make focused changes.
3. Update `data/questions.json` when adding or correcting quiz content.
4. Run `npm test` and manually run `npm start` to verify interactive behavior.
5. Open a pull request with a clear description of the changes.

## License

This project is licensed under the MIT License, as declared in `package.json`.
