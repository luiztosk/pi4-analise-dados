# pi4-analise-dados

Projeto Integrador IV - UNIVESP — Tintas MGMT: Sistema de Organização e Análise de Dados Empresarial.

## Relatório Final (LaTeX)

O relatório final está sendo desenvolvido em:

`Relatorio_Final/latex/relatorio_final.tex`

Para compilar o PDF localmente:

```bash
pdflatex -interaction=nonstopmode -output-directory Relatorio_Final/latex Relatorio_Final/latex/relatorio_final.tex
```

Rodar duas vezes para resolver sumário e referências cruzadas.

## Extensão LaTeX Workshop (VS Code)

Recomenda-se utilizar a extensão **LaTeX Workshop** no Visual Studio Code para edição e compilação do relatório.

### Instalação

1. Abra o VS Code.
2. Vá em Extensões (`Ctrl+Shift+X`).
3. Busque por "LaTeX Workshop" (James Yu).
4. Clique em Instalar.

### Configuração recomendada

Crie ou edite o arquivo `.vscode/settings.json` na raiz do projeto com:

```json
{
    "latex-workshop.latex.tools": [
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-interaction=nonstopmode",
                "-output-directory",
                "Relatorio_Final/latex",
                "Relatorio_Final/latex/relatorio_final.tex"
            ]
        }
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "pdflatex (duas passagens)",
            "tools": ["pdflatex", "pdflatex"]
        }
    ],
    "latex-workshop.latex.recipe.default": "pdflatex (duas passagens)",
    "latex-workshop.view.pdf.viewer": "tab",
    "latex-workshop.chktex.enabled": false
}
```

### Como compilar

- Abra o arquivo `Relatorio_Final/latex/relatorio_final.tex`.
- Pressione `Ctrl+Alt+B` (ou use o botão de compilar na barra superior) para gerar o PDF.
- O PDF será gerado em `Relatorio_Final/latex/relatorio_final.pdf`.

### Visualização do PDF

Com a extensão instalada, o PDF é exibido automaticamente ao lado do editor após a compilação. Você também pode abri-lo diretamente pelo VS Code.

## Estrutura do projeto

- `Relatorio_Final/latex/relatorio_final.tex` — fonte principal do relatório final
- `Relatorio_Final/latex/relatorio_final.pdf` — PDF compilado
- `Relatorio_Final/latex/figures/` — figuras/wireframes inseridas no relatório

## Observações

- Todo o texto do relatório deve estar em **Português do Brasil**, seguindo as normas da UNIVESP (Manual de Normalização de Trabalhos Acadêmicos, NBR 14724/2011).
- Não edite a pasta `Relatorio_Parcial/` (arquivada).
