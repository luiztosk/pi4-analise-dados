# Plano de Atualização de Texto do Relatório Final

## Apenas alterações de conteúdo textual (formatação LaTeix já definida pelo usuário)

### 1. Introdução (linhas 111-121)
- **Remover** menção à "produção média aproximada de 150 baldes por semana" da linha 115
- Manter desenvolvimento do tema, importância da investigação, contexto da área e motivações
- Reduzir contextualização da empresa

### 2. Objetivos específicos (linhas 131-139)
Reescrever com fórmula: "Desenvolver ... por meio de ... onde será registrado ..."

- **Cadastros base**: "Desenvolver cadastros base por meio de catálogos organizados onde serão registrados produtos, cores, embalagens, matérias-primas, fornecedores, equipamentos, tanques e clientes"
- **Produção e vendas**: "Desenvolver sistema de monitoramento de produção e vendas por meio de controle de lotes de produção, pedidos e movimentações de estoque onde será possível rastrear a entrada de produtos acabados a fim de possibilitar maior controle dos produtos"
- **Perdas e atrasos**: "Desenvolver registro de perdas e atrasos por meio de controle de paradas de máquinas onde serão registrados motivos e responsáveis com data"
- **Manutenção**: "Desenvolver organização de manutenção por meio de controle de revisões periódicas onde serão registrados equipamentos com QR code e paradas (preventiva e corretiva)"
- **Interface e indicadores**: "Desenvolver interface e indicadores por meio de dashboard onde serão apresentados indicadores de produção, vendas, estoque e manutenção para apoio à decisão"
- **Base de dados**: "Preparar base de dados por meio de esquema relacional no Supabase com RLS onde serão organizados dados para futuras análises e sensores"

### 3. Terminologia (linha 160)
- Substituir "pergunta-problema" por "problema de pesquisa"
- Linha 160: "formula-se o seguinte problema de pesquisa que orienta este estudo..."

### 4. Justificativa (linhas 141-158)
- Manter citando estudos que embasam afirmações sobre MES/ERP para PMEs
- Garantir referências no final do relatório
- Manter contexto sobre complexidade, custo e excesso para PMEs

### 5. Contribuições Socioeconômicas (linhas 177-183)
- **Remover** subitem "Justificativa acadêmica" (linha 182)
- Manter: Apoio a empresas reais, Identificação de perdas e ganhos, Suporte ao crescimento

### 6. Metodologia (linhas 210-221)
Substituir descrição das 5 fases do Design Thinking pelas 3 etapas solicitadas:

**Atual → Proposto:**

```
\textbf{Ouvir e Interpretar o Contexto} — Etapa de levantamento do problema junto à empresa, identificação das necessidades operacionais e compreensão do contexto da fábrica de tintas.

\textbf{Criar / Prototipar} — Etapa de organização da estrutura inicial do aplicativo, desenvolvimento de wireframes, criação de cadastros básicos e definição de perfis de acesso.

\textbf{Implementar / Testar} — Etapa de implantação do protótipo e validação com a comparação entre registros do sistema e informações da empresa, verificando compreensibilidade das telas e correspondência com a realidade da operação.
```

### 7. Testagem do protótipo (após linha 221)
Inserir nova seção após Métodologia ou reestruturar seção existente:

- Informar se o protótipo já foi testado: [DEFINIR BASEADO NO CONTEXTO]
- Se foi testado, escrever como a solução foi testada
- Registrar quais devolutivas sobre a solução foram coletadas
- Indicar quais melhorias foram sugeridas para as soluções propostas/desenvolvidas

### 8. Seção de Resultados: Solução Final (linhas 306-330)
Reescrever para apresentar APENAS resultados finais, não preliminares:

- Descrição detalhada do protótipo e de sua aplicação
- Imagens e storyboards que demonstrem visualmente a solução
- Relato de como se deu o processo de construção da solução final
- Melhorias realizadas a partir de feedbacks da comunidade
- Apresentação dos resultados obtidos em cada etapa (Ouvir, Criar, Implementar)
- Feedback da comunidade incluindo validações e sugestões de melhoria

### 9. Fundamentação teórica (linhas 193-208)
Garantir inclusão de descrição das aplicações das disciplinas estudadas no Projeto Integrador:
- Desenvolvimento web
- Banco de dados
- Organização da informação
- Análise de dados
- Visualização

Manter princípios de Norman (2013) e Nielsen (1994) já presentes.

### 10. Contribuições para o Público Externo (linhas 164-191)
- Manter estrutura de contribuições
- Já terá sido removida justificativa acadêmica de Contribuições Socioeconômicas
- Manter RBAC nativo em Contribuições Acadêmicas e Técnicas