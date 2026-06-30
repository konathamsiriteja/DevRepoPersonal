## Project description

`quiz-cli` is an interactive command-line quiz game for learning JavaScript. It runs entirely in Node.js, loads quiz content from a local JSON file, and guides the user through choosing a category and the number of questions to answer. The app then runs an interactive quiz loop, shows the results, and offers the option to play again.

The project is built with ES modules and is designed to be simple to run from the terminal.

## Key features

- Interactive CLI experience with prompts and formatted terminal output
- Loads quiz questions from `data/questions.json`
- Lets the user choose a category and number of questions before starting
- Uses a `Quiz` class to manage quiz flow and scoring
- Includes input helpers for terminal interaction
- Uses color helpers for readable, styled output
- Supports replaying the quiz after completion
- Prints errors with colored formatting and exits with a non-zero status code on failure
- Built for Node.js 18+ using native ES modules

## Setup instructions

**Requirements**

- Node.js `18.0.0` or newer
- A terminal capable of running Node.js CLI applications

**Installation**

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd quiz-cli
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

   > The current `package.json` does not declare external dependencies, but running `npm install` is still a standard setup step and will prepare the project for local use.

**Project structure**

- `index.js` — CLI entry point and application bootstrap
- `data/questions.json` — quiz question data loaded by the app
- `src/input.js` — input/prompt helper functions
- `src/quiz.js` — quiz logic and state management
- `src/colors.js` — terminal color/formatting helpers
- `package.json` — project metadata, scripts, and Node.js engine requirement

**Available scripts**

- `npm start` — runs the application with `node index.js`
- `npm test` — runs Node.js built-in tests with `node --test`

## How to run the project

Start the quiz from the repository root with either of the following commands:

```bash
npm start
```

or:

```bash
node index.js
```

When launched, the app will:

1. Display a banner
2. Prompt you to choose a quiz category
3. Ask how many questions you want to answer
4. Run the quiz interactively
5. Show your results
6. Ask whether you want to play again

**Notes**

- The app uses the `"type": "module"` setting in `package.json`, so it relies on native ES module syntax.
- The CLI entry point includes a shebang, which makes it suitable for direct execution in Unix-like environments as well.
- If an error occurs during startup or execution, it is printed with colored formatting and the process exits with code `1`.
- Quiz content is read from `data/questions.json`; updating that file is the primary way to add or change questions.
- The repository currently exposes only the scripts listed in `package.json`.