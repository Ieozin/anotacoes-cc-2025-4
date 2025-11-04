# Tema 4: Aprofundamento de Funções
**Data:** 30/10/2025 - 04/11/2025

## 1. Conceito de Função (Revisão)

Aprofundando o que vi no Tema 3. A ideia principal de uma função é que ela é uma relação matemática que segue regras.

* **Definição:** É uma relação entre dois conjuntos (A e B) onde cada elemento do primeiro (Domínio) se liga a *exatamente um* elemento do segundo (Imagem).
* **Regra Chave (Teste da Reta Vertical):** De um `x` só pode sair uma seta. Se um `x` se divide e aponta para dois `y` diferentes, **não é uma função**.
* **Domínio (D):** É o conjunto de partida (Conjunto A), de onde saem as setas. É o valor que "entra" (variável independente `x`).
* **Contradomínio (CD):** É o conjunto de chegada (Conjunto B), *todo ele*, incluindo os elementos que "sobram" (que não recebem setas).
* **Imagem (Im):** São *apenas* os valores do Contradomínio (B) que *realmente* recebem uma seta. A Imagem é um subconjunto do Contradomínio.

---

## 2. Domínio (D) na Prática - As Restrições

O domínio nem sempre é "todos os reais" (`R`). Tenho que olhar a fórmula da função e ver se tem alguma restrição matemática que quebra a conta.

### Restrição 1: Divisão por Zero (Denominador)
* **Exemplo:** `f(x) = 1/x`.
* **Raciocínio:** Não dá pra dividir por zero.
* **Conclusão:** O que está no denominador não pode ser zero.
* **Domínio (1/x):** `D = {x ∈ R | x ≠ 0}` ou `R*`.

### Restrição 2: Raiz Quadrada (Radiciando)
* **Exemplo:** `f(x) = sqrt(x)`.
* **Raciocínio:** Não existe raiz quadrada de número negativo (no conjunto dos Reais).
* **Conclusão:** O que está dentro da raiz tem que ser positivo ou zero (`≥ 0`).
* **Domínio (sqrt(x)):** `D = {x ∈ R | x ≥ 0}`.

### Restrição Mista
* **Exemplo:** `f(x) = 1 / sqrt(x-3)`.
* **Raciocínio:** Duas restrições: 1. `x-3 ≥ 0` (raiz) e 2. `sqrt(x-3) ≠ 0` (denominador).
* **Conclusão:** Juntando as duas, a restrição real é `x-3 > 0` => `x > 3`.

---

## 3. Imagem (Im) na Prática

A Imagem é o conjunto de todos os valores de "saída" (`y`) que a função pode gerar.

### Método 1: Achando a Função Inversa
* **Lógica:** O **Domínio da Inversa** é igual à **Imagem da Original**.
* **Exemplo: `f(x) = 1/x`**
    * Inversa: `y = 1/x` -> `x = 1/y` -> `y = 1/x`. A inversa é ela mesma.
    * Domínio da inversa: `R*` (não pode ser zero).
    * **Conclusão:** A Imagem da `f(x)` original é `R*`.

### Método 2: Análise Direta (Ex: Módulo)
* **Exemplo: `f(x) = |x|`**
    * O domínio (entrada `x`) é `R`.
    * Mas a saída `y` é *sempre* positiva ou zero (ex: `f(-3) = 3`).
    * **Conclusão:** A Imagem é `Im = {y ∈ R | y ≥ 0}`.

### Método 3: Projeção no Gráfico
* **Domínio:** "Amassar" o gráfico no **eixo X** (horizontal).
* **Imagem:** "Amassar" o gráfico no **eixo Y** (vertical).

---

## 4. Tipos de Funções (Injetora, Sobrejetora, Bijetora)

Classificação de como os elementos se relacionam.

* **Função Injetora (Injetiva):**
    * **Definição:** `x` diferentes *sempre* levam a `y` diferentes. É "um para um".
    * **Teste da Reta Horizontal:** Se uma reta horizontal corta o gráfico em **mais de um ponto**, ela **NÃO é** injetora.
    * **Exemplo (Não Injetora):** `f(x) = x²`. Falha no teste (`f(-2) = 4` e `f(2) = 4`).

* **Função Sobrejetora (Sobrejetiva):**
    * **Definição:** Não sobra nenhum elemento no Contradomínio.
    * **Regra:** `Imagem = Contradomínio`.
    * **Exemplo (Não Sobrejetora):** `f(x) = x²` (com CD = `R`). A Imagem é `[0, +∞)`. Os `y` negativos "sobram".

* **Função Bijetora (Bijetiva):**
    * **Definição:** É as duas coisas: Injetora **E** Sobrejetora.
    * **Exemplo:** `f(x) = 2x+1` (de `R` para `R`) é bijetora.

---

## 5. Funções Crescentes e Decrescentes

* **Crescente:** Se `x` aumenta, `y` também aumenta (gráfico "sobe").
* **Decrescente:** Se `x` aumenta, `y` diminui (gráfico "desce").

---

## 6. Funções Periódicas

* **O que é:** O padrão do gráfico se repete em intervalos regulares (Período `T`).
* **Definição:** `f(x + T) = f(x)`.

---

## 7. Resumo das Atividades (Tema 4) (03/11)

Refiz os exercícios. O resultado foi bem melhor.

* **Desempenho Geral:** Acertei 6 de 9 questões.
* **O que eu entendi (Acertos):**
    * A lógica de `f(2x)=2f(x)` (Q1/Q6).
    * Funções periódicas `f(x+T) = f(x)` (Q2).
    * Classificar funções por partes e achar inversa `f⁻¹(y)=x` (Q3).
    * Regra de domínio de denominador simples `1/(x-2)` (Q4).
    * Classificação de função afim `2x+1` (Q5).

* **Os Erros que Sobraram (3):**
    * **Q7 (Imposto):** Função por partes complexa. Calculei as imagens de cada faixa (`[0, 1000]` e `(4000, +∞)`), mas errei na alternativa. A imagem final é uma *união* com um "buraco", não um intervalo contínuo.
    * **Q8 (senx):** Erro de conceito de trigonometria. `senx` não é par (é ímpar) e não é sobrejetora de R em R (Imagem é só `[-1, 1]`). Preciso revisar isso.
    * **Q9 (Domínio Misto):** O mais difícil. `f(x) = sqrt(x²-6x+5) / sqrt(x²-4)`. São duas restrições que precisam ser resolvidas e depois achar a interseção: (1) `x²-6x+5 ≥ 0` (numerador) e (2) `x²-4 > 0` (denominador). Errei por não fazer a interseção das duas inequações.

**Conclusão:** O progresso foi claro. Saí de "chutei tudo" para "entendi a lógica, mas errei os 3 problemas mais difíceis que misturam vários conceitos". Os pontos fracos agora são claros: Domínio Misto (inequação) e conceitos de Trigonometria.