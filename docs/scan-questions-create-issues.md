# Scan for Questions, Create Issues, and Remove Questions

This workflow automatically scans your codebase for specially formatted questions, creates GitHub issues for each question, and then removes the questions from the code.

## Workflow File

`.github/workflows/scan_questions.yml`

## Trigger

This workflow is triggered on:
- Push to the `main` branch
- Manual dispatch

## Functionality

1. Scans all files in the `src` directory for lines containing specially formatted questions.
2. Creates a GitHub issue for each question found, including a link to the relevant code.
3. Removes the question comments from the code.
4. Commits and pushes the changes back to the repository.

## Question Format

Questions should be formatted as follows:

`//Q[before]:[after] Issue title` or `#Q[before]:[after] Issue title` or `--Q[before]:[after] Issue title`

Where:
- `[before]` is the number of lines before the question to include in the issue link
- `[after]` is the number of lines after the question to include in the issue link