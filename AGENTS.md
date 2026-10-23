# Agent Instructions

## DOCX Editing with python-docx

- Use `python-docx` library to edit `.docx` files
- After each block of edits, convert to PDF using:
  ```bash
  soffice --headless --convert-to pdf 'documento.docx'
  ```
- Compare the generated PDF with the delivered version to verify no formatting degradation
- Maintain a file with all previous versions for comparison
- Use `soffice` (LibreOffice CLI), not `libreoffice` command directly