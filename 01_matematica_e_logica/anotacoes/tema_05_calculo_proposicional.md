# Tema 5: Cálculo Proposicional
**Status:** Concluído

## 1. Proposições
* Sentença q pode ser V ou F.
* **Não é proposição:** Pergunta, ordem, paradoxo.

## 2. Conectivos (Tabela-Verdade)
A base de toda a lógica digital.

| Conectivo | Símbolo | Nome | Regra (Quando é V?) |
| :--- | :---: | :--- | :--- |
| **NÃO** | `~` | Negação | Inverte o valor. |
| **E** | `^` | Conjunção | Só se **tudo** for V. |
| **OU** | `v` | Disjunção | Se **pelo menos um** for V. |
| **OU..OU**| `v_` | Disj. Exclusiva| Se forem **diferentes**. |
| **SE..ENTÃO**| `->` | Condicional | Só é F no caso "Vera Fischer" (V->F). |
| **SE, SÓ SE**| `<->` | Bicondicional| Se forem **iguais**. |

## 3. Tabela-Verdade na Mão
* Número de linhas = `2^n` (n = número de variáveis).
* **Ordem:** `()` > `~` > `^/v` > `->` > `<->`.

## 4. Equivalências e Inferência (Atalhos)
* **Tautologia:** Sempre V. **Contradição:** Sempre F.
* **Morgan:**
    * `~(A e B)` = `~A ou ~B`
    * `~(A ou B)` = `~A e ~B`
* **Contrapositiva (Muito Útil):** `P -> Q` é igual a `~Q -> ~P`. (Se chove molha = Se não molhou, não choveu).
* **Modus Ponens:** `P -> Q` e `P` são verdade => `Q` é verdade.
* **Modus Tollens:** `P -> Q` e `~Q` são verdade => `~P` é verdade.