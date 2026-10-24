# Plano Detalhado de Correções - Relatório Parcial

Baseado no repositório: https://github.com/RafaelMassao/TintasMGMT

---

## 1. Stack Tecnológica (para seção 2.5 / Solução Inicial)

**Frontend:**
- React 19 + TypeScript
- TanStack Router (file-based routing) + TanStack Start (SSR)
- TanStack Query v5 (data fetching/caching)
- Tailwind CSS v4 + Radix UI (componentes acessíveis)
- Recharts (gráficos)
- React Hook Form + Zod (validação)

**Backend/Banco:**
- Supabase (PostgreSQL + Auth + Real-time)
- Row Level Security (RLS) para controle de acesso

**Estrutura de Rotas (19 módulos):**
```
/login, /cadastro, /recuperar-senha, /redefinir-senha
/_painel/dashboard, /_painel/cadastros, /_painel/producao, /_painel/pedidos
/_painel/estoque, /_painel/envase, /_painel/compras, /_painel/perdas
/_painel/manutencao, /_painel/atrasos, /_painel/alertas, /_painel/relatorios
/_painel/configuracoes, /_painel/sem-acesso
```

**Perfis de Acesso:**
- administrador, gestor, producao, vendas, estoque, manutencao

---

## 2. Modelo de Dados (Supabase - para fundamentação e metodologia)

**Catálogos (cadastros base):**
- `unidades_medida`, `cores`, `embalagens`, `produtos`, `clientes`, `fornecedores`
- `materiais` (matérias-primas), `equipamentos`, `tanques`, `motivos_perda_atraso`

**Operacionais:**
- `lotes` (produção), `envases`, `pedidos` + `itens_pedido` (vendas)
- `movimentacoes_estoque`, `saldos_estoque` (produtos, materiais, embalagens)
- `perdas`, `paradas`, `manutencoes`

**Segurança:**
- `perfis_usuario`, `permissoes` (RLS policies)

---

## 3. Dashboard Implementado (para item 8 - imagens/prints)

**Indicadores (StatCards) por perfil:**
- Produção: unidades/litros produzidos (Factory icon)
- Vendas: unidades/litros vendidos, pedidos atrasados (PackageCheck, ClipboardList)
- Estoque: itens abaixo do mínimo (Boxes)
- Perdas: valor estimado, qtd registros (AlertTriangle)
- Manutenção: horas paradas, preventiva vs corretiva (Timer)

**Gráficos (Recharts):**
- Produção vs Vendas por período (linha)
- Ranking embalagens (barras: unidades e litros)
- Cores mais vendidas (barras + evolução temporal + tabela participação/receita)
- Estoque por categoria (barras: saldo + alertas)
- Perdas por motivo (barras)
- Paradas por equipamento (barras horas)

**Filtros globais:** período, produto, cor, embalagem, status, equipamento

---

## 4. Design Thinking - Mapeamento para Código (item 7)

| Etapa DT | Implementação no Código |
|----------|------------------------|
| **Empatizar** | Levantamento in loco: equipamentos (tanque 2000L, 3 motores, bomba, envase manual), embalagens (1L, 3.6L, 18L), ~150 baldes/semana |
| **Definir** | Problem statement: "Como organizar dados dispersos de produção/vendas/estoque/manutenção?" → Requisitos em `src/lib/dashboard/useDashboardData.ts`, `src/lib/permissoes.ts` |
| **Idear** | Wireframes baixa fidelidade (Anexos Figs 1-4) → Estrutura de rotas e componentes em `src/routes/_painel.*` |
| **Prototipar** | App funcional: autenticação (Supabase Auth), cadastros (`_painel.cadastros`), dashboard com dados mock + reais, RBAC |
| **Testar** | Validação prevista: comparar registros do sistema com planilhas da empresa, testes usabilidade com operadores |

---

## 5. Dificuldades Identificadas → Estratégias no Sistema (item 9)

| Dificuldade Real | Estratégia Implementada/Planejada |
|------------------|-----------------------------------|
| Produção "150 baldes/semana" sem detalhe | Formulário lote: campos obrigatórios (produto, cor, embalagem, qtd planejada/realizada, tanque, datas) |
| Quando produto entra no estoque | Gatilho: ao finalizar envase (`envase.status = concluido`) → `movimentacao_estoque` type=entrada + atualiza `saldos_estoque` |
| Registro de perdas/consumo | Tela `/perdas` com tipos: processo, quebra embalagem, vencimento, contaminação, outro; campo `valor_estimado` |
| Acompanhamento máquinas | Cadastro equipamentos com QR code; checklist revisão; parada: equipamento, causa, início/fim, lote/pedido relacionado |
| Dados dispersos (papel/memória) | Base única Supabase + RLS; cada perfil vê só seu módulo; dashboard unifica indicadores |

---

## 6. Referências Técnicas para Fundamentação (item 6)

Já citadas no relatório + podem ser conectadas:
- **TanStack Router/Start/Query**: arquitetura moderna full-stack React
- **Supabase/PostgreSQL + RLS**: Elmasri & Navathe (modelagem relacional + segurança)
- **Radix UI + Tailwind**: Norman/Nielsen (usabilidade, acessibilidade - componentes compostos, ARIA)
- **Recharts**: visualização de dados industriais (Cleveland/McGill - percepção gráfica)
- **Zod + React Hook Form**: validação declarativa (prevenção erros entrada dados)
- **OWASP Top 10**: autenticação Supabase (MFA, sessões), RLS (controle acesso), HTTPS (Vercel)

---

## 7. Justificativa Acadêmica - Lacunas (item 4)

**Estudos relacionados:**
- Sistemas MES/ERP para PMEs: complexos, caros, overkill para fábrica pequena
- Manufatura 4.0: foco em grandes indústrias, sensores IoT, não em organização básica de dados
- Análise de dados em PMEs: gap entre "ter dados" e "usar dados" - falta ferramenta acessível

**Lacuna preenchida pelo Tintas MGMT:**
- Solução web simples, low-code, deploy gratuito (Vercel + Supabase free tier)
- Foco em organização ANTES de análise avançada (base para futuro ML/sensores)
- RBAC nativo para separação de responsabilidades (produção vs vendas vs manutenção)
- Extensível: schema Supabase permite adicionar sensores/ML sem refatorar frontend

---

## 8. Contribuições para Empresa Parceira (item 5)

1. **Centralização**: substitui cadernos/planilhas/whatsapps por base única
2. **Rastreabilidade**: lote → envase → estoque → pedido → entrega (cadeia completa)
3. **Alertas automáticos**: estoque mínimo, pedidos atrasados, manutenções vencidas
4. **Histórico**: base para comparar períodos, identificar sazonalidade (cores/embalagens)
5. **Fundação Indústria 4.0**: schema pronto para sensores (temperatura tanque, vibração motores, contador envase)