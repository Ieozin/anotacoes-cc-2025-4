# Tema 6: Cálculo de Predicados
**Data:** 10/11/2025 - 17/11/2025

## 1. O que é Cálculo de Predicados?

O Tema 5 (Cálculo Proposicional) lidava com sentenças q já eram V ou F (ex: "2 < 5").
O Cálculo de Predicados lida com **sentenças abertas**, q são expressões com variáveis (ex: "x < 5").

### Sentença Aberta (ou Proposição Aberta)
* **Definição:** Uma sentença com variável, tipo `p(x)`. Não é V ou F sozinha. Vira proposição (V/F) qnd troco `x` por um valor.
* **Exemplo 1:** "Alguém foi craque do futebol na Argentina". "Alguém" é a variável.
    * Se `Alguém = Maradona` -> Proposição Verdadeira (V).
    * Se `Alguém = Pelé` -> Proposição Falsa (F).
* **Exemplo 2:** `p(x): 2x - 3 = 5`.
    * `x` é a variável. A sentença é aberta.
    * Se `x = 4` -> `2(4)-3 = 5` -> `5 = 5`. Vira uma proposição V.
    * Se `x = 2` -> `2(2)-3 = 5` -> `1 = 5`. Vira uma proposição F.

### Conjunto Universo (U) e Conjunto Verdade (Vp)
* **Conjunto Universo (U):** O conjunto de todos os valores q `x` *pode* assumir (ex: N, Z, R). É o domínio da sentença aberta.
* **Conjunto Verdade (Vp):** O subconjunto de `U` q contém *apenas* os valores q tornam `p(x)` verdadeira. `Vp` é o q realmente importa no final.
    * **Ex 1:** `p(x): x+15=8` em `U=Z` (Inteiros). Resposta `x=-7`. Como `-7` pertence a `Z`, `Vp = {-7}`.
    * **Ex 2:** `p(x): 2x²+5x=0` em `U=Z`. Soluções da equação: `x(2x+5)=0` -> `x=0` ou `x=-2.5`. Como `U=Z`, o valor `-2.5` não serve (é uma "raiz estranha ao universo"). `Vp = {0}`.

### Predicados
* "Predicado" é o nome formal da propriedade q atribuímos à variável.
* `p(x)`: "x é alto e elegante". O predicado é "é alto e elegante".
* `q(x, y)`: "x é professor de y". O predicado é "é professor de".
* Basicamente, a mesma ideia da sentença aberta.

### Operações Lógicas em Sentenças Abertas
Podemos usar os mesmos conectivos (`~, ∧, ∨, →, ↔`) em sentenças abertas. O Conjunto Verdade da operação é simplesmente a operação equivalente nos Conjuntos Verdade:

* **Negação (`V(¬p)`):** `U - Vp` (O Complementar. Tudo q está no Universo *menos* o q está no Conjunto Verdade).
* **Conjunção (`V(p ∧ q)`):** `Vp ∩ Vq` (Interseção. O q torna *ambas* V).
* **Disjunção (`V(p ∨ q)`):** `Vp ∪ Vq` (União. O q torna *pelo menos uma* V).
* **Condicional (`V(p → q)`):** Usa a equivalência `p → q ⇔ ~p ∨ q`.
    * Portanto, `V(p → q) = V(~p) ∪ V(q)`.
* **Bicondicional (`V(p ↔ q)`):** Usa a equivalência `(p → q) ∧ (q → p)`.
    * Portanto, `V(p ↔ q) = V(p → q) ∩ V(q → p)`.

---

## 2. Quantificadores (Fechando a Sentença)

Sentenças abertas (`x < 5`) não são V ou F. Quantificadores (`∀`, `∃`) "fecham" a sentença, transformando-a em uma proposição q pode ser V ou F.

### Quantificador Universal (∀)
* **Símbolo:** `∀` (um "A" de cabeça para baixo, de "All").
* **Lê-se:** "Para todo", "Qualquer que seja".
* **Quando é Verdadeiro (V)?** Só é V se `Vp = U`. A propriedade tem q valer para **todos** os elementos do Conjunto Universo.
* **Quando é Falso (F)?** Basta **um único contraexemplo**.
* **Ex (V):** `(∀x ∈ N)(x+2 > x)`. Isso é V, pois `Vp = N`.
* **Ex (F):** `(∀x ∈ R)(x² = x)`. Isso é F. Contraexemplo: `x=2` (pois `2² = 4`, não 2). O `Vp` aqui é só `{0, 1}`, q é diferente do Universo `R`.

### Quantificador Existencial (∃)
* **Símbolo:** `∃` (um "E" virado, de "Existe").
* **Lê-se:** "Existe pelo menos um", "Existe algum", "Algum".
* **Quando é Verdadeiro (V)?** Só é V se *pelo menos um* `x` do Universo funcionar. Ou seja, `Vp ≠ ∅` (O Conjunto Verdade não pode ser vazio).
* **Quando é Falso (F)?** Só é F se for uma condição impossível (`Vp = ∅`).
* **Ex (V):** `(∃x ∈ R)(x > 4)`. (Ex: `x=5`). `Vp` não é vazio.
* **Ex (F):** `(∃x ∈ R)(x = x + 2)`. Impossível. `Vp = ∅`.

### Quantificador de Unicidade (∃!)
* **Símbolo:** `∃!`
* **Lê-se:** "Existe um, e apenas um" (ou "existe um único").
* **Ex:** `p(x): x²=25` em `U=N` (Naturais). Soluções: `x=5` e `x=-5`. `-5` não tá em `N`. `Vp = {5}`. Como só tem um, `(∃!x ∈ N)(x² = 25)` é V.

---

## 3. Variáveis e Negação

### Variáveis Livres vs. Ligadas
* **Ligada:** A variável q está "presa" a um quantificador (`∀x` ou `∃x`).
* **Livre:** A variável q não tem quantificador no seu escopo.
* **Importante:** Se uma expressão tem *qualquer* variável livre, ela **ainda é uma sentença aberta** (não é V ou F).
    * Ex: `(∃x)(x + y < 4)`. `x` é ligada. `y` é livre. O valor (V/F) depende de `y`.
    * Na atividade `∀y((p(x) ∧ ∃x(...)))`, o primeiro `x` em `p(x)` está fora do escopo do `∃x`, então ele é uma variável livre. (Ok)

### Ordem dos Quantificadores Importa
* `(∀x ∈ Z)(∃y ∈ Z)(x < y)` -> "Para todo inteiro x, existe um inteiro y maior q x". **(Verdadeiro)**.
* `(∃y ∈ Z)(∀x ∈ Z)(x < y)` -> "Existe um inteiro y q é maior q todos os x". **(Falso)**, não existe "o maior inteiro".

### Negação de Quantificadores (Regra-chave)
* **`~ (∀x, p(x)) ⇔ ∃x (~p(x))`**
    * **Negação de "Todos** os gatos são pardos" é "**Existe** um gato q **não** é pardo".
    * Ex: `~ (∀x)(x-3 ≥ 4) ⇔ (∃x)(x-3 < 4)`. (Troca `∀` por `∃` e nega a proposição `≥` -> `<`).

* **`~ (∃x, p(x)) ⇔ ∀x (~p(x))`**
    * **Negação de "Existe** algum homem elegante" é "**Todos** os homens **não** são elegantes" (ou "Nenhum homem é elegante").
    * Ex: `~ (∃x)(x+3 = x) ⇔ (∀x)(x+3 ≠ x)`.

* **Negação com Conectivos (De Morgan):** Nega o quantificador e o conectivo.
    * Ex: `~ [ (∀x)(p(x)) ∧ (∃x)(q(x)) ]` vira:
    * `~ (∀x)(p(x)) ∨ ~ (∃x)(q(x))` (Negação de "E" vira "OU")
    * `(∃x)(~p(x)) ∨ (∀x)(~q(x))` (Nega os quantificadores)

---

## 4. Aplicações em Computação

* **Prolog (Programming in Logic):** Linguagem declarativa baseada nisso. Usa fatos e regras.
    * **Fato:** Define um predicado. `amigo(paulo, carlos).` Regra: tudo minúsculo (senão é variável).
    * **Regra:** Usa inferência. `gosta(luiza, X) :- gosta(X, corrida).` (Luiza gosta de X *se* X gosta de corrida).
* **Sistemas Especialistas:** Simulam raciocínio de um especialista (ex: diagnóstico médico). Usam base de fatos e regras.
* **Prova de Correção:** Usar lógica formal pra provar q um programa está correto (se a entrada `A` é V, a saída `B` é V). Diferente de "Teste" (q usa dados).

---

## Conclusão do Tema 6

Fechei o Tema 6. Foi denso, mas é a base da lógica formal. O principal pra revisar é:
1.  **Diferença de `∀` (Todos) e `∃` (Pelo menos um).**
2.  **Regras de Negação:** Troca `∀` ⇔ `∃` e nega o predicado.
3.  **Ordem Importa:** `(∀x)(∃y)` é diferente de `(∃y)(∀x)`.
4.  **Aplicação:** Prolog e Prova de Correção.