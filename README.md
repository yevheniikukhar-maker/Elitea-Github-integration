# quiz-cli

## Project Overview

`quiz-cli` is an interactive command-line quiz game for learning JavaScript and related programming concepts.

It runs in the terminal, loads questions from a local JSON file, and supports category-based quiz rounds with score tracking, results review, and replay.

## Features

- Interactive terminal-based quiz experience
- Loads quiz content from a local JSON question bank
- Category selection before starting a round
- Selection of the number of questions to answer
- Randomized question order
- Score tracking during the quiz
- Final results summary
- Review of incorrect answers
- Ability to replay another round
- Supports these categories:
  - JavaScript Basics
  - Node.js Fundamentals
  - General Programming

## Technology Stack

| Area | Details |
| --- | --- |
| Language | JavaScript |
| Runtime | Node.js `>= 18.0.0` |
| Module System | ES Modules (`"type": "module"`) |
| Package Manager | npm |
| Built-in Modules | `node:fs/promises`, `node:url`, `node:path`, `node:readline` |
| External Runtime Dependencies | None declared |
| Testing | Node.js built-in test runner (`node --test`) |

## Installation

### Prerequisites

- Node.js 18 or later
- npm

### Install steps

The repository content indicates the application lives in `test-app/`.

```bash
cd test-app
npm install
```

## Configuration

No environment variables, `.env` files, or additional configuration files were found in the provided repository information.

### Relevant project file

- `test-app/package.json`
  - Project metadata
  - Entry point
  - npm scripts
  - Node.js engine requirement
  - Module type

## Usage

### Run the application

From the `test-app` directory:

```bash
npm start
```

This runs:

```bash
node index.js
```

### Test the application

```bash
npm test
```

This runs:

```bash
node --test
```

### Application flow

The quiz CLI:

1. Starts in the terminal
2. Loads quiz questions from `data/questions.json`
3. Prompts the user to choose a category
4. Prompts the user to choose the number of questions
5. Randomizes the question order
6. Tracks the score
7. Displays final results
8. Shows a review of incorrect answers
9. Offers to replay another round

## Project Structure

```text
README.md
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

### Important files

| File | Purpose |
| --- | --- |
| `test-app/index.js` | CLI application entry point |
| `test-app/package.json` | Project metadata and npm scripts |
| `test-app/src/quiz.js` | Quiz logic and results handling |
| `test-app/src/input.js` | Terminal input helpers |
| `test-app/src/colors.js` | ANSI terminal color helpers |
| `test-app/data/questions.json` | Quiz categories and question bank |

### Architecture overview

The application appears to be organized into a small CLI architecture:

- **Entry point**: `index.js`
- **Quiz orchestration**: `src/quiz.js`
- **User input handling**: `src/input.js`
- **Terminal formatting**: `src/colors.js`
- **Question data**: `data/questions.json`

## Testing

- The project uses Node.js built-in testing via `node --test`
- No dedicated test files were listed in the repository structure provided
- As a result, `npm test` may not discover any tests until test files are added

## Additional Notes

- No Docker, CI/CD, or Makefile configuration was found in the provided repository content
- No separate license file was listed
- No external runtime dependencies are declared in `package.json`
- The source files include JSDoc-style comments and inline documentation describing:
  - quiz flow
  - input handling
  - progress display
  - scoring and result logic
  - terminal color formatting
  - data loading

## License

No separate license file was found in the provided repository listing.
