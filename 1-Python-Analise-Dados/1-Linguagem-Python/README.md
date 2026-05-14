# 📌 Módulo: Linguagem Python

Este módulo aborda os fundamentos da linguagem Python, incluindo tipos de dados, variáveis, constantes, nomenclatura, conversão de tipos e funções de entrada e saída.

---

# 🎯 Objetivos do Módulo

Ao final deste módulo, você será capaz de:

- Compreender os diferentes tipos de dados em Python
- Declarar e manipular variáveis e constantes
- Aplicar as regras de nomenclatura (Snake Case)
- Realizar conversões entre tipos de dados
- Utilizar as funções de entrada (input) e saída (print)

---

# 📚 Conteúdos Abordados

## 🔹 Tipos de Dados

Tipos de dados definem características e comportamentos de um objeto para o interpretador.

### Principais tipos de dados em Python:

| Categoria | Tipos | Descrição |
|-----------|-------|-----------|
| **Texto** | str | Cadeias de caracteres |
| **Numérico** | int, float, complex | Números inteiros, decimais e complexos |
| **Sequência** | list, tuple, range | Coleções ordenadas |
| **Mapa** | dict | Pares chave-valor |
| **Coleção** | set, frozenset | Coleções não ordenadas sem duplicatas |
| **Booleano** | bool | True ou False |
| **Binário** | bytes, bytearray, memoryview | Dados binários |

### Exemplos de cada tipo:

```python
# Texto
nome = "Rodrigo"
mensagem = 'Olá, mundo!'

# Numérico
idade = 23          # int
altura = 1.75       # float
numero_complexo = 2 + 3j  # complex

# Sequência
lista = [1, 2, 3, 4]           # list (mutável)
tupla = (1, 2, 3, 4)           # tuple (imutável)
numeros = range(0, 10)         # range

# Mapa
dicionario = {"nome": "Rodrigo", "idade": 23}  # dict

# Coleção
conjunto = {1, 2, 3, 4, 5}     # set (não ordenado, sem duplicatas)
conjunto_congelado = frozenset([1, 2, 3])  # frozenset (imutável)

# Booleano
aprovado = True
finalizado = False

# Binário
dados_bytes = b"Hello"          # bytes
```

## 🔹 Variáveis

Variáveis são valores que podem sofrer alterações no decorrer do código.

### Declaração de variáveis:

```python
# Declaração simples
age = 23
name = "Rodrigo"

# Declaração múltipla (atribuição simultânea)
age, name = 23, "Rodrigo"

# Declaração com mesmo valor
x = y = z = 0
```

## 🔹 Constantes

Uma constante é um valor que permanece igual até o final da execução do programa, ele é imutável.

**Importante:** O Python não oferece suporte nativo para constantes. Portanto, declaramos uma variável com letras todas maiúsculas para sinalizar que é uma constante e não deve ser alterada.

### Exemplo de constante:

```python
# Por convenção, constantes são escritas em MAIÚSCULAS
PI = 3.14159
GRAVIDADE = 9.81
DIAS_DA_SEMANA = 7

# NÃO é uma prática recomendada alterar uma constante
# PI = 3.14  # Evite fazer isso!
```

## 🔹 Nomenclatura (Snake Case)

Python utiliza o padrão **Snake Case** para nomes de variáveis, funções e métodos.

### Regras de nomenclatura:

| Tipo | Padrão | Exemplo |
|------|--------|---------|
| Variáveis | snake_case | `nome_completo` |
| Funções | snake_case | `calcular_media()` |
| Constantes | MAIÚSCULAS | `VALOR_MAXIMO` |
| Classes | PascalCase | `MeuPrimeiroCodigo` |

**Boas práticas:**
- Escolher nomes sugestivos e descritivos
- Constantes em letras maiúsculas
- Evitar nomes muito curtos ou genéricos (ex: `a`, `b`, `x`)

### Exemplos:

```python
# Boas práticas
nome_completo = "Rodrigo Silva"
idade_cliente = 23
valor_total = 1500.50

# Evitar
n = "Rodrigo"      # nome pouco descritivo
idadeCliente = 23  # não utiliza snake_case
```

## 🔹 Conversão de Tipo (Type Casting)

Em alguns casos é necessário converter tipos para serem utilizados. Utilizamos a função ligada ao tipo do dado.

### Funções de conversão:

| Função | Conversão | Exemplo |
|--------|-----------|---------|
| `int()` | Converte para inteiro | `int("10")` → `10` |
| `float()` | Converte para decimal | `float("10.5")` → `10.5` |
| `str()` | Converte para string | `str(10)` → `"10"` |
| `bool()` | Converte para booleano | `bool(1)` → `True` |
| `list()` | Converte para lista | `list("abc")` → `["a", "b", "c"]` |

### Exemplos de conversão:

```python
# String para inteiro
idade_str = "23"
idade_int = int(idade_str)
print(idade_int + 1)  # 24

# Inteiro para string
numero = 100
texto = str(numero)
print("O número é " + texto)  # O número é 100

# Float para inteiro (perde a parte decimal)
valor = 10.75
valor_int = int(valor)
print(valor_int)  # 10

# String para float
preco_str = "49.90"
preco_float = float(preco_str)
print(preco_float * 2)  # 99.8

# Cuidado: conversão inválida gera erro
# int("abc")  # ValueError!
```

## 🔹 Funções de Entrada e Saída

### Função de Saída: print()

A função `print()` mostra na tela o valor passado como parâmetro. É possível passar vários parâmetros separados por vírgula.

**Características:**
- Cada parâmetro pode ter um tipo diferente
- Por padrão, os valores são separados por espaço
- O parâmetro `sep` altera o separador
- O parâmetro `end` altera o final da linha

### Exemplos de print:

```python
# Print simples
print("Olá, mundo!")

# Múltiplos parâmetros
nome = "Rodrigo"
idade = 23
print("Nome:", nome, "Idade:", idade)  # Nome: Rodrigo Idade: 23

# Alterando o separador
print("Maçã", "Banana", "Laranja", sep=" - ")  # Maçã - Banana - Laranja

# Alterando o final da linha
print("Olá", end=" ")
print("Mundo!")  # Olá Mundo!

# Print com f-string (formatação moderna)
nome = "Rodrigo"
print(f"Meu nome é {nome}")
```

### Função de Entrada: input()

A função `input()` é utilizada para entrada de dados pelo usuário.

**Características importantes:**
- O valor retornado pelo `input()` é sempre do tipo **string** (texto)
- Se precisar de números, é necessário converter com `int()` ou `float()`
- Aceita um parâmetro opcional como texto de ajuda (prompt)

### Exemplos de input:

```python
# Input simples
nome = input("Digite seu nome: ")
print(f"Olá, {nome}!")

# Input numérico (com conversão)
idade_str = input("Digite sua idade: ")
idade = int(idade_str)  # Converte string para inteiro
print(f"Você tem {idade} anos")

# Input decimal (com conversão)
altura = float(input("Digite sua altura: "))
print(f"Sua altura é {altura}m")

# Exemplo completo com validação simples
nome = input("Digite seu nome: ")
idade = int(input("Digite sua idade: "))
print(f"{nome} tem {idade} anos e daqui 5 anos terá {idade + 5} anos.")
```

---

# 🧠 Boas Práticas

- Utilize nomes de variáveis sugestivos e descritivos
- Siga o padrão snake_case para variáveis e funções
- Constantes devem ser escritas em letras maiúsculas com underscore
- Converta tipos explicitamente quando necessário (não confie em conversão automática)
- Use f-strings para formatação de strings (mais legível)
- Sempre valide ou converta o input do usuário quando esperar números

---

# ⚠️ Pontos de Atenção

- O Python não possui constantes nativas - a convenção de letras maiúsculas é apenas uma sinalização
- O `input()` sempre retorna string - converta para outros tipos explicitamente
- Conversões inválidas (ex: `int("abc")`) geram `ValueError`
- Variáveis em Python são dinamicamente tipadas - não precisam declarar o tipo
- Uma variável pode mudar de tipo durante a execução (mas evite isso)

---

# 🧪 Exemplos Práticos

**Exemplo completo integrando entrada, processamento e saída:**

```python
# Programa de cálculo de IMC
print("=== CALCULADORA DE IMC ===\n")

# Entrada de dados
nome = input("Digite seu nome: ")
peso = float(input("Digite seu peso (kg): "))
altura = float(input("Digite sua altura (m): "))

# Processamento
imc = peso / (altura ** 2)

# Saída com formatação
print(f"\nOlá, {nome}!")
print(f"Seu IMC é: {imc:.2f}")

# Classificação
if imc < 18.5:
    print("Classificação: Abaixo do peso")
elif imc < 25:
    print("Classificação: Peso normal")
elif imc < 30:
    print("Classificação: Sobrepeso")
else:
    print("Classificação: Obesidade")
```

**Exemplo de conversão de tipos em operações:**

```python
# Calculadora simples
num1 = float(input("Digite o primeiro número: "))
num2 = float(input("Digite o segundo número: "))

soma = num1 + num2
print(f"Soma: {soma}")

# Concatenando número com texto
valor = 100
print("O valor é: " + str(valor))  # Necessário converter para string
```

---

# 🚀 Conclusão

Este módulo apresentou os fundamentos da linguagem Python, incluindo os principais tipos de dados (texto, numérico, sequência, mapa, coleção, booleano e binário), declaração de variáveis e constantes (por convenção), regras de nomenclatura no padrão snake_case, conversão entre tipos utilizando funções como `int()`, `str()` e `float()`, e as funções de entrada (`input()`) e saída (`print()`). Esses conhecimentos são essenciais para iniciar a programação em Python.

---

> [🏠 Voltar ao índice](../../README.md) | [⬆ Módulo superior: Python para Análise de Dados](../README.md) | [⬇ Próximo módulo: Operadores](../2-Operadores/README.md)