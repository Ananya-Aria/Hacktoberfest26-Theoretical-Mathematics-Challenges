# Contributing guide

This guide takes you from zero to a merged pull request. If you've never used git before, follow it step by step.

Throughout this guide, replace `<your-username>` with your GitHub username.

This assumes that you have both git and github authenticated and set up, if you have not then please check the e-mail sent around the time of git workshop on your MU e-mail.

---

## 1. Fork the repository

Click **Fork** at the top right of this repository's page. This makes your own copy under your GitHub account.

## 2. Clone your fork to your computer

```bash
git clone https://github.com/<your-username>/enigma-tmc-hacktoberfest-2026.git
cd enigma-tmc-hacktoberfest-2026
```

Cloning automatically connects your computer to your fork under the name `origin`, so you don't need `git remote add origin`.

## 3. Connect to the Enigma repository (only once)

```bash
git remote add upstream https://github.com/MU-Enigma/enigma-tmc-hacktoberfest-2026.git
git remote -v
```

You should see two names: `origin` (your fork) and `upstream` (the Enigma repository). You'll use `upstream` to stay up to date.

## 4. Create a branch for the task you're doing

```bash
git switch -c 1a
```

`-c` creates the branch and switches to it. Use a new branch for every task, for example `1b` or `2a`.

## 5. Create your folder and add your work

Every task has its own folder. For task 1A, that's `Level_1/A_bridges`:

```bash
mkdir Level_1/A_bridges/<your-username>
```

On Windows without a terminal, you can create the folder by hand. The result must be `Level_1/A_bridges/<your-username>/`.

Put your work in that folder, in any format: a `solution.md`, a scanned PDF of handwritten pages, or photos. Keep each file under 2 MB. The end of the task's README lists what we expect to see. (Git only notices a folder once it has a file in it.)

**Only add or change files inside your own folder.** Everyone works in their own folder, so pull requests never clash with each other (no merge conflicts), everyone can name their file `solution.md`, and nobody can accidentally overwrite someone else's work.

## 6. Commit your work

```bash
git add Level_1/A_bridges/<your-username>
git commit -m "1A: <your-username>"
```

## 7. Push the branch to your fork

```bash
git push -u origin 1a
```

`-u` makes git remember where this branch goes. From now on, a plain `git push` is enough for this branch.

## 8. Open a pull request

Go to your fork on GitHub. You'll see a button to **Compare & pull request**. Click it, check that the pull request goes into the **main** branch of the Enigma repository, and fill in the template that appears.

## 9. Fixing things after review

Reviewers may ask for changes. Make them in the same folder, then:

```bash
git add Level_1/A_bridges/<your-username>
git commit -m "1A: fix after review"
git push
```

Your pull request updates automatically. **Don't open a new pull request.**

---

## Starting the next task

Every task gets its own branch and its own pull request. Keep your fork up to date before starting a new task:

```bash
git switch main
git fetch upstream
git merge upstream/main
git push
git switch -c 1b
```

The first time you push the new branch, use `git push -u origin 1b`. After that, `git push` is enough.

If you don't like fetch and merge, you can do `git pull upstream main` instead: pull = fetch + merge. Plain `git pull` won't work here, because it pulls from your own fork, not from the Enigma repository.

---

## What a good pull request looks like

- The title is `<task>: <your-username>`, for example `1A: math-cat7`.
- It covers **one task** and only adds or changes files inside `Level_N/<task-folder>/<your-username>/`.
- Your work covers what the task asks for (see the end of the task's README), with your guesses written before your working.
- Your explanations are in your own words.
- At the end of your submission, you said who and what helped you (including AI).

---

## Common git problems

**"Updates were rejected" when pushing.** Your branch is behind. Run `git pull`, then `git push` again.

**"error: remote origin already exists".** You don't need `git remote add origin`: cloning already set it up. Check with `git remote -v`.   Yep we screwed it up around here in the workshop, I forgot I had cloned a repository. 

**"'switch' is not a git command".** Your git is older than version 2.23. Update git, or use `git checkout -b 1a` instead of `git switch -c 1a`, and `git checkout main` instead of `git switch main`.

**I named my folder wrong.** Rename it with `git mv Level_1/A_bridges/wrong-name Level_1/A_bridges/<your-username>`, then commit and push.

**I committed to `main` by mistake.** Create a branch from where you are with `git switch -c 1a`, then run `git push -u origin 1a` and open the pull request from that branch.

**My pull request shows files I didn't change.** You probably branched from an old `main`. Follow "Starting the next task" above to update, then ask in the Enigma group if it's still messy.

**I'm stuck.** Open an issue or ask in the Enigma group. Everyone was a beginner once.

{Yes this is AI generated too, good use of tools lmao }
