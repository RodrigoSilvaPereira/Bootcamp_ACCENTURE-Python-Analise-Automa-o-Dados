# 📌 Módulo: Estruturas Condicionais e Repetição (If-Else-For-While)

Este módulo aborda as estruturas de controle de fluxo em Python, incluindo indentação, estruturas condicionais (if, elif, else) e estruturas de repetição (for, while).

---

# 🎯 Objetivos do Módulo

Ao final deste módulo, você será capaz de:

- Compreender a importância da indentação em Python
- Utilizar estruturas condicionais para desviar o fluxo do programa
- Aplicar estruturas de repetição para iterar sobre sequências
- Utilizar a função range() para gerar sequências numéricas
- Diferenciar quando usar for e quando usar while

---

# 📚 Conteúdos Abordados

## 🔹 Indentação e Blocos

Identar código é uma forma de manter o código fonte mais legível e manutenível. Mas em Python ela exerce um segundo papel: através da indentação, o interpretador consegue determinar onde um bloco de comando inicia e onde ele termina.

**Regras de indentação:**
- Utilizar 4 espaços por nível (recomendado pela PEP 8)
- Manter a consistência em todo o código
- Blocos são delimitados pela indentação, não por chaves `{}`

```python
# Exemplo de indentação correta
if verdadeiro:
    print("Este código está indentado")
    print("Também pertence ao bloco do if")
print("Este código está fora do bloco")

# Exemplo incorreto (geraria erro)
# if verdadeiro:
# print("Faltou indentação")  # Erro: IndentationError
```

## 🔹 Estruturas Condicionais

A estrutura condicional permite o desvio de fluxo de controle, quando determinadas expressões lógicas são atendidas.

### Comando if

Cria uma estrutura condicional simples. O comando irá testar uma expressão lógica; se ela for verdadeira, o bloco de código do `if` será executado.

```python
saldo = 2000
saque = 1000

if saldo >= saque:
    print("Realizando saque!")

if saldo < saque:
    print("Saldo insuficiente")
```

### Comando if/else

Para criar uma condição com dois desvios: se a expressão lógica do `if` não for verdadeira, o bloco do `else` será executado.

```python
saldo = 2000
saque = 1000

if saldo >= saque:
    print("Realizando saque!")
else:
    print("Saldo insuficiente")
```

### Comando if/elif/else

Quando queremos mais de dois desvios, usamos o `elif`. Ele cria uma condição adicional após o `if`. Se a expressão do `if` não for verdadeira, o programa vai para o próximo `elif`, que verifica mais uma condição. O número de `elif` é ilimitado, porém é bom evitar grandes estruturas condicionais.

```python
import sys

opcao = int(input("Informe uma opção: 1 ou 2: "))

if opcao == 1:
    print("Opção 1 escolhida")
elif opcao == 2:
    print("Opção 2 escolhida")
else:
    sys.exit("Opção inválida")
```

### Exemplo completo com múltiplas condições:

```python
# Classificação de nota escolar
nota = float(input("Digite a nota do aluno: "))

if nota >= 9:
    print("Conceito: A - Excelente!")
elif nota >= 7:
    print("Conceito: B - Bom")
elif nota >= 5:
    print("Conceito: C - Regular")
elif nota >= 3:
    print("Conceito: D - Insuficiente")
else:
    print("Conceito: E - Reprovado")
```

## 🔹 Estruturas de Repetição

São estruturas utilizadas para repetir um trecho de código um determinado ou indeterminado número de vezes, podendo também ser aplicadas a expressões lógicas.

### Comando for

É usado para percorrer um objeto iterável (strings, listas, tuplas, dicionários, ranges). É utilizado quando temos um número determinado de repetições ou quando precisamos iterar sobre cada elemento de uma sequência.

```python
# Percorrendo caracteres de uma string
texto = input("Informe um texto: ")
VOGAIS = "AEIOU"

print("\nVogais encontradas:")
for letra in texto:
    if letra.upper() in VOGAIS:
        print(letra, end=" ")

print()  # Quebra de linha

# Percorrendo lista de frutas
frutas = ["maçã", "banana", "laranja", "uva"]
print("\nLista de frutas:")
for fruta in frutas:
    print(f"- {fruta}")
```

### Função range()

A função `range()` é uma função built-in do Python usada para produzir uma sequência de números inteiros a partir de um início (inclusivo) até um fim (exclusivo).

**Sintaxe:** `range(start, stop, step)`

| Parâmetro | Descrição | Obrigatório |
|-----------|-----------|-------------|
| **stop** | Valor final (exclusivo) | Sim |
| **start** | Valor inicial (inclusivo) | Não (padrão: 0) |
| **step** | Incremento entre números | Não (padrão: 1) |

```python
# Exemplos com range

# range(stop) - de 0 até stop-1
print("range(5):")
for i in range(5):
    print(i, end=" ")  # 0 1 2 3 4
print()

# range(start, stop) - de start até stop-1
print("range(2, 8):")
for i in range(2, 8):
    print(i, end=" ")  # 2 3 4 5 6 7
print()

# range(start, stop, step) - com passo
print("range(0, 10, 2):")
for i in range(0, 10, 2):
    print(i, end=" ")  # 0 2 4 6 8
print()

# range decrescente (step negativo)
print("range(10, 0, -2):")
for i in range(10, 0, -2):
    print(i, end=" ")  # 10 8 6 4 2
print()
```

### Comando while

É usado para repetir um bloco de código várias vezes. Faz sentido usar o `while` quando **não sabemos** o número exato de vezes que o código será executado, dependendo de uma condição lógica.

```python
# Exemplo básico de while
opcao = -1

while opcao != 0:
    print("\n--- MENU ---")
    opcao = int(input("Selecione uma opção: 0 [sair], 1 ou 2: "))
    
    if opcao == 1:
        print("Opção 1 selecionada")
    elif opcao == 2:
        print("Opção 2 selecionada")
    elif opcao != 0:
        print("Opção inválida!")

print("Programa encerrado!")

# Exemplo com contador
contador = 1
while contador <= 5:
    print(f"Execução número {contador}")
    contador += 1

# Exemplo com validação de entrada
senha = ""
while senha != "1234":
    senha = input("Digite a senha: ")
    if senha != "1234":
        print("Senha incorreta! Tente novamente.")
print("Acesso permitido!")
```

### Controle de loops: break e continue

| Comando | Descrição |
|---------|-----------|
| `break` | Interrompe completamente a execução do loop |
| `continue` | Pula a iteração atual e vai para a próxima |

```python
# Exemplo com break
print("Comando break - para quando encontra o número 3:")
for i in range(1, 6):
    if i == 3:
        break
    print(i, end=" ")  # 1 2
print()

# Exemplo com continue
print("Comando continue - pula o número 3:")
for i in range(1, 6):
    if i == 3:
        continue
    print(i, end=" ")  # 1 2 4 5
print()
```

---

# 🧠 Boas Práticas

- Utilize 4 espaços para indentação (não use tabs misturados)
- Evite estruturas condicionais muito aninhadas (if dentro de if)
- Prefira `for` quando o número de iterações é conhecido
- Prefira `while` quando a condição de parada depende de uma lógica de negócio
- Use `break` com moderação - estruturas mal planejadas podem causar loops infinitos
- Sempre garanta que a condição do `while` eventualmente se torne falsa

---

# ⚠️ Pontos de Atenção

- Esquecer a indentação causa erro de sintaxe (`IndentationError`)
- O `range(stop)` gera valores até `stop-1` (não inclui o stop)
- O `while` pode gerar loop infinito se a condição nunca mudar
- Comparação com `=` (atribuição) em vez de `==` (comparação) não gera erro, mas causa comportamento inesperado
- Muitos `elif` podem tornar o código confuso - considere usar dicionários ou match-case (Python 3.10+)

---

# 🧪 Exemplos Práticos

**Exemplo de sistema de menu com while:**

```python
# Sistema de calculadora simples
print("=== CALCULADORA ===\n")

while True:
    print("1 - Somar")
    print("2 - Subtrair")
    print("3 - Multiplicar")
    print("4 - Dividir")
    print("0 - Sair")
    
    opcao = int(input("\nEscolha uma opção: "))
    
    if opcao == 0:
        print("Encerrando programa...")
        break
    
    if opcao < 1 or opcao > 4:
        print("Opção inválida! Tente novamente.")
        continue
    
    num1 = float(input("Digite o primeiro número: "))
    num2 = float(input("Digite o segundo número: "))
    
    if opcao == 1:
        print(f"Resultado: {num1 + num2}")
    elif opcao == 2:
        print(f"Resultado: {num1 - num2}")
    elif opcao == 3:
        print(f"Resultado: {num1 * num2}")
    elif opcao == 4:
        if num2 != 0:
            print(f"Resultado: {num1 / num2}")
        else:
            print("Erro: Divisão por zero!")
    print()
```

**Exemplo de for com lista e condicionais:**

```python
# Análise de números
numeros = [10, 25, 7, 42, 18, 3, 31, 8]

pares = 0
impares = 0
maiores_que_20 = 0

for numero in numeros:
    if numero % 2 == 0:
        pares += 1
    else:
        impares += 1
    
    if numero > 20:
        maiores_que_20 += 1

print(f"Lista: {numeros}")
print(f"Números pares: {pares}")
print(f"Números ímpares: {impares}")
print(f"Números maiores que 20: {maiores_que_20}")
```

**Exemplo de validação de entrada com while:**

```python
# Sistema de login simples
usuario_correto = "admin"
senha_correta = "1234"
tentativas = 3

print("=== SISTEMA DE LOGIN ===\n")

while tentativas > 0:
    usuario = input("Usuário: ")
    senha = input("Senha: ")
    
    if usuario == usuario_correto and senha == senha_correta:
        print("\n✅ Login realizado com sucesso!")
        print(f"Bem-vindo, {usuario}!")
        break
    else:
        tentativas -= 1
        print(f"\n❌ Usuário ou senha incorretos.")
        print(f"Tentativas restantes: {tentativas}\n")

if tentativas == 0:
    print("Conta bloqueada! Muitas tentativas incorretas.")
```

---

# 🚀 Conclusão

Este módulo apresentou as principais estruturas de controle de fluxo em Python. Aprendemos sobre a importância da indentação para delimitar blocos de código, as estruturas condicionais (`if`, `elif`, `else`) para criar desvios no fluxo do programa, e as estruturas de repetição (`for` para iterações determinadas e `while` para iterações indeterminadas). Também vimos a função `range()` para gerar sequências numéricas e os comandos `break` e `continue` para controle fino de loops. Esses conceitos são fundamentais para criar programas com lógica condicional e repetitiva.

---

> [🏠 Voltar ao índice](../../README.md) | [⬆ Módulo anterior: Operadores](../2-Operadores/README.md) | [⬇ Próximo módulo: Strings](../4-Strings/README.md)