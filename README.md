# quiz-cli

An interactive command-line quiz game for learning JavaScript and general programming concepts.

## Project Overview

**quiz-cli** is a terminal-based quiz application that loads questions from a JSON file, lets the user choose a category and number of questions, runs an interactive quiz session, and then shows the final score along with a review of incorrect answers.

The application is implemented in JavaScript and runs on Node.js using ES Modules.

## Features

- Interactive terminal quiz flow
- Category selection
- Question count selection
- Randomized question order
- Score tracking
- Final result summary
- Review of incorrect answers
- ANSI-colored terminal output
- Option to play again

## Technology Stack

| Area | Details |
| --- | --- |
| Language | JavaScript |
| Runtime | Node.js `>=18.0.0` |
| Module System | ES Modules (`"type": "module"`) |
| Package Manager | npm |
| Frameworks | None detected |
| Runtime Libraries | No external runtime libraries declared |
| Built-in Node.js Modules | `node:fs/promises`, `node:path`, `node:url`, `node:readline` |
| Testing | Node.js built-in test runner via `node --test` |

## Installation

### Prerequisites

- Node.js `18` or later
- npm

### Setup

The application is located in the `test-app/` directory.

1. Clone the repository.
2. Change into the application directory:
   ```bash
   cd test-app
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

> Note: No external runtime dependencies were found in `package.json`, but running `npm install` is still a standard setup step for Node.js projects.

## Configuration

No additional configuration files were found in this branch.

### Known configuration files

- `test-app/package.json`

### Environment variables

- No `.env` file or environment variable configuration was found.

### Data source

The quiz questions are stored in:

- `test-app/data/questions.json`

## Usage

### Run the application

From inside the `test-app/` directory:

```bash
npm start
```

This runs:

```bash
node index.js
```

### Run tests

```bash
npm test
```

This runs Node.js’s built-in test runner:

```bash
node --test
```

### Application flow

When you start the app, it:

1. Loads quiz data from `data/questions.json`
2. Prompts you to choose a category
3. Prompts you to choose how many questions to answer
4. Runs the quiz interactively in the terminal
5. Shows your score and a summary of incorrect answers
6. Offers to play again

## Project Structure

```text
README.md
test-app/
├── data/
│   └── questions.json
├── src/
│   ├── colors.js
│   ├── input.js
│   └── quiz.js
├── index.js
└── package.json
```

### Key files

| File | Purpose |
| --- | --- |
| `test-app/index.js` | Main application entry point and CLI orchestration |
| `test-app/src/quiz.js` | Quiz state, scoring, and result display logic |
| `test-app/src/input.js` | `readline`-based input handling |
| `test-app/src/colors.js` | ANSI color/styling helpers for terminal output |
| `test-app/data/questions.json` | Quiz question data |
| `test-app/package.json` | Project metadata and scripts |

### Architecture overview

The application is organized into small modules:

- **`index.js`** coordinates the overall CLI flow
- **`quiz.js`** manages quiz behavior and score calculation
- **`input.js`** handles user interaction through `readline`
- **`colors.js`** provides terminal styling helpers
- **`questions.json`** stores the quiz content

## Testing

The repository uses the built-in Node.js test runner.

```bash
npm test
```

### Notes on tests

- No dedicated test files were included in the provided repository structure.
- The test command is configured in `package.json` as `node --test`.

## Additional Notes

- The package metadata identifies the project as:
  - **Name:** `quiz-cli`
  - **Version:** `1.0.0`
  - **Description:** “An interactive command-line quiz game for learning JavaScript”
  - **License:** `MIT`
  - **Keywords:** `cli`, `quiz`, `game`, `educational`
- No Docker configuration, CI/CD workflows, or `.env.example` file were found.
- No build system files such as `Makefile`, `pom.xml`, or `build.gradle` were found.
- Inline comments and doc comments are present in the source files and describe the application purpose, quiz logic, input handling, ANSI color helpers, and file loading behavior.
