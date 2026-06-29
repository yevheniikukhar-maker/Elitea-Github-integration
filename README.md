# Project Overview

**quiz-cli** is an interactive command-line quiz game for learning JavaScript and related programming concepts.

The application:
- runs in a terminal
- loads quiz content from a local JSON file
- lets the user choose a category and number of questions
- tracks score and shows results at the end
- uses Node.js built-in modules and ES modules

## Features

- Interactive terminal-based quiz experience
- Category selection from bundled quiz content
- Flexible question count selection:
  - all questions
  - 3 questions
  - 5 questions
- Randomized question order within a quiz session
- Score tracking and end-of-quiz summary
- Review of incorrect answers
- Terminal styling using ANSI color codes
- Uses only Node.js built-in modules; no external runtime dependencies are declared
- Designed as an educational example of:
  - ES modules
  - async/await
  - file system access
  - readline-based input handling
  - classes and basic OOP
  - array methods and destructuring

## Technology Stack

| Area | Technology |
| --- | --- |
| Language | JavaScript |
| Runtime | Node.js `>= 18.0.0` |
| Module System | ES Modules (`"type": "module"`) |
| CLI Input | Node.js `readline` |
| File Access | `node:fs/promises` |
| Path Handling | `node:path`, `node:url` |
| Testing | Node.js built-in test runner (`node --test`) |
| Package Manager | npm |

## Prerequisites

- Node.js 18 or newer
- npm (bundled with Node.js)

## Installation

1. Clone the repository.
2. Change into the application directory:

   ```bash
   cd test-app
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

   > Note: No external dependencies are listed in `package.json`. Running `npm install` will still prepare the project in the standard Node.js way.

## Configuration

No environment variables or external configuration files were found in the provided repository contents.

### Important project files

- `test-app/package.json` — project metadata and scripts
- `test-app/data/questions.json` — quiz categories and questions
- `test-app/index.js` — application entry point

## Usage

### Run the application

From the `test-app` directory:

```bash
npm start
```

Or run the entry file directly:

```bash
node index.js
```

### What the app does

When started, the quiz:
1. displays a banner
2. loads questions from `data/questions.json`
3. prompts you to choose a category
4. prompts you to choose how many questions to answer
5. asks each question one by one
6. shows whether each answer is correct
7. displays a final score summary
8. optionally lets you play again

### Example flow

- Choose a category such as:
  - JavaScript Basics
  - Node.js Fundamentals
  - General Programming
- Choose the number of questions
- Enter answers by selecting the numbered option in the terminal

## Scripts

| Script | Command | Description |
| --- | --- | --- |
| `start` | `node index.js` | Starts the interactive quiz application |
| `test` | `node --test` | Runs Node.js built-in tests |

## Project Structure

```text
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

### File responsibilities

- **`index.js`**  
  Main entry point. Loads questions, handles the quiz loop, and coordinates user interaction.

- **`src/quiz.js`**  
  Quiz logic, including:
  - shuffling questions
  - tracking progress
  - scoring
  - displaying results and review output

- **`src/input.js`**  
  Readline-based terminal input helpers:
  - prompt
  - select
  - confirm
  - pressEnter

- **`src/colors.js`**  
  ANSI color helpers for terminal output.

- **`data/questions.json`**  
  Quiz categories and question data.

- **`package.json`**  
  Project metadata, scripts, module type, and Node.js engine requirement.

## Testing

The repository includes a test script:

```bash
npm test
```

This runs:

```bash
node --test
```

### Testing notes

- No dedicated test files were present in the provided repository structure.
- As a result, `node --test` may complete without discovering any tests unless test files are added later.
- If you add tests, place them in a format recognized by Node’s built-in test runner.

## Additional Notes

- The application is intentionally dependency-free at runtime and uses only built-in Node.js APIs.
- The repository appears to be focused on learning and demonstrating core JavaScript/Node.js concepts through a simple CLI game.
- The quiz content is stored locally in JSON, so updating or expanding categories and questions can be done by editing `data/questions.json`.
- The package metadata specifies the MIT license and an engine requirement of Node.js `>= 18.0.0`.
