# Tema 7: Métodos de Demonstração
**Data:** 19/11/2025 - 21/11/2025
**Status:** Concluído

## 1. Introdução
Demonstrar é provar matematicamente que uma afirmação é verdadeira para **todos** os casos do conjunto universo. É como validar a lógica de um algoritmo para garantir que ele nunca quebra.
* **Estrutura:** `P(x) -> Q(x)` ("Se P acontece, então Q acontece").
* **Regra de ouro:** Sempre definir o conjunto universo (ex: `n` em Z, `x` em R). Sem isso, a prova não vale.

---

## 2. Tipos de Demonstração (O Cinto de Utilidades)

### A. Trivial
* **O que é:** Quando a conclusão `Q` é verdadeira para **qualquer** valor, independente da premissa `P`.
* **Lógica:** Se `Q` é V, a implicação `P -> Q` é sempre V.
* **Exemplo:** "Se `x < 0`, então `x² + 1 > 0`".

### B. Vacuidade
* **O que é:** Quando a premissa `P` é **falsa** para todos os elementos (impossível de acontecer).
* **Lógica:** Se `P` é F, a implicação `P -> Q` é sempre V (pela tabela-verdade).
* **Exemplo:** "Se `x² - 2x + 2 <= 0`, então `x³ >= 8`".

### C. Direta
* **O que é:** O método padrão. Assume que `P` é verdade e usa álgebra/lógica para chegar em `Q`.
* **Como fazer:** Encadeamento lógico. Usa definições básicas (par = 2k, ímpar = 2k+1).

### D. Contrapositiva (Contraposição)
* **O que é:** Provar `~Q -> ~P` em vez de `P -> Q`. Elas são logicamente equivalentes.
* **Quando usar:** Quando provar o caminho direto é difícil.

### E. Redução ao Absurdo (Contradição)
* **O que é:** Assumir que a tese é mentira e mostrar que isso gera um erro lógico (uma contradição).
* **Passo a passo:**
    1. Assume que a premissa `P` é V.
    2. Assume que a conclusão `Q` é **Falsa**.
    3. Desenvolve até achar um absurdo (tipo "x é par e ímpar ao mesmo tempo" ou "1 = 0").
    4. Se deu absurdo, a suposição de que `Q` era falsa estava errada. Logo, `Q` é V.

---

## 3. Princípio da Indução (O "Efeito Dominó")
Usado para provar propriedades em conjuntos infinitos ordenados (Naturais).

### A. Indução Matemática (Padrão)
Para provar que vale para todo `n`:
1. **Base (Âncora):** Provar que vale para o primeiro número (`n=1`). (O primeiro dominó cai).
2. **Passo Indutivo:** Assumir que vale para `k` (Hipótese) e provar que vale para `k+1` (Tese).
    * Se vale para um, e esse um derruba o próximo, vale para todos.

### B. Indução Forte
* **Diferença:** No passo indutivo, assume que vale para **todos** os anteriores (`1, 2...` até `k`) para provar `k+1`.
* **Uso:** Sequências recursivas onde o termo atual depende de vários anteriores (tipo Fibonacci).

---

## 4. Resumo Prático para Provas

* **Identificar o método:**
    * Tem "Para todo n"? -> Provavelmente Indução.
    * Tem "Se... então..." e álgebra complexa? -> Tente Direta ou Contrapositiva.
    * Tem negação ou irracionais? -> Tente Absurdo.
* **Definições úteis:**
    * Par: `2k`
    * Ímpar: `2k + 1`
    * Racional: `p/q` (com q != 0)