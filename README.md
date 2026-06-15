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
- **Manipulação** — criação de colunas numéricas (cálculo), categóricas (concatenação) e booleanas (comparação), além de `replace` e `apply`

Além da aula principal, o `notebook_desafios.ipynb` resolve **todos os desafios** propostos: análises da base de aluguel (média de quartos, bairros únicos, ranking de preço) e dois desafios de tratamento com a base de alunos (`alunos.csv`) — limpeza de nulos, remoção de registros, filtros, exportação e engenharia de colunas (pontos extras, nota final, aprovação).

## 📁 Estrutura do projeto

```
pandas-conhecendo-a-biblioteca/
├── README.md                    ← você está aqui
├── CONFIGURACAO_AMBIENTE.md     ← como rodar o projeto do zero
├── notebooks/
│   ├── notebook_inicial.ipynb   ← aula principal (ETL + análise + manipulação)
│   └── notebook_desafios.ipynb  ← todos os desafios resolvidos (aluguel + alunos)
└── dados/
    ├── alunos.csv               ← fonte de entrada dos desafios (versionada)
    ├── dados_apartamentos.csv   ← saída gerada pelo notebook (não versionada)
    └── alunos_aprovados.csv     ← saída gerada pelo notebook (não versionada)
```

## 🚀 Como rodar

1. Configure o ambiente seguindo o [CONFIGURACAO_AMBIENTE.md](CONFIGURACAO_AMBIENTE.md).
2. Abra o `notebooks/notebook_inicial.ipynb` no VS Code.
3. Selecione o kernel **"Python 3.XX (Dados)"** e execute as células de cima para baixo.

> ⚠️ No VS Code, o notebook executa a partir da **própria pasta** (`notebooks/`). Por isso os caminhos
> de arquivo sobem um nível com `../`, ex: `pd.read_csv('../dados/alunos.csv')`. Rode as células de
> cima para baixo para garantir que imports e variáveis existam.

## 🛠️ Stack

- Python 3.13 (casa) / 3.14 (trabalho)
- Pandas · Matplotlib
- Jupyter (via VS Code)

## 📊 Dados

Bases públicas disponibilizadas pela [Alura](https://github.com/alura-cursos/pandas-conhecendo-a-biblioteca):
a de **aluguel** é carregada direto da URL no notebook; a de **alunos** (`alunos.csv`) é versionada em `dados/`
por ser uma fonte de entrada. Os demais arquivos `.csv` em `dados/` são **resultados derivados** — basta
rodar o notebook para regerá-los, por isso não vão para o repositório.
