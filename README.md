# CINS 5318: Software Engineering - Assignment 1

## Version Control and Collaborative Development using Git and GitHub

**Author:** James Hawkins (`jwhawkins68`)  
**Course:** CINS 5318 Software Engineering (Fall 2026)  
**Institution:** Prairie View A&M University  
**Repository:** <https://github.com/jwhawkins68/SE-Git-hw>

## Project overview

This repository demonstrates the practical use of Git and GitHub for a small
Python project. The assignment covers repository setup, feature isolation,
pull-request integration, merge-conflict resolution, issue traceability, and
project documentation.

## File index

| File | Type | Description |
| --- | --- | --- |
| `README.md` | Markdown | Project overview, workflow documentation, and contributor record. |
| `hello.py` | Python script | Prints the reconciled greeting produced by the Branch A and Branch B workflow. |
| `apple.py` | Python script | Feature script that prints `I eat apple`. |

## Branching strategy

| Branch | Purpose |
| --- | --- |
| `main` | Stable integrated branch. |
| `feature-1` | Isolated branch used to add `apple.py` before pull-request integration. |
| `conflict-branch-a` | First branch used to create a competing greeting change. |
| `conflict-branch-b` | Parallel branch used to create and resolve the competing greeting change. |

## Conflict simulation and resolution

The two conflict branches changed the same line in `hello.py` to different
greetings. Git therefore required a manual resolution. The final reconciled
implementation is:

```python
print("Hello, World from Branch A and Branch B reconciled!")
```

The resulting history can be inspected with:

```bash
git log --graph --oneline --all
```

## Running the scripts

Use Python 3 from the repository root:

```bash
python3 hello.py
python3 apple.py
```

## Contributors

| Contributor | Responsibility |
| --- | --- |
| `jwhawkins68` / James Hawkins | Repository owner and assignment implementation. |
| `hemzz2020` | Collaborator for the version-control assignment. |
| GitHub Copilot | Pair-programming and documentation assistance. |

## Common Git workflow

```bash
git status
git add <file>
git commit -m "Describe the change"
git push origin <branch>
```

Issue and commit references are retained in the repository history to provide
traceability for the assignment work.
