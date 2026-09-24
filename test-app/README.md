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
