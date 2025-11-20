# Tema 7: Métodos de Demonstração
**Data:** 19/11/2025
**Status:** Iniciado

## 1. Introdução
Demonstrar é provar matematicamente q uma afirmação é verdadeira para todos os casos do conjunto universo. É como garantir q um algoritmo não tem bugs lógicos.
* **Estrutura:** `P(x) -> Q(x)` (Se P acontece, então Q acontece).

---

## 2. Tipos de Demonstração

### A. Demonstração Trivial
* **Conceito:** Qdo a conclusão `Q` é verdadeira para **qualquer** valor, independente da premissa `P`.
* **Lógica:** Se `Q` é V, a implicação `P -> Q` é sempre V.
* **Exemplo:** "Se `x < 0`, então `x² + 1 > 0`".
    * O termo `x² + 1` é sempre positivo nos Reais. Não importa se `x` é negativo ou não. A conclusão se sustenta sozinha.

### B. Demonstração por Vacuidade
* **Conceito:** Qdo a premissa `P` é **falsa** para todos os elementos. É impossível de acontecer.
* **Lógica:** Se `P` é F, a implicação `P -> Q` é sempre V (pela tabela-verdade, F -> qualquer coisa = V).
* **Exemplo:** "Se `x² - 2x + 2 <= 0`, então..."
    * A equação `x² - 2x + 2` tem delta negativo, ou seja, é sempre positiva. Nunca vai ser `<= 0`.
    * Como a premissa é impossível, a afirmação é considerada verdadeira por vacuidade.

### C. Demonstração Direta
* **Conceito:** O método padrão. Assume q `P` é verdade e usa álgebra p/ chegar em `Q`.
* **Aplicação:** Usa muito definições básicas:
    * Par: `n = 2k`
    * Ímpar: `n = 2k + 1`
* **Exemplo:** "Se `n` é ímpar, `5n + 3` é par".
    1.  Substitui `n` por `2k + 1`.
    2.  `5(2k + 1) + 3` = `10k + 5 + 3` = `10k + 8`.
    3.  Fatora o 2: `2(5k + 4)`. Se é múltiplo de 2, é par. Provado.

### D. Contrapositiva (Contraposição)
* **Conceito:** Provar `~Q -> ~P` em vez de `P -> Q`. Elas são logicamente equivalentes.
* **Quando usar:** Qdo a demonstração direta fica travada ou complexa.
* **Exemplo:** "Se `3x - 15` é par, então `x` é ímpar".
    * **Contrapositiva:** Se `x` é par (`~Q`), então `3x - 15` é ímpar (`~P`).
    * Prova: Se `x` é par (`2k`), `3(2k) - 15` = `6k - 15`. Isso dá pra escrever como `2(3k - 8) + 1`, q é a fórmula de ímpar. Provado.

### E. Redução ao Absurdo (Contradição)
* **Conceito:** Assumir q a tese é mentira e mostrar q isso gera um erro lógico.
* **Passo a passo:**
    1.  Assume q `P` é V.
    2.  Assume q `Q` é F (nega a conclusão).
    3.  Desenvolve até achar um absurdo (tipo `0 = 1` ou `x` é par e ímpar ao mesmo tempo).
    4.  Se deu erro, a suposição de q `Q` era falsa está errada. Logo, `Q` é V.
* **Exemplo clássico:** Provar q a soma de Racional com Irracional é Irracional.
    * Supõe q dá Racional. A álgebra vai mostrar uma contradição (tipo dizer q um número irracional pode ser escrito como fração).

---

## 3. Resumo Prático (Pra não esquecer)

* **Trivial:** A conclusão já é óbvia/sempre verdade.
* **Vacuidade:** A premissa é impossível/mentira.
* **Direta:** Caminho reto (`P` leva a `Q`).
* **Contrapositiva:** Inverte e nega (`não Q` leva a `não P`).
* **Absurdo:** Tenta provar o contrário e quebra a cara (acha erro).

---

## 4. Atividades e Exercícios
* **Q1 (Paridade):** Usar a definição algébrica de par/ímpar resolve a maioria.
* **Q2 (Equivalência):** Lembrar q `P -> Q` é o mesmo que `~P ou Q`.
* **Q3 (Lógica):** Em provas de múltipla escolha, testar a contrapositiva ajuda a eliminar alternativas erradas.

*Parei aqui. Próximo passo: Indução Matemática.*