# 🛠️ Configuração do Ambiente — Pandas no VS Code

> Guia para deixar o notebook rodando do zero em qualquer máquina Windows.
> Criado em 08/06/2026 após resolver os erros da primeira aula de Pandas.

---

## 💻 Máquinas deste projeto

Trabalho em **duas máquinas Windows** com versões diferentes de Python. Use sempre a versão da máquina onde você está — não fixe uma só.

| Máquina | Python | Nome do kernel | Display no VS Code |
|---------|--------|----------------|--------------------|
| 🏠 Casa | 3.13 | `python313-dados` | "Python 3.13 (Dados)" |
| 💼 Trabalho | 3.14 | `python314-dados` | "Python 3.14 (Dados)" |

> Sempre que registrar o kernel, troque `3XX` pela versão real da máquina (descubra com `py --version`).

---

## 🎯 Resumo do que precisa estar funcionando

Para um notebook `.ipynb` rodar Pandas no VS Code, **um único Python** precisa ter as duas coisas:

1. **`pandas`** — a biblioteca em si
2. **`ipykernel`** — o "motor" que o Jupyter/VS Code usa para executar o notebook

Se faltar `ipykernel`, o VS Code não consegue usar esse Python e cai em outro (vazio) → erro `No module named 'pandas'`.

---

## ✅ Passo a passo para configurar na máquina do trabalho

### 1. Confirmar que o Python está instalado
Abra o **PowerShell** e rode:
```powershell
py --version
```
Se não existir, baixe em https://www.python.org/downloads/ (marque **"Add Python to PATH"** na instalação).

### 2. Instalar Pandas e ipykernel
```powershell
py -m pip install --user pandas ipykernel
```
> Convenção do projeto: sempre instalar com `py -m pip install --user [pacote]`.

### 3. Registrar o kernel com nome amigável
Use a versão da **sua** máquina (veja a tabela no topo). Exemplos:
```powershell
# Casa (Python 3.13)
py -m ipykernel install --user --name=python313-dados --display-name "Python 3.13 (Dados)"

# Trabalho (Python 3.14)
py -m ipykernel install --user --name=python314-dados --display-name "Python 3.14 (Dados)"
```
Isso faz aparecer um kernel **"Python 3.XX (Dados)"** na lista do VS Code.

### 4. No VS Code
1. Instale a extensão **Jupyter** (e a **Python**), da Microsoft.
2. Abra o notebook `.ipynb`.
3. `Ctrl + Shift + P` → **"Reload Window"** (para o VS Code enxergar o kernel novo).
4. Clique no **seletor de kernel** (canto superior direito) → escolha **"Python 3.XX (Dados)"** da sua máquina.
5. Rode as células de cima para baixo.

---

## 🔍 Diagnóstico rápido (se der erro de novo)

### "ModuleNotFoundError: No module named 'pandas'"
Quase nunca é a lib que falta — é o **kernel apontando para o Python errado**.

Rode numa célula do notebook para ver qual Python ele está usando:
```python
import sys
print(sys.executable)
```
- Se apontar para `...\WindowsApps\python.exe` → é o "Python falso" da Microsoft Store. Troque o kernel.
- O certo é apontar para onde o pandas está instalado (ex: `...\Programs\Python\Python313\python.exe`).

### Checar o que cada Python tem instalado
```powershell
# Lista todos os Pythons da máquina
py -0p

# Confere se um Python específico tem pandas e ipykernel
& "CAMINHO\DO\python.exe" -c "import pandas, ipykernel; print('tudo OK')"
```

### Listar os kernels registrados
```powershell
py -m jupyter_client.kernelspecapp list
```
> ⚠️ O comando `py -m jupyter kernelspec list` pode falhar (aconteceu na máquina do trabalho, Python 3.14). O comando acima é o que funciona nas duas.

---

## 📦 Bibliotecas usadas no projeto (instalar todas de uma vez)

```powershell
py -m pip install --user pandas ipykernel matplotlib seaborn scipy openpyxl
```
> `openpyxl` é necessário para ler/escrever arquivos Excel (`.xlsx`) com o Pandas.

---

## 📝 Armadilhas de código já encontradas

### CSV vindo com "tudo numa coluna só"
Datasets brasileiros costumam usar **`;`** como separador (porque a vírgula é o separador decimal). Especifique:
```python
dados = pd.read_csv(url, sep=';')
```
Outros parâmetros úteis do `read_csv`:
- `encoding='latin-1'` ou `encoding='utf-8'` → conserta acentos quebrados
- `decimal=','` → quando os números usam vírgula decimal (R$ 1.700,50)

### Atribuir URL a variável
Texto (string) sempre entre aspas, e use `=` para guardar na variável:
```python
url = 'https://...arquivo.csv'   # ✅ com aspas e =
dados = pd.read_csv(url, sep=';')
```
