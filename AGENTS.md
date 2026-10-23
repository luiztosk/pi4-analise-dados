# Agent Instructions

## REGRAS PERMANENTES (obrigatórias, sempre seguir)

1. **Idioma**: Todo texto visível no documento deve estar em **Português do Brasil**.
2. **Normas UNIVESP**: Seguir o Manual de Normalização de Trabalhos Acadêmicos da UNIVESP (`docs/Manual_de_Normalizacao_v2018.pdf`), baseado na NBR 14724/2011 e ABNT.
3. **Formatação de texto**:
   - Fonte: Arial ou Times New Roman, tamanho 12
   - Espaçamento: 1,5
   - Cor: preta
   - Papel: A4 (21cm x 29,7cm)
   - Margens: Esquerda e superior 3cm; Direita e inferior 2cm
   - Título: letras minúsculas, exceto primeira letra, nomes próprios e científicos
   - Citações: sistema autor-data (SOBRENOME, ano)
   - Referências: ordem alfabética pelo sobrenome do autor

## Estrutura obrigatória do trabalho (UNIVESP)

### Elementos pré-textuais (obrigatórios)
- Capa: nome da instituição, curso, nome(s) do(s) autor(es), título, cidade e estado, ano
- Folha de rosto: autor(es), título, nota descritiva (disciplina, curso, instituição), cidade/estado, ano
- Resumo em português: parágrafo único, ~500 palavras
- Palavras-chave: 3 a 5, separadas por ponto e vírgula
- Sumário: com números de página

### Elementos textuais (obrigatórios)
- Introdução
- Desenvolvimento
- Conclusão ou considerações finais

### Elementos pós-textuais (obrigatórios)
- Referências

### Opcionais
- Anexos (ANEXO A – Título), Apêndices, Glossário, Índices

## Paginacao
- A partir da folha de rosto, todas as páginas são contadas
- Numeração só aparece a partir da primeira folha da parte textual (Introdução)
- Numeração: canto superior direito, 2cm da borda superior e 2cm da borda direita

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
3. **Render pages** - `pdftoppm -png -r 100 versoes/relatorio_vX.pdf versoes/relatorio_vX/pages/page` (images stored in `versoes/<version>/pages/`)
4. **Save Version** - Copy new DOCX and PDF to `versoes/relatorio_vX.docx/pdf`
5. **Compare** - Verify no formatting degradation vs delivered version