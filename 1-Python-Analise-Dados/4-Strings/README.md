# 📌 Módulo: Strings e Fatiamento em Python

Este módulo aborda manipulação de strings em Python, incluindo métodos essenciais, interpolação de valores e técnicas de fatiamento.

Strings são fundamentais em cenários de dados, sendo amplamente utilizadas em:

- Limpeza de dados (data cleaning)
- Padronização de informações
- Processamento de arquivos (CSV, JSON)
- Extração de informações (parsing)

---

# 🎯 Objetivos do Módulo

Ao final deste módulo, você será capaz de:

- Manipular e transformar strings utilizando métodos built-in
- Aplicar técnicas de padronização e limpeza de dados textuais
- Utilizar diferentes métodos de interpolação (% , format(), f-strings)
- Extrair partes específicas de textos com fatiamento (slicing)
- Trabalhar com dados textuais de forma eficiente

---

# 📚 Conteúdos Abordados

## 🔹 Conceitos Fundamentais

Strings em Python são:

| Característica | Descrição |
|----------------|-----------|
| **Sequências imutáveis** | Não podem ser alteradas após criadas |
| **Indexadas** | Podem ser acessadas por posição (índice) |
| **Iteráveis** | Podem ser percorridas com loops (for, while) |

## 🔹 Funcionamento das Strings

Cada caractere possui um índice (posição) na string:

```
texto = "Python"

P  y  t  h  o  n
0  1  2  3  4  5
```

**Índices negativos (acesso de trás para frente):**

```
P  y  t  h  o  n
-6 -5 -4 -3 -2 -1
```

## 🔹 Métodos Úteis da Classe String

### Transformação de Texto

| Método | Descrição | Exemplo |
|--------|-----------|---------|
| `upper()` | Converte para maiúsculas | `"python".upper()` → `"PYTHON"` |
| `lower()` | Converte para minúsculas | `"PYTHON".lower()` → `"python"` |
| `title()` | Primeira letra de cada palavra em maiúscula | `"rodrigo silva".title()` → `"Rodrigo Silva"` |
| `capitalize()` | Primeira letra da frase em maiúscula | `"python é legal".capitalize()` → `"Python é legal"` |

**Exemplo aplicado (padronização de dados):**

```python
nome_cliente = "rOdRiGo sIlVa"

print(nome_cliente.upper())   # RODRIGO SILVA
print(nome_cliente.lower())   # rodrigo silva
print(nome_cliente.title())   # Rodrigo Silva
```

📌 Muito utilizado para normalizar dados inconsistentes (ex: nomes, endereços, categorias).

### Remoção de Espaços

| Método | Descrição | Exemplo |
|--------|-----------|---------|
| `strip()` | Remove espaços (ou caracteres) do início e fim | `"  texto  ".strip()` → `"texto"` |
| `lstrip()` | Remove espaços do início (lado esquerdo) | `"  texto".lstrip()` → `"texto"` |
| `rstrip()` | Remove espaços do fim (lado direito) | `"texto  ".rstrip()` → `"texto"` |

**Exemplo aplicado (dados sujos):**

```python
email = "   usuario@email.com   "

print(email.strip())   # remove ambos os lados → "usuario@email.com"
print(email.lstrip())  # remove esquerda → "usuario@email.com   "
print(email.rstrip())  # remove direita → "   usuario@email.com"
```

📌 Fundamental em pipelines de ETL para limpeza de dados de entrada.

### Verificação e Busca

| Método | Descrição | Exemplo |
|--------|-----------|---------|
| `startswith(x)` | Verifica se começa com x | `"Python".startswith("Py")` → `True` |
| `endswith(x)` | Verifica se termina com x | `"Python".endswith("on")` → `True` |
| `find(x)` | Retorna índice da primeira ocorrência de x | `"Python".find("th")` → `2` |
| `count(x)` | Conta ocorrências de x | `"banana".count("a")` → `3` |
| `in` | Verifica se contém | `"Py" in "Python"` → `True` |

```python
texto = "O rato roeu a roupa do rei de Roma"

print(texto.startswith("O"))      # True
print(texto.endswith("Roma"))     # True
print(texto.find("roeu"))         # 6
print(texto.count("r"))           # 4
print("rato" in texto)            # True
```

### Substituição e Divisão

| Método | Descrição | Exemplo |
|--------|-----------|---------|
| `replace(old, new)` | Substitui old por new | `"banana".replace("a", "o")` → `"bonono"` |
| `split(sep)` | Divide a string em lista | `"a,b,c".split(",")` → `["a", "b", "c"]` |
| `join(iterável)` | Junta elementos com separador | `"-".join("Python")` → `"P-y-t-h-o-n"` |

```python
# replace
texto = "Python é incrível"
print(texto.replace("incrível", "maravilhoso"))

# split
dados = "Rodrigo;23;São Paulo"
partes = dados.split(";")
print(partes)  # ['Rodrigo', '23', 'São Paulo']

# join
print("-".join("Python"))  # P-y-t-h-o-n
```

📌 `join()` é muito usado para reconstruir strings de forma eficiente.

---

## 🔹 Interpolação de Variáveis

Permite inserir valores dentro de strings.

### Método % (Legado)

```python
nome = "Rodrigo"
idade = 28

print("Nome: %s | Idade: %d" % (nome, idade))
# Nome: Rodrigo | Idade: 28
```

| Símbolo | Tipo |
|---------|------|
| `%s` | String |
| `%d` | Inteiro |
| `%f` | Float |

📌 Não recomendado em código moderno (pouco legível).

### Método format()

```python
nome = "Rodrigo"
idade = 28

# Posicional
print("Nome: {} | Idade: {}".format(nome, idade))

# Com índices
print("Nome: {1} | Idade: {0}".format(idade, nome))

# Com dicionário
pessoa = {"nome": "Rodrigo", "idade": 28}
print("Nome: {nome} | Idade: {idade}".format(**pessoa))
```

### f-strings (Recomendado - Python 3.6+)

```python
nome = "Rodrigo"
idade = 28

print(f"Nome: {nome} | Idade: {idade}")

# Formatação numérica
PI = 3.14159
print(f"{PI:.2f}")      # 3.14
print(f"{PI:10.2f}")    # alinhamento à direita com 10 espaços
print(f"{PI:<10.2f}")   # alinhamento à esquerda
print(f"{PI:^10.2f}")   # centralizado

# Expressões dentro de f-strings
print(f"Soma: {10 + 20}")
print(f"Maior: {max(10, 20, 30)}")
```

📌 Mais legível, performático e moderno. **Prefira sempre f-strings!**

---

## 🔹 Fatiamento de Strings (Slicing)

Permite extrair partes específicas de uma string.

### Estrutura

```
string[inicio:fim:passo]
```

| Parâmetro | Descrição |
|-----------|-----------|
| `inicio` | Índice inicial (inclusivo) - padrão: 0 |
| `fim` | Índice final (exclusivo) - padrão: até o fim |
| `passo` | Intervalo entre índices - padrão: 1 |

### Exemplos aplicados

```python
nome = "Guilherme Arthur"

print(nome[:9])      # Guilherme (do início até índice 8)
print(nome[10:])     # Arthur (do índice 10 até o fim)
print(nome[10:16])   # Arthur (do 10 ao 15)
print(nome[::2])     # GuhreAtu (pega de 2 em 2)
print(nome[2:12:3])  # ihe (índices 2, 5, 8, 11)
```

### Inversão de String

```python
nome = "Python"
print(nome[::-1])  # nohtyP
```

📌 Muito útil em algoritmos e validações (ex: verificar se uma palavra é palíndromo).

---

## 🔹 Strings de Múltiplas Linhas

Utilizadas para textos longos, logs, relatórios e templates.

```python
nome = "Rodrigo"

mensagem = f"""
Olá, meu nome é {nome}.
Estou aprendendo Python.
Este é um texto com múltiplas linhas.
"""

print(mensagem)
```

---

# 🧠 Boas Práticas

- **Normalize dados sempre:** `nome = nome.strip().title()`
- **Prefira f-strings:** mais legível, mais rápida e moderna
- **Evite concatenação com +** (cria várias strings intermediárias)
- **Use `join()` para concatenar listas** (mais eficiente que `+`)
- **Atenção à imutabilidade:** strings não podem ser alteradas diretamente
- **Use slicing com validação:** evite índices fixos sem verificar o tamanho

---

# ⚠️ Pontos de Atenção

| Erro Comum | Correção |
|------------|----------|
| `nome[0] = "A"` (imutável) | `nome = "A" + nome[1:]` |
| `"texto" + 123` (tipos diferentes) | `f"texto {123}"` |
| Índice fora do intervalo | Verificar `len()` antes de fatiar |
| `split()` sem argumento | Divide por qualquer espaço em branco |
| Misturar `%` e `format()` | Padronizar uso de f-strings |

---

# 🧪 Exemplos Práticos

**Exemplo: Limpeza de dados de clientes**

```python
# Dados sujos vindo de um arquivo
clientes = [
    "  joão silva  ",
    "MARIA SANTOS",
    "pedro almeida  ",
    "    ANA OLIVEIRA    "
]

print("=== CLIENTES NORMALIZADOS ===\n")
for cliente in clientes:
    nome_limpo = cliente.strip().title()
    print(f"Cliente: {nome_limpo}")
```

**Exemplo: Extração de dados de e-mail**

```python
email = "usuario.exemplo@empresa.com.br"

# Extrair usuário e domínio
usuario = email[:email.index("@")]
dominio = email[email.index("@") + 1:]

print(f"E-mail: {email}")
print(f"Usuário: {usuario}")
print(f"Domínio: {dominio}")

# Verificar formato
if "@" in email and "." in email:
    print("Formato de e-mail válido!")
```

**Exemplo: Verificação de palíndromo**

```python
def eh_palindromo(texto):
    texto_limpo = texto.lower().replace(" ", "")
    return texto_limpo == texto_limpo[::-1]

palavras = ["radar", "python", "arara", "banana", "socorram me subi no onibus"]

for palavra in palavras:
    if eh_palindromo(palavra):
        print(f"'{palavra}' é palíndromo!")
    else:
        print(f"'{palavra}' não é palíndromo.")
```

---

# 🚀 Conclusão

A manipulação de strings é essencial para qualquer profissional que trabalha com dados.

Dominar este módulo permite:
- Limpar dados inconsistentes (strip, replace, regex)
- Padronizar informações (upper, lower, title)
- Extrair dados relevantes (split, slicing, find)
- Preparar dados para análise e machine learning

Strings são a base do processamento de dados textuais. Combine os métodos aprendidos com fatiamento e f-strings para construir pipelines de limpeza eficientes.

---

> [🏠 Voltar ao índice](../../README.md) | [⬆ Módulo anterior: If-Else-For-While](../3-If-Else-For-While/README.md) | [⬇ Próximo módulo: Manipulação de Dados](../../2-Manipulacao-Dados-Python/README.md)