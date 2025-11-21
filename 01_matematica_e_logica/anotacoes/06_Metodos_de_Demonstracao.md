# Tema 7: Métodos de Demonstração e Quantificadores Avançados
**Data:** 19/11/2025 - 21/11/2025
**Status:** Concluído

## 1. Introdução
Demonstração matemática é provar que um teorema é verdadeiro para todos os casos, usando axiomas e lógica. É como validar que um código não tem bugs lógicos.
* **Estrutura:** `P(x) -> Q(x)` ("Se P, então Q").
* **Essencial:** Sempre definir o conjunto universo (S) da variável.

---

## 2. Aprofundamento em Quantificadores (20/11)
Ferramentas essenciais para as demonstrações.

### Universal (`∀`)
* **Lê-se:** "Para todo", "Qualquer que seja".
* **Uso:** Afirma que a regra vale para **100%** do conjunto.
* **Validade:** Verdadeiro só se `P(x)` for V para *todos*. Falso se tiver **um** contraexemplo.
    * Ex (V): `∀x ∈ N, x + 2 > x`.
    * Ex (F): `∀x ∈ R, x² = x` (Contraexemplo: `x=2`).

### Existencial (`∃`)
* **Lê-se:** "Existe", "Pelo menos um".
* **Uso:** Afirma que a regra vale para **algum** elemento.
* **Validade:** Verdadeiro se achar **um** `x` que funcione. Falso só se for impossível.
    * Ex (V): `∃x ∈ R, x² = 3`. (Verdadeiro, `x = √3`).

### Regra de Negação (Importante p/ Provas)
* **Negar `∀`:** Vira `∃` + nega o predicado.
    * "Todo A é B" -> "Existe A que **NÃO** é B".
* **Negar `∃`:** Vira `∀` + nega o predicado.
    * "Existe A que é B" -> "Todo A **NÃO** é B" (Nenhum é).

---

## 3. Tipos de Demonstração (19/11)

### A. Trivial
* **Quando:** A conclusão `Q` é **sempre verdadeira**, não importa `P`.
* **Exemplo:** "Se `x < 0`, então `x² + 1 > 0`". O `x² + 1` é positivo pra qualquer `x`.

### B. Vacuidade
* **Quando:** A premissa `P` é **sempre falsa** (impossível).
* **Exemplo:** "Se `x² - 2x + 2 <= 0`, então...". A equação nunca é `<= 0`. Premissa falsa torna a implicação verdadeira.

### C. Direta
* **Quando:** O padrão. Assume `P` (V) e chega em `Q` (V) usando álgebra.
* **Exemplo:** "Se `n` é ímpar, `5n+3` é par".
    1. `n = 2k + 1`
    2. `5(2k+1) + 3` = `10k + 8`
    3. `2(5k + 4)`. Múltiplo de 2 é par. Provado.

### D. Contrapositiva
* **Quando:** Direta é difícil. Inverte a lógica: `~Q -> ~P`.
* **Exemplo:** "Se `3x - 15` par, então `x` ímpar".
    * Contrapositiva: "Se `x` par, `3x - 15` ímpar". Fácil de provar.

### E. Redução ao Absurdo
* **Quando:** Negar a tese é mais fácil.
* **Lógica:** Assume que `P` é V e `Q` é F. Tenta achar uma contradição (tipo `1 = 0`).

---

## 4. Princípio da Indução (21/11)
Técnica para provar algo para **todos** os números naturais. O "efeito dominó".

### A. Indução Padrão (Fraca)
1.  **Base:** Provar que vale para o primeiro número (`n=1`). (O primeiro dominó cai).
2.  **Passo Indutivo:** Assumir que vale para `k` e provar que vale para `k+1`. (Se um cai, o próximo cai).
    * **Exemplo (Soma):** `1 + ... + n = n(n+1)/2`.
    * Assume para `k`, soma `k+1` dos dois lados e fatora até chegar na fórmula para `k+1`.

### B. Indução Forte
* **Diferença:** No passo indutivo, assume que vale para **todos** os anteriores (`1` até `k`) para provar `k+1`.
* **Uso:** Sequências recursivas (onde `a_n` depende de `a_{n-1}` e `a_{n-2}`).

---

## 5. Resumo Prático das Atividades

* **Quantificadores:** Identificar palavras-chave ("Todo" vs "Existe").
* **Divisibilidade:** Em provas de indução, o segredo é manipular a álgebra para fazer aparecer a expressão da hipótese.
* **Lógica:** A negação de "Todos são" não é "Nenhum é", mas sim "Existe um que não é".