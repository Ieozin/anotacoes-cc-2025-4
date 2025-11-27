# Tema 6: Cálculo de Predicados
**Período:** 10/11 - 18/11

## 1. Sentenças Abertas
* Expressão com variável (`x`). Vira V/F quando `x` é definido.
* **Conjunto Universo (U):** Opções disponíveis p/ x.
* **Conjunto Verdade (Vp):** Opções que tornam a frase Verdadeira.

## 2. Quantificadores
* **Universal (`∀`):** "Para todo". V se vale pra 100% de U. F se tiver 1 contraexemplo.
* **Existencial (`∃`):** "Existe". V se tiver pelo menos 1 caso. F se for impossível.
* **Unicidade (`∃!`):** "Existe um único".

## 3. Negação (Regras)
* **Negar `∀`:** `∃` + nega verbo.
    * "Todo A é B" -> "Existe A que **não** é B".
* **Negar `∃`:** `∀` + nega verbo.
    * "Existe A que é B" -> "Todo A **não** é B" (Nenhum A é B).

## 4. Computação
* **Prolog:** Fatos e Regras. Letra minúscula p/ constantes, Maiúscula p/ variáveis.
* **Prova de Correção:** Lógica p/ validar algoritmos.

## Resumo Prático das Atividades
* **Negação:** Cuidado com o português. Negar "Todo" não é "Nenhum".
* **Prolog:** Sintaxe importa (`?-` para queries).
* **Múltiplos Quantificadores:** A ordem muda o sentido. `∀x∃y` != `∃y∀x`.