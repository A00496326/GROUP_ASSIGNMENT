# GROUP_ASSIGNMENT

# Group Git Collaboration Project

## Project Overview

This repository contains a collaborative group project completed by three students. The purpose of the assignment is to demonstrate our understanding of **Git version control, collaborative development, branching, merging, and merge-conflict resolution**.

Each student is responsible for implementing specific mathematical operations across three text files. The assignment is intentionally structured so that multiple students make changes to the same files, allowing the group to practice handling **merge conflicts** that can occur when different branches modify the same file.

The project consists of three files:

* `File1.txt`
* `File2.txt`
* `File3.txt`

Each student contributes different mathematical operations to each file according to the assignment requirements.

---

## Group Members

| Student     | A Number    | Assigned Student |
| ----------- | ----------- | ---------------- |
| **Johnson** | `A00496326` | Student 1        |
| **Ahanaah** | `A00497567` | Student 2        |
| **Armaan**  | `A00497601` | Student 3        |

---

## Assignment Requirements

Each group member is required to add their assigned mathematical feature to **each of the three files**.

The required contributions are:

| File        | Student 1 — Johnson | Student 2 — Ahanaah | Student 3 — Armaan |
| ----------- | ------------------- | ------------------- | ------------------ |
| `File1.txt` | Addition `+`        | Subtraction `-`     | Multiplication `*` |
| `File2.txt` | Division `/`        | Mod `%`             | Min — `Math.min()` |
| `File3.txt` | Max — `Math.max()`  | Avg — `Math.avg()`  | Pow — `Math.pow()` |

---

# Individual Contributions

## Student 1 — Johnson

**A Number:** `A00496326`

Johnson is responsible for implementing the following features:

### File1.txt

* Addition `+`

### File2.txt

* Division `/`

### File3.txt

* Maximum `Math.max()`

The purpose of these contributions is to demonstrate the addition, division, and maximum mathematical operations within the respective files.

---

## Student 2 — Ahanaah

**A Number:** `A00497567`

Ahanaah is responsible for implementing the following features:

### File1.txt

* Subtraction `-`

### File2.txt

* Modulus `%`

### File3.txt

* Average `Math.avg()`

These contributions demonstrate subtraction, modulus, and average-related mathematical functionality.

> **Note:** `Math.avg()` is included here according to the assignment specification. If the implementation language does not provide a built-in `Math.avg()` function, the average operation may need to be implemented manually.

---

## Student 3 — Armaan

**A Number:** `A00497601`

Armaan is responsible for implementing the following features:

### File1.txt

* Multiplication `*`

### File2.txt

* Minimum `Math.min()`

### File3.txt

* Power `Math.pow()`

These contributions demonstrate multiplication, minimum-value calculation, and exponentiation.

---

# File Structure

The repository follows the structure below:

```text
.
├── File1.txt
├── File2.txt
├── File3.txt
└── README.md
```

### File1.txt

`File1.txt` contains three mathematical operations:

* Addition — Student 1
* Subtraction — Student 2
* Multiplication — Student 3

### File2.txt

`File2.txt` contains:

* Division — Student 1
* Modulus — Student 2
* Minimum — Student 3

### File3.txt

`File3.txt` contains:

* Maximum — Student 1
* Average — Student 2
* Power — Student 3

---

# Git Collaboration Strategy

This assignment is designed to demonstrate how multiple developers can work on the same project using Git.

Each student works on their own branch rather than directly modifying the main branch.

A possible branch structure is:

```text
main
│
├── feature/A00496326
├── feature/A00497567
└── feature/A00497601
```

Each student creates a branch from the main branch and implements their assigned features.

For example:

```bash
git checkout -b feature/A00496326
```

Example for Ahanaah:

```bash
git checkout -b feature/A00497567
```

Example for Armaan:

```bash
git checkout -b feature/A00497601

```

The student then makes the required changes, commits them, and pushes the branch to the remote repository.

---

# Recommended Git Workflow

Each group member follows the general workflow below.

## 1. Clone the Repository

First, clone the repository to the local computer:

```bash
git clone <repository-url>
```

Then navigate into the project directory:

```bash
cd <repository-name>
```

---

## 2. Create a Personal Branch

Each student should work on a separate branch.

Example for Johnson:

```bash
git checkout -b feature/A00496326
```

Example for Ahanaah:

```bash
git checkout -b feature/A00497567
```

Example for Armaan:

```bash
git checkout -b feature/A00497601

```

---

## 3. Make the Assigned Changes

Each student modifies the three files according to the assignment table.

For example, Johnson modifies:

```text
File1.txt → Addition (+)
File2.txt → Division (/)
File3.txt → Math.max()
```

Ahanaah modifies:

```text
File1.txt → Subtraction (-)
File2.txt → Mod (%)
File3.txt → Math.avg()
```

Armaan modifies:

```text
File1.txt → Multiplication (*)
File2.txt → Math.min()
File3.txt → Math.pow()
```

---

## 4. Stage the Changes

After completing the assigned features:

```bash
git add File1.txt File2.txt File3.txt
```

The changes can be checked using:

```bash
git status
```

---

## 5. Commit the Changes

Each student should make a meaningful commit describing their work.

For example:

```bash
git commit -m "Add Johnson mathematical operations"
```

or:

```bash
git commit -m "Add Ahanaah mathematical operations"
```

or:

```bash
git commit -m "Add Armaan mathematical operations"
```

---

## 6. Push the Branch

The branch is then pushed to the remote repository:

```bash
git push -u origin feature/<A00***>
```

For example:

```bash
git push -u origin feature/A00496326
```

---

# Merge Conflict Demonstration

One of the main objectives of this assignment is to demonstrate how the group handles **merge conflicts**.

A merge conflict occurs when Git cannot automatically determine which changes should be kept when two branches have modified the same part of a file.

Since all three students are required to modify the same three files, there is a possibility that their changes will overlap.

For example, `File1.txt` may be modified by all three students:

```text
Addition (+)
Subtraction (-)
Multiplication (*)
```

If two branches modify the same lines of the file differently, Git may produce a conflict during the merge.

A conflict may look similar to:

```text
<<<<<<< HEAD
Addition (+)
=======
Subtraction (-)
>>>>>>> ahanaah
```

The section between:

```text
<<<<<<< HEAD
```

and:

```text
=======
```

represents one version of the changes.

The section between:

```text
=======
```

and:

```text
>>>>>>> ahanaah
```

represents the incoming branch's changes.

---

# Resolving a Merge Conflict

When a conflict occurs, the team member responsible for the merge should inspect the conflicting file and determine how both contributions can be preserved.

For example, instead of keeping only one operation:

```text
Addition (+)
```

or:

```text
Subtraction (-)
```

the resolved file should contain the required contributions:

```text
Addition (+)
Subtraction (-)
```

The conflict markers must then be removed.

After resolving the conflict:

```bash
git add File1.txt
```

The merge can then be completed with:

```bash
git commit
```

The team should verify that all required features from the three students remain in the final files.

---

# Why Merge Conflicts Are Important

The merge-conflict portion of this assignment demonstrates an important aspect of collaborative software development.

In a real development environment, multiple developers frequently work on the same codebase at the same time. Their changes can sometimes affect the same files or even the same lines of code.

Git provides tools for identifying these conflicts, but the developers are responsible for deciding how the conflicting changes should be combined.

Through this assignment, the group demonstrates the ability to:

* Work with Git branches
* Make independent changes
* Commit changes
* Push branches to a remote repository
* Merge branches
* Identify merge conflicts
* Understand Git conflict markers
* Resolve conflicts manually
* Preserve contributions from multiple developers
* Verify the final state of the project

---

# Final Expected Result

After all branches have been merged successfully, the repository should contain all nine required mathematical operations.

### File1.txt

```text
Addition (+)
Subtraction (-)
Multiplication (*)
```

### File2.txt

```text
Division (/)
Modulus (%)
Minimum — Math.min()
```

### File3.txt

```text
Maximum — Math.max()
Average — Math.avg()
Power — Math.pow()
```

The final repository should therefore represent the combined work of all three students.

---

# Team Contribution Summary

| Student | A Number  | File 1             | File 2               | File 3               |
| ------- | --------- | ------------------ | -------------------- | -------------------- |
| Johnson | A00496326 | Addition `+`       | Division `/`         | Maximum `Math.max()` |
| Ahanaah | A00497567 | Subtraction `-`    | Modulus `%`          | Average `Math.avg()` |
| Armaan  | A00497601 | Multiplication `*` | Minimum `Math.min()` | Power `Math.pow()`   |

---

# Learning Objectives

By completing this project, the group demonstrates an understanding of:

1. **Git repository management**
2. **Branch creation and management**
3. **Collaborative development**
4. **Making and tracking commits**
5. **Pushing changes to a remote repository**
6. **Merging branches**
7. **Identifying merge conflicts**
8. **Resolving merge conflicts**
9. **Maintaining contributions from multiple developers**
10. **Working as a team using version control**

---

# Conclusion

This project demonstrates a basic collaborative software-development workflow using Git. Each student is responsible for a defined set of mathematical operations, while all students contribute to the same three files.

The shared-file structure intentionally creates opportunities for merge conflicts. Resolving these conflicts allows the group to demonstrate not only that they can use Git to make changes, but also that they understand how to combine multiple developers' work into one consistent final version.

The completed repository represents the combined contributions of:

* **Johnson — A00496326**
* **Ahanaah — A00497567**
* **Armaan — A00497601**

The final goal is to successfully integrate all assigned features while maintaining a clear Git history and demonstrating effective collaboration and conflict resolution.
