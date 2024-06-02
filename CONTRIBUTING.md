<!-- https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors -->

# Contributing to gitAssistant

Thank you for considering contributing to gitAssistant! Your help is essential for keeping this project active and up-to-date.

## Table of Contents

- [Contributing to gitAssistant](#contributing-to-gitassistant)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Opening an Issue](#opening-an-issue)
  - [Creating a Patch](#creating-a-patch)
  - [Working with Submodules](#working-with-submodules)
    - [Adding a Submodule](#adding-a-submodule)
    - [Updating Submodules](#updating-submodules)
    - [Cloning with Submodules](#cloning-with-submodules)
  - [Creating the CONTRIBUTORS.md File](#creating-the-contributorsmd-file)

## Introduction

gitAssistant is a system composed of multiple repositories integrated as submodules. Each submodule represents a piece of the entire system. The current submodules are:
- Logger
- Communications

## Opening an Issue

Before opening a new issue, please check the existing issues to avoid duplicates. Here's how you can do it:

1. Navigate to the [Issues](https://github.com/[your-username]/gitAssistant/issues) section of the repository.
2. Use the search bar to see if your issue has already been reported.
3. If the issue doesn't exist, click the "New Issue" button.
4. Provide a clear and descriptive title and detailed description of the issue.
5. Include any relevant information, such as steps to reproduce the issue, screenshots, or error messages.
6. Click "Submit new issue" to create the issue.

## Creating a Patch

To create a patch (pull request) for this project, follow these steps:

1. **Fork the Repository**: Click the "Fork" button at the top right corner of the repository page of the submodule you want to contribute to (e.g., Logger, Communications).
2. **Clone the Forked Repository**:
   ```bash
   git clone https://github.com/your-username/[submodule-repo].git
   cd [submodule-repo]
   ```
3. **Create a New Branch**: Create a new branch for your feature or bug fix.
   ```bash
   # for a new feature
   git checkout -b feature/your-feature-name
   ```
   ```bash
   # for a fix
   git checkout -b fix/your-fix-name
   ```

4. **Make Your Changes**: Implement your changes in this branch.
5. **Commit Your Changes**:
   ```bash
   git add .
   git commit -m "Description of your changes"
   ```
6. **Push to Your Fork**:
   ```bash
   git push origin branch-name
   ```

7. **Open a Pull Request**:
   - Go to your forked repository on GitHub.
   - Click the "Compare & pull request" button.
   - Ensure the base repository is `[your-username]/[submodule-repo]` and the base branch is `develop`.
   - Provide a clear title and description for your pull request.
   - Click "Create pull request".

## Working with Submodules

gitAssistant uses git submodules to manage its components. Here’s how to work with submodules:

### Adding a Submodule

To add a new submodule:
```bash
git submodule add https://github.com/[submodule-repo-url] path/to/submodule
git commit -m "Add new submodule"
```

### Updating Submodules

To update submodules to the latest commit:
```bash
git submodule update --remote --merge
```

### Cloning with Submodules

When cloning the repository, you need to initialize and update the submodules:
```bash
git clone --recurse-submodules https://github.com/your-username/gitAssistant.git
cd gitAssistant
```

If you've already cloned the repository without the `--recurse-submodules` flag, you can initialize and update the submodules with:
```bash
git submodule update --init --recursive
```

## Creating the CONTRIBUTORS.md File

To recognize all the wonderful contributors to this project, we maintain a `CONTRIBUTORS.md` file. Here’s how you can add yourself to the list:

1. Add your name and (optionally) a link to your GitHub profile in the `CONTRIBUTORS.md` file in alphabetical order. Here's an example:
   ```markdown
   # Contributors

   - [Your Name](https://github.com/your-username)
   ```
2. Commit your changes:
   ```bash
   git add CONTRIBUTORS.md
   git commit -m "Add [Your Name] to contributors list"
   ```
3. Push the changes to your fork and open a pull request as described above.

---

Thank you for contributing to gitAssistant! We appreciate your support and involvement.
