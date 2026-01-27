# Tema 3: Python Básico

**Data:** 27/01/2026 | **Status:** Concluído

## 1. Características Principais

* **Sintaxe Limpa:** Usa-se **indentação** (espaços) para definir blocos de código, em vez de chaves `{}`.
* **Case Sensitive:** `idade` é diferente de `Idade`.
* **Comentários:** Usa-se `#` para uma linha ou `'''` para blocos.

## 2. Variáveis e Tipagem Dinâmica

Não é preciso declarar o tipo da variável (como `int x`). O Python descobre sozinho pelo valor atribuído.

```python
nome = "Leonardo"  # str (String)
idade = 25         # int (Inteiro)
altura = 1.75      # float (Ponto Flutuante - usa ponto, não vírgula!)
estudando = True   # bool (Booleano - Primeira letra maiúscula!)
```

Dica: Use `type(variavel)` para descobrir o tipo de dado.

## 3. Entrada e Saída de Dados

Como o programa interage com o usuário.

### Saída (print):
Mostra dados na tela.

```python
print("Olá", nome)
# Ou usando f-strings (mais moderno):
print(f"Olá {nome}, sua idade é {idade}")
```

### Entrada (input):
Recebe dados do teclado.

⚠️ Atenção: O input sempre retorna uma STRING. Se quiser fazer conta, precisa converter (Casting).

```python
idade = input("Digite sua idade: ")         # Retorna "25" (texto)
idade_num = int(input("Digite sua idade: ")) # Retorna 25 (número)
```

## 4. Operadores Essenciais

### Aritméticos

| Símbolo | Função | Exemplo |
| :--- | :--- | :--- |
| +, -, *, / | Básicos | 10 / 2 = 5.0 |
| // | Divisão Inteira | 10 // 3 = 3 (Ignora o resto) |
| % | Módulo (Resto) | 10 % 3 = 1 |
| ** | Potência | 2 ** 3 = 8 |

### Relacionais (Comparação)

Retornam sempre True ou False.
`==` (Igual), `!=` (Diferente), `>`, `<`, `>=`, `<=`.

### Lógicos

* **and:** As duas condições precisam ser verdadeiras.
* **or:** Pelo menos uma precisa ser verdadeira.
* **not:** Inverte o valor (True vira False).

## Resumo Rápido

* **Indentação:** É obrigatória. Sem ela o código dá erro.
* **Tipagem:** O Python decide o tipo na hora da atribuição.
* **Input:** Sempre lê como texto. Use `int()` ou `float()` para converter se for número.
* **Boolean:** True e False (Sempre com maiúscula).
