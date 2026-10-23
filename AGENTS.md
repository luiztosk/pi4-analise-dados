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
   - **Unicode**: todo texto em português deve usar caracteres Unicode nativos (ex: á, ã, ç, ê, ó) em vez de sequências de escape LaTeX (ex: `\'{a}`, `\~{a}`, `\c{c}`)

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

- **NOTE**: We no longer use .docx. The LaTeX file `Relatorio_Parcial/latex/relatorio.tex` is the reference source from now on.

## Instrução Importante para Seções .md
- Ao copiar e compor seções nos arquivos `docs/secoes_relatorio/.md`, **mantenha o código puro em LaTeX** - não use sintaxe markdown (como `**negrito**`, itálico com `*`, etc.)
- O LaTeX tem seu próprio sistema de formatação; markdown syntax no .tex causará erros de compilação (asteriscos dobrados aparecendo no texto)
- Todo texto em negrito no LaTeX deve usar `\textbf{}` ou ser escrito normalmente (o documento já usa fonte ptm com formatação padrão)
- Após copiar da fonte .docx para o .md e depois para o .tex, verifique se não restaram caracteres markdown

## Trabalho Atual
- Edição do arquivo `latex/relatorio.tex` baseada nas seções em `docs/secoes_relatorio/`
- Processo: copiar seção → preparar em docs/secoes_relatorio.md → aplicar no relatorio.tex
- After each block of edits to the .tex, compile to PDF using:
  ```bash
  pdflatex -interaction=nonstopmode -output-directory Relatorio_Parcial/latex Relatorio_Parcial/latex/relatorio.tex
  ```
  (run twice to resolve table of contents / cross-references)
- Render pages for visual check:
  ```bash
  pdftoppm -png -r 100 Relatorio_Parcial/latex/relatorio.pdf Relatorio_Parcial/latex/page
  ```
- Compare the generated PDF vs previous version to verify no formatting degradation
- Use `pdflatex` (TeX Live / TinyTeX), not `soffice`/`libreoffice` for the main report