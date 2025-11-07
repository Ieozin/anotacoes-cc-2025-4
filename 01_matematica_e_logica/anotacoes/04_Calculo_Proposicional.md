# Tema 5: Cálculo Proposicional
**Período:** 05/11/2025 - 07/11/2025

## 1. Introdução à Lógica Proposicional (05/11)

A lógica matemática é a "caixa de ferramentas" para TI. A base vem de Aristóteles (silogismo), mas a notação simbólica de Boole e De Morgan é que deu rigor matemático à coisa.

## 2. Proposições (A Base do Cálculo) (05/11)

* **Proposição:** Sentença declarativa com sentido completo que pode ser V ou F. (Ex: "2 < 5").
* **Não é proposição:** Perguntas, ordens, exclamações.
* **Princípios:** 3º Excluído (é V ou F), Não Contradição (não pode ser V e F), Identidade (é igual a si mesma).
* **Tipos:** Simples (`p`, `q`) e Composta (ligada por conectivos).

---

## 3. Conectivos Lógicos e Tradução (05/11 - 07/11)

* **Negação (`~` ou `¬`):** Inverte o valor. `~V = F`.
* **Conjunção (`∧`, E):** Verdadeira só se **ambas** forem V.
* **Disjunção Inclusiva (`∨`, OU):** Falsa só se **ambas** forem F.
* **Disjunção Exclusiva (`⊻`, OU... OU):** Verdadeira se tiverem valores **diferentes** (uma V, outra F).
* **Condicional (`→`, SE... ENTÃO):** Falsa só no caso "Vera Fischer" (`V → F = F`).
* **Bicondicional (`↔`, SE E SOMENTE SE):** Verdadeira se tiverem valores **iguais** (VV ou FF).

---

## 4. Tabela-Verdade e Valoração (07/11)

Ferramenta para determinar o valor lógico de qualquer proposição composta.
* **Número de linhas:** `2^n` (onde `n` é o número de proposições simples). Ex: 3 proposições (p, q, r) = `2³ = 8` linhas.
* **Ordem de Precedência:** 1. Parênteses; 2. Negação (`~`); 3. Conjunção/Disjunção (`∧`, `∨`); 4. Condicional (`→`); 5. Bicondicional (`↔`).

### Classificação das Proposições
* **Tautologia:** Sempre Verdadeira (última coluna toda V).
* **Contradição:** Sempre Falsa (última coluna toda F).
* **Contingência:** Às vezes V, às vezes F.

---

## 5. Álgebra Booleana (07/11)

A lógica dos computadores (bits 0 e 1).
* **Variáveis:** Assumem 1 (V) ou 0 (F).
* **Operações:**
    * **AND (`·`):** Multiplicação Lógica. Equivale a `∧`. `1·1 = 1`, resto é 0.
    * **OR (`+`):** Adição Lógica. Equivale a `∨`. `0+0 = 0`, resto é 1.
    * **NOT (`'` ou barra em cima):** Inversão. Equivale a `~`. `1' = 0`, `0' = 1`.

---

## 6. Implicação, Equivalência e Inferência (07/11)

* **Implicação Lógica (`p ⇒ q`):** Quando `p` é V, `q` *também* tem que ser V.
* **Equivalência Lógica (`p ⇔ q`):** As tabelas-verdade são idênticas.
    * **Leis de Morgan:** `~(p ∧ q) ⇔ ~p ∨ ~q`  e  `~(p ∨ q) ⇔ ~p ∧ ~q`. (Negar "E" vira "OU", negar "OU" vira "E").
    * **Contrapositiva:** `p → q ⇔ ~q → ~p`. (Muito útil!).

* **Regras de Inferência (Argumentos Válidos):**
    * **Modus Ponens:** Se `p → q` e acontece `p`, então acontece `q`.
    * **Modus Tollens:** Se `p → q` e *não* acontece `q` (`~q`), então *não* aconteceu `p` (`~p`).
    * **Silogismo Hipotético:** Se `p → q` e `q → r`, então `p → r` (efeito dominó).

---

## 7. Resumo das Atividades (Tema 5) (07/11)

Fiz as atividades durante o estudo do módulo.

* **Q1 (Aristóteles):** Contribuição? Teoria do silogismo. (Ok).
* **Q1 (Proposição):** O que é? Sentença declarativa com sentido completo (V ou F). (Ok).
* **Q1 (Conectivos):** Identificar E, OU, SE...ENTÃO, SE E SOMENTE SE, NÃO. (Ok).
* **Q1 (Simbólica):** "Nem Carlos é engenheiro nem Paulo é professor" -> `~p ∧ ~q`. (Acertei, "nem... nem" é "não um E não outro").
* **Q1 (Tautologia - ENADE):** Analisei as tabelas. `p → (q → p)` deu tudo V. (Ok).
* **Q1 (Álgebra Booleana - ENADE):** Ordem de precedência. Multiplicação (`AND`) vem antes da adição (`OR`). A expressão correta era `(~p + q) * r`. (Ok).
* **Q1 (Argumento Válido):** `p → q` (V), `~q` (V). Conclusão `~p` é V? Sim, Modus Tollens. (Ok).
* **Q1 (Inferência):** `Se Maria estuda, passa` (`p → q`). `Maria não passou` (`~q`). Logo, `Maria não estudou` (`~p`). É Modus Tollens. (Ok).

**Conclusão do Tema 5:** Fechei Cálculo Proposicional. A parte de Tabela-Verdade é trabalhosa mas mecânica. O mais importante foi entender as Leis de Morgan e as Regras de Inferência (Modus Ponens/Tollens), que são muito usadas para validar argumentos sem ter que fazer tabela gigante toda hora.