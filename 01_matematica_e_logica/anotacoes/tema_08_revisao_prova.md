# Tema 8: Revisão Geral e Preparação
**Status:** Concluído

## 1. A Interseção Lógica e Matemática
A base da computação não é apenas "fazer contas", mas estruturar o pensamento.
*   **Matemática:** Fornece as ferramentas (conjuntos, funções).
*   **Lógica:** Fornece a estrutura de validade (verdadeiro/falso, causa/consequência).
*   **Python:** É a ferramenta prática onde aplicamos esses conceitos para resolver problemas reais.

## 2. Pontos Chave para a Prova

### Lógica Proposicional
*   **Princípio do Terceiro Excluído:** Uma proposição só pode ser V ou F, nunca "mais ou menos".
*   **Não Contradição:** Uma proposição não pode ser V e F ao mesmo tempo.
*   **Conectivos:**
    *   `^` (E): Exigente, tudo tem que ser V.
    *   `v` (OU): Flexível, basta um V.
    *   `->` (SE...ENTÃO): Só falha na "Vera Fischer" (V -> F = F).
*   **Leis de Morgan (Negação):**
    *   Negar "Gosto de café **E** leite" = "Não gosto de café **OU** não gosto de leite".
    *   `~(p ^ q) <=> ~p v ~q`.

### Equivalências Importantes
*   **Contrapositiva:** `p -> q` é igual a `~q -> ~p`. (Se chove, molha = Se não molhou, não choveu).

## 3. Aplicação Prática
Resolver problemas complexos exige quebrar o problema em partes menores (Lógica) e modelar essas partes (Matemática/Funções).