# Tema 07: Revisão Turbo - Paradigmas e Python (Foco na Prova)
**Data:** 03/02/2026 | **Status:** Concluído

## 1. O "Mapa Mental" dos Paradigmas
A prova costuma cobrar a associação entre o **Paradigma**, suas **Características** e as **Linguagens**.

| Paradigma | Foco Principal | Características Chave | Linguagens Típicas |
| :--- | :--- | :--- | :--- |
| **Imperativo / Procedural** | *Como* fazer (passo a passo). | Mudança de estado, variáveis, loops (`for`/`while`), atribuição. | **C**, **Pascal**, Fortran, Cobol. |
| **Orientado a Objetos (OO)** | Modelar o mundo real. | **Classes**, Objetos, Encapsulamento, Herança, Polimorfismo. | **Java**, **Smalltalk** (pura), C++, Python. |
| **Funcional** | *O que* é (matemático). | **Imutabilidade** (dados não mudam), Funções de Alta Ordem, Recursão (sem loops). | **Haskell**, Lisp, Scheme, Erlang. |
| **Lógico** | Regras e Fatos. | Baseado em lógica formal (predicados). O motor de inferência acha a resposta. | **Prolog**. |

> **Atenção:** Python é **Multiparadigma**. Ele suporta Imperativo, OO e Funcional. Não é exclusivo de nenhum.

## 2. Python: Características Essenciais (Teoria)
*   **Interpretada:** Executa linha a linha. Se houver erro na linha 10, ele roda até a 9 e para.
*   **Tipagem Dinâmica:** Não precisa declarar `int x`. O Python entende `x = 10`.
*   **Tipagem Forte:** Não faz conversões mágicas perigosas. `10 + "5"` gera **Erro** (`TypeError`).
*   **Indentação:** Define os blocos de código (substitui as chaves `{}`).

## 3. Estruturas de Dados
Saber quem é mutável e imutável é essencial para a avaliação.

1.  **Listas `[]`:** **Mutáveis**.
    ```python
    lista = [1, 2]
    lista.append(3) # A lista mudou para [1, 2, 3]
    ```
2.  **Tuplas `()`:** **Imutáveis**.
    ```python
    tupla = (1, 2)
    tupla[0] = 9 # ERRO! TypeError.
    ```
3.  **Dicionários `{}`:** **Mutáveis**. Estrutura Chave-Valor.
    ```python
    d = {'a': 1}
    d['b'] = 2 # OK.
    ```

## 4. Python Funcional na Prática
Questões de `lambda` são comuns.

*   **Lambda:** Função anônima de uma linha. `lambda x: x + 1`.
*   **Map:** Aplica função em todos os itens.
    *   `map(lambda x: x*2, [1, 2])` -> `[2, 4]`.
*   **Filter:** Seleciona itens baseados em uma condição.
    *   `filter(lambda x: x > 5, [1, 10])` -> `[10]`.

## 5. Orientação a Objetos (Sintaxe)
*   **`class`:** Cria o molde.
*   **`__init__`:** Método construtor (inicializa atributos).
*   **`self`:** Referência obrigatória ao próprio objeto.

```python
class Aluno:
    def __init__(self, nome):
        self.nome = nome # Atributo de instância
```

## 6. Simulado Rápido (Previsão)

**Q1. O que imprime?**
```python
a = [1, 2]
b = a
b.append(3)
print(a)
```
**Resposta:** `[1, 2, 3]`. (Listas são referências na memória. Ao mexer em `b`, altera-se `a`).

**Q2. Qual código dá erro?**
*   A) `print("Olá" * 3)` -> Imprime "OláOláOlá"
*   B) `print(10 + "10")` -> **ERRO** (`TypeError`, devido à Tipagem Forte)

**Q3. Qual paradigma foca na imutabilidade?**
**Resposta:** Funcional.

## Resumo Rápido
- **Paradigmas:** Imperativo (passo a passo), OO (objetos/classes), Funcional (imutabilidade), Lógico (regras).
- **Python:** Multiparadigma, Interpretado, Tipagem Dinâmica e Forte.
- **Mutabilidade:** Listas mudam `[]`, Tuplas não mudam `()`.
- **Funcional:** Lambda (função anônima), Map (transforma), Filter (seleciona).
- **Ponteiros/Ref:** Atribuir uma lista a outra variável copia a referência, não os dados.