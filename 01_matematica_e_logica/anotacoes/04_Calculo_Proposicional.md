 # Tema 5: Cálculo Proposicional
**Período:** 05/11 - 07/11

## 1. Introdução (05/11)
Lógica é a "caixa de ferramentas" p/ TI. Base de Aristóteles (silogismo), mas Boole e De Morgan criaram a notação simbólica rigorosa.

## 2. Proposições
* **Proposição:** Sentença declarativa (V ou F). Ex: "2 < 5".
* **Não é:** Pergunta, ordem, exclamação.
* **3 Princípios:** 3º Excluído (V ou F, sem meio-termo), Não Contradição (não V e F), Identidade (p é p).
* **Tipos:** Simples (`p`, `q`) e Composta (ligada por conectivos).

---

## 3. Conectivos Lógicos
Símbolos p/ transformar linguagem natural em simbólica.

* **Negação (`~` ou `¬`):** Inverte o valor. `~V = F`.
* **Conjunção (`∧`, E):** V só se **ambas** forem V.
* **Disjunção Inclusiva (`∨`, OU):** F só se **ambas** forem F.
* **Disjunção Exclusiva (`⊻`, OU... OU):** V se tiverem valores **diferentes**.
* **Condicional (`→`, SE... ENTÃO):** F só no caso `V → F = F` ("Vera Fischer").
* **Bicondicional (`↔`, SE E SOMENTE SE):** V se tiverem valores **iguais** (VV ou FF).

---

## 4. Tabela-Verdade (07/11)
Ferramenta p/ achar o valor de proposições compostas.
* **Linhas:** `2^n` (onde `n` = nº de proposições simples). 3 props = `2³ = 8` linhas.
* **Precedência:** 1º Parênteses, 2º `~`, 3º `∧` e `∨`, 4º `→`, 5º `↔`.

### Classificação
* **Tautologia:** Sempre Verdadeira (última coluna da tabela só tem V).
* **Contradição:** Sempre Falsa (última coluna só tem F).
* **Contingência:** Misto de V e F.

---

## 5. Álgebra Booleana
Lógica de computador (bits 0 e 1).
* **Valores:** 1 (V) e 0 (F).
* **Operações:**
    * **AND (`·`):** Multiplicação (equivale a `∧`). `1·1 = 1`, resto é 0.
    * **OR (`+`):** Adição (equivale a `∨`). `0+0 = 0`, resto é 1.
    * **NOT (`'`):** Inversão (equivale a `~`). `1' = 0`, `0' = 1`.

---

## 6. Implicação, Equivalência e Inferência
* **Implicação Lógica (`p ⇒ q`):** Qnd `p` é V, `q` *também* tem q ser V.
* **Equivalência Lógica (`p ⇔ q`):** Tabelas-verdade idênticas.
    * **Leis de Morgan:** `~(p ∧ q) ⇔ ~p ∨ ~q` (Nega "E" vira "OU").
    * **Leis de Morgan:** `~(p ∨ q) ⇔ ~p ∧ ~q` (Nega "OU" vira "E").
    * **Contrapositiva:** `p → q ⇔ ~q → ~p`. (Muito útil).
* **Regras de Inferência (Argumentos Válidos):**
    * **Modus Ponens:** Se `p → q` e `p` é V, então `q` é V.
    * **Modus Tollens:** Se `p → q` e `~q` é V, então `~p` é V.
    * **Silogismo Hipotético:** Se `p → q` e `q → r`, então `p → r` (efeito dominó).

---

## 7. Resumo das Atividades (Tema 5) (07/11)
Exercícios tranquilos.
* **Tradução:** "Nem... nem..." é `~p ∧ ~q`. (Ok).
* **Tautologia:** `p → (q → p)` sempre dá V. (Ok).
* **Álgebra Booleana:** Precedência: `·` (AND) antes de `+` (OR). (Ok).
* **Inferência:** `(p → q)` + `~q` = `~p` (Modus Tollens). (Ok).

**Conclusão:** Tema 5 fechado. Tabela-Verdade é mecânico. O importante é decorar Morgan e as regras de Inferência (Ponens/Tollens) p/ validar argumentos.