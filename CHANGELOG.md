# Changelog

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
