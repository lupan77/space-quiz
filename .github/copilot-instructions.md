# Project instructions

## Overview and constraints

Orbit is a standalone space exploration quiz. The entire application lives in
`index.html`, with inline CSS and vanilla JavaScript. Keep it usable directly via
`file://` without a server, dependencies, build step, external fonts, or network
requests. Do not split the application into additional runtime files.

## Structure and behavior

- The `questions` array contains 10 questions, each with `category`, `icon`,
  `question`, four `answers`, a zero-based `correct` index, and an explanatory `fact`.
- State consists of `current`, `score`, and `answered`. The `$` helper looks up DOM
  elements by ID.
- `renderQuestion()` renders answers and resets per-question feedback.
- `selectAnswer()` locks all answers, awards at most one point, highlights the
  correct answer in green, shakes a wrong selection in red, and reveals feedback.
- The Next button advances explicitly; after the final answer it displays results.
  Results include score, accuracy, and an emoji reaction for scores of 8-10, 5-7,
  or 0-4. Restart resets the complete quiz state.
- The progress bar measures answered questions, starting at 0 and ending at 10.

## UI and accessibility

Preserve the centered, responsive column with a maximum width of 480px and the
polished space-themed design. Use system sans-serif fonts and 14-16px body text.
Use existing CSS custom properties for colors and preserve automatic
`prefers-color-scheme` light/dark styling.

Retain native buttons, visible keyboard focus, accessible answer labels,
live feedback and score announcements, and focus management when advancing or
restarting. Correctness must be communicated with text/symbols as well as color.
Honor `prefers-reduced-motion` for all animations and transitions.

Match the existing two-space HTML/CSS indentation and four-space script
indentation. Prefer DOM construction and `textContent` for question and feedback
content; do not introduce a framework.

## Running and checking changes

Open `index.html` directly in a browser, preferably the integrated browser.
There is no package manifest, automated test suite, build, or lint command.

For behavior changes, exercise all 10 questions with perfect, mixed, and all-wrong
answers. Check that answers lock after selection, scoring cannot repeat, feedback
and progress update correctly, all result tiers render, and replay resets state.
For styling changes, check narrow screens, light/dark appearance, keyboard
navigation, and reduced-motion behavior. Keep quiz facts accurate.
