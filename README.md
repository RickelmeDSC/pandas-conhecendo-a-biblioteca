# 🐼 Pandas — Conhecendo a Biblioteca

Projeto de estudo da **Semana 4 (Fase 2)** da minha jornada de transição para Análise de Dados.
O foco é solidificar o Pandas — da leitura de dados à limpeza, filtragem e exportação — usando uma
base real de imóveis para aluguel no Rio de Janeiro.

## 🎯 O que este projeto cobre

A análise parte de uma base com **32.960 imóveis** e percorre o fluxo completo de uma análise exploratória:

- **Conhecendo a base** — leitura de CSV, `head`/`tail`, `info`, `shape`, seleção de colunas
- **Análise exploratória** — valor médio de aluguel por tipo de imóvel (`groupby` + gráfico)
- **Recorte dos dados** — remoção de imóveis comerciais e foco em apartamentos
- **Tratamento de nulos** — `isnull`, `fillna` e remoção de registros inválidos
- **Filtros** — seleção por múltiplas condições com máscaras booleanas
- **Exportação** — salvando o resultado tratado com `to_csv`

## 📁 Estrutura do projeto

```
pandas-conhecendo-a-biblioteca/
├── README.md                    ← você está aqui
├── CONFIGURACAO_AMBIENTE.md     ← como rodar o projeto do zero
├── notebooks/
│   ├── notebook_inicial.ipynb   ← aula principal (ETL + análise)
│   └── notebook_desafios.ipynb  ← desafios extras de análise por bairro
└── dados/
    └── dados_apartamentos.csv   ← saída gerada pelo notebook (não versionada)
```

## 🚀 Como rodar

1. Configure o ambiente seguindo o [CONFIGURACAO_AMBIENTE.md](CONFIGURACAO_AMBIENTE.md).
2. Abra o `notebooks/notebook_inicial.ipynb` no VS Code.
3. Selecione o kernel **"Python 3.XX (Dados)"** e execute as células de cima para baixo.

> ⚠️ Os caminhos de arquivo (ex: `dados/dados_apartamentos.csv`) são relativos à **raiz do projeto**,
> que é o diretório padrão de execução de notebooks no VS Code. Abra a pasta do projeto na raiz.

## 🛠️ Stack

- Python 3.13 (casa) / 3.14 (trabalho)
- Pandas · Matplotlib
- Jupyter (via VS Code)

## 📊 Dados

Base pública de aluguel disponibilizada pela [Alura](https://github.com/alura-cursos/pandas-conhecendo-a-biblioteca),
carregada diretamente da URL dentro do notebook. O arquivo em `dados/` é um **resultado derivado**
(apartamentos tratados) — basta rodar o notebook para regerá-lo.
