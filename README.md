# 📄 Professional CV - Bruno Cabado

![Build Status](https://github.com/Kr4is/cv/actions/workflows/build-pdf-pr.yml/badge.svg)
![Pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)
![License](https://img.shields.io/github/license/Kr4is/cv)
![LaTeX](https://img.shields.io/badge/LaTeX-Project-blue.svg?style=flat&logo=latex)

> **A modern, automated, and version-controlled Curriculum Vitae built with LaTeX.**

## 🚀 About The Project

This repository hosts the source code for my professional Curriculum Vitae.
It leverages the power of **LaTeX** for precise typesetting and **GitHub Actions** for continuous integration and automated PDF generation.

The goal is to treat the CV as a software project: versioned, linted, and automatically built to ensure high quality and consistency.

## ✨ Features

- **Automated Builds**: Every Pull Request triggers a workflow to compile the LaTeX source and generate a PDF artifact.
- **Code Quality**: Integrated `pre-commit` hooks ensure consistent formatting and catch common errors before they are committed.
- **Modern Tooling**: Uses `latexmk` for robust compilation and `markdownlint` for documentation standards.
- **Version Control**: Full history of changes and improvements to the CV.

## 🛠️ Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and editing.

### Prerequisites

You need a standard LaTeX distribution and Python installed on your system.

- **LaTeX Distribution** (e.g., TeX Live)
  - Ensure you have `latexmk` and `lualatex` available.
- **Python 3.x** (for pre-commit)
  - Ensure you have `pre-commit` installed.

### Installation

1. **Clone the repository**

    ```bash
    git clone https://github.com/Kr4is/cv.git
    cd cv
    ```

2. **Install pre-commit hooks**
    This ensures your changes meet the quality standards before committing.

    ```bash
    uvx install pre-commit
    pre-commit install
    ```

## 💻 Usage

### Building the CV Locally

To compile the CV and generate the PDF on your machine, run:

```bash
latexmk -pdflua cv.tex
```

This will produce a `cv.pdf` file in the root directory.

### Linting and Formatting

To manually run the quality checks on all files:

```bash
pre-commit run --all-files
```

This checks for:

- Trailing whitespace
- YAML syntax errors
- File endings
- Merge conflicts
- Markdown formatting

## 🛠️ Development Guidelines

This is a personal CV project, so direct contributions are not expected.
However, if you are using this repository as a template or modifying it for your own use, here are some guidelines:

- **Modifying the Content**: The main content is located in `cv.tex`. You can edit this file to update your experience, education, and skills.
- **Adding New Sections**: Use the existing custom commands like `\resumeExperience` and `\resumeItem` to maintain consistency.
- **Quality Checks**: Always run `pre-commit run --all-files` before committing changes to ensure formatting and linting standards are met.
- **Commit Messages**: Please follow [Conventional Commits](https://www.conventionalcommits.org/) style for your commit messages.

---

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.
