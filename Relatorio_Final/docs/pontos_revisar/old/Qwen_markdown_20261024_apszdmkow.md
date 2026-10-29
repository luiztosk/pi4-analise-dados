# Análise de Indícios de Geração por IA
## Documento: Relatório Final – Tintas MGMT (Projeto Integrador UNIVESP)
### Data da análise: Julho/2026

---

## Resumo Executivo

O texto apresenta **indícios fortes e múltiplos** de ter sido gerado (ou amplamente estruturado) por Inteligência Artificial, com posterior colagem no documento sem revisão humana adequada. Os problemas abaixo estão ordenados do **mais grave** (que pode resultar em reprovação imediata) ao **mais leve** (que gera suspeita, mas pode ser atribuído a descuido).

---

## 🔴 GRAVIDADE CRÍTICA

### 1. Placeholders literais deixados no texto (Seções 3 e 4)

O texto contém instruções de "espaço reservado" que jamais deveriam aparecer em um relatório final:

> **3.0.1 Solução adotada**
> "Placeholder para descrição detalhada da solução final adotada, incluindo arquitetura, tecnologias utilizadas e funcionalidades implementadas."

> **3.0.2 Resultados obtidos**
> "Placeholder para apresentação dos resultados obtidos em cada etapa da metodologia(ouvir, criar, implementar), com indicação de melhorias realizadas com base em feedbacks."

> **3.0.3 Feedback da comunidade**
> "Placeholder para registros de feedbacks coletados junto à comunidade onde o projeto foi desenvolvido..."

> **4 CONSIDERAÇÕES FINAIS**
> "Placeholder para considerações finais detalhadas, conectando os resultados do projeto aos objetivos iniciais e discutindo o impacto da solução na comunidade externa."

**Por que é grave:** Qualquer tutor identifica imediatamente que o texto não foi redigido pelo aluno. A palavra "Placeholder" é um termo técnico de programação/design que um aluno não usaria espontaneamente em um relatório acadêmico.

---

### 2. Instruções do template/manual da UNIVESP copiadas literalmente

A Seção 3 contém parágrafos que são **instruções do manual do Projeto Integrador**, não texto do aluno:

> "É importante que o grupo inclua imagens, storyboards ou ilustrações que demonstrem visualmente a solução adotada, junto aos passos desenvolvidos."

> "Dessa forma, sugere-se que, neste capítulo, seja feita a descrição detalhada do protótipo e de sua aplicação..."

> "Importante: quando se tratar de projetos desenvolvidos com a participação de crianças e adolescentes, não é permitida a inclusão de fotos deles sem a autorização de seus pais ou responsáveis."

A Seção 4 também contém:

> "Deve-se retomar os objetivos e o contexto em que o Projeto Integrador foi desenvolvido e apresentar:
> • Retomada dos resultados à luz das referências estudadas;
> • Contribuições e limitações do trabalho realizado;
> • Impacto da solução na comunidade externa."

**Por que é grave:** Demonstra que o aluno copiou o template e colou texto por cima sem apagar as instruções. Isso é interpretado como plágio de estrutura ou uso indiscriminado de IA sem leitura posterior.

---

## 🟠 GRAVIDADE ALTA

### 3. Termos em inglês "vazando" no meio do texto em português

Dois trechos específicos entregam geração por IA:

| Trecho | Localização | Problema |
|--------|-------------|----------|
| **"- Support for growth:"** | Seção 2.3 (aparece **duas vezes**) | Tópico em inglês no meio de texto em português. A IA gerou o outline em inglês e não traduziu este item. |
| **"...representam overkill para fábricas de pequeno porte"** | Seção 2.2 | Gíria técnica em inglês em texto acadêmico formal. Nenhum aluno brasileiro usaria "overkill" naturalmente. |

**Por que é grave:** São "artefatos de tradução" que só ocorrem quando um modelo de linguagem gera texto a partir de raciocínio interno em inglês.

---

### 4. Repetição literal de parágrafos entre seções diferentes

A IA reciclou o mesmo conteúdo em múltiplas seções sem adaptação:

| Conteúdo repetido | Onde aparece |
|---|---|
| Lista de equipamentos ("tanque de 2.000 litros, três motores trituradores, bomba...") | Introdução (p.5) **E** Metodologia/Empatizar (p.12-13) |
| Parágrafo de delimitação ("A delimitação do problema concentra-se no desenvolvimento inicial...") | Seção 2.2 (p.9) **E** Metodologia/Definir (p.13) |
| Pergunta-problema ("Como desenvolver uma solução digital simples...") | Seção 2.2 (p.9) **E** Seção 2.5 (p.14) |
| Descrição dos wireframes e dados demonstrativos | Seção 2.5/Prototipar (p.14) **E** Seção 2.6 (p.15) |

**Por que é grave:** Um aluno humano que escreve seção por seção naturalmente reformula ou resume. A repetição **palavra por palavra** é característica de IA que recebe prompts separados e recicla o mesmo contexto.

---

## 🟡 GRAVIDADE MODERADA

### 5. Jargão técnico injetado em contexto de justificativa acadêmica

Trechos que parecem anotações técnicas de prompt misturadas com redação acadêmica:

> "...deploy gratuito(Vercel+ Supabase free tier)..."

> "...possui RBAC nativo para separação de responsabilidades(produção, vendas, estoque, manutenção) e é extensível: o schema do Supabase permite adicionar sensores e ML sem refatorar o frontend."

> "...utilizando TanStack Router para roteamento baseado em arquivos e TanStack Start para renderização no servidor(SSR)."

**Por que é moderado:** O conteúdo técnico em si não é problema, mas a forma como está inserido (listando stack tecnológico dentro da "Justificativa Social e Econômica") soa como se a IA tivesse recebido um prompt com requisitos técnicos e os despejado no texto sem contextualização natural.

---

### 6. Estrutura formulaica e transições mecânicas

O texto usa padrões repetitivos de transição típicos de IA:

> "A mesma necessidade existe em relação às vendas."

> "A manutenção também precisa ser considerada."

> "Essas informações mostram que existe uma operação produtiva que pode ser acompanhada por meio de dados."

As justificativas são divididas de forma excessivamente simétrica:
- Justificativa social e econômica
- Justificativa cultural
- Justificativa acadêmica

Cada uma começa com "A justificativa [tipo] está relacionada à..." — estrutura de template.

**Por que é moderado:** Não é prova isolada, mas reforça o padrão geral de geração automatizada.

---

## 🟢 GRAVIDADE LEVE

### 7. Erros de espaçamento (artefatos de copy-paste)

| Erro | Trecho |
|------|--------|
| Falta espaço antes de aspas | `entre"ter dados" e"usar dados"` |
| Falta espaço antes de parêntese | `gratuito(Vercel+ Supabase free tier)` |
| Falta espaço antes de parêntese | `paradas(preventiva e corretiva)` |
| Falta espaço antes de parêntese | `renderização no servidor(SSR)` |
| Falta espaço em "módulospara" | `Inclui módulospara login, cadastro...` |

**Por que é leve:** Pode acontecer em qualquer copy-paste, mas a frequência e o padrão (sempre antes de parênteses/aspas) sugerem cópia direta de interface de chat de IA.

---

### 8. Referências genéricas e pouco específicas

As referências incluem itens como:
- IBM CRISP-DM (não citado no texto)
- React Learn (documentação genérica)
- Supabase Docs (documentação genérica)

Não há citação de artigos científicos específicos sobre MES/ERP para PMEs, nem sobre Indústria 4.0 em pequenas empresas — temas que o texto menciona na fundamentação. Isso sugere que a IA "inventou" a fundamentação sem base em leitura real.

---

## 📋 Tabela Resumo

| # | Achado | Gravidade | Risco |
|---|--------|-----------|-------|
| 1 | Placeholders ("Placeholder para...") | 🔴 Crítica | Reprovação |
| 2 | Instruções do manual UNIVESP no texto | 🔴 Crítica | Reprovação |
| 3 | "Support for growth" / "overkill" | 🟠 Alta | Detecção de IA |
| 4 | Parágrafos repetidos literalmente | 🟠 Alta | Detecção de IA |
| 5 | Jargão técnico fora de contexto | 🟡 Moderada | Suspeita |
| 6 | Transições mecânicas / estrutura formulaica | 🟡 Moderada | Suspeita |
| 7 | Erros de espaçamento | 🟢 Leve | Descuido |
| 8 | Referências genéricas | 🟢 Leve | Suspeita |

---

## ⚠️ Recomendação

**Não submeter o documento neste estado.** Antes de entregar:

1. **Reescrever completamente as Seções 3 e 4** com conteúdo real do projeto.
2. **Apagar todas as instruções de template** (parágrafos que dizem "É importante que o grupo inclua...", "Deve-se retomar...", "Importante: quando se tratar de projetos...").
3. **Traduzir** "Support for growth" → "Suporte ao crescimento" e substituir "overkill" → "exagero" ou "desproporcional".
4. **Eliminar repetições**: se a informação já foi dada na Introdução, na Metodologia apenas referencie brevemente.
5. **Revisar espaçamentos** e formatação geral.
6. **Reescrever com linguagem própria**, adicionando detalhes que só quem participou do projeto saberia (dificuldades reais, conversas com a empresa, decisões do grupo).
7. **Adicionar referências reais e específicas** aos temas citados na fundamentação teórica.

---

*Análise gerada para fins de revisão acadêmica. O objetivo é auxiliar o grupo a corrigir o documento antes da submissão.*