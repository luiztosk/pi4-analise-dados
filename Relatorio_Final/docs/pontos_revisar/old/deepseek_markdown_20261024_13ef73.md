# Relatório de Análise Textual — Tintas MGMT

## Parecer geral

Não é possível provar com certeza, apenas pela leitura, se o texto foi escrito por IA. Detectores automáticos também não são confiáveis como prova.

O parecer mais seguro é que o documento apresenta **fortes indícios de texto híbrido**: partes conceituais, justificativas e trechos de template com características de IA generativa, combinadas com inserções e edições humanas em detalhes técnicos, dados específicos do projeto e referências.

Classificação sugerida: **muito provavelmente texto assistido por IA, com edição humana parcial e revisão final incompleta**.

---

## Pontos salientes, do mais grave ao mais leve

### 1. Crítico — Placeholders e instruções de template não removidos

O documento contém trechos que indicam que a versão final não foi concluída ou que o template da UNIVESP foi colado sem revisão.

Evidências:

- “Placeholder para descrição detalhada da solução final adotada...”
- “Placeholder para apresentação dos resultados obtidos...”
- “Placeholder para registros de feedbacks coletados...”
- “Placeholder para considerações finais detalhadas...”
- “É importante que o grupo inclua imagens, storyboards ou ilustrações...”
- “sugere-se que, neste capítulo, seja feita a descrição detalhada...”
- “Espera-se que o grupo demonstre quais foram as melhorias...”

**Impacto:** é o problema mais grave. Compromete a ideia de “relatório final”, indica texto inacabado e mistura instruções do modelo com conteúdo do trabalho.

**Recomendação:** remover todos os placeholders e instruções de template antes de qualquer submissão.

---

### 2. Alto — Fortes sinais de texto gerado ou assistido por IA em partes conceituais

Há características recorrentes de escrita gerada por IA, especialmente nas seções de introdução, justificativa e fundamentação teórica.

Evidências:

- Repetições frequentes de expressões como “RBAC nativo”, “base organizada”, “tomada de decisão mais segura” e “justificativa acadêmica”.
- Uso repetido de conectivos padronizados: “Nesse contexto”, “Dessa forma”, “Diante dessas necessidades”, “Além disso”.
- Parágrafos genéricos sobre análise de dados, Indústria 4.0, usabilidade e banco de dados, com pouca conexão específica com o caso real.
- Termos em inglês no meio do português: **“Support for growth”**, “overkill”, “deploy gratuito”, “free tier”, “placeholder”.
- Repetição de explicações já apresentadas, como se o texto estivesse “preenchendo” seções.

**Impacto:** não prova autoria por IA, mas é o principal conjunto de sinais textuais. O texto parece ter sido gerado em blocos e parcialmente editado.

**Recomendação:** reescrever os trechos genéricos com exemplos concretos da fábrica, eliminar repetições e padronizar a linguagem.

---

### 3. Alto/Médio — Inconsistências entre figuras, legendas e sumário

Há problemas claros de organização visual e referência às figuras.

Evidências:

- A lista de figuras indica: Figura 1 – Wireframe Gestão; Figura 2 – Wireframe Estoque; Figura 3 – Wireframe Tela de Produção; Figura 4 – Wireframe Manutenção.
- No corpo, a Figura 1 aparece associada à tela de Estoque, mas está legendada como “Wireframe Gestão”.
- A Figura 2 não aparece de forma clara.
- A Figura 3 aparece associada à tela de Manutenção, mas está legendada como “Wireframe Tela de Produção”.
- A Figura 4 aparece associada à tela de Produção, mas está legendada como “Wireframe Manutenção”.

**Impacto:** compromete a credibilidade técnica do relatório e a compreensão dos wireframes.

**Recomendação:** revisar a numeração, as legendas e a ordem das imagens; garantir que cada figura seja citada no texto.

---

### 4. Médio — Referências e citações mal formatadas

A seção de referências está comprimida e pouco padronizada.

Evidências:

- Título “REFERENCIAS” sem acento.
- Referências todas em um único bloco, sem espaçamento adequado.
- “CRISP- DM” com espaço indevido.
- Datas de acesso genéricas como “Acesso em: 2026”.
- Falta de padronização entre autores, títulos e links.
- Algumas afirmações conceituais não têm citação direta no texto.

**Impacto:** reduz o rigor acadêmico e dificulta a verificação das fontes.

**Recomendação:** padronizar conforme ABNT ou norma indicada pela UNIVESP, separar cada referência e inserir citações no corpo do texto.

---

### 5. Médio — Repetições e redundâncias

O texto repete ideias e expressões em vários pontos.

Exemplos:

- “RBAC nativo” aparece várias vezes.
- “Justificativa acadêmica” é repetida em seções diferentes.
- A mesma explicação sobre dados dispersos, planilhas e memória individual aparece mais de uma vez.
- A ideia de “base organizada para decisões mais seguras” é reapresentada com pouca variação.

**Impacto:** deixa o texto artificial, cansativo e com aparência de geração automática sem revisão.

**Recomendação:** consolidar ideias repetidas e eliminar parágrafos que apenas reformulam o anterior.

---

### 6. Médio — Inconsistência de escopo e de metodologia

Há uma tensão entre “resultados preliminares”, “protótipo inicial” e “solução final”.

Evidências:

- O texto afirma que os módulos ainda não estão completamente finalizados.
- A seção 3 é chamada “RESULTADOS: SOLUÇÃO FINAL”, mas contém apenas placeholders.
- A metodologia cita Design Thinking com cinco fases, enquanto a seção de resultados menciona os passos da UNIVESP: “ouvir, criar e implementar”.
- Há mistura entre proposta inicial, wireframes e solução final.

**Impacto:** o leitor não entende claramente o que foi efetivamente entregue e o que ainda é proposta futura.

**Recomendação:** deixar explícito o estágio do projeto e alinhar a metodologia com a seção de resultados.

---

### 7. Baixo/Médio — Erros de revisão linguística e padronização

Há vários sinais de falta de revisão final.

Exemplos:

- Termos em inglês sem necessidade: “Support for growth”, “overkill”, “deploy”.
- Legendas de figuras trocadas.
- Tabela com formatação compacta e pouco legível.
- Numeração e títulos irregulares.
- Uso de “Placeholder” no corpo do relatório.

**Impacto:** prejudica a apresentação, mas é corrigível com revisão editorial.

**Recomendação:** fazer revisão ortográfica, padronizar termos e corrigir legendas e tabelas.

---

### 8. Baixo — Elementos que sugerem participação humana ou conhecimento específico do projeto

Nem tudo indica IA. Há conteúdos específicos que dificilmente seriam inventados sem contato com o projeto.

Exemplos:

- Dados concretos: tanque de 2.000 litros, três motores trituradores, produção média de 150 baldes por semana, embalagens de 1 L, 3,6 L e 18 L.
- Link do GitHub: `https://github.com/RafaelMassao/TintasMGMT`.
- Stack detalhada: React 19, TypeScript, TanStack Router/Start, Tailwind CSS, Supabase, RLS.
- Tabela de mitigação com estratégias técnicas específicas.
- Descrição de perfis de acesso e estrutura de rotas.

**Impacto:** esses pontos enfraquecem a hipótese de geração 100% automática. Eles indicam que houve participação humana ou pelo menos uso de informações reais do projeto.

---

## Recomendações prioritárias

1. **Remover todos os placeholders e instruções de template.**
2. **Corrigir a numeração e as legendas das figuras.**
3. **Padronizar as referências e inserir citações no texto.**
4. **Reescrever os trechos genéricos e repetitivos.**
5. **Eliminar termos em inglês desnecessários.**
6. **Alinhar a metodologia com a seção de resultados.**
7. **Fazer uma revisão final de português, formatação e coerência.**
8. **Se houver preocupação com autoria, verificar histórico de edição no Google Docs/Word, versões no Git ou registros de prompts.**

---

## Conclusão

O documento não parece ser 100% escrito por humano nem 100% gerado por IA sem edição. O padrão mais consistente é de **texto híbrido**: base gerada ou assistida por IA nas partes conceituais e de template, com inserção humana nos detalhes técnicos e específicos do projeto.

O problema mais grave não é apenas o possível uso de IA, mas a **falta de revisão final**: placeholders, legendas trocadas, referências mal formatadas e repetições comprometem a qualidade do relatório.