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

## 4-Step Edit Workflow

1. **Edit** - Modify DOCX using `python-docx`
2. **Convert** - `soffice --headless --convert-to pdf 'versoes/relatorio_vX.docx' --outdir versoes`
3. **Save Version** - Copy new DOCX and PDF to `versoes/relatorio_vX.docx/pdf`
4. **Compare** - Verify no formatting degradation vs delivered version