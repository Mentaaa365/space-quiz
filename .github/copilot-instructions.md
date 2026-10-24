# Copilot instructions

## Project shape

This is a standalone Spanish-language space-exploration quiz. The complete application lives in the root `index.html`: semantic markup defines the intro, quiz, and results views; the inline stylesheet handles layout, responsive behavior, motion, and themes; and the inline script supplies question data and drives the view transitions. There is no framework, module system, server, or dependency layer.

Quiz content is data-driven through the `questions` array. Each entry has a question `text`, four `options`, a zero-based correct `answer` index, and a short explanatory `fact`. The script tracks the current question and score, renders answer buttons, and switches between the intro, quiz, and results views.

## Build, test, and lint

- There are no build, test, or lint commands configured in the project.
- To run the app, open `index.html` directly in a browser; it does not require a server or package installation.
- There is no automated single-test command. For a browser smoke test, exercise start, correct and incorrect answers, score/progress updates, results, and replay from the local HTML file.

## Codebase conventions

- Keep the app self-contained in `index.html`; do not introduce external assets, libraries, or a build step unless the project requirements change.
- Keep user-facing copy in Spanish. Add quiz entries using the existing question shape and zero-based answer index.
- Keep view changes and score/progress updates in the existing quiz functions (`startQuiz`, `renderQuestion`, `selectAnswer`, and `showResults`) so the state flow stays centralized.
- Use the existing CSS custom properties for shared colors, with corresponding values in `prefers-color-scheme: dark`; retain the reduced-motion treatment and visible keyboard focus styles.
- Preserve native button controls and the focus handoff to the active question or results heading when changing views.
