# CLAUDE.md — Fase 2: Ferramentas Práticas

## Sobre este momento da jornada
**Fase atual:** Fase 2 — Ferramentas Práticas (Semanas 4–7)
**Foco:** Consolidar o stack que aparece em 90% das vagas júnior/pleno
**Objetivo final da fase:** Entregar o Projeto 2 — Análise E-commerce End-to-End (Olist)

## Quem sou
Rickelme David (RickelmeDSC). Backend Developer (Node.js, NestJS, PostgreSQL) em transição para carreira dupla **Backend + Análise de Dados**. Seguindo um roadmap estruturado de 22 semanas.

## O que já completei

### ✅ Fase 1 — Fundamentos (Semanas 1–3) CONCLUÍDA

**Cursos:**
- Python para Dados — primeiros passos
- Python para Dados — funções, estruturas de dados e exceções
- Estatística com Python — frequências e medidas
- SQLite online — instruções SQL
- Excel — editor de planilhas

**Projetos publicados:**
- `python-fundamentos` — exercícios de curso organizados
- `jornada-dados-ia` — 3 scripts iniciais (calculadora, conversor, gerador de senhas)
- `analise-descritiva-pnad-2015` — análise da PNAD 2015 com Pandas + Seaborn + SciPy
- `analise-titanic-sql-estatistica` — SQL aplicado + estatística em Python puro

**Skills consolidadas:**
- Python: variáveis, condicionais, loops, funções, estruturas de dados, exceções
- SQL básico: SELECT, WHERE, GROUP BY, JOIN, agregações
- Pandas introdutório: DataFrames, leitura de CSV, groupby simples
- Estatística: medidas de tendência central, dispersão, separatrizes, assimetria
- Visualização: Matplotlib, Seaborn (histogramas, boxplots, gráficos de barra)
- Storytelling: README narrativo, interpretação de resultados, contexto social/de negócio
- Git/GitHub: workflow básico, commits semânticos, repositórios organizados

## Onde estou agora

✅ **Semana 4 concluída — Pandas avançado**

Curso **Pandas — conhecendo a biblioteca** finalizado, com o notebook de ETL publicado no GitHub (`pandas-conhecendo-a-biblioteca`). Cobriu o fluxo completo: exploração, análise por tipo/bairro, remoção de comerciais, tratamento de nulos, filtros, exportação e criação de colunas (numéricas, categóricas e booleanas). Todos os desafios da aula resolvidos em notebook separado.

🚀 **Próximo passo imediato:** Semana 5 — **SQL avançado** (Joins, Views, transações).

## Roadmap da Fase 2 (Semanas 4–7)

### ✅ Semana 4 — Pandas avançado (CONCLUÍDA)
**Foco:** Solidificar Pandas após o "aprender no susto" do projeto PNAD.

| Dia | Curso/Tópico | Entregável |
|-----|---|---|
| Seg | Pandas — conhecendo a biblioteca | Series, DataFrame, indexação |
| Ter | Pandas — conhecendo (continuação) | Filtros, colunas, tipos |
| Qua | Pandas I/O — formatos de arquivos | CSV, Excel, JSON, Parquet |
| Qui | Pandas I/O + prática integrada | Mesclar múltiplas fontes |
| Sex | Pandas — selecionando e agrupando | loc, iloc, groupby profundo |
| Sáb | Pandas — limpeza e tratamento | nulos, duplicatas, normalização |

**Entregável:** ✅ Notebook de ETL profissional sobre dataset real (público no GitHub) — **entregue**.

### Semana 5 — SQL avançado
**Foco:** SQL além do básico. Joins são cobrados em 100% das entrevistas técnicas.

| Dia | Curso/Tópico |
|-----|---|
| Seg-Ter | Consultas SQL — Joins, Views, transações |
| Qua | Joins na prática — exercícios pesados |
| Qui | Views e transações |
| Sex | SQLite — análise de dados com SQL |
| Sáb | Pandas — transformação (encerrar Pandas) |

**Entregável:** Arquivo `.sql` no GitHub com 15 queries de negócio (ticket médio, LTV, sazonalidade).

### Semana 6 — Power BI
**Foco:** Ferramenta #1 de BI no mercado brasileiro.

| Dia | Curso/Tópico |
|-----|---|
| Seg-Ter | Power BI — analisando dados |
| Qua-Qui | Power BI — modelagem (star schema) |
| Sex | Power BI — conceitos de DAX |
| Sáb | Prática: primeiro dashboard do zero |

### Semana 7 — Storytelling + Projeto Portfólio
**Foco:** Entregar o projeto mais importante até agora.

| Dia | Foco |
|-----|---|
| Seg | Data Storytelling |
| Ter | Data Visualization — gráficos Python |
| Qua | Projeto: download Olist + ETL Pandas |
| Qui | Projeto: SQLite + queries de negócio |
| Sex | Projeto: Power BI dashboard |
| Sáb | Projeto: vídeo demo + README |

## ❌ Cursos a PULAR nesta fase

Conforme análise estratégica anterior:

- ❌ **MySQL (módulos 10–13 do N1):** redundante com SQLite + BigQuery (vai pra Fase 3)
- ❌ **Excel avançado (N1 #09, #17):** já tem base suficiente
- ❌ **SQLite Online executando consultas (N1 #03):** redundante com o curso da Base
- ❌ **Trabalhando com dados — fundamentos (N1 #01):** muito teórico, conteúdo já dominado

## Stack utilizada nesta fase

### Já dominada
- Python 3.14
- SQLite 3 (módulo nativo)
- Estatística descritiva em Python puro
- Matplotlib, Seaborn, SciPy

### A solidificar nesta fase
- **Pandas avançado** — limpeza, transformação, merge, pivot
- **SQL com joins complexos** — INNER, LEFT, RIGHT, FULL, CTEs, Views
- **Power BI Desktop** — modelagem, DAX, dashboards
- **Storytelling de dados** — narrativa, comunicação visual

### Ferramentas auxiliares
- VS Code com Jupyter
- DBeaver ou DB Studio (para SQL)
- Power BI Desktop
- Git/GitHub

⚠️ Comando para instalar pacotes Python: `py -m pip install --user [pacote]`

## Projeto da Fase 2: Análise E-commerce End-to-End (Olist)

**Escopo do projeto final da fase:**

```
ecommerce-analytics/
├── README.md (narrativa com achados de negócio)
├── DOCUMENTACAO.md
├── requirements.txt
├── data/
│   └── olist_*.csv (dataset Kaggle)
├── notebooks/
│   ├── 01_etl_e_limpeza.ipynb
│   └── 02_analise_negocio.ipynb
├── sql/
│   └── queries_negocio.sql
├── powerbi/
│   └── dashboard_ecommerce.pbix
└── images/
    └── dashboard_prints/
```

**Análises esperadas:**
- Ticket médio por categoria
- Tempo médio de entrega por estado
- Taxa de retorno/devolução
- Cohort de retenção de clientes
- Sazonalidade de vendas
- Top produtos por receita e por volume
- Análise de avaliações vs entrega
- Mapa de calor geográfico

**Stack do projeto:**
- ETL: Pandas
- Storage: SQLite (modelagem star schema)
- Análise SQL: 8 queries de negócio documentadas
- Visualização: Power BI com 3 páginas (Visão Geral, Produtos, Clientes)
- DAX: 5 medidas calculadas (ticket médio, crescimento MoM, LTV simplificado, retenção, %)
- Entrega: vídeo demo de 2 min + post no LinkedIn

## Regras de código para esta fase

- Comentários em português explicando o raciocínio
- Markdown rico entre células de notebook — narrativa, não só código
- snake_case para variáveis e funções
- DataFrames com nomes descritivos (`df_vendas` em vez de `df`)
- SQL formatado com uma cláusula por linha
- Conclusões em prosa após cada análise
- Gráficos com título, labels e cores intencionais

## Convenções de commit

- `feat: adiciona [funcionalidade]`
- `feat: implementa [análise]`
- `docs: atualiza README com [seção]`
- `style: ajusta visualização do gráfico [Y]`
- `fix: corrige cálculo de [métrica]`
- `refactor: melhora função de [tópico]`

## Como me ajudar (instruções para o Claude Code)

### Filosofia geral
Quero APRENDER fazendo. **Escreva o código direto nas células, mas explique cada decisão passo a passo.** Avance UMA SEÇÃO POR VEZ, conforme eu autorizar.

### Para Pandas
- Antes do código, explique o conceito (groupby, merge, pivot)
- Mostre alternativas quando houver (loc vs query, apply vs map)
- Aponte armadilhas comuns (SettingWithCopyWarning, indices)
- Mostre como **validar** o resultado (.shape, .info, .describe)

### Para SQL
- Explique o que a query vai responder ANTES de escrevê-la
- Quebre queries complexas em CTEs (mais legível)
- Interprete o resultado: o que ele revela sobre o negócio?

### Para Power BI
- Explique decisões de modelagem (por que star schema, por que essa relação)
- Mostre como pensar em medida DAX vs coluna calculada
- Sugira layout antes de construir

### Estilo de explicação
- Português sempre
- Analogias do dia a dia
- Interpretação de negócio, não só técnica
- Conectar com aplicação real

## O que NÃO fazer

- ❌ NÃO adiantar várias seções de uma vez
- ❌ NÃO usar bibliotecas além das do roadmap
- ❌ NÃO escrever conclusões sem interpretação de negócio
- ❌ NÃO usar nomes de variáveis em inglês
- ❌ NÃO pular o "por quê" para ir direto ao "como"
- ❌ NÃO usar features avançadas ainda não estudadas

## Próximos passos depois desta fase

1. ✅ Concluir Fase 2 com o projeto Olist publicado
2. **Semana 8:** começar a aplicar para vagas júnior + freelances pequenos
3. Iniciar **Fase 3 — Profissionalização (Semanas 8–13)**:
   - Python e APIs (Requests)
   - BigQuery (cloud SQL)
   - n8n + Make (automação)
   - Primeiros passos com Claude API
4. **Projeto 3:** Pipeline de Notícias com IA

## Repositórios do portfólio

```
github.com/RickelmeDSC/
├── python-fundamentos              ← exercícios consolidados ✅
├── jornada-dados-ia                ← scripts iniciais ✅
├── analise-descritiva-pnad-2015    ← Projeto Fase 1 (PNAD) ✅
├── analise-titanic-sql-estatistica ← SQL + estatística pura ✅
├── ecommerce-analytics             ← PROJETO ATUAL (Fase 2)
├── pipeline-noticias-ia            ← futuro Projeto Fase 3
└── agente-analista-dados           ← futuro Projeto Fase 4
```

## Indicadores de sucesso desta fase

Ao final da Semana 7, devo ter:
- [ ] Pandas dominado (limpeza, merge, groupby, pivot, transformação)
- [ ] SQL com joins complexos sem consulta
- [ ] Power BI: criar dashboard do zero com modelagem star schema
- [ ] 5+ medidas DAX escritas com confiança
- [ ] Projeto Olist publicado com README profissional
- [ ] Vídeo demo de 2 minutos gravado
- [ ] Post no LinkedIn sobre o projeto
- [ ] Pronto para aplicar a vagas júnior na Semana 8