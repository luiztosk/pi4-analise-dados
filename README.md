# PI4 - Análise de Dados e Dashboard

## Objetivo

Desenvolver uma análise de vendas em escala a partir de **100 mil pedidos** gerados pelo **Contoso Data Generator V2**, aplicar análise offline e aprendizado de máquina e publicar um dashboard estático.

O projeto atende ao Plano Curricular ao combinar análise de dados, aprendizado de máquina e uma interface para visualização dos resultados.

## Arquitetura escolhida

- **Geração dos dados:** Contoso Data Generator V2, executado localmente.
- **Volume:** `OrdersCount = 100000`.
- **Análise e ML:** offline, em Python, com DuckDB ou Polars e scikit-learn.
- **Dashboard:** React + Vite + Apache ECharts.
- **Publicação:** Cloudflare Workers Static Assets, como site estático/SPA.
- **Dados no dashboard:** agregados, resultados e artefatos calculados previamente; não haverá análise ou ML em tempo real.

## Estrutura do repositório

```text
.
├── README.md
├── .gitignore
├── contoso/
│   ├── config/                 # config.json do gerador
│   ├── scripts/                # comandos e wrappers do Contoso
│   └── output/                 # CSVs gerados localmente
├── analysis/
│   ├── notebooks/              # exploração e experimentos
│   ├── scripts/                # ETL, features, treinamento e exportação
│   ├── output/                 # tabelas e JSON para o dashboard
│   └── models/                 # modelos e métricas persistidos
├── data/
│   ├── raw/                    # dados brutos gerados ou importados
│   └── processed/              # dados tratados intermediários
└── dashboard/
    ├── src/                    # aplicação React/Vite
    └── public/data/            # agregados finais consumidos pelo frontend
```

## Fluxo de trabalho

1. Configurar o Contoso Data Generator V2 para gerar 100 mil pedidos em CSV.
2. Salvar os arquivos brutos em `data/raw/`.
3. Executar scripts offline para limpeza, enriquecimento, agregação e criação de features.
4. Treinar e avaliar modelos simples e explicáveis, como:
   - previsão de receita ou quantidade;
   - segmentação de clientes;
   - identificação de produtos, lojas ou períodos de maior valor;
   - detecção de anomalias em vendas e margens.
5. Exportar apenas resultados leves para `analysis/output/` e `dashboard/public/data/`.
6. Construir o dashboard com React, Vite e ECharts.
7. Publicar o build estático no Cloudflare Workers com `assets.not_found_handling = "single-page-application"`.

## Configuração inicial do Contoso

O gerador recebe um arquivo `config.json`, um arquivo `data.xlsx`, uma pasta de saída e uma pasta de cache. A configuração inicial deve usar:

```json
{
  "OrdersCount": 100000,
  "OutputFormat": "CSV",
  "SalesOrders": "BOTH",
  "CsvMaxOrdersPerFile": -1,
  "CsvGzCompression": 0
}
```

Os scripts de execução ficam em `contoso/scripts/`. O arquivo `data.xlsx` e o binário do gerador podem ser mantidos fora do Git, conforme a disponibilidade local.

## Resultado esperado

O dashboard deve apresentar:

- indicadores gerais de vendas;
- evolução temporal;
- comparação por categoria, produto, cliente e loja;
- distribuição de quantidade, receita e margem;
- resultados e métricas dos modelos de ML;
- explicações curtas sobre as conclusões encontradas.

## Regras do projeto

- Manter a solução simples e reproduzível.
- Executar a análise pesada apenas offline.
- Publicar no Cloudflare somente arquivos estáticos e dados já processados.
- Não commitar dados brutos, caches, builds, dependências ou arquivos de ambiente.
- Manter os scripts e a documentação suficientes para reproduzir o fluxo.

## Próximos passos

1. Adicionar `config.json` e o script de execução do Contoso.
2. Gerar os 100 mil pedidos.
3. Implementar a pipeline offline de análise e ML.
4. Criar o dashboard estático.
5. Publicar o build no Cloudflare Workers.
