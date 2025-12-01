# Tema 6: Cálculo de Predicados
**Status:** Concluído

## 1. A Novidade: Variáveis
Cálculo Proposicional era estático (P é V). Aqui entra o `x`.
* **Sentença Aberta:** `x > 5`. Não sei se é V ou F até definir o `x`.
* **Conjunto Verdade (Vp):** Os valores do universo q fazem a frase ser V.

## 2. Quantificadores
Transformam a sentença aberta em proposição (V/F).
* **Universal (`∀`):** "Para todo".
    * V se funcionar para 100% dos casos.
    * F se tiver **um** contraexemplo.
* **Existencial (`∃`):** "Existe".
    * V se tiver pelo menos um caso q funcione.
    * F se for impossível.

## 3. Negação (Atenção aqui)
Como negar frases com "Todo" e "Existe".
* **Negar `∀`:** Vira `∃` + nega o verbo.
    * "Todo político é honesto" -> Negação: "Existe político que **não** é honesto". (Não é "Nenhum é"!).
* **Negar `∃`:** Vira `∀` + nega o verbo.
    * "Existe um cisne azul" -> Negação: "Todo cisne **não** é azul" (Nenhum é).

## 4. Computação (Prolog)
* **Fato:** `pai(joao, pedro).` (Letra minúscula, ponto no fim).
* **Regra:** `avo(X, Z) :- pai(X, Y), pai(Y, Z).`
* **Query:** `?- pai(X, pedro).`