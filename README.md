# Git and GitHub notes

Notes I made while going through a Git training. It is one PDF, 32 pages:

**[Git_and_GitHub_Notes.pdf](Git_and_GitHub_Notes.pdf)**

I rewrote the training material in the order that is easiest for me to learn and use: setup, basic commands, branches, rebase, pull requests.

## What is inside

| Pages | Part | Covers |
|---|---|---|
| 3-4 | Daily development workflow | The process we follow for every task: update main, branch, commit, rebase, push, pull request, clean up |
| 5-8 | Setup | What Git is, install, config, connecting to GitHub (token or SSH), init and clone |
| 9-15 | Commands | status, add, commit, .gitignore, log and diff, undoing mistakes, push, fetch, pull |
| 16-18 | Branches | Branches, merging, conflicts, stash, tags |
| 19-22 | Rebase | How rebase works, interactive rebase, rebasing before a pull request |
| 23-27 | Pull requests and GitHub | Forks, pull requests, reviews, GitHub CLI, Actions |
| 28-32 | Reference | Advanced commands, commit conventions, 20 common errors with fixes, cheat sheet |

## The short version

```bash
git switch main
git pull
git switch -c feature/login

# write code

git status
git diff
git add .
git commit -m "Add login functionality"

git fetch origin
git rebase origin/main

git push -u origin feature/login
# then open a pull request on GitHub
```

## Mistakes I made first

These were in my first version of the rebase notes, so I am leaving them here:

- `git add.` does not work. It needs a space: `git add .`
- Commit before you rebase, not after. Git will not rebase with uncommitted changes.
- `git rebase --continue` is only for when the rebase stops on a conflict. If the rebase already finished, Git says "No rebase in progress?" and nothing is broken.

## Corrections

If you find something wrong or outdated, open an issue or send a pull request.
