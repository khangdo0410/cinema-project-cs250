# Rebuilding the Smart Cinema design

This package contains the editable content model, document and diagram generators, vector figures, Markdown design, and the unmodified SRS input. It produces the same Smart Cinema System project, with Design as Chapter 6.

Unzip the package into the project repository root. The source scripts belong in `source/`; the generated figures belong in `diagrams/`. Keep `Smart_Cinema_System_SRS_Original.pdf` at the root.

## Requirements

Use Python 3 with `python-docx`, `reportlab`, and `PyMuPDF`. Use Microsoft Word or LibreOffice to export the generated Word document as PDF. No web service is required to create the diagrams.

## Build sequence

1. Edit `source/design_model.py` for the class, attribute, operation, enumeration, and data-transfer definitions. Edit `source/build_document.py` for the surrounding design chapter. When the class model changes, also update its representative UML attributes, operations, and relationships in `source/build_diagrams.py`.
2. Run `python source/build_diagrams.py`. This creates the five diagrams as SVG, PDF, and high-resolution PNG files.
3. Run `python source/build_document.py`. This creates `Smart_Cinema_System_Software_Design_Specification.docx` and its Markdown version.
4. Open the Word document, update page fields if needed, and export it as `Smart_Cinema_System_Software_Design_Specification.pdf` in the root directory. Inspect every page, especially tables, captions, and UML labels. The submitted version has 32 pages; edits may change that count.
5. Run `python source/assemble_report.py`. This creates `Smart_Cinema_System_Project_Report.pdf`, preserves the original SRS input, and places the SVG figures beside the Markdown file so its links work on GitHub. The submitted version has 42 pages. The assembly script expects the source SRS supplied in this package and its existing nine-page requirements body; it should not be applied to an unrelated PDF.
6. Inspect the cumulative PDF and its contents page. Commit the edited source and the matching exported PDFs together.

The original SRS remains unchanged. The cumulative report replaces unused template front matter and corrects one typographical artifact in the integer-cents sentence in a copy. The original requirements and analysis diagrams remain the baseline. Section 6.2 states the design interpretations explicitly.

The source archive does not represent completed software implementation. Its scripts build the specification and figures. Planned acceptance checks in Section 6.10 still need to be implemented and executed during development.

See `CONTRIBUTING.md` for each member's individual review and commit responsibilities.
