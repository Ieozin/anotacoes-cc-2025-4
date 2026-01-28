# Tema 04: Python Estruturado
**Data:** 28/01/2026 | **Status:** Concluído

Neste tema, exploramos as estruturas que permitem controlar o fluxo de execução, modularizar o código para reutilização e lidar com situações excepcionais. É a transição do código sequencial simples para a lógica de programação robusta.

---

## 1. Controle de Fluxo: Decisão
Em Python, o controle de decisão é feito através de `if`, `elif` (else if) e `else`. A **indentação** é obrigatória e define o escopo do bloco.

### Comparação de Condições (Python vs C)
Ao contrário da linguagem C, Python possui um tipo `bool` nativo.

| Python | C | Descrição |
| :--- | :--- | :--- |
| `True` | Qualquer valor != 0 | Verdadeiro |
| `False` | 0 ou vazio | Falso |
| `if condicao:` | `if (condicao) {` | Sintaxe de abertura |

```python
idade = int(input("Idade: "))
if idade < 18:
    print("Menor de idade")
elif idade >= 65:
    print("Idoso")
else:
    print("Adulto")
```

---

## 2. Estruturas de Repetição

### Laço `for` e a função `range()`
O `for` em Python é usado para iterar sobre sequências (listas, strings) ou intervalos numéricos gerados pelo `range()`.

*   `range(stop)`: De 0 até stop-1.
*   `range(start, stop)`: De start até stop-1.
*   `range(start, stop, step)`: Início, fim (exclusivo) e o passo do incremento.

```python
# Exemplo de tabuada do 5
for i in range(1, 11):
    print(f"5 x {i} = {5*i}")
```

### Laço `while`
Executa um bloco de código enquanto a condição for verdadeira. Útil quando não sabemos o número exato de repetições.

### Instruções de Controle
*   **`break`**: Interrompe o laço imediatamente.
*   **`continue`**: Pula para a próxima iteração do laço.
*   **`pass`**: Um "espaço reservado" que não faz nada (evita erros de sintaxe em blocos vazios).

---

## 3. Tipos de Dados Sequenciais e Dicionários

| Tipo | Exemplo | Características |
| :--- | :--- | :--- |
| **Listas** | `[1, 2, 3]` | Mutáveis, ordenadas. |
| **Tuplas** | `(1, 2, 3)` | **Imutáveis**, ordenadas. |
| **Strings** | `"Python"` | Sequência imutável de caracteres. |
| **Dicionários**| `{"id": 1}` | Pares Chave-Valor, acesso rápido. |

---

## 4. Subprogramas (Funções)
Funções são blocos de código reutilizáveis definidos pela palavra-chave `def`.

*   **Parâmetros Formais:** Definidos na assinatura da função.
*   **Parâmetros Reais (Argumentos):** Passados na chamada da função.
*   **Escopo:** Variáveis definidas dentro de funções são **locais**. Para alterar uma variável fora da função, usa-se a palavra-chave `global`.

### Recursividade
Uma função é recursiva quando chama a si mesma. Deve sempre possuir uma **condição de parada** (caso base).

```python
def fatorial(n):
    if n == 0 or n == 1: # Caso base
        return 1
    return n * fatorial(n - 1)
```

---

## 5. Bibliotecas e Módulos
Python permite importar funcionalidades prontas para acelerar o desenvolvimento.

*   **`math`**: Operações matemáticas (sqrt, ceil, floor).
*   **`random`**: Geração de números pseudoaleatórios.
*   **`tkinter`**: Criação de interfaces gráficas (GUI).
*   **`pip`**: Gerenciador de pacotes para instalar bibliotecas externas (como `pandas` ou `flask`).

---

## 6. Tratamento de Exceções
Erros em tempo de execução são chamados de **exceções**. Usamos o bloco `try/except` para capturá-los e evitar que o programa trave.

```python
try:
    res = 10 / 0
except ZeroDivisionError:
    print("Erro: Divisão por zero não permitida!")
finally:
    print("Operação finalizada.") # Executa sempre
```

> **Dica:** Use exceções específicas (como `ValueError` ou `TypeError`) em vez de um `except` genérico para facilitar o debug.

---

## Resumo Rápido
*   **Indentação:** É o que define os blocos em Python (substitui as chaves).
*   **`range()`:** É o melhor amigo do laço `for`.
*   **Imutabilidade:** Tuplas e Strings não podem ser alteradas após criadas.
*   **Modularização:** Use funções para não repetir código (DRY - Don't Repeat Yourself).
*   **Try/Except:** Essencial para lidar com entradas de usuário imprevisíveis.