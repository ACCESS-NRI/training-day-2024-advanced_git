# Advanced Git and GitHub best practices for software developers
S
## Exercises

1. The Git DAG:
  - a)  Inspect the DAG. Can you identify the existing branches and tags? How many merge commits are there?
  - b)  Compare the last commit in branch `undo` with the parent of the last commit in branch `update_maintainers`. How do they differ? (Hint: use `git show\^ to display the commit metadata)
2. Merges
  - a) Do a `git diff` of branches `main` and `update_maintainers` and verify that the `package.py` file differs by two lines.
  - b) Now merge `update_maintainers` into `main`. Can you explain why there is a conflict in one of the lines, but not the other?
  - c) Resolve the conflict keeping the version from `main` and finish the merge.
  - d) Look at the DAG again. Can you tell if merging branch `undo` into `main` will be a fast-forward merge?
3. Rebases
  - a) Rebase branch `undo` onto `main`. Verify that after the rebase it is possible to fast-forward merge `undo` into `main`.
  - b) Rebase branch  `change_version` from `update_maintainers` onto `main` (hint: you need to use the `--onto` option). What happens if you don't specify `update_maintainers` when doing the rebase?
4. Fixing mistakes
  - a) The changes from the last commit in branch `mistake` are wrong (version should be `1.0.0`, not `1.1.0`). Try to fix the error using:
    - `git commit  --amend`
    - `git reset`
  - b) Which of the above methods rewrite the history?
  - c) Is `git revert` appropriate for fixing the above mistake?
