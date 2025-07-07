# University of Melbourne Thesis Template

This is a modernized version of the University of Melbourne PhD thesis template. It has been updated to use modern LaTeX packages and best practices, making it easier to use, customize, and maintain.

## Features

*   **Modern Bibliography Management:** Uses `biblatex` for flexible and powerful bibliography management.
*   **Precise Page Layout:** Uses the `geometry` package for easy and precise control over page margins.
*   **Unicode Support:** Uses the `fontspec` package for full Unicode support, allowing you to use any font installed on your system.
*   **Code Quality Tools:** Includes configuration files for `chktex` (linter) and `latexindent` (formatter) to help you maintain a clean and consistent codebase.
*   **Automated Build Process:** Includes a `.latexmkrc` file to automate the compilation process, including running `biber` for the bibliography.

## Requirements

To use this template, you will need a full LaTeX distribution, such as [TeX Live](https://www.tug.org/texlive/), [MiKTeX](https://miktex.org/), or [MacTeX](https://www.tug.org/mactex/). You will also need the following tools:

*   `biber`: For processing the bibliography.
*   `chktex`: For linting the LaTeX code.
*   `latexindent`: For formatting the LaTeX code.

## Usage

### Compilation

To compile the thesis, navigate to the `example` directory and run the following command:

```bash
latexmk Thesis.tex
```

This will automatically compile the document, run `biber` to process the bibliography, and generate a PDF file.

### Linting

To lint the LaTeX code, run the following command:

```bash
chktex **/*.tex
```

### Formatting

To format the LaTeX code, run the following command:

```bash
latexindent -w -s -y **/*.tex
```

## Customization

To customize the template, you will need to edit the following files:

*   `Thesis.tex`: This is the main file for your thesis. You can change the title, author, and other details here.
*   `Thesis.cls`: This is the class file for the thesis. You can change the page layout, fonts, and other settings here.
*   `Bibliography.bib`: This is the bibliography file. You can add your references here.
*   `Chapters/`: This directory contains the chapters of your thesis. You can add, remove, or rename the files in this directory.
*   `Preamble/`: This directory contains the preamble files, such as the abstract, declaration, and acknowledgements. You can edit these files to add your own content.
