# 📌 Módulo: Operadores

Este módulo aborda os diferentes tipos de operadores em Python, incluindo operadores aritméticos, de comparação, atribuição, lógicos, de identidade e de associação.

---

# 🎯 Objetivos do Módulo

Ao final deste módulo, você será capaz de:

- Utilizar operadores aritméticos para realizar operações matemáticas
- Aplicar operadores de comparação para comparar valores
- Utilizar operadores de atribuição para inicializar e modificar variáveis
- Combinar condições com operadores lógicos (and, or, not)
- Comparar identidade de objetos com operadores is e is not
- Verificar pertencimento em sequências com operadores in e not in

---

# 📚 Conteúdos Abordados

## 🔹 Operadores Aritméticos

Executam operações matemáticas.

| Operador | Descrição | Exemplo | Resultado |
|----------|-----------|---------|-----------|
| `+` | Adição | `10 + 5` | `15` |
| `-` | Subtração | `10 - 5` | `5` |
| `*` | Multiplicação | `10 * 5` | `50` |
| `/` | Divisão | `10 / 3` | `3.333...` |
| `//` | Divisão Inteira | `10 // 3` | `3` |
| `%` | Módulo (Resto) | `10 % 3` | `1` |
| `**` | Exponenciação | `2 ** 3` | `8` |
| `()` | Combinatório (parênteses) | `(2 + 3) * 4` | `20` |

### Exemplos de operadores aritméticos:

```python
# Operações básicas
soma = 10 + 5
subtracao = 10 - 5
multiplicacao = 10 * 5
divisao = 10 / 3          # 3.3333333333333335
divisao_inteira = 10 // 3  # 3
resto = 10 % 3            # 1
potencia = 2 ** 3         # 8

# Precedência de operadores
resultado1 = 2 + 3 * 4    # 14 (multiplicação primeiro)
resultado2 = (2 + 3) * 4  # 20 (parênteses primeiro)

print(f"Soma: {soma}")
print(f"Divisão inteira: {divisao_inteira}")
print(f"Resto: {resto}")
```

## 🔹 Operadores de Comparação

Operadores utilizados para comparar dois valores. O resultado sempre é um valor booleano (`True` ou `False`).

| Operador | Descrição | Exemplo | Resultado |
|----------|-----------|---------|-----------|
| `==` | Igualdade | `10 == 10` | `True` |
| `!=` | Diferente | `10 != 5` | `True` |
| `<` | Menor | `10 < 5` | `False` |
| `>` | Maior | `10 > 5` | `True` |
| `>=` | Maior ou igual | `10 >= 10` | `True` |
| `<=` | Menor ou igual | `10 <= 5` | `False` |

### Exemplos de operadores de comparação:

```python
idade = 18
saldo = 1000
limite = 1500

# Igualdade
print(idade == 18)      # True
print(idade == 20)      # False

# Diferença
print(idade != 20)      # True

# Maior / Menor
print(saldo > limite)   # False
print(saldo < limite)   # True

# Maior ou igual / Menor ou igual
print(saldo >= 1000)    # True
print(saldo <= 500)     # False
```

## 🔹 Operadores de Atribuição

Utilizados para atribuir valor inicial ou sobrescrever o valor de uma variável.

| Operador | Descrição | Exemplo | Equivalente |
|----------|-----------|---------|-------------|
| `=` | Atribuição simples | `x = 10` | - |
| `+=` | Atribuição com adição | `x += 5` | `x = x + 5` |
| `-=` | Atribuição com subtração | `x -= 5` | `x = x - 5` |
| `*=` | Atribuição com multiplicação | `x *= 5` | `x = x * 5` |
| `/=` | Atribuição com divisão | `x /= 5` | `x = x / 5` |
| `//=` | Atribuição com divisão inteira | `x //= 5` | `x = x // 5` |
| `%=` | Atribuição com módulo | `x %= 5` | `x = x % 5` |
| `**=` | Atribuição com exponenciação | `x **= 2` | `x = x ** 2` |

### Exemplos de operadores de atribuição:

```python
# Atribuição simples
saldo = 1000
print(saldo)  # 1000

# Atribuição com adição
saldo += 500  # saldo = saldo + 500
print(saldo)  # 1500

# Atribuição com subtração
saldo -= 200  # saldo = saldo - 200
print(saldo)  # 1300

# Atribuição com multiplicação
saldo *= 2    # saldo = saldo * 2
print(saldo)  # 2600

# Atribuição com divisão
saldo /= 2    # saldo = saldo / 2
print(saldo)  # 1300.0

# Atribuição com exponenciação
x = 2
x **= 3       # x = x ** 3
print(x)      # 8
```

## 🔹 Operadores Lógicos

Utilizados para combinar condições e expressões booleanas.

| Operador | Descrição | Exemplo | Resultado |
|----------|-----------|---------|-----------|
| `and` | E (ambas condições verdadeiras) | `True and True` | `True` |
| `or` | OU (pelo menos uma condição verdadeira) | `True or False` | `True` |
| `not` | Negação (inverte o valor) | `not True` | `False` |

### Operador AND (E)

Possibilita fazer duas comparações, sendo que **as duas devem ser verdadeiras** para cumprir a condição.

```python
saldo = 1000
saque = 500
limite = 1500

# Ambas condições precisam ser verdadeiras
if saldo >= saque and saque <= limite:
    print("Saque permitido")
else:
    print("Saque não permitido")

# Exemplo com False
saque = 2000
if saldo >= saque and saque <= limite:
    print("Saque permitido")
else:
    print("Saque não permitido")  # Será executado
```

### Operador OR (OU)

Possibilita fazer duas comparações, sendo que **pelo menos uma das duas deve ser verdadeira** para cumprir a condição.

```python
saldo = 1000
saque = 500
limite = 1500

# Pelo menos uma condição precisa ser verdadeira
if saldo >= saque or saque <= limite:
    print("Condição atendida")  # Será executado

# Exemplo onde ambas são falsas
saque = 2000
if saldo >= saque or saque <= limite:
    print("Condição atendida")
else:
    print("Nenhuma condição foi atendida")
```

### Operador NOT (Negação)

Faz o inverso do resultado da comparação.

```python
# Negação simples
print(not 1000 > 1500)  # True (pois 1000 > 1500 é False, e not inverte para True)

# Exemplos práticos
aprovado = True
print(not aprovado)  # False

saldo = 500
print(not saldo > 1000)  # True (saldo não é maior que 1000)
```

### Precedência com Parênteses

Devemos utilizar parênteses para delimitar as precedências quando houver mais de duas comparações ou operadores lógicos.

```python
# Sem parênteses - precedência confusa
resultado = True and False or True
print(resultado)  # True (and tem precedência sobre or)

# Com parênteses - claro e explícito
resultado1 = (True and False) or True   # True
resultado2 = True and (False or True)   # True
resultado3 = (True and False) or (True and False)  # False

# Exemplo prático com números
idade = 25
saldo = 1000
limite = 500

# Verifica se a pessoa pode fazer a operação
if (idade >= 18) and (saldo >= limite):
    print("Operação permitida")
else:
    print("Operação negada")
```

## 🔹 Operadores de Identidade

Operadores utilizados para comparar se os dois objetos testados ocupam a mesma posição na memória.

| Operador | Descrição | Exemplo |
|----------|-----------|---------|
| `is` | Verdadeiro se ambos os objetos são o mesmo | `curso is nome_curso` |
| `is not` | Verdadeiro se os objetos são diferentes | `curso is not nome_curso` |

### Exemplos de operadores de identidade:

```python
# Strings
curso = "Curso de Python"
nome_curso = curso

print(curso is nome_curso)      # True (mesmo objeto na memória)
print(curso is not nome_curso)  # False (são o mesmo objeto)

# Números
saldo = 200
limite = 200

print(saldo is limite)   # True (Python reutiliza números pequenos)
print(saldo is not limite)  # False

# Listas (comportamento diferente)
lista_a = [1, 2, 3]
lista_b = [1, 2, 3]

print(lista_a is lista_b)  # False (objetos diferentes, mesmo conteúdo)
print(lista_a == lista_b)  # True (mesmo conteúdo)
```

## 🔹 Operadores de Associação

Operadores utilizados para verificar se um objeto está presente em uma sequência (string, lista, tupla, dicionário, etc.).

| Operador | Descrição | Exemplo |
|----------|-----------|---------|
| `in` | Verdadeiro se o objeto está na sequência | `"Python" in curso` |
| `not in` | Verdadeiro se o objeto NÃO está na sequência | `"maçã" not in frutas` |

### Exemplos de operadores de associação:

```python
# Strings
curso = "Curso de Python"
print("Python" in curso)     # True
print("Java" in curso)       # False
print("Cursos" not in curso) # True

# Listas
frutas = ["laranja", "uva", "limão"]
print("uva" in frutas)       # True
print("maçã" in frutas)      # False
print("maçã" not in frutas)  # True

# Números em lista
saques = [1500, 100]
print(200 in saques)         # False
print(1500 in saques)        # True

# Dicionários (verifica nas chaves)
pessoa = {"nome": "Rodrigo", "idade": 23}
print("nome" in pessoa)      # True
print("Rodrigo" in pessoa)   # False (verifica apenas chaves)
```

---

# 🧠 Boas Práticas

- Utilize parênteses para deixar explícita a precedência de operadores lógicos
- Prefira `is` para comparar com `None` (ex: `var is None`)
- Use `in` para verificar pertencimento em sequências
- Evite comparar tipos diferentes implicitamente (ex: `1 == "1"` é False)
- Para números, use operadores de comparação em vez de `is` (preferência por `==`)

---

# ⚠️ Pontos de Atenção

- O operador `is` compara identidade (mesmo objeto na memória), não valor
- Para comparar valores, use `==` em vez de `is`
- Python reutiliza números pequenos (-5 a 256) - `is` pode funcionar nesses casos
- O operador `/` sempre retorna float (ponto flutuante)
- O operador `//` retorna inteiro (despreza o resto)
- Operadores `and` e `or` têm precedência diferente - use parênteses para evitar ambiguidade

---

# 🧪 Exemplos Práticos

**Exemplo completo com múltiplos operadores:**

```python
# Sistema de verificação de saque
print("=== SISTEMA DE SAQUE ===\n")

saldo = float(input("Digite seu saldo: "))
saque = float(input("Digite o valor do saque: "))
limite = float(input("Digite o limite: "))

# Verificações
saldo_suficiente = saldo >= saque
dentro_limite = saque <= limite
conta_ativa = True

# Operadores lógicos combinados
if (saldo_suficiente and dentro_limite) and conta_ativa:
    print("\n✅ Saque autorizado!")
    saldo -= saque
    print(f"Novo saldo: R$ {saldo:.2f}")
elif not conta_ativa:
    print("\n❌ Conta inativa. Saque não permitido.")
elif not saldo_suficiente:
    print(f"\n❌ Saldo insuficiente. Saldo atual: R$ {saldo:.2f}")
elif not dentro_limite:
    print(f"\n❌ Valor acima do limite. Seu limite: R$ {limite:.2f}")

# Operadores de associação
extras = ["cheque_especial", "cartao_credito", "investimentos"]
opcao = input("\nDeseja usar algum serviço extra? ")

if opcao in extras:
    print(f"✅ {opcao} está disponível para você!")
else:
    print("❌ Opção não disponível.")
```

**Exemplo de operadores aritméticos combinados:**

```python
# Cálculo de área de um círculo
raio = float(input("Digite o raio do círculo: "))

# Operadores aritméticos com constantes
PI = 3.14159
area = PI * (raio ** 2)

print(f"\nRaio: {raio}")
print(f"Área: {area:.2f}")
```

---

# 🚀 Conclusão

Este módulo apresentou os diferentes tipos de operadores em Python: operadores aritméticos para cálculos matemáticos, operadores de comparação para comparar valores, operadores de atribuição para modificar variáveis, operadores lógicos (and, or, not) para combinar condições, operadores de identidade (is, is not) para comparar objetos na memória, e operadores de associação (in, not in) para verificar pertencimento em sequências. Esses operadores são fundamentais para construir expressões, condições e lógica de programação em Python.

---

> [🏠 Voltar ao índice](../../README.md) | [⬆ Módulo anterior: Linguagem Python](../1-Linguagem-Python/README.md) | [⬇ Próximo módulo: If-Else-For-While](../3-If-Else-For-While/README.md)