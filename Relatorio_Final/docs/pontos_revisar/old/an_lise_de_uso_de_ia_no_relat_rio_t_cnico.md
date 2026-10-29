# Relatório de Análise: Detecção de Uso de IA no Documento

**Documento Analisado:** `relatorio_final.pdf`  
**Título do Projeto:** Tintas MGMT: Sistema de Organização e Análise de Dados Empresarial  
**Instituição:** Universidade Virtual do Estado de São Paulo (UNIVESP)  
**Conclusão Geral:** **Sinalização Positiva/Alta para uso de Inteligência Artificial.** O texto foi fortemente gerado ou auxiliado por modelo de linguagem (LLM) e apresenta falhas de revisão humana (sobras de *prompts* e *placeholders* não preenchidos).

---

## 1. Indícios de Alta Gravidade (Erros Estruturais e Vazamento de Prompts/Templates)

Estes são os indícios mais claros de uso de IA sem a devida revisão humana, pois contêm comandos de sistema, instruções do modelo e textos de substituição.

* **Presença de *Placeholders* de IA nas Seções Finais (Página 23 e 24):**
  * **Capítulo 3 (Resultados: Solução Final):** O capítulo está totalmente preenchido com textos genéricos de marcação gerados por IA em vez de conteúdo real do projeto.
    * *Exemplo:* `3.0.1 Solução adotada: Placeholder para descrição detalhada da solução final adotada, incluindo arquitetura...`
    * *Exemplo:* `3.0.2 Resultados obtidos: Placeholder para apresentação dos resultados obtidos...`
    * *Exemplo:* `3.0.3 Feedback da comunidade: Placeholder para registros de feedbacks coletados...`
  * **Capítulo 4 (Considerações Finais):** Mantém a mesma estrutura de rascunho de IA:
    * *Exemplo:* `Placeholder para considerações finais detalhadas, conectando os resultados do projeto aos objetivos iniciais...`

* **Instruções e Diretrizes do Manual Vazadas no Texto (Página 23):**
  * O modelo de IA absorveu o roteiro/rubrica fornecido no *prompt* e o cuspiu diretamente no corpo do relatório técnico como se fosse parte da redação.
  * *Trecho citado:* `"É importante que o grupo inclua imagens, storyboards ou ilustrações que demonstrem visualmente a solução adotada..."` e `"Deve-se retomar os objetivos e o contexto em que o Projeto Integrador foi desenvolvido..."`

* **Erros de Interpretação e Inconsistências de Código/Anexo:**
  * **Uso indevido de sintaxe LaTeX (Páginas 9 e 23):** O modelo gerou caracteres do ecossistema LaTeX que não foram compilados corretamente no documento final (ex.: `$\tilde{E}$` na pág. 9 e `$\hat{F}$` na pág. 23).
  * **Troca de Títulos em Legendas de Figuras (Páginas 17 a 20):** A IA gerou os rótulos de figuras com incompatibilidade lógica em relação ao texto do capítulo. (Exemplo: A "Figura 3" está legendada como *Wireframe Tela de Produção*, mas o conteúdo na imagem exibe a tela de *Manutenção*; a "Figura 4" está legendada como *Wireframe Manutenção*, mas exibe a tela de *Produção*).

---

## 2. Indícios de Média Gravidade (Estilo da Redação e Estrutura Textual)

Trata-se de marcas estilísticas e comportamentais típicas de grandes modelos de linguagem (LLMs) durante o processo de geração de texto acadêmico.

* **Repetitividade Extrema e Redundância de Conteúdo:**
  * O dado de contexto (*"150 baldes por semana, tanque de 2.000 litros, 3 motores, bomba e envase manual"*) é recontado quase idêntico em pelo menos 4 capítulos diferentes (Introdução, Justificativa, Fundamentação Teórica e Metodologia). 
  * Modelos de IA tendem a repetir os dados fornecidos no contexto inicial a cada nova seção gerada para garantir o preenchimento de palavras.

* **Mudança Repentina no Idioma (Inglês Comercial):**
  * No meio do texto em português acadêmico na seção de Contribuições (Página 10), o texto salta para expressões em inglês sem motivo aparente: `"Support for growth: Uma base de dados organizada facilita o crescimento..."`. Esse comportamento ocorre quando a IA mescla respostas de treinamentos em múltiplos idiomas.

* **Alucinação / Generalização de Conceito:**
  * O texto tenta encaixar justificativas socioeconômicas e acadêmicas exageradas para um sistema de cadastro de fábrica de tintas de pequeno porte, utilizando frases vazias recorrentes em geradores de texto (*ex.: "preservação do conhecimento operacional acumulado nas fábricas de tintas da região..."*).

---

## 3. Indícios de Leve Gravidade (Marcas Linguísticas e Fluidez)

Características sutis de vocabulário e padrão transicional comuns na escrita assistida por IA.

* **Estrutura de Frases e Transições Genéricas:**
  * O texto faz uso recorrente de conectivos sintéticos e repetitivos no início dos parágrafos, tais como: *"Nesse contexto..."*, *"Diante dessas necessidades..."*, *"Dessa forma, o Tintas MGMT..."*, *"De modo geral, os resultados..."*.

* **Ritmo e Tom de Voz Impessoal Excessivamente Padronizado:**
  * O documento mantém um tom perfeitamente homogêneo e linear, sem variação de estilo entre parágrafos, o que é atípico em relatórios acadêmicos escritos a doze mãos (por seis autores diferentes).

---

## Resumo das Ações Recomendadas para Correção

1. **Remover todos os parágrafos com a palavra `Placeholder`** e redigir os Capítulos 3 e 4 com os dados reais do projeto.
2. **Apagar as instruções do roteiro da UNIVESP** que ficaram perdidas no texto da página 23.
3. **Corrigir as falhas de formatação:** Trocar os caracteres `$\tilde{E}$` e `$\hat{F}$` pelas letras normais `É`.
4. **Ajustar as legendas das Figuras 1, 2, 3 e 4** para baterem exatamente com o conteúdo de cada imagem.
5. **Revisar e enxugar o texto:** Eliminar as repetições sobre a capacidade da fábrica (150 baldes/tanque 2000L) nos capítulos 2.2, 2.4 e 2.5.