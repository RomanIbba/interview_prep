# Contributing to Interview Prep

Thank you for considering contributing to **Interview Prep**! Your contributions help create a valuable resource for software engineering interview preparation. Follow the steps below to get started.

---

## Table of Contents
- [How to Contribute](#how-to-contribute)
- [Branch Naming Guidelines](#branch-naming-guidelines)
- [Code and Documentation Style](#code-and-documentation-style)
- [Submitting Your Changes](#submitting-your-changes)
- [Keeping Your Fork Updated](#keeping-your-fork-updated)

---

## How to Contribute

Contributions are welcome in various forms:
- Adding new topics or subtopics
- Improving existing explanations
- Adding practice problems or solutions
- Fixing typos, broken links, or formatting issues

Follow these steps to contribute:

### **Step 1: Fork the Repository**
Click the `Fork` button at the top-right corner of this repository to create a copy in your GitHub account.

### **Step 2: Clone Your Fork**
Clone your forked repository to your local machine:

git clone https://github.com/<your-username>/interview_prep.git
cd interview_prep

### **Step 3: Create a New Branch**
Create a new branch for your changes:

git checkout -b feature/<topic-name>

For exapmle:  

git checkout -b feature/add-binary-search

### **Step 4: Make Your Changes**
Add your changes or contributions based on the repository's folder structure.
Ensure your contributions are clear, well-documented, and appropriately placed in the relevant category.

### **Step 5: Commit Your Changes**
Stage your changes:

git add .

Commit your changes with a meaningful message:

git commit -m "Add Binary Search Section"

### **Step 6: Push Your Changes**
Push your branch to your forked repository:

git push origin feature/<topic-name>

### **Step 7: Submit a Pull Request**
Go to your forked repository on GitHub.

Click the Compare & pull request button.

Provide a clear title and description for your pull request:
    Title: Add Binary Search Section in Data Structures
    Description: This PR adds a comprehensive explanation, examples, and practice problems for binary search.

Click Create pull request.

## Branch Naming Guidelines

Use descriptive names for your branches to make it clear what your contribution is about:

- Feature additions: feature/<topic-name> (e.g., feature/add-linked-list)
- Bug fixes: fix/<issue-name> (e.g., fix/typo-in-recursion)
- Documentation updates: docs/<topic> (e.g., docs/add-contributing-guide)

## Code and Documentation Style

- Markdown: Use proper Markdown syntax for .md files.
- Code: Include comments and follow best practices for the language you're contributing in.
- Documentation: Be clear, concise, and include examples wherever possible.

## Submitting Your Changes

Once your pull request is submitted, the maintainers will:
- Review your changes.
- Provide feedback if needed.
- Merge the changes once approved.

If feedback is provided:
- Make the required changes in your branch.
- Commit and push the updates:

git add .
git commit -m "Update based on review feedback"
git push

## Keeping Your Fork Updated

To avoid merge conflicts and ensure your fork is up-to-date:

### **Step 1: Add the Upstream Repository**

git remote add upstream https://github.com/original-author/interview_prep.git

### **Step 2: Fetch and Merge Changes**

git fetch upstream
git checkout main
git merge upstream/main

### **Step 3: Push Updates to Your Fork**

git push origin main

# Thank you for contributing to Interview Prep! Your support helps build a valuable resource for the community.