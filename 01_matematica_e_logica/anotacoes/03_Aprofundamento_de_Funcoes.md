# Tema 4: Aprofundamento de Funções (Parte 1)
**Data:** 30/10/2025

## 1. Conceito de Função (Revisão)

Aprofundando o que vi no Tema 3. A ideia principal de uma função é que ela é uma relação matemática que segue regras.

* **Definição:** É uma relação entre dois conjuntos (A e B) onde cada elemento do primeiro (Domínio) se liga a *exatamente um* elemento do segundo (Imagem).
* **Regra Chave (Teste da Reta Vertical):** De um `x` só pode sair uma seta. Se um `x` (como o 'b' no diagrama "Não é função" do PDF) se divide e aponta para dois `y` diferentes, **não é uma função**.
* **Domínio (D):** É o conjunto de partida (Conjunto A), de onde saem as setas. É o valor que "entra" (variável independente `x`).
* **Contradomínio (CD):** É o conjunto de chegada (Conjunto B), *todo ele*, incluindo os elementos que "sobram" (que não recebem setas).
* **Imagem (Im):** São *apenas* os valores do Contradomínio (B) que *realmente* recebem uma seta. A Imagem é um subconjunto do Contradomínio.

---

## 2. Domínio (D) na Prática - As Restrições

O domínio nem sempre é "todos os reais" (`R`). Tenho que olhar a fórmula da função e ver se tem alguma restrição matemática que quebra a conta.

### Restrição 1: Divisão por Zero (Denominador)
* **Exemplo:** `f(x) = 1/x`.
* **Raciocínio:** Não dá pra dividir por zero. O exemplo do PDF "8 pizzas pra 0 pessoas" não faz sentido.
* **Conclusão:** O que está no denominador não pode ser zero.
* **Domínio (1/x):** `D = {x ∈ R | x ≠ 0}` ou `R*`. O gráfico "salta" o eixo Y.
* **Exercício (Q2 Lucro):** `L(x) = 1 / (x+2)`.
    * Restrição: `x+2 ≠ 0` => `x ≠ -2`. Domínio: `R - {-2}`. (Ok).

### Restrição 2: Raiz Quadrada (Radiciando)
* **Exemplo:** `f(x) = sqrt(x)`.
* **Raciocínio:** Não existe raiz quadrada de número negativo (no conjunto dos Reais).
* **Conclusão:** O que está dentro da raiz tem que ser positivo ou zero (`≥ 0`).
* **Domínio (sqrt(x)):** `D = {x ∈ R | x ≥ 0}`. O gráfico começa em (0,0) e só vai para a direita.
* **Exercício (Q5 Contador):** Pedia uma função com domínio `x ≥ 0`. `f(x) = sqrt(x)` era a resposta óbvia. (Ok).

### Restrição Mista (Exemplo da Boleira)
* **Exercício (Q1 Boleira):** `f(x) = 1 / sqrt(x-3)`.
* **Raciocínio:** Tinha duas restrições ao mesmo tempo:
    1.  `x-3 ≥ 0` (por causa da raiz).
    2.  `sqrt(x-3) ≠ 0` (por causa do denominador).
* **Conclusão:** Juntando as duas, a restrição real é `x-3 > 0` => `x > 3`.
* **Domínio:** `D = {x ∈ R | x > 3}` ou `(3, +∞)`. (Ok).

---

## 3. Imagem (Im) na Prática

A Imagem é o conjunto de todos os valores de "saída" (`y`) que a função pode gerar.

### Método 1: Achando a Função Inversa
* **Lógica:** Se `f(x)` leva `x` -> `y`, a inversa `f⁻¹(x)` leva `y` -> `x`. O **Domínio da Inversa** é igual à **Imagem da Original**.
* **Exemplo 1: `f(x) = 2x + 1`**
    1.  Troca `f(x)` por `y`: `y = 2x + 1`.
    2.  Troca `x` por `y`: `x = 2y + 1`.
    3.  Isola `y`: `y = (x-1)/2`. Essa é a `f⁻¹(x)`.
    4.  Achar o domínio da inversa: `f⁻¹(x) = (x-1)/2` não tem restrição. Domínio é `R`.
    5.  **Conclusão:** A Imagem da `f(x)` original é `R`.
* **Exemplo 2: `f(x) = 1/x`**
    1.  Inversa: `y = 1/x` -> `x = 1/y` -> `y = 1/x`. A inversa é ela mesma.
    2.  Domínio da inversa: `R*` (não pode ser zero).
    3.  **Conclusão:** A Imagem da `f(x)` original é `R*` (`Im = {y ∈ R | y ≠ 0}`).

### Método 2: Análise Direta (Ex: Módulo)
* **Exemplo: `f(x) = |x|`**
    * O domínio (entrada `x`) é `R`.
    * Mas a saída `y` é *sempre* positiva ou zero (ex: `f(-3) = |-3| = 3`). O gráfico 'V' mostra isso.
    * **Conclusão:** A Imagem é `Im = {y ∈ R | y ≥ 0}`.

### Método 3: Projeção no Gráfico
* **Domínio:** "Amassar" (projetar) o gráfico no **eixo X** (horizontal). Onde o gráfico "deixar uma sombra" é o domínio.
* **Imagem:** "Amassar" (projetar) o gráfico no **eixo Y** (vertical). Onde "deixar sombra" é a imagem.

---

## 4. Tipos de Funções (Injetora, Sobrejetora, Bijetora)

Aqui é onde se classifica como os elementos do domínio se relacionam com o contradomínio.

* **Função Injetora (Injetiva):**
    * **Definição:** `x` diferentes *sempre* levam a `y` diferentes. É "um para um".
    * **No Diagrama:** Nenhum elemento da Imagem recebe mais de uma seta.
    * **Teste da Reta Horizontal:** Se uma reta horizontal corta o gráfico em **mais de um ponto**, ela **NÃO é** injetora.
    * **Exemplo (Não Injetora):** `f(x) = x²`. Falha no teste, pois `f(-2) = 4` e `f(2) = 4`. `y=4` recebe duas setas.

* **Função Sobrejetora (Sobrejetiva):**
    * **Definição:** "Cobre tudo". Não sobra nenhum elemento no Contradomínio.
    * **Regra:** `Imagem = Contradomínio`.
    * **Exemplo (Não Sobrejetora):** `f(x) = x²` (com Contradomínio = `R`). A Imagem é só `[0, +∞)`. Todos os números negativos do Contradomínio "sobram".

* **Função Bijetora (Bijetiva):**
    * **Definição:** É as duas coisas ao mesmo tempo: Injetora **E** Sobrejetora.
    * **No Diagrama:** Cada `x` tem um `y` único, e não sobra nenhum `y`.
    * **Exemplo:** `f(x) = 4x` (com Domínio `R` e CD `R`). É injetora (reta inclinada) e sobrejetora (imagem é `R`).

* **Exercício (Q4 Consultores):** 8 consultores (Domínio) para 6 projetos (Contradomínio). Todo projeto deve ter pelo menos 1.
    * **Raciocínio:** Como todo projeto é atingido, ela é **Sobrejetora**. Como tem mais consultores que projetos (8 > 6), pelo menos um projeto vai receber dois consultores (Casa dos Pombos). Logo, **Não é Injetora**. Resposta: Sobrejetora, mas não injetora. (Ok).

---

## 5. Funções Crescentes e Decrescentes

* **Função Crescente:** Se `x` aumenta, `y` também aumenta. O gráfico "sobe" da esquerda para a direita.
    * Ex: `f(x) = x`, `f(x) = e^x`.
* **Função Decrescente:** Se `x` aumenta, `y` diminui. O gráfico "desce" da esquerda para a direita.
    * Ex: `f(x) = -x`, `f(x) = -sqrt(x)`.
* **Exercício (Q (UFPE)):** `f(x)` cresce ou decresce em partes. Ela não é "estritamente" nenhuma das duas no gráfico todo.

---

## 6. Funções Periódicas

* **O que é:** O padrão do gráfico se repete em intervalos regulares (`T`, o período).
* **Definição:** `f(x + T) = f(x)`.
* **Exemplos:** Eletrocardiograma, `f(x) = sen(t)` (período `2π`), `f(x) = (-1)^x` (período 2, alternando 1, -1, 1, -1...).

---
*Terminei a primeira parte do Tema 4 (até Funções Periódicas). Os exercícios parecem aplicar bastante esses conceitos de restrição de domínio e análise de gráfico.*