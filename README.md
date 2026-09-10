# SE-Git-hw

Homework 1 for Software Engineering: version control using Git and GitHub.

## Project overview

This repository demonstrates a small Python project and a collaborative Git
workflow. It includes the original greeting program, an additional feature
script, parallel branch updates, conflict resolution, and merge history.

## Files

| File | Description |
| --- | --- |
| `hello.py` | Prints the reconciled greeting from the Branch A and Branch B workflow. |
| `apple.py` | Feature script that prints an apple-related message. |

## Git workflow demonstrated

| Step | Result |
| --- | --- |
| Initial project setup | Created the Python greeting program and repository. |
| Feature development | Added `apple.py` on `feature-1`. |
| Parallel work | Updated `hello.py` independently on `conflict-branch-a` and `conflict-branch-b`. |
| Conflict resolution | Reconciled the competing greetings into a single final message. |
| Documentation | Added this project overview and file reference. |

## Contributors

| Contributor | Responsibility |
| --- | --- |
| `jwhawkins68` | Repository owner and project implementation. |
| `hemzz2020` | Collaborator for the version-control assignment. |
| GitHub Copilot | Pair-programming and documentation assistance. |

## Running the scripts

Run either script with Python 3:

```bash
python3 hello.py
python3 apple.py
```

## Repository workflow

The main branch contains integrated work. Feature and conflict branches are
used to demonstrate isolated changes before they are merged and pushed:

```bash
git status
git log --graph --oneline --all
git add <file>
git commit -m "Describe the change"
git push origin <branch>
```
