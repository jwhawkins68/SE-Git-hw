# CINS 5318: Software Engineering — Assignment 1
## Version Control and Collaborative Development using Git & GitHub

**Author:** James Hawkins 
**Course:** CINS 5318 Software Engineering (Fall 2026)  
**Instructor:** Dr. Mary Kim  
**Institution:** Prairie View A&M University  
**Repository:** `https://github.com/jwhawkins68/SE-Git-hw`

---

## 1. Project Overview
This repository satisfies the practical requirements of **Assignment #1: Version Control using GitHub**. The primary objective of this project is to apply modern version control principles, distributed team workflows, and systematic documentation standards as detailed in Sommerville’s *Software Engineering* (10th Edition). 

Key engineering competencies demonstrated:
* Initializing, configuring, and maintaining a remote Git repository with meaningful semantic commit histories.
* Feature isolation using distributed topic branches (`feature-1`).
* Collaborative peer reviews and code integration via GitHub Pull Requests (PRs).
* Controlled merge conflict simulation, diff inspection, and manual three-way resolution.
* Lifecycle traceability and task management through GitHub Issues.

---

## 2. File Index & Manifest

| File | Type | Description |
| :--- | :--- | :--- |
| `README.md` | Markdown Documentation | Comprehensive project overview, execution manifest, branching model, conflict analysis, and issue log. |
| `hello.py` | Python Script | Initial source file printing `"Hello, World!"`, later utilized for simulating and resolving branch merge conflicts. |
| `apple.py` | Python Script | Feature script introduced in branch `feature-1` printing `"I eat apple"`, merged via collaborative Pull Request. |

---

## 3. Branching Strategy & Lifecycle Model

This repository follows a feature-branching workflow designed to isolate experimental development from the protected baseline:

* **`main`**: The stable production branch representing deployable releases. All functional code is merged into `main` only after review or controlled resolution.
* **`feature-1`**: Isolated feature branch created from `main` (`git checkout -b feature-1`) to implement `apple.py` without risking destabilization of the main codebase.
* **`conflict-branch-a`**: Staging branch used to simulate conflicting modifications to stdout statements in `hello.py`.
* **`conflict-branch-b`**: Parallel staging branch modifying the identical lines of `hello.py` to trigger a non-fast-forward merge collision.

---

## 4. Conflict Simulation & Resolution Workflow (Part 5)

A merge conflict occurs when Git cannot automatically reconcile diverging modifications made to the exact same line of code across different commits. A controlled collision was engineered and resolved as follows:

### Step 1: Divergent Commits Creation
Two separate branches were spawned from `main`:
1. On branch `conflict-branch-a`, line 1 of `hello.py` was updated to:
   ```python
   print("Hello, World from Branch A!")
