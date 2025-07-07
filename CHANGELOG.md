# Changelog

## YYYY-MM-DD - Further Enhancements & Documentation (Jules)

**Note:** Full compilation testing was not possible in the execution environment. Some changes, particularly the modification of `example/Thesis.tex` to use `\usepackage{vector}` (instead of `../template/vector`), could not be applied due to tool errors and require manual intervention and testing. Files in `reference-documents/` also require manual renaming to remove `:Zone.Identifier` suffixes.

### Added
*   **`.gitignore` Refinements:** Added common editor backup patterns (`*.bak`, `*~`), specific error files (`Thesis.bcf-SAVE-ERROR`), and the `example/out/` directory.
*   **`template/Thesis.cls` Enhancements:**
    *   Added extensive comments explaining package choices (`fontspec`, `geometry`, `biblatex`, `hyperref`, etc.) and customization points.
    *   Commented out `\usepackage{epstopdf}` with an explanatory note regarding `lualatex` usage.
    *   Clarified metadata commands with detailed comments.
    *   Modified `\includegraphics` for the logo to use `unimelb_logo.eps` directly, relying on `\graphicspath`.
*   **`example/` Content Expansion:**
    *   `Chapters/Chapter1.tex`: Significantly expanded to showcase various citation styles (`\cite`, `\parencite`, `\textcite`, `\autocite`), single and subfigures (`subcaption`), `booktabs` tables, `amsmath` math environments (`equation`, `align`, `gather`), and `listings` for code blocks.
    *   `Bibliography.bib`: Added diverse entry types (`@book`, `@inproceedings`, `@thesis`, `@online`).
    *   `Preamble/Abstract.tex`: Improved placeholder text.
    *   `Preamble/Declaration.tex`: Clarified "NAME OF AWARD" placeholder.
*   **`README.md` Major Update:**
    *   Added section on Overleaf usage (compiler settings, main file).
    *   Expanded "Customization" section (fonts with `fontspec`, `biblatex` styles, `hyperref` colors).
    *   Added "Troubleshooting" section.
    *   Added "LaTeX Best Practices" section.
    *   Added placeholder "Contributing" guidelines.
    *   Added "License" section with MIT example and advice.
    *   Updated "Features" and "Usage" sections to reflect current state.
*   **Repository Management Files:**
    *   Created `.github/ISSUE_TEMPLATE/bug_report.md`.
    *   Created `.github/ISSUE_TEMPLATE/feature_request.md`.
    *   Created `.github/workflows/compile-test.yml` for basic GitHub Actions CI.

### Changed
*   **`.latexmkrc`:** Uncommented and configured `ensure_path('TEXINPUTS', 'template//');` to allow direct `\usepackage` for items in the `template` directory.
*   **Style File Consolidation:**
    *   Verified `lstpatch.sty` and `vector.sty` were duplicated in `example/` and `template/`.
    *   Deleted `example/lstpatch.sty` and `example/vector.sty`.
    *   (Attempted to change `example/Thesis.tex` to use `\usepackage{vector}` but was blocked by tool error - **manual fix needed**).

### Known Issues / Pending Manual Actions
*   `example/Thesis.tex` requires `\usepackage{../template/vector}` to be changed to `\usepackage{vector}`.
*   Files in `reference-documents/` (e.g., `Preparation-of-GR-theses-rules-June-2020.pdf:Zone.Identifier`) need the `:Zone.Identifier` suffix removed.
*   The entire template requires a full compilation test with `latexmk` in a suitable LaTeX environment to verify all changes and ensure no errors were introduced.

## 2025-07-06 - Modernization and Restructuring

**Attribution:** Dylan A Mordaunt

### Updated

*   **Dependency Modernization:**
    *   Migrated from `natbib` to `biblatex` for improved bibliography management.
    *   Replaced `vmargin` with `geometry` for precise control over page margins (set to 3cm as per university guidelines).
    *   Implemented `fontspec` for full Unicode support and modern font handling.
*   **Code Quality & Readability:**
    *   Integrated `latexindent` for consistent code formatting.
    *   Configured `chktex` for LaTeX linting (initial configuration, further refinement may be needed).
*   **Repository Structure:**
    *   Restructured the repository into `template/`, `example/`, and `reference-documents/` directories for better organization and separation of concerns.
    *   Added a `.gitignore` file to exclude generated LaTeX auxiliary files and the compiled PDF.
*   **Build Process:**
    *   Created a `.latexmkrc` file to automate the compilation process using `lualatex` and `biber`.
    *   Updated `README.md` with clear instructions for compilation, linting, and formatting, reflecting the new repository structure.

### Reverted

*   **University Logo:** Re-added the University of Melbourne logo to the cover page of the example thesis, based on user feedback and common university thesis practices, overriding the strict interpretation of the guideline.
