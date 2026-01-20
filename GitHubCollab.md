# Collaborative GitHub Workflow

## Overview
1. Pull before starting any work, push upon completing any 'unit' of code (e.g., a loop), and at the end of each session.
2. Do not work off the `main` branch, instead create a branch for a small and specific goal. When ready, merge any changes from `main` into your branch before merging it back to `main`. Resolve any conflicts, then delete your branch. We favor `merge` over `rebase` for the reasons detailed [here](https://www.atlassian.com/git/tutorials/merging-vs-rebasing).
3. Use issues to discuss aspects of the project and keep track of future tasks. Close the issues only when any relevant decision or information has been documented in the `README`.