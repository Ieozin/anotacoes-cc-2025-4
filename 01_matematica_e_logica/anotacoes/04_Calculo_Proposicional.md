# Tema 6: Cálculo de Predicados
**Período:** 10/11 - 17/11

## 1. Sentenças Abertas (Predicados)
O Tema 5 era V/F. O Tema 6 é sobre sentenças com variáveis (ex: "x < 5"), q não são V ou F sozinhas.

* **Sentença Aberta (p(x)):** Vira V ou F qnd se substitui `x` por um valor. Ex: `p(x): 2x - 3 = 5`. Se `x=4`, `p(4)` é V.
* **Conjunto Universo (U):** O domínio da sentença (ex: N, Z, R).
* **Conjunto Verdade (Vp):** O subconjunto de U q torna p(x) verdadeira. É o q realmente importa.
    * **Ex 1:** `p(x): x+15=8` em `U=Z`. `x=-7`. Como `-7` tá em `Z`, `Vp = {-7}`.
    * **Ex 2:** `p(x): 2x²+5x=0` em `U=Z`. Soluções `x=0` ou `x=-2.5`. Como `U=Z`, `-2.5` não serve ("raiz estranha ao universo"). `Vp = {0}`.
* **Operações:** Os conectivos (`~, ∧, ∨`) funcionam nos Conjuntos Verdade. Ex: `V(p ∧ q)` = `Vp ∩ Vq`.

---

## 2. Quantificadores (Fechando a Sentença)
Fecham a sentença p/ ela virar V ou F.

* **Universal (∀):**
    * **Lê-se:** "Para todo", "Qualquer que seja".
    * **Quando é V?** Só se a propriedade valer p/ **todos** os elementos do Universo (`Vp = U`).
    * **Quando é F?** Basta **um** contraexemplo.
    * Ex (F): `(∀x ∈ R)(x² = x)`. É Falso. Contraexemplo: `x=2`.

* **Existencial (∃):**
    * **Lê-se:** "Existe pelo menos um", "Algum".
    * **Quando é V?** Se *pelo menos um* `x` funcionar (`Vp != ∅`).
    * **Quando é F?** Só se for impossível (`Vp = ∅`).
    * Ex (V): `(∃x ∈ R)(x > 4)`. (Ex: `x=5`).
    * Ex (F): `(∃x ∈ R)(x = x + 2)`. Impossível.

* **Unicidade (∃!):**
    * **Lê-se:** "Existe um, e apenas um".
    * Ex: `(∃!x ∈ N)(x² = 25)`. V, pq `Vp = {5}` (o `-5` não tá em N).

---

## 3. Variáveis e Negação

### Variáveis Livres vs. Ligadas
* **Ligada:** "Presa" a um quantificador (`∀x` ou `∃x`).
* **Livre:** Solta, sem quantificador no seu escopo.
* **Ponto chave:** Se tiver *qualquer* variável livre, a expressão inteira ainda é uma sentença aberta.
    * Ex: `(∃x)(x + y < 4)`. `x` é ligada, `y` é livre. O valor (V/F) depende de `y`.
    * Na atividade `∀y((p(x) ∧ ∃x(...)))`, o primeiro `x` em `p(x)` é livre. (Ok)

### Ordem dos Quantificadores
A ordem importa MUITO.
* `(∀x ∈ Z)(∃y ∈ Z)(x < y)` -> "Para todo x, existe um y maior". **(Verdadeiro)**.
* `(∃y ∈ Z)(∀x ∈ Z)(x < y)` -> "Existe um y q é maior q todos os x". **(Falso)**, não existe "o maior inteiro".

### Negação de Quantificadores (Regra Chave)
Equivalente às Leis de Morgan.
* **`~ (∀x, p(x)) ⇔ ∃x (~p(x))`**
    * **Negação de "Todos** são" é "**Existe** um q **não** é".
    * Ex: `~ (∀x)(x-3 >= 4) ⇔ (∃x)(x-3 < 4)`. (Troca `∀` por `∃` e nega a proposição `>=` -> `<`).

* **`~ (∃x, p(x)) ⇔ ∀x (~p(x))`**
    * **Negação de "Existe** um" é "**Todos não** são" (ou "Nenhum é").
    * Ex: `~ (∃x)(x+3 = x) ⇔ (∀x)(x+3 != x)`.

---

## 4. Aplicações em Computação
* **Prolog (Programming in Logic):** Linguagem declarativa. Usa fatos e regras.
    * **Fato:** `amigo(paulo, carlos).` (Regra: tudo minúsculo).
    * **Regra:** `gosta(luiza, X) :- gosta(X, corrida).` (Luiza gosta de X *se* X gosta de corrida).
* **Sistemas Especialistas:** Simulam raciocínio (ex: diagnóstico médico).
* **Prova de Correção:** Usar lógica formal p/ provar q um programa é correto. Diferente de "Teste" (q usa dados).

---

## Conclusão (Tema 6)
Fechei o Tema 6. É o Tema 5 com variáveis. O principal p/ revisar é:
1.  Diferença de `∀` (Todos) e `∃` (Pelo menos um).
2.  Regras de Negação (Troca `∀` ⇔ `∃` e nega o predicado).
3.  A ordem dos quantificadores importa.