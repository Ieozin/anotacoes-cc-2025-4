# Tema 7: Métodos de Demonstração
**Status:** Concluído

## 1. O que é provar?
Garantir q uma afirmação é V para **todo** o conjunto universo, sem testar um por um (pq o conjunto pode ser infinito).

## 2. Tipos de Prova
* **Trivial:** A conclusão já é óbvia. (Ex: Se x>0, então x²+1 > 0. O final é sempre positivo, nem preciso olhar pro x).
* **Vacuidade:** A premissa é impossível. (Ex: Se 1=2, então eu sou o Batman. Verdadeiro, pq a premissa é falsa).
* **Direta:** Álgebra pura. Sai de P e chega em Q.
* **Contrapositiva:** Prova `~Q -> ~P`. Útil qdo o direto é difícil.
* **Absurdo (Contradição):** Assume q a tese é mentira e prova q isso quebra a matemática (tipo `0=1`). Ótimo p/ provar irracionalidade.

## 3. Indução Matemática (O "Efeito Dominó")
Essencial para provar algoritmos recursivos e propriedades de números naturais.

**Passo a Passo:**
1.  **Base:** Provar q vale para o primeiro (`n=1`). (Derruba o 1º dominó).
2.  **Passo Indutivo:** Assumir q vale para `k` (Hipótese) e provar q vale para `k+1` (Tese).
    * Se vale para um e ele derruba o próximo, vale para todos.

**Indução Forte:** No passo 2, assume q vale para **todos** os anteriores (1 até k), não só o último. Usado em recorrências complexas (tipo Fibonacci).

## Pontos Práticos
* Em provas de divisibilidade por indução, o segredo é manipular a álgebra do `k+1` para fazer aparecer a expressão do `k`.