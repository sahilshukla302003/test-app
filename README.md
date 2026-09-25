# quiz-cli

A dependency-free, interactive command-line quiz application built with Node.js and ES modules.

`quiz-cli` lets users choose a quiz category and question count, answer shuffled questions interactively, receive immediate feedback with explanations, and review incorrect answers at the end.

## Overview

The quiz includes 15 questions across three categories:

- JavaScript Basics
- Node.js Fundamentals
- General Programming

The application runs entirely in the terminal and uses ANSI escape codes for colored output. It does not require third-party packages or a build step.

## Features

- Interactive category selection
- Configurable number of questions
- Three quiz categories
- Shuffled question order
- Immediate answer feedback
- Explanations for answers
- Progress bar during the quiz
- Score calculation
- Incorrect-answer review
- Option to replay the quiz
- ANSI-colored terminal output
- No external dependencies

## Technology Stack

- Node.js
- JavaScript ES modules
- Node.js built-in `readline` functionality
- JSON question data
- ANSI terminal color codes

## Requirements

- Node.js version 18 or later

Verify your Node.js version with:

```bash
node --version
```

## Setup

No installation step is required because the project has no external dependencies.

Clone the repository and move into the project directory:

```bash
git clone https://github.com/sahilshukla302003/test-app.git
cd test-app
```

The application can be run immediately with Node.js.

## How to Run

Start the quiz using the npm script:

```bash
npm start
```

This runs:

```bash
node index.js
```

You can also start the application directly:

```bash
node index.js
```

Follow the interactive prompts to:

1. Select a quiz category.
2. Select the number of questions.
3. Answer each question.
4. Review your score and incorrect answers.
5. Choose whether to play again.

## Testing

The project defines the following test script:

```bash
npm test
```

This runs Node.js's built-in test runner:

```bash
node --test
```

There are currently no test files in the repository, so no automated tests are presently executed.

## Project Structure

```text
.
├── data/
│   └── questions.json
├── src/
│   ├── colors.js
│   ├── input.js
│   └── quiz.js
├── index.js
├── package.json
└── README.md
```

### Key Files

| File | Description |
|---|---|
| `index.js` | Application entry point |
| `src/colors.js` | ANSI color and terminal formatting utilities |
| `src/input.js` | Interactive command-line input handling |
| `src/quiz.js` | Quiz flow, scoring, feedback, and review logic |
| `data/questions.json` | Quiz question data |
| `package.json` | Project metadata and npm scripts |

## Question Data Format

Quiz content is stored in:

```text
data/questions.json
```

The application uses this file as its question source and supports category-based questions with answer choices, correct answers, and explanations.

When adding or updating questions, preserve the existing JSON structure and field names used in `data/questions.json`. The JSON must remain valid for the application to load successfully.

The available categories are:

- `JavaScript Basics`
- `Node.js Fundamentals`
- `General Programming`

Because the application reads the data file at runtime, changes to the question set can be made without adding dependencies or running a build command.

## Configuration

There is no separate configuration file or environment-variable setup.

The application is configured through:

- `data/questions.json` for quiz content
- Interactive prompts for category and question count selection

## Dependencies

The project has no external runtime or development dependencies.

It uses:

- Node.js built-in functionality
- JavaScript ES modules
- ANSI escape sequences for terminal colors

No `npm install` command is required.

## Build and Deployment

There is no build process or deployment configuration. Run the application directly with Node.js.

## Limitations and Notes

- The application is terminal-based and does not provide a graphical or web interface.
- Node.js 18 or later is required.
- Quiz content must remain valid JSON.
- The test command is configured, but no test files currently exist.
- The application uses ANSI color output, which may not render as intended in terminals that do not support ANSI escape sequences.
- There is no build, packaging, or deployment configuration included.

## Contributing

Contributions are welcome. When making changes:

1. Preserve the existing ES-module structure.
2. Keep the project dependency-free unless a dependency is clearly necessary.
3. Validate any changes to `data/questions.json` as valid JSON.
4. Run the application manually with:

   ```bash
   npm start
   ```

5. Run the configured test command:

   ```bash
   npm test
   ```

6. Update this README when user-facing behavior or project structure changes.

## License

This project is intended to be released under the MIT License.

The repository analysis did not identify a `LICENSE` file. To formally distribute the project under MIT, add a `LICENSE` file containing the standard MIT License text and the applicable copyright year and holder.
