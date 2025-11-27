# Tema 5: Cálculo Proposicional
**Período:** 05/11 - 07/11

## 1. Proposições
* Sentença que pode ser V ou F.
* **Não é:** Pergunta, ordem, paradoxo.
* **Princípios:** 3º Excluído (V ou F), Não Contradição.

## 2. Conectivos
* **NÃO (`~`):** Inverte.
* **E (`^`):** V se **tudo** V.
* **OU (`v`):** V se **pelo menos um** V.
* **OU...OU (`v` sublinhado):** V se forem **diferentes**.
* **SE...ENTÃO (`->`):** Falso só se V -> F ("Vera Fischer").
* **SE, SÓ SE (`<->`):** V se forem **iguais**.

## 3. Tabela-Verdade
* Linhas = `2^n`.
* Precedência: `()` > `~` > `^/v` > `->` > `<->`.

## 4. Lógica
* **Tautologia:** Sempre V.
* **Contradição:** Sempre F.
* **Equivalências Chave:**
    * **Morgan:** `~(p ^ q)` = `~p v ~q` (Nega E vira OU).
    * **Contrapositiva:** `p -> q` = `~q -> ~p`.
* **Inferência:**
    * **Modus Ponens:** `p->q` e `p` => `q`.
    * **Modus Tollens:** `p->q` e `~q` => `~p`.