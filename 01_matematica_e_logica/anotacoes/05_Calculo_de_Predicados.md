 # Tema 6: Cálculo de Predicados (Parte 1)
**Data:** 10/11/2025

## 1. Introdução e Conceitos Básicos

O Cálculo de Predicados expande a lógica proposicional. Enquanto a proposicional lida com frases inteiras (V ou F), a de predicados entra na estrutura da frase, usando variáveis. É fundamental para algoritmos e banco de dados.

### Sentenças Abertas
São expressões que contêm variáveis e não têm valor lógico (V ou F) até que essas variáveis sejam substituídas por valores específicos.
* **Exemplo:** "Ele é um jogador de futebol". Quem é "ele"? Sem saber, não dá pra dizer se é V ou F.
* **Exemplo Matemático:** `2x - 3 = 5`.
    * Se `x = 4`: `2(4) - 3 = 5` -> `8 - 3 = 5` (V).
    * Se `x = 2`: `2(2) - 3 = 5` -> `1 = 5` (F).

### Predicados
É a parte da sentença que atribui uma propriedade ao sujeito (variável).
* **Notação:** `p(x)` ou `q(x, y)`.
* **Exemplo:** Em `x é alto`, "é alto" é o predicado. `p(x): x é alto`.
* **Exemplo Matemático:** `p(x): 2x = 8`.

---

## 2. Conjuntos Universo e Verdade

Para trabalhar com sentenças abertas, precisamos definir onde estamos "buscando" os valores.

* **Conjunto Universo (U):** É o conjunto de **todos** os valores possíveis para a variável. O contexto geral.
    * Ex: Se estamos falando de números inteiros, `U = Z`.
* **Conjunto Verdade (Vp):** É o subconjunto de U com **apenas** os valores que tornam a sentença verdadeira.
    * `Vp = {x ∈ U | p(x) é V}`
    * Ex: Se `p(x): x + 15 = 8` e `U = Z`, então `Vp = {-7}`.

### Tipos de Sentença Aberta (com base no Conjunto Verdade):
* **Universal:** Verdadeira para **todos** os elementos de U. (`Vp = U`). Ex: `2x + 1 > x` em N.
* **Possível:** Verdadeira para **alguns** elementos de U. (`Vp ≠ ∅` e `Vp ≠ U`). Ex: `2x + 3 > 6` em N (`Vp = {2, 3, 4...}`).
* **Impossível:** Falsa para **todos** os elementos. (`Vp = ∅`). Ex: `x + 3 = x` em N.

---

## 3. Operações Lógicas sobre Sentenças Abertas

Podemos combinar sentenças abertas usando os mesmos conectivos da lógica proposicional. Isso gera novos conjuntos verdade.

Sejam `p(x)` e `q(x)` sentenças em um universo `U`.

### Negação (`~p(x)`)
* O conjunto verdade é o **complementar** de `Vp` em relação a `U`.
* `V~p = U - Vp`
* Ex (em N): `p(x): x + 2 < 6` -> `Vp = {1, 2, 3}`.
* `~p(x): x + 2 ≥ 6` -> `V~p = N - {1, 2, 3} = {4, 5, 6, ...}`.

### Conjunção (`p(x) ∧ q(x)`)
* O conjunto verdade é a **interseção** dos conjuntos verdade.
* `V(p∧q) = Vp ∩ Vq`
* Ex (em Z): `p(x): x² + 6x + 5 = 0` (`Vp = {-1, -5}`) E `q(x): x² + 5x = 0` (`Vq = {0, -5}`).
* `V(p∧q) = {-1, -5} ∩ {0, -5} = {-5}`.

### Disjunção (`p(x) ∨ q(x)`)
* O conjunto verdade é a **união** dos conjuntos verdade.
* `V(p∨q) = Vp ∪ Vq`
* Usando o exemplo anterior: `V(p∨q) = {-1, -5} ∪ {0, -5} = {0, -1, -5}`.

### Condicional (`p(x) → q(x)`)
* Lembrar da equivalência: `p → q` é o mesmo que `~p ∨ q`.
* O conjunto verdade é a união do complementar de Vp com Vq.
* `V(p→q) = V(~p ∨ q) = (U - Vp) ∪ Vq`

### Bicondicional (`p(x) ↔ q(x)`)
* Lembrar que `p ↔ q` é `(p → q) ∧ (q → p)`.
* O conjunto verdade é a interseção dos conjuntos verdade das duas condicionais.
* `V(p↔q) = V(p→q) ∩ V(q→p)`

---
*Terminei a primeira parte do Tema 6. O foco foi entender como as variáveis entram na lógica e como isso se relaciona com conjuntos.*