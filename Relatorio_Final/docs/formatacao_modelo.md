# Modelo_Relatorio_Final — Detalhes de Formatação (extraído do PDF modelo)

Este arquivo documenta os requisitos de formatação observados no
`Relatorio_Final/docs/modelos/Modelo_Relatorio_Final.pdf` para evitar perda
de informações entre sessões.

## 1. Capa (Front page)

Elementos na ordem em que aparecem:

1. `UNIVERSIDADE VIRTUAL DO ESTADO DE SÃO PAULO` — fonte Arial ou Times, 14 pt
2. `Nome dos integrantes` — Times New Roman 14 pt (place holder para nomes)
3. `Título do trabalho` (Frase curta que sintetize o foco do trabalho) — Times New Roman 14 pt, negrito
4. Caixa com borda: `Vídeo de apresentação do Projeto Integrador` + `<link>`
5. `Cidade - SP` / `ano`

Não há número de página na capa.

## 2. Folha de rosto (Rosto page)

Elementos na ordem em que aparecem:

1. `UNIVERSIDADE VIRTUAL DO ESTADO DE SÃO PAULO` — fonte Arial ou Times, 14 pt
2. `Título do trabalho` (Frase curta que sintetize o foco do trabalho) — Times New Roman 14 pt, negrito
3. Texto descritivo: `Relatório Técnico-Científico apresentado na disciplina de Projeto Integrador para o curso de (incluir seu curso) da Universidade Virtual do Estado de São Paulo (UNIVESP).` — Times 12 pt
4. `Cidade - SP` / `Ano`

**Importante: não há nomes de autores na folha de rosto.** Os nomes aparecem apenas na capa e na página do resumo.

## 3. Página do Resumo (Resumo page)

Elementos no topo da página (antes do texto do resumo):

- Nomes dos autores
- Título do trabalho
- Tipo do trabalho (Relatório Técnico-Científico)
- Nome do curso
- Nome da tutora/tutor
- Ano

Texto do resumo:

- Título: `RESUMO` (negrito)
- Até 250 palavras incluindo: breve introdução, objetivos, metodologia adotada, resultados obtidos e considerações finais.
- Formatação: **espaçamento simples**, **parágrafo único**.

Após o resumo:

- Título: `PALAVRAS-CHAVE:` — 3 a 5 palavras separadas por ponto e vírgula.

## 4. Formatação geral do texto (do manual de normalização, página 7 do modelo)

- Fonte: Times New Roman, tamanho 12 para texto, 10 para citações de mais de três linhas e notas de rodapé. Cor preta.
- Margens: superior e esquerda 3 cm; inferior e direita 2 cm.
- Títulos ou subtítulos: alinhados à esquerda, iniciando sempre em uma nova página. Todas as letras dos títulos dos capítulos em negrito e maiúsculas.
- Paginação: canto superior direito, começando na introdução em algarismos arábicos (1, 2, 3...). Capa e rosto não têm número.
- Espaçamento: 1,5 para o texto geral. Exceções com espaçamento simples: citações longas (>3 linhas), notas de rodapé, referências bibliográficas, legendas de ilustrações e tabelas.
- Parágrafos separados por uma linha em branco.
- Citações > 3 linhas: fonte tamanho 10, espaçamento simples, recuo de 4 cm da margem esquerda.
- Notas de rodapé: fonte tamanho 10.

## 5. Itens opcionais

- Lista de Ilustrações (opcional)
- Listas de Tabelas (opcional)
- Anexos (opcional) — ordenados por letras (Anexo A, Anexo B...)
- Apêndices (opcional) — ordenados por letras (Apêndice A, Apêndice B...)

## 6. Estrutura de seções (do modelo)

1. INTRODUÇÃO
2. DESENVOLVIMENTO
   2.1 OBJETIVOS
   2.2 JUSTIFICATIVA E DELIMITAÇÃO DO PROBLEMA
   2.3 CONTRIBUIÇÕES PARA O PÚBLICO EXTERNO
   2.4 FUNDAMENTAÇÃO TEÓRICA
   2.5 METODOLOGIA
   2.6 RESULTADOS PRELIMINARES: SOLUÇÃO INICIAL
3. RESULTADOS: SOLUÇÃO FINAL
4. CONSIDERAÇÕES FINAIS
5. REFERÊNCIAS

## 7. Comandos LaTeX já aplicados (desabilitar separação silábica)

O arquivo `relatorio_final.tex` já inclui:

```latex
\hyphenpenalty=10000
\exhyphenpenalty=10000
\sloppy
```

para desabilitar a separação silábica.
