# Tema 7: Quantificadores
**Data:** 20/11/2025
**Status:** Iniciado

## 1. Introdução aos Quantificadores
Quantificadores transformam sentenças abertas (como "x é maior que 2") em proposições que podem ser V ou F, definindo *quantos* elementos do conjunto satisfazem a condição.

### Expressões Comuns
* **"Para todo" / "Qualquer que seja":** Indica que a regra vale para 100% dos casos.
* **"Existe" / "Pelo menos um":** Indica que a regra vale para, no mínimo, 1 caso.

---

## 2. Quantificador Universal (`∀`)

* **Símbolo:** `∀` (A invertido).
* **Significado:** "Para todo x em S, P(x) é verdade".
* **Notação:** `∀x ∈ S, P(x)`.
* **Verificação:**
    * **Verdadeiro:** Se a sentença `P(x)` for verdadeira para **todos** os elementos de `S`.
    * **Falso:** Se existir **um único** contraexemplo (um x onde P(x) falha).

### Exemplos
* **Sentença:** `P(x): x + 2 > x` em `N` (Naturais).
    * `∀x ∈ N, x + 2 > x`. **Verdadeiro** (sempre soma, sempre aumenta).
* **Sentença:** `P(x): x² = x` em `R` (Reais).
    * `∀x ∈ R, x² = x`. **Falso**. Contraexemplo: `x=2` (4 != 2).

---

## 3. Quantificador Existencial (`∃`)

* **Símbolo:** `∃` (E invertido).
* **Significado:** "Existe pelo menos um x em S tal que P(x) é verdade".
* **Notação:** `∃x ∈ S, P(x)`.
* **Verificação:**
    * **Verdadeiro:** Se você encontrar **pelo menos um** exemplo que funcione.
    * **Falso:** Se a sentença for falsa para **todos** os elementos (impossível).

### Exemplos
* **Sentença:** `P(x): x > 4` em `R`.
    * `∃x ∈ R, x > 4`. **Verdadeiro** (ex: `x=5`).
* **Sentença:** `P(x): x = x + 2` em `R`.
    * `∃x ∈ R, x = x + 2`. **Falso** (0 = 2 é impossível).

---

## 4. Negação de Quantificadores
Regra prática para negar frases com quantificadores (importante para provas).

* **Negar "Para todo" (`~∀`):**
    * A negação de "Todos são" **NÃO É** "Nenhum é".
    * A negação é **"Existe pelo menos um que NÃO é"**.
    * Lógica: `~(∀x, P(x))` <=> `∃x, ~P(x)`.
    * *Ex:* Negação de "Todo número ao quadrado é positivo" -> "Existe um número real cujo quadrado **não** é positivo" (ou seja, é negativo ou zero).

* **Negar "Existe" (`~∃`):**
    * A negação de "Existe algum" é **"Para todo x, NÃO é"** (ou "Nenhum é").
    * Lógica: `~(∃x, P(x))` <=> `∀x, ~P(x)`.
    * *Ex:* Negação de "Existe um número real tal que x² = 3" -> "Para todo número real, x² **diferente** de 3".

---

## 5. Resumo Prático das Atividades

* **Q1 (Identificação):**
    * "Todos os gatos..." -> Universal (`∀`).
    * "Existe um número..." -> Existencial (`∃`).
    * "Para todo natural..." -> Universal (`∀`).
    * "Existe estudante..." -> Existencial (`∃`).
    * *Dica:* É só olhar a palavra chave: "Todo" vs "Existe".

* **Q2 (Veracidade):**
    * `∃x ∈ R, x² = 3`.
    * **Verdadeiro**, pois `x = √3` e `x = -√3` são números reais. Basta um existir para a frase ser V.

---

**Para Revisar:**
* A negação de `∀` vira `∃` (com o predicado negado).
* A negação de `∃` vira `∀` (com o predicado negado).
* Universal só é V se **todos** forem V. Existencial só é F se **todos** forem F.