# quiz-cli

## Project Description

`quiz-cli` is an interactive command-line quiz game for learning JavaScript and general programming concepts.

It is a Node.js CLI application that:
- loads quiz questions from a JSON file,
- lets the user choose a category and number of questions,
- runs the quiz interactively in the terminal,
- shows results at the end, and
- optionally allows the user to restart.

## Features

- Interactive terminal-based quiz experience
- Category selection from a question bank
- Choice of number of questions to answer
- Multiple-choice questions with explanations
- Score tracking during the quiz
- Final results summary
- Review of incorrect answers
- ANSI color output for a nicer terminal experience
- Organized separation between quiz logic, input handling, and colors
- Question data stored separately in JSON
- No third-party dependencies

## Technologies Used

- Node.js
- ES Modules
- Built-in Node modules:
  - `fs/promises`
  - `url`
  - `path`
  - `node:readline`
- JSON for quiz content
- MIT licensed project

## Prerequisites

- Node.js **18.0.0 or later**

The `package.json` file specifies:

- `engines: { node: ">=18.0.0" }`

## Setup and Installation

1. Clone the repository.
2. Change into the project directory:
   ```bash
   cd test-app
   ```
3. There are no external dependencies to install.

Because the project has no third-party packages, `npm install` is not required for dependency installation.

## How to Run

From the `test-app` directory, run:

```bash
npm start
```

This executes the main entry point:

```bash
node index.js
```

You can also run the application directly with:

```bash
node index.js
```

## Usage

When started, the CLI:

1. Clears the terminal
2. Displays a banner
3. Prompts you to select a quiz category
4. Prompts you to choose how many questions to answer
5. Runs the quiz question by question
6. Shows your final score and results
7. Lets you decide whether to restart the quiz

### Quiz content

The visible question bank includes these categories:

- `javascript` — JavaScript Basics
- `nodejs` — Node.js Fundamentals
- `general` — General Programming

Each category contains **5 multiple-choice questions** with:

- a question
- answer options
- the correct answer
- an explanation

## Project Structure

```text
test-app/
├── data/
│   └── questions.json
├── index.js
├── package.json
└── src/
    ├── colors.js
    ├── input.js
    └── quiz.js
```

### File summary

- `index.js`  
  Main CLI entry point. Loads questions, handles the quiz flow, and manages errors.

- `data/questions.json`  
  Contains the quiz question bank and category data.

- `src/quiz.js`  
  Contains the core quiz logic, including shuffling, scoring, progress tracking, and final review.

- `src/input.js`  
  Provides terminal input helpers built with `node:readline`.

- `src/colors.js`  
  Provides ANSI color formatting helpers for terminal output.

- `package.json`  
  Defines the package metadata, scripts, module type, and Node.js engine requirement.

## Available Commands

From the `test-app` directory:

### Start the application
```bash
npm start
```

Runs:
```bash
node index.js
```

### Run tests
```bash
npm test
```

Runs:
```bash
node --test
```

> Note: A test script is defined in `package.json`, but no test files were visible in the supplied repository structure.

## Testing

The project includes a test script:

```bash
npm test
```

This invokes Node’s built-in test runner:

```bash
node --test
```

No test files were included in the provided repository contents, so there may be no tests to execute in the current state of the project.

## How the Quiz Works

The quiz flow is implemented in `index.js` and `src/quiz.js`:

- Questions are loaded from `data/questions.json`
- The user selects a category
- The user selects how many questions to answer
- A `Quiz` instance is created
- Questions are shuffled
- The user answers questions interactively
- Progress and score are tracked
- Final results are displayed
- Incorrect answers are reviewed
- The user can choose to restart

## API / Integrations

There are no external APIs or third-party integrations in the supplied repository.

The application uses only built-in Node.js modules and local project files.

## Build and Deployment

No build, deployment, CI/CD, or Docker configuration files were present in the supplied repository.

The application runs directly with Node.js.

## Troubleshooting

### Node version issues
If the application does not start correctly, verify that you are using Node.js 18 or later.

The project uses:
- ES Modules (`"type": "module"`)
- Node’s built-in test runner
- modern Node.js APIs

### Terminal display issues
The app uses ANSI color output. If colors do not display correctly, your terminal may not support ANSI formatting.

## Additional Information

- Package name: `quiz-cli`
- Version: `1.0.0`
- Description: interactive command-line quiz game for learning JavaScript
- Keywords: `cli`, `quiz`, `game`, `educational`
- License: MIT

The repository content shows that quiz data is kept separate from application logic, which makes it easier to update questions without changing the core quiz code.