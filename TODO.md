# TODO - Correções do Relatório Parcial

*Detalhes técnicos em `docs/plano-detalhado.md`*

## 🔴 EXIGEM APROVAÇÃO - Escrita de textos longos (mais que 1 frase/legenda)

### 1. Sintetizar o resumo (RESUMO, linhas 177-185)
- [ ] Reduzir para ≤ 250 palavras (atualmente ~300)
- [ ] Manter: problema, Tintas MGMT, escopo inicial, palavras-chave
- [ ] Remover detalhes excessivos de equipamentos/números

### 2. Resumir e delimitar objetivos específicos (2.1, linhas 265-293)
- [ ] Reduzir 10 → 5-6 objetivos bem delimitados
- [ ] Agrupar relacionados (cadastros, produção/vendas, estoque/perdas, manutenção, interface, base dados)

### 3. Adicionar justificativa cultural (2.2, antes linha 307)
- [ ] Subseção "Justificativa Cultural": indústria tintas na região, preservação conhecimento, impacto socioeconômico (Araçariguama, Iperó, Itapetininga, Salto)

### 4. Reescrever justificativa acadêmica (2.2, linhas 307-308)
- [ ] Basear em estudos: MES/PMEs, Manufatura 4.0, análise dados PMEs
- [ ] Citar lacuna: ausência solução simples/acessível para fábricas pequenas
- [ ] Conectar: como Tintas MGMT preenche (stack moderna, low-cost, extensível)

### 5. Descrever contribuições para público externo (2.2, após linha 306)
- [ ] Benefícios empresa: centralização, rastreabilidade lote→entrega, alertas, histórico, base Indústria 4.0

### 6. Fundamentação: articular referenciais com problema (2.3, linhas 315-335)
- [ ] Conectar cada referencial ao problema:
  - Análise dados → acompanhar produção/vendas/estoque/perdas
  - Manutenção preditiva → paradas motores/bomba/tanque
  - Indústria 4.0/sensores → evolução futura
  - ML → previsão demanda/risco (futuro)
  - Norman/Nielsen → perfis usuários diversos (RBAC)
  - Elmasri/Navathe → modelagem relacional catálogos/operacional
  - OWASP → autenticação Supabase + RLS + perfis acesso
- [ ] Expandir para 5-6 parágrafos articulados

### 7. Metodologia: demonstrar passos Design Thinking (2.4, linhas 343-359)
- [ ] Estruturar em 5 fases: Empatizar, Definir, Idear, Prototipar, Testar
- [ ] Mapear cada fase ao código real (ver `docs/plano-detalhado.md` tabela)
- [ ] Substituir "primeira/segunda etapa" por nomes fases DT

### 8. Solução inicial: descrever com imagens da interface (2.5, linhas 379-395)
- [ ] Mover Figs 1-4 dos Anexos para corpo da seção 2.5
- [ ] Para cada wireframe: imagem + legenda "Figura X – Wireframe [nome]. Fonte: Elaboração própria, 2026" + descrição campos/componentes
- [ ] Detalhar arquitetura: React 19 + TanStack Start + Supabase + Tailwind + Recharts
- [ ] Incluir prints telas reais (login, dashboard, cadastros) - stack em `package.json`

### 9. Clarificar minimização dificuldades empresa (2.5, linhas 389-392)
- [ ] Transformar "dificuldades" em "estratégias de mitigação" (tabela)
- [ ] Mapear: detalhar produção → formulário lote; entrada estoque → gatilho envase; perdas → tela dedicada; máquinas → cadastro QR + checklist + parada

## 🟢 PODEM SER FEITOS DIRETAMENTE - Formatação/ajustes curtos

### 10. Revisar texto, estrutura, organização e figuras
- [x] Remover páginas em branco, padronizar formatação
- [x] Verificar numeração figuras/tabelas, ajustar sumário
- [x] Completar referências ABNT (edição, local, editora)
- [x] Mover 4 wireframes para seção 2.5 com legendas padronizadas
- [x] Atualizar Lista de Ilustrações com páginas corretas